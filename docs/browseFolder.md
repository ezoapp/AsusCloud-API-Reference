##browseFolder##
[瀏覽目錄(/inforelay/browsefolder/)](https://www.google.com/url?q=https%3A%2F%2Fcreative.asuscloud.com%2Fcontent%2Findex.jsp%3Fp%3Dir%26index%3D3%26len%3D10%26id%3D1%26cid%3D2&sa=D&sntz=1&usg=AFQjCNFnj9p_6nkDNlF6mmj_6weM8cCr-w)
###Input Params###
	{
		"language": locale,
		"folderid": folderId,
		"type": [ FOLDER | DOC | IMAGE | VIDEO | MUSIC | OTHERS ],
		"pageno": pageNo,
		"pagesize": pageSize,
		"sortby": [ 1 | 2 ],
		"sortdirection": [ 0 | 1 ]
	}

###Output Results###
	{
		"status": statusCode,
		"rawfoldername": browseFolderName,
		"parent": parentFolderId,
		"rootfolderid": rootFolderId,
		"page": {
		"pageno": pageNo,
		"pagesize": pageSize,
		"totalcount": totalCount,
		"hasnextpage": [ 0 | 1 ]
	},
	"folder": [
		{
			"id": folderId,
			"rawfoldername": rawFolderName,
			"treesize": totalFileSize,	
			"isgroupaware": [ 0 | 1 ],
			"isbackup": [ 0 | 1 ],                                   
			"isorigdeleted": [ 0 | 1 ],
			"ispublic": [ 0 | 1 ],
			"createdtime": [yyyy-MM-dd HH:mm:ss],
			"markid": markId
		}
	],
	"file": [
		{
			"id": fileId,
			"rawfilename": rawFileName,
			"isgroupaware": [ 0 | 1 ],
			"size": fileSize,
			"isbackup": [ 0 | 1 ],
			"isorigdeleted": [ 0 | 1 ],
			"isinfected": [ 0 | 1 ],
			"ispublic": [ 0 | 1 ],
			"headversion": versionNumber,
			"createdtime": [yyyy-MM-dd HH:mm:ss],
			"markid": markId
		}
	],
	"owner": ownerId
	}