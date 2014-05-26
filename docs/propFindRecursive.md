##propFindRecursive
查詢路徑中的檔案、目錄是否存在

相關API：
[查詢檔案、目錄是否存在(/find/propfind/)](https://creative.asuscloud.com/content/index.jsp?p=ir&index=3&len=10&id=6&cid=6)

###Input Params
	{
		"path": path ✻
	}

###Output Results
	{
		"status": statusCode,
		"isencrypted": [ 0 | 1 ],
		"size": fileSize,
		"scrip": scrip,
		"type": [ system.folder | system.file | system.notfund ]
		"id": fileId / folderId 
	}