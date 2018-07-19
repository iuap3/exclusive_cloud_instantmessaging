### 获取UserToken

#### 1.功能说明:
*调用该接口获取指定租户指定应用下的指定用户的UserToken，UserToken是客户端登录IM服务器认证以及调用服务端接口中的需要验证用户token的接口的口令*
*特别提示：当应用模式为开放注册模式时，调用此接口如果参数userid对应的用户不存在，服务端会创建该用户。*
***

#### 2.请求体说明：


|URL|https://im.yyuap.com/sysadmin/rest/{etpId}/{appId}/token|
|----|----|
|method|POST|
|Header|{"Content-Type":"application/json"}|

#### 3.请求参数说明:
*参数以JSON格式提交，如下：*

	{
		"clientId":"762a8f681f5e5b32760d0b5f8276bb52",
		"clientSecret":"7E39BD8fgh2991D060AB420A6A3123C2",
		"userid":"zongtf",
		"nickname":"宗腾飞",
		"photo":"ancasdsderere"
	}

|参数名称|类型|意义|是否必须|
|----|----|----|----|
|eptId|String|企业ID|是|
|appId|String|应用ID|是|
|clientId|String|创建应用时产生|是|
|clientSecret|String|创建应用时产生|是|
|userid|String|要获取token的用户的用户名|是|
|nickname|String|用户的昵称|否，当传入此参数且不为空时，服务端会将该用户的昵称更新为参数中的值|
|photo|String|用户的头像|否，当传入此参数且不为空时，服务端会将该用户的头像更新为参数中的值|

#### 4.成功返回内容：


|格式|JSON|
|----|----|
|token|String类型，对应的token值|
|expiration|Long类型，token的过期时间戳|


	{
  		"token": "9c1e769b-4228-41df-bd9d-f28b7e8b4bed",
  		"expiration": "1441120983396"
	}