# Skill
Html, Javascript, Chrome debug mode.

# Prepare install
## Postman
Download and install from [here](https://www.getpostman.com/downloads/).
## Nodejs
Download and install from [here](https://nodejs.org/en/).
### Verify nodejs install success
Open terimal, and input command.

```
node -v
```
If console show node's version, it mean you install success.

### install newman plugin
```
npm install -g newman
```
Verify newman install success.

```
newman -v
```


# Postman tutorial
## Global variable and environment variable
### environment variable
可以從右上角齒輪設定
![manage environment](images/manage_environment.png)

### global variable
在不同的environment中共同使用
若environment variable跟global variable重複的話，會以environment為主

## preScript and Tests process
![process](https://pic1.xuehuaimg.com/proxy/csdn/https://img-blog.csdn.net/20171014222417298?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvdTAxMzYxMzQyOA==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

## Tests script
![script sample](images/script_sample.png)

## Mock Server
### Create mock server
![create mock server](images/postman_create_mock_server.png)

### Configuration mock server
![config](images/postman_configuration_mock_server.png)

### Get mock server url
![mock server url](images/postman_get_mock_server_url.png)

### Add mock api
![add mock api](images/postman_add_mock_api.png)

### Add response example
![add response example](images/postman_add_example.png)
![save response example](images/postman_save_example.png)

### Send mock api from postman
![mock api](images/postman_send_mock_api.png)

### Send mock api from Chrome
![mock api from Chrome](images/chrome_send_mock_api.png)

# Cathay holdings login url
[員工入口網](https://w3.cathaylife.com.tw/eai/ZPWeb/login.jsp?)

## Use Chrome debug mode
Setting->更多工具->開發人員工具(shortcut: command + option + i)
![chrome](images/chrome.png)

### Network
#### Review api history and detail.
![network](images/chrome_network.png)
#### Api detail information.
![detail infomation](images/api_detail.png)

## api list


# run newman command
## Check in
```bash
newman run checkin.postman_collection.json --environment cathay.prod.postman_environment.json 
```
## Check out
```bash
newman run checkout.postman_collection.json --environment cathay.prod.postman_environment.json 
```

# Setting crontab on Mac

# Restrict
Must use cathaybk wifi.

# Q & A
## Q1. Why I can not use api login?
### Answer
Someone will get 302 error when they login, it is server side bug, but I don't who will happen.

## Q2. Account and password wrong.
### Answer
You need modify cathay.prod.postman_environment.json.
To change username and password.