##writeStringToFile

將字串資料寫入指定檔案

相關API：
[Multipart Upload(/webrelay/directupload/)](https://creative.asuscloud.com/content/index.jsp?p=updownload&index=7&len=6&id=1&cid=1&list3=1)

###Input Params
	{
		// path有傳值時寫入路徑中的檔案，反之則以fileId存取檔案
		"path": path ✻, 
		"fi": fileId ✻,
		"stringdata": stringData ✻
	}

###Output Results
	{
		"status": statusCode,
		"fileid": fileId,
		"rawfilename": fileName
	}