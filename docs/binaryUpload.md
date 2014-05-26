##binaryUpload
以[串流(Stream)](https://creative.asuscloud.com/content/?p=updownload&index=7&len=6&id=2&cid=3&list3=1)為基礎所進行檔案上傳，支援斷點自動續傳。

相關API：  

[Step1:初始化串流檔案上傳／續傳(/webrelay/initbinaryupload/)](https://creative.asuscloud.com/content/?p=updownload&headerId=3&index=7&len=6&id=3&cid=4&list3=1)  
[Step2:串流檔案上傳／續傳(/webrelay/resumebinaryupload/)](https://creative.asuscloud.com/content/?p=updownload&headerId=3&index=7&len=6&id=4&cid=5&list3=1)  
[Step3:完成串流檔案上傳／續傳(/webrelay/finishbinaryupload/)](https://creative.asuscloud.com/content/?p=updownload&headerId=3&index=7&len=6&id=5&cid=6&list3=1)  

###Input Params
	{
		"na": fileName ✻,
		"pa": parentFolderId ✻,
		"at": attribute,
		"fs": fileSize,
		"fi": fileId,
		"sc": syncFolderId,
		"igw": [ 0 | 1 ]
	}

###Output Results
	{
		"status": statusCode,
		"fileid": fileId,
	}