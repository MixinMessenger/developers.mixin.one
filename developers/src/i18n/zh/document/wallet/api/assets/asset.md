# 资产详情

### `GET /assets/:id` 

返回用户的单个资产信息, 第一次访问会同时获取这个资产的充值地址, 需要注意的问题:

- 机器人用户访问，需要用自己的私钥签名
- 如果要访问其它用户的资产信息，需要获取用户授权
- 第一次请求资产详情时 destination 可能不会马上有值，可间隔 2 秒轮询获取用户的充值地址

```
$$XIN:curl$$ "https://api.mixin.one/assets/3596ab64-a575-39ad-964e-43b37f44e8cb"
```

```json
{
  "data":{
    $$XIN:asset$$
  }
}
```
