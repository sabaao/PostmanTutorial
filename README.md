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

# Cathay holdings login url
[員工入口網](https://w3.cathaylife.com.tw/eai/ZPWeb/login.jsp?)

# Postman tutorial
## Global variable and environment variable
### environment variable
可以從右上角齒輪設定

### global variable
在不同的environment中共同使用
若environment variable跟global variable重複的話，會以environment為主

## preScript and Tests process
![process](https://pic1.xuehuaimg.com/proxy/csdn/https://img-blog.csdn.net/20171014222417298?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvdTAxMzYxMzQyOA==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

## Tests script
![script sample](images/script_sample.png)

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