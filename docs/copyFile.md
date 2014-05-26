##copyFile
[複製檔案(/file/copy/)](https://creative.asuscloud.com/content/index.jsp?p=ffoperation&index=4&len=8&id=5&cid=6)

###Input Params
	{
		"parent": parentFolderId ✻,
		"fileid": [fileIds...] ✻,
		"isgroupaware": [ 0 | 1 ]
	}

###Output Results
	{
		"status": statusCode,
		"fileid": [fileIds...],
		"failid": [failids...]
	}