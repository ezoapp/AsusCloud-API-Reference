##renameFileRecursive

重新命名路徑中的檔案

相關API：
[重新命名檔案(/file/rename/)](https://creative.asuscloud.com/content/?p=ffoperation&index=4&len=8&id=7&cid=8)

###Input Params
	{
		"path": path ✻,
		"display": fileName,
		"isencrypted": [ 0 | 1 ],
		"isgroupaware": [ 0 | 1 ]
	}

###Output Results
	{
		"status": statusCode,
	}