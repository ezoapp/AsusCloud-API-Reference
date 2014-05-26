getSharedEntries
[取得用戶分享的檔案目錄清單(/fsentry/getsharedentries/)](https://creative.asuscloud.com/content/index.jsp?p=share&index=5&len=14&id=8&cid=9)

##Input Params
	{
		"kind": [ 0 | 1 | 2 ],
		"pagesize": pageSize,
		"password": password,
		"sortby": [ 0 | 1 ],
		"sortdirection": [ 0 | 1 ],
		"firstentrybound": yyyy-MM-dd HH:mm:ss / entryId
	}

##Output Results
	{
		"status": statusCode,
		"lastentrybound": yyyy-MM-dd HH:mm:ss / entryId,
		"entry": [
			{
				"id": fileId / folderId,
				"parent": parentFolderId,
				"rawentryname": rawFileName / rawFolderName,
				"isfolder": [ 0 | 1 ],
				"isbackup": [ 0 | 1 ],
				"sharingavailabletime": [yyyy-MM-dd HH:mm:ss],
				"createdtime": [yyyy-MM-dd HH:mm:ss],
				"lastchangetime": timeMillis,
				"isorigdeleted": [ 0 | 1 ],
				"marks": marks,
				"attribute": fileInfo / folderInfo,
				"isinfected": [ 0 | 1 ],
				"size": fileSize,
				"ispublic": [ 0 | 1 ]
			}
		]
	}