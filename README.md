# SwitchLanguage
    关于我，欢迎关注~
 [我的博客](http://blog.csdn.net/u011974987) 本Demo地址:[click here](http://blog.csdn.net/u011974987/article/details/50801770);
* 项目描述：
    本Demo主要运用于切换系统语言的功能，一般会在做出厂设置的App 会有这需求，但是Google并没有开放更改系统语言的接口，查看‘FrameWork’ 层'Settings' 源码下，有相关的功能，属于隐藏接口，所以我们利用反射机制来调用系统的API，虽然不是很靠谱，但是满足了我们的需求，我把项目整理的下，放在[GitHub](https://github.com/git-xuhao/SwitchLanguage) 上面了。

* 本Demo效果截图示例如下：

 ![](https://github.com/git-xuhao/SwitchLanguage/raw/master/SwitchLanguage/screenshot/language.gif)  

更新日志：
---------
  * v1.0:
    初始化该项目
    添加了icon。
###NOTICE!!!
----------
   * 需要注意的是调用此方法：
// objIActMag.updateConfiguration(config);
mtdIActMag$updateConfiguration.invoke(objIActMag, config);

    *需要加上权限：android.permission.CHANGE_CONFIGURATION
并且此处会重新调用onCreate方法，我就在这个地方处被坑了一把。（如果调用此方法的时候做了一些逻辑，就注意下）。

最后声明：
----------------
既然是更改系统的配置当然你的签名也应该是系统签名和sharedUserId。不然会类似以下的错误！

error：
------
java.lang.SecurityException: Permission Denial: updateConfiguration() from pid=31594, uid=10099 requires android.permission.CHANGE_CONFIGURATION

各位都注意下吧~

##Thanks!

*[SwitchLanguage](https://github.com/git-xuhao/SwitchLanguage)
