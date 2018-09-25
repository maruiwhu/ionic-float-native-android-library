# ionic-float-native-android-library
the plugin name is cordova-plugin-float-window
the plugin clobbers name is cordova.plugins.FloatWindow
## How to install
cordova plugin add https://github.com/maruiwhu/ionic-float-native-android-library
## How to uninstall
cordova plugin rm cordova-plugin-float-window
### Api
#### 显示悬浮窗
showFloat(content, success, error)
  > content 悬浮窗内容 优惠券信息，需要传数组形式
  > success 点击悬浮窗事件会调用到这里
  > error 方法调用异常
 example： cordova.plugins.FloatWindow.showFloat(['this is a title'],result=>alert(result),error=>alert(error))
#### 隐藏悬浮窗
hideFloat(arg0, success, error)
  > content 传空数组
  > success 方法调用成功
  > error 方法调用异常
example： cordova.plugins.FloatWindow.hideFloat([],result=>alert(result),error=>alert(error))
#### 注册监听剪切板
registerClipBoard(arg0, success, error)
 > content 传空数组
  > success 方法调用成功，剪切板有内容会调用这里
  > error 方法调用异常
example： cordova.plugins.FloatWindow.registerClipBoardListener([],result=>alert(result),error=>alert(error))
#### 解注册监听剪切板
unRegisterClipBoard(arg0, success, error)
  > content 传空数组
  > success 方法调用成功
  > error 方法调用异常
example： cordova.plugins.FloatWindow.unRegisterClipBoardListener([],result=>alert(result),error=>alert(error))
