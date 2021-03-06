
# ionic-float-native-android-library
1. the plugin name is **cordova-plugin-float-window**
2. the plugin clobbers name is **cordova.plugins.FloatWindow**
## How to install
```shell
cordova plugin add https://github.com/maruiwhu/ionic-float-native-android-library
```
## How to uninstall
```shell
cordova plugin rm cordova-plugin-float-window
```
### Api
#### 显示悬浮窗
showFloat(arg0, successCallBack, errorCallBack)

|    param |    type |   description  |
| --- | --- | --- |
|  arg0   |  array   |   图片名称，显示的优惠券信息，需要传数组形式  |
|    successCallback |  	onSuccess（function）   |  点击悬浮窗事件会调用到这里   |
|errorCallBack  | onError(function) | 执行失败的回调|

 example：
```javascript
 cordova.plugins.FloatWindow.showFloat(['icon.png','券：200.0 佣金：4.18 '],result=>alert(result),error=>alert(error))
 ```
#### 隐藏悬浮窗
hideFloat(arg0, successCallBack, errorCallBack)

|    param |    type |   description  |
| --- | --- | --- |
|  arg0   |  array   |   不需要参数，传空即可  |
|    successCallback |  	onSuccess（function）   |  调用成功   |
|errorCallBack  | onError(function) | 执行失败的回调|

example：
```javascript
cordova.plugins.FloatWindow.hideFloat([],result=>alert(result),error=>alert(error))
```
#### 注册监听剪切板
registerClipBoard(arg0, successCallBack, errorCallBack)

|    param |    type |   description  |
| --- | --- | --- |
|  arg0   |  array   |   不需要参数，传空即可  |
|    successCallback |  	onSuccess（function）   |  方法调用成功，剪切板有内容会调用这里   |
|errorCallBack  | onError(function) | 执行失败的回调|

example：
```javascript
cordova.plugins.FloatWindow.registerClipBoardListener([],result=>alert(result),error=>alert(error))
```
#### 解注册监听剪切板
unRegisterClipBoard(arg0, successCallBack, errorCallBack)

|    param |    type |   description  |
| --- | --- | --- |
|  arg0   |  array   |   不需要参数，传空即可  |
|    successCallback |  	onSuccess（function）   |  调用成功   |
|errorCallBack  | onError(function) | 执行失败的回调|

example： 
```javascript
cordova.plugins.FloatWindow.unRegisterClipBoardListener([],result=>alert(result),error=>alert(error))
```
#### 获取剪切板内容
getClipboardContent(arg0, successCallBack, errorCallBack)

|    param |    type |   description  |
| --- | --- | --- |
|  arg0   |  array   |   不需要参数，传空即可  |
|    successCallback |  	onSuccess（function）   |  方法调用成功，剪切板内容通过这个函数返回   |
|errorCallBack  | onError(function) | 执行失败的回调|

example：
```javascript
cordova.plugins.FloatWindow.getClipboardContent([],result=>alert(result),error=>alert(error))
```

#### 启动app
startApp(arg0, successCallBack, errorCallBack)

|    param |    type |   description  |
| --- | --- | --- |
|  arg0   |  array   |   包名  |
|    successCallback |  	onSuccess（function）   |  启动成功   |
|errorCallBack  | onError(function) | 执行失败的回调（可能未安装指定包名应用）|

example： 
```javascript
cordova.plugins.FloatWindow.startApp(['com.taobao.taobao'],result=>alert(result),error=>alert(error))
```

#### 检测app是否安装
checkAppInstalled(arg0, successCallBack, errorCallBack)

|    param |    type |   description  |
| --- | --- | --- |
|  arg0   |  array   |   包名  |
|    successCallback |  	onSuccess（function）   |  已安装回调  |
|errorCallBack  | onError(function) | 未安装或其他异常回调|

example： 
```javascript
cordova.plugins.FloatWindow.checkAppInstalled(['com.taobao.taobao'],result=>alert(result),error=>alert(error))
```

#### 检测是否有悬浮窗权限
checkOverlaysPermission(arg0, successCallBack, errorCallBack)

|    param |    type |   description  |
| --- | --- | --- |
|  arg0   |  array   |   空  |
|    successCallback |  	onSuccess（function）   |  有权限  |
|errorCallBack  | onError(function) | 无权限|

example： 
```javascript
cordova.plugins.FloatWindow.checkOverlaysPermission([],result=>alert(result),error=>alert(error))
```

#### 启动悬浮窗设置页面
requestOverlaysPermission(arg0, successCallBack, errorCallBack)

|    param |    type |   description  |
| --- | --- | --- |
|  arg0   |  array   |   空  |
|    successCallback |  	onSuccess（function）   |  启动成功  |
|errorCallBack  | onError(function) | 启动失败|

example： 
```javascript
cordova.plugins.FloatWindow.requestOverlaysPermission([],result=>alert(result),error=>alert(error))
```
## 调用时序图

![时序图](https://github.com/maruiwhu/privateNote/blob/master/images/1537925889632.png)
