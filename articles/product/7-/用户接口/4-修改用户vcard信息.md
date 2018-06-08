### 修改用户vcard信息

#### 1.功能说明:
*调用该接口修改指定用户的vcard信息，包括昵称、邮箱、职位、手机号、分机号、头像等属性。不能修改usernam和组织。在开放模式下用户如果不存在会创建该用户和相应vcard信息。*
***

#### 2.请求体说明：


|URL|https://im.yyuap.com/sysadmin/rest/remotevcard/{etpId}/{appId}/updateVcard|
|----|----|
|Header|{"Content-Type":"application/json"}|
|Header|{"Authorization"：apptoken}|
|method|PUT|

#### 3.请求参数说明:

*参数以JSON格式提交，如下：*

	{
		"username": "zongtengfei",
		"nickname": "昵称",
		"password": "密码",
		"email": "邮箱",
		"orgId": "组织ID",
		"photo": "头像",
		"position": "职位",
		"location": "工位",
		"number": "工号",
		"gender": "性别",
		"remarks": "备注信息",
		"mobile": "手机",
		"telephone": "分机号"
	}

|参数名称|类型|意义|是否必须|
|----|----|----|----|
|token|String|App的token|是|
|etpId|String|企业Id|是|
|appId|String|应用Id|是|
|username|String|用户名|是|
|nickname|String|新的用户的昵称|否，仅在需要修改时传入|
|password|String|新的密码|否，仅在需要修改时传入|
|email|String|新的邮箱|否，仅在需要修改时传入|
|photo|String|新的头像|否，仅在需要修改时传入|
|position|String|新的职位|否，仅在需要修改时传入|
|location|String|新的办公地点|否，仅在需要修改时传入|
|number|String|新的工号|否，仅在需要修改时传入|
|gender|String|新的性别|否，仅在需要修改时传入|
|remarks|String|新的备注|否，仅在需要修改时传入|
|mobile|String|新的手机号|否，仅在需要修改时传入|
|telephone|String|新的分机号|否，仅在需要修改时传入|

#### 4.返回值：

	{
   	 "result": "success"
	}

	