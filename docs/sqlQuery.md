##sqlQuery
[檔案或目錄名稱查詢(/fulltext/sqlquery/)](https://creative.asuscloud.com/content/?p=search)

###Input Params
	{
		"keyword": keyword ✻,
		"markid": markId,
		"kind": [ 0 | 1 ],
		"ancestorid": parentFolderId,
		"pagesize": pageSize,
		"offset": offset,
		"ext": fileExtension
	}

###Output Results
	{
		"status": statusCode,
		"total": total,
		"entry": [
			{
				"id": fileId / folderId,
				"parent": parentFolderId,
				"rawentryname": rawFileName / rawFolderName,
				"kind": [ 0 | 1 ],
				"isinfected": [ 0 | 1 ],
				"time": [yyyy-MM-dd HH:mm:ss],
				"ispublic": [ 0 | 1 ],
				"isorigdeleted": [ 0 | 1 ],
				"marks": markIds,
				"attribute": attribute,
				"size": fileSize,
				"lastchangetime": [yyyy-MM-dd HH:mm:ss]	
			}
		]
	}