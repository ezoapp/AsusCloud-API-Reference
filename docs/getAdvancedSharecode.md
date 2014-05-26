##getAdvancedSharecode
[用檔案、目錄ID查詢分享狀態(/fsentry/getadvancedsharecode/)](https://creative.asuscloud.com/content/index.jsp?p=share&index=5&len=14&id=2&cid=3)

###Input Params
	{
		"isfolder": [ 0 | 1 ] ✻,
		"entryid": fileId / folderId ✻
	}

###Output Results
	{
		"status": statusCode,
		"scrip": scrip,
		"sharecode": shareCode,
		"ispasswordneeded": [ 0 | 1 ],
		"isgroupaware": [ 0 | 1 ],
		"shareforuserid": [ shareForUserIds... ],
		"expiredtime": [yyyy-MM-dd HH:mm:ss],
		"folderquota": folderQuotaOfBytes
	}