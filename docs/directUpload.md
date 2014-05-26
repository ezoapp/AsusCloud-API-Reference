##directUpload
[Multipart Upload(/webrelay/directupload/)](https://creative.asuscloud.com/content/index.jsp?p=updownload&index=7&len=6&id=1&cid=1&list3=1)

###Input Params
	{
		"pa": parentFolderId,
			"fileuri": fileUri,
		"d": fileName,
		"u": responseURL,
		"pr": progressId,
		"at": attribute,
		"fs": fileSize,
		"fi": fileId,
		"ar": [ 0 | 1 ],
		"rn": rename
	}

###Output Results
	{
		"status": statusCode,
		"fileid": fileId,
		"rawfilename": fileName
	}