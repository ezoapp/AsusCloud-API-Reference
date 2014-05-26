##readFileToString

將指定檔案讀出為字串資料

相關API：
[下載(/webrelay/directdownload/)](https://creative.asuscloud.com/content/index.jsp?p=updownload&index=7&len=6&id=8&cid=2)

###Input Params
	{
		// path有傳值時讀取路徑中的檔案，反之則以fileId存取檔案
		"path": path ✻, 
		"fi": fileId ✻
	}

###Output Results
	{
		"status": statusCode,
		"stringdata": stringData
	}