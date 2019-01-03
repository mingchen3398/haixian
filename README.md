# 小程序壕生鲜说明
`Don't panic`
## 1.1代码说明
该小程序是编者入行业以来的第一个小程序,代码逻辑思维不够成熟,因而使用面向过程的方式编写了这个小程序,致使代码顺序比较乱;其中部分变量,函数及注释命名不太规范,大量的`console.log()`没来得及注释清理,有可能使得小程序在使用过程中缓存体积越来越大
## 1.2文件配置说明
在`project.config.json`里的`appid`里填上你申请的小程序appid,效果如下:
```javascript
	"compileType": "miniprogram",
	"libVersion": "2.4.3",
	"appid": "你的appid",
	"projectname": "00%E5%A3%95%E7%94%9F%E9%B2%9C",
```
在`app.js`里的`globalData`里配置你的域名,其中,`serverUrl`为服务器接口域名,`imgUrl`为所有非头像图片的域名,:exclamation:注意,两个域名地址必须以`/`结尾,否则会导致无法解析域名,导致报错,例如,正确域名:`https://api.poshir.top/index.json`,这是域名后加`/`的,错误域名:`https://api.poshir.topindex.json`,这是没加`/`的
## 1.3部分重要接口
微信支付接口:`wxPayCart`,注意,普通开发者没有微信支付id,以及appid与代码里的服务器地址里的appid不一致,所以会提示失败
登录接口:`pages/loginIdex/loginIndex`里的`getUserInfo`方法,注意,appid不一致,导致获取的code不一致,登录会失败,code生成需要后台编写,`code仅参与session检查与微信支付使用`
## 1.4目录说明
--/  
----images(小程序图片文件目录)  
--------agency(代理商页面)  
--------apply(团长申请页面)  
--------bbs(美食家页面)  
--------index(首页页面)  
--------joinHand(商家合作页面)  
--------lib(不好分类的)  
--------message(消息页面)  
--------mine(我的页面)  
--------needU(团长申请静态页面)  
--------pay(微信支付)  
--------purse(钱包页面)  
--------recharge(充值页面)  
--------shopcart(购物车页面)  
--------purse(钱包页面)  
--------sign(签到页面)  
--------purse(钱包页面)  
--------tabbar(底部按钮)  
----pages(小程序页面文件目录)  
--------addTalk(发表评价)  
--------apply(团长申请)  
--------addTalk(发表评价)  
--------bargNotice(交易通知)  
--------bbs(美食家)  
--------bbs----bbsItem(评价详情)  
--------bbsNotice(论坛消息通知)  
--------book(订购)  
--------bookHistory(订购记录)  
--------clearing(购物车结算)  
--------complaint(意见箱)  
--------complaintHistory(意见箱历史记录)  
--------contribute(投稿)  
--------contributeHistory(投稿历史记录)  
--------forgetPwd(忘记密码)  
--------index(首页)  
--------joinHand(商家合作)  
--------login(手机登录)  
--------loginIndex(微信登录;手机登录按钮已删除)  
--------map(地图)  
--------message(我的消息)  
--------mine(我的含代理商)  
--------mine----aFunction(代理商功能页面)  
--------mine----userInfo(我的信息)  
--------msgNotice(我的消息里的消息通知)  
--------needU(团长招募静态)  
--------order(订单)  
--------order----create(详情页面直接购买)  
--------order----done(已完成订单)  
--------orderDetail(待付款订单详情)  
--------presell(预售)  
--------productItem(商品详情)  
--------purse(钱包)  
--------recharge(充值)  
--------refund----applicationForRefund(申请退款)  
--------refund(退款)  
--------register(手机注册)  
--------shopcart(购物车)  
--------signIn(签到)  
--------tricket(直接购买使用优惠券)  
--------tricket----tricketCart(购物车下单使用优惠券)  
--------waitGoods(待提货)  
--------withdrawlDeposit(提现)  
--------withdrawlDeposit----withdrawlAgency(代理商提现)  
----utils(小程序引用文件目录)  

##
##
