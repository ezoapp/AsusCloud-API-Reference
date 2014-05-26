##getInfo##
[使用者帳戶資訊(/member/getinfo/)](https://www.google.com/url?q=https%3A%2F%2Fcreative.asuscloud.com%2Fcontent%2Findex.jsp%3Fp%3Dir%26index%3D3%26len%3D10%26id%3D0%26cid%3D1&sa=D&sntz=1&usg=AFQjCNGFd0-SxEg4lh-qWY_eP7at2OdSpg)
###Input Params###
	{
	"time": timeStamp,
	}
###Output Results###
	{
		"status": statusCode,
		"account": accountId,
		"email": email,
		"regyear: regYear,
		"language": locale,
		"activateddate": [yyyy-MM-dd HH:mm:ss],
		"credential": OTP_Credential_ID,
		"credentialstate": credentialState,
		"usedbackuppc": usedBackupPc_num,
		"backuppc": [
			{
				"name": name,
				"createdtime": [yyyy-MM-dd HH:mm:ss]		
			}
		],
		"package": {
			"id": packageId,
			"display": packageName,
			"capacity": capacity,
			"uploadbandwidth": uploadbandwidth,
			"downloadbandwidth": downloadbandwidth,
			"upload": upload,
			"download": download,
			"concurrentsession": concurrentsession,
			"maxfilesize": maxfilesize,
			"hasencryption": [ 0 | 1 ],
			"expire": [yyyy-MM-dd HH:mm:ss],
			"maxbackuppc": maxBackupPc,
			"featurelist": [
				{
					"name": featureName,
					"enable": [ 0 | 1 ],
					"property": [
						{
							"name": propertyName,
							"value": propertyValue
						}
					]
				}
			]
	},
		"usedcapacity": usedCapacity,
		"freecapacity": freeCapacity
	}