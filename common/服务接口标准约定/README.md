## 服务接口标准约定  

### API 地址规则
规则: `http://{server}/api/{api-name}` `{api-name}` 为接口名称, 把中间的 . 替换成 / 即可.

比如 connect.oauth2.me - 查询当前, 对应的地址为 http://{server}/api/connect/oauth2/me

### AccessToken 授权
部分接口访问需要相关的授权验证. 相关接口 参考 `connect.oauth.*`_

系统在 OAuth 2.0 接口验证授权后, 获得 AccessToken, 需要加在接口末尾.

比如 http://{server}/api/connect/oauth2/me?access_token={accessToken}

### HTTP 请求方式
默认 HTTP 请求方式: `POST`

### Content-Type 格式
请求内容如果是 ``JSON`` 格式的文本需要设置 ``Content-Type: application/json``

错误信息格式
```json
{
  "code": "1",
  "description": "error msg"
}
```

> code = 0, 默认情况下表示执行成功.

## connect.oauth.*
OAuth 2.0 接口

### connect.oauth2.authorize
*身份验证*

**输入参数**

| 名称            | 数据类型       | 描述                     |
| ---             | ---            | ---                      |       
| client_id       | 字符串         | App Key                  |
| response_type   | 字符串         | 响应类型 空, code, token |
| redirectUri     | 字符串         | 回调地址                 |
| username        | 字符串         | 帐号                     |
| password        | 字符串         | 密码                     |

**输出参数**

response_type = 空, 返回如下内容

| 名称             | 数据类型      | 描述                     |
| ---              | ---           | ---                      |
| access_token     | 字符串        | 访问令牌                 |
| token_type       | 字符串        | 令牌类型                 |
| expires_in       | 字符串        | 过期时间(单位:秒)        |
| refresh_token    | 字符串        | 新的刷新令牌             |

response_type = code , 跳转到回调地址, 参数为授权码

response_type = token , 跳转到回调地址, 参数为访问令牌信息

### connect.oauth2.token
*获取访问令牌*

**输出参数**

| 名称             | 数据类型      | 描述                     |
| ---              | ---           | ---                      |
| access_token     | 字符串        | 访问令牌                 |
| token_type       | 字符串        | 令牌类型                 |
| expires_in       | 字符串        | 过期时间(单位:秒)        |
| refresh_token    | 字符串        | 新的刷新令牌             |

### connect.oauth2.me
*获取当前用户信息*

### connect.oauth2.refresh
*刷新访问令牌*

**输入参数**

| 名称             | 数据类型      | 描述                     |
| ---              | ---           | ---                      |
| client_id        | 字符串        | App Key                  |
| refresh_token    | 字符串        | 刷新令牌                 |

**输出参数**

| 名称             | 数据类型      | 描述                     |
| ---              | ---           | ---                      |
| access_token     | 字符串        | 访问令牌                 |
| token_type       | 字符串        | 令牌类型                 |
| expires_in       | 字符串        | 过期时间(单位:秒)        |
| refresh_token    | 字符串        | 新的刷新令牌             |
