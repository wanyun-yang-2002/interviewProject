# 测试
## 注册用户
```bash
curl --location "http://127.0.0.1:8000/signup/" --header "Content-Type: application/json" --data-raw "{\"email\": \"test@test.com\", \"password\": \"123\"}"
```
## 登录用户
```bash
curl --location "http://127.0.0.1:8000/signin/" --header "Content-Type: application/json" --data-raw "{\"email\": \"test@test.com\", \"password\": \"123\"}"
```
记下响应中的 access_token。
## 获取用户信息
```bash
curl --location "http://127.0.0.1:8000/me/" --header "Authorization: Bearer "从登录用户处获得的access_token""
```