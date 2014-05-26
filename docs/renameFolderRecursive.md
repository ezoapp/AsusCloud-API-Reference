##renameFolderRecursive

重新命名路徑中的目錄

相關API：
[重新命名目錄(/folder/rename/)](https://creative.asuscloud.com/content/index.jsp?p=ffoperation&index=4&len=8&id=6&cid=7)

###Input Params
	{
		"path": path ✻,
		"display": folderName,
		"isencrypted": [ 0 | 1 ],
		"isgroupaware": [ 0 | 1 ]
	}

###Output Results
	{
		"status": statusCode,
	}