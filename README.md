#AsusCloud API Reference#
- [共同性說明](#AsusCloud-01)
- [語法基本結構](#AsusCloud-02)
- [建立操作授權](#AsusCloud-03)
  
  
-------
<a name="AsusCloud-01"></a>
##共同性說明##
AsusCloud.js 是 EZoApp 雲端開發工具和華碩雲端 WebStorage 之間的界接程式，協助開發者在網頁前端即可用 JavaScript 程式調用華碩雲端 WebStorage 提供的 API 服務，節省 XML Payload 組譯以及 Base64 轉碼等底層作業，並大量簡化 API 的使用方式及程式代碼量。  
  
此文件的目的在於說明：  

- AsusCloud.js 的基本語法結構及授權建立方式
- AsusCloud.js 包裝的函式方法與 WebStorage API 的名稱對應關係。
- Request 輸入變數與 Response 輸出結果的 JSON 資料格式。  

在「語法基本結構」、「建立操作授權」之後的章節，為 AsusCloud.js 調用 WebStorage API 服務的函式說明。章節標題即函式名稱，相對應的 WebStorage API其用途及參數欄位的詳細定義，請參考連結官方文件的說明。  

JSON 資料格式中出現的特殊符號說明如下：

<table>
<tr>
<td style="font-size:30px; color:red;">*</td><td>此為必要的參數；
若無此記號則為選擇性欄位，視需要傳入即可</td>
</tr>
<tr>
<td>[ CONST ]</td><td>此參數為固定的常數值</td>
</tr>
<tr>
<td>[ OPT_1 | OPT_2 | ...]</td><td>參數值必須為列舉的選項其中之一</td>
</tr>
<tr>
<td>[yyyy-MM-dd HH:mm:ss]</td><td>參數值為時間格式</td>
</tr>
<tr>
<td>[objects...]</td><td>此參數為陣列型態的資料</td>
</tr>
</table>
<br/>
  
<a name="AsusCloud-02"></a>
##語法基本結構##
除了操作授權相關的函式，透過 AsusCloud.js 呼叫 WebStorage API 服務的函式皆依循下述的語法結構：  
`AsusCloud.function([params], [success], [failure])`

- **params**  
*Type: Object*  
以 JSON 格式將 Request 欄位包裝為一個物件，作為傳給 API 服務的輸入值。若該 API 服務不需要輸入值時，亦可略過這個參數，惟使用時必須為函式的第一個參數。
- **success**  
*Type: Function*  
當API服務請求成功時 ( 回傳狀態碼為 0 )，所要執行的回呼函式。此回呼函式的第一個參數值為Response 回傳的 JSON 格式物件。如不需要在API服務回傳成功訊息後做任何處理時，亦可略過這個參數，惟使用時必須為函式中 params 之後的參數。
- **failure**  
*Type: Function*  
當API服務請求失敗時 ( 回傳狀態碼不為 0 )，所要執行的回呼函式。此回呼函式的第一個參數值為 Response 回傳的 JSON 格式物件。如不需要在API服務回傳錯誤訊息後做任何處理時，亦可略過這個參數，惟使用時必須為函式中 success 之後的參數，且不可單獨使用。  

特別需注意的是，由於使用者資訊 ( userinfo ) 及授權金鑰 ( token ) 的資料，會在 AsusCloud.js 建立操作授權之後，則以私有資料成員的方式隱含在其中，供每次呼叫 API 服務時重覆利用，所以這二類的變數值無需放入 params 物件當中，相關的參數欄位亦在輸入／輸出的資料格式中省略。操作授權的建立方式，請參閱下個章節的說明。  
<br/>

<a name="AsusCloud-03"></a>
##建立操作授權##
在經由 AsusCloud.js 函式使用 WebStorage 的 API 服務之前，須事先建立授權，取得授權金鑰 ( token ) 之後方可進行後續的操作。建立授權需要傳入以下的資訊：  

- 開發金鑰：Sid, ProgKey (開發者向華碩創意雲註冊申請)
- WebStorage使用者帳號密碼 (終端使用者自行註冊申請)  

資訊齊全之後即可透過 **AsusCloud.build()** 方法取得授權，往後的階段 AsusCloud.js 會重覆利用授權金鑰來進行API服務的調用；若授權金鑰逾時失效，系統會再自動取得新的授權金鑰。  
  
- **sid**  
*Type: String*  
輸入開發金鑰 Sid。  
`AsusCloud.setSid(sid)`

- **progKey**  
*Type: String*  
輸入開發金鑰 ProgKey。  
`AsusCloud.setProgKey(progKey)`

- **userId**  
*Type: String*  
輸入 WebStorage 使用者 UserId。  
`AsusCloud.setUserId(userId)`

- **password**  
*Type: String*  
輸入 WebStorage 使用者 Password。  
`AsusCloud.setPassword(password)`

<br/>
使用上述四個函式輸入取得授權所需的資訊之後，呼叫 **AsusCloud.build()** 建立授權：
`AsusCloud.build([success], [failure])`

- **success**  
*Type: Function*  
當建立授權成功時 ( 回傳狀態碼為 0 )，所要執行的回呼函式。此回呼函式的第一個參數值為 Response 回傳的 JSON 格式物件。如不需要在回傳成功訊息後做任何處理時，亦可略過這個參數。  
- **failure**  
*Type: Function*  
當建立授權失敗時 ( 回傳狀態碼不為 0 )，所要執行的回呼函式。此回呼函式的第一個參數值為 Response 回傳的 JSON 格式物件。如不需要在回傳錯誤訊息後做任何處理時，亦可略過這個參數，惟使用時必須為函式中 success 之後的參數，且不可單獨使用。 
 
<br/>
授權所需的資訊亦可直接以params物件的方式傳入：
`AsusCloud.build(params, [success], [failure])`  

- **params**  
*Type: Object*  
將授權資訊一次放進此物件中，可省略分別輸入的步驟。

		{
		"sid": Sid,
		"progKey": ProgKey,
		"userid": UserId,
		"password": Password
		}	

	最後，可以此函式回傳的布林值判斷AsusCloud.js是否成功建立授權：  
	`AsusCloud.isBuild()`