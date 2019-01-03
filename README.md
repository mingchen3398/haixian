# 小程序壕生鲜说明
`Don't panic`
## 代码说明
该小程序是编者入行业以来的第一个小程序,代码逻辑思维不够成熟,因而使用面向过程的方式编写了这个小程序,致使代码顺序比较乱;其中部分变量,函数及注释命名不太规范,大量的`console.log()`没来得及注释清理,有可能使得小程序在使用过程中缓存体积越来越大
## 文件配置说明
在`project.config.json`里的`appid`里填上你申请的小程序appid,效果如下:
```javascript
	"compileType": "miniprogram",
	"libVersion": "2.4.3",
	"appid": "你的appid",
	"projectname": "00%E5%A3%95%E7%94%9F%E9%B2%9C",
```
在`app.js`里的`globalData`里配置你的域名,其中,`serverUrl`为服务器接口域名,`imgUrl`为所有非头像图片的域名,:exclamation:注意,两个域名地址必须以`/`结尾,否则会导致无法解析域名,导致报错,例如,正确域名:`https://api.poshir.top/index.json`,这是域名后加`/`的,错误域名:`https://api.poshir.topindex.json`,这是没加`/`的
## 部分重要接口
微信支付接口:`wxPayCart`,注意,普通开发者没有微信支付id,以及appid与代码里的服务器地址里的appid不一致,所以会提示失败
登录接口:`pages/loginIdex/loginIndex`里的`getUserInfo`方法,注意,appid不一致,导致获取的code不一致,登录会失败,code生成需要后台编写,`code仅参与session检查与微信支付使用`
##
##
##
