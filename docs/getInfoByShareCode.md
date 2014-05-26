##getInfoByShareCode
[用雲端分享碼查詢檔案、目錄的資料(/fsentry/getinfobysharecode/)](https://creative.asuscloud.com/content/index.jsp?p=share&index=5&len=14&id=3&cid=4)

###Input Params
	{
		"sharecode": shareCode ✻
	}

###Output Results
	{
		"status": statusCode,
		"entryid": fileId / folderId,
		"entrytype": [ 0 | 1 ]
	}