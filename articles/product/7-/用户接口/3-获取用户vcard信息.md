### 获取用户vcard信息

#### 1.功能说明:
*调用该接口获取指定用户的vcard信息，包括昵称、邮箱、职位、手机号、分机号、头像等属性。请求的用户如果不存在接口会返回一个空的vcard对象。*
***

#### 2.请求体说明：

|----|----|
|URL|https://im.yyuap.com/sysadmin/rest/remotevcard/{etpId}/{appId}?username=|
|Header|{"Authorization"：apptoken}|
|method|GET|


#### 3.参数说明：

|参数名称|类型|意义|是否必须|
|----|----|----|----|
|token|String|App的token|是|
|etpId|String|企业Id|是|
|appId|String|应用Id|是|
|username|String|要获取的用户的用户名|是|

#### 4.成功返回内容：

|----|----|
|格式|JSON|
|username|String，用户标识|
|name|String，用户的昵称|
|email|String，邮箱|
|orgId|String，组织id|
|photo|String，头像|
|position|String，职位|
|location|String，办公地点|
|number|String，工号|
|gender|String，性别|
|remarks|String，备注|
|mobile|String，手机号|
|telephone|String，分机号|


	{
    	"appId": "im_pre",
    	"email": "邮箱",
    	"etpId": "yonyou",
    	"gender": "性别",
    	"location": "工位",
    	"mobile": "手机",
    	"nickname": "昵称",
    	"number": "工号",
    	"orgId": "组织ID",
    	"photo": "头像",
    	"position": "职位",
    	"remarks": "备注信息",
    	"telephone": "分机号",
    	"username": "zongtengfei.im_pre.yonyou"
	}