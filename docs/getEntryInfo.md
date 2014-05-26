##getEntryInfo##
[檔案或目錄相關資料(/fsentry/getentryinfo/)](https://creative.asuscloud.com/content/index.jsp?p=ir&index=3&len=10&id=5&cid=5)
	
###Input Params###
	{
		"isfolder": [ 0 | 1 ] ✻,
		"entryid": fileId / folderId ✻
	}

###Output Results###
	{
		"status": statusCode,
		"isfolder": [ 0 | 1 ],
		"display": fileName / folderName,
		"parent": parentFolderId,
		"isbackup": [ 0 | 1 ],
		"attribute": fileInfo / folderInfo,
		"mimetype": file_MIME-Type,
		"isinfected": [ 0 | 1 ],
		"filesize": fileSize,
		"createdtime": [yyyy-MM-dd HH:mm:ss],
		"headversion": versionNumber,
	}


