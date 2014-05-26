##setAdvancedSharecode
[分享檔案或目錄(/fsentry/setadvancedsharecode/)](https://creative.asuscloud.com/content/index.jsp?p=share&index=5&len=14&id=1&cid=2)

###Input Params
	{
		"isfolder": [ 0 | 1 ] ✻,
		"entryid": fileId / folderId ✻,
		"clearshare": [ 0 | 1 ],
		"clearpassword": [ 0 | 1 ],
		"clearvalidityduration": [ 0 | 1 ],
		"releasequotalimit": [ 0 | 1 ],
		"password": password,
		"validityduration": validityDurationOfHrs,
		"isgroupaware": [ 0 | 1 ],
		"shareforuserid": [ shareForUserIds... ],
		"folderquota": folderQuotaOfBytes
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
		"folderquota": folderQuotaOfBytes,
		"invaliduserid": [ invalidUserIds... ]
	}