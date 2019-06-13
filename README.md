# Postman tutorial and auto login
## Skill
Html, Javascript, Chrome debug mode.

## Postman install
Download and install from [here](https://www.getpostman.com/downloads/).

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

# Mock Server
## Create mock server
![create mock server](images/postman_create_mock_server.png)

## Configuration mock server
![config](images/postman_configuration_mock_server.png)

## Get mock server url
![mock server url](images/postman_get_mock_server_url.png)

## Add mock api
![add mock api](images/postman_add_mock_api.png)

## Add response example
![add response example](images/postman_add_example.png)
![save response example](images/postman_save_example.png)

## Send mock api from postman
![mock api](images/postman_send_mock_api.png)

### Send mock api from Chrome
![mock api from Chrome](images/chrome_send_mock_api.png)

# Monitor Server

## Create Collection
Url is [https://httpbin.org/json](https://httpbin.org/json)
and add default test case of http 200.
![test collection](images/monitor_test_collection.png)

## Create monitor
![create monitor](images/monitor_create_monitor.png)

## Monitor configuration
Free account only can use hour timer.
You can setting receive email when run fail.
![config](images/monitor_configuration.png)
![create success](images/monitor_create_success.png)

## Run monitor
### Open web page
Click monitor column will open monitor web page.
![open web page](images/monitor_web_page.png)
If click run button, it will create report.
![report](images/monitor_report.png)

## Auto send alert mail
Add a fail test case in test script.
```javascript
pm.test("Your test name", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.slideshow.author).to.eql("lalala");
});
```
And run it, you will receive alert mail.

![alert mail](images/monitor_alert_mail.png)

# Demo auto login

## Use Chrome debug mode
Setting->更多工具->開發人員工具(shortcut: command + option + i)
![chrome](images/chrome.png)

### Network
#### Review api history and detail.
![network](images/chrome_network.png)
#### Api detail information.
![detail infomation](images/api_detail.png)

## api list
[checkin](checkin.postman_collection.json)

[checkout](checkout.postman_collection.json)



# Auto login Robo
## Install nodejs
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

## Check in
```bash
newman run checkin.postman_collection.json --environment cathay.prod.postman_environment.json 
```
## Check out
```bash
newman run checkout.postman_collection.json --environment cathay.prod.postman_environment.json 
```

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

# Reverence
[Monitor](https://medium.com/%E4%B8%80%E5%80%8B%E4%BA%BA%E7%9A%84%E6%96%87%E8%97%9D%E5%BE%A9%E8%88%88/postman-monitor-api%E7%9B%A3%E6%8E%A7%E8%87%AA%E5%8B%95%E5%9B%9E%E5%A0%B1-5fd55aeb880d)

[Mock](https://www.itread01.com/content/1543261216.html)