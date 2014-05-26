##createFolde##
[建立目錄(/folder/create/)](https://creative.asuscloud.com/content/index.jsp?p=ffoperation&index=4&len=8&id=0&cid=1)

###Input Params###
	{
		"parent": parentFolderId ✻, 
		"isencrypted": [ 0 | 1 ],
		"display": folderName ✻,
		"attribute": folderInfo,
		"isgroupaware": [ 0 | 1 ]
	}

###Output Results###
	{
		"status": statusCode,
		"id": folderId,
	}