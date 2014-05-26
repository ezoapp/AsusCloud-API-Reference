##isChildrenExist##
[檢查目錄是否有使用(/folder/ischildrenexist/)](https://creative.asuscloud.com/content/index.jsp?p=ir&index=3&len=10&id=7&cid=8)

###Input Params###
	{
		"folderids": [folderIds...] ✻, 
	}

###Output Results###
	{
		"status": statusCode,
		"requestfolders": [
			{
				"id": folderId,
				"childrenexist": [ 0 | 1 ]
			}
		]
	}