使用Fiddler抓取APP https接口数据
==============================

* 设置fiddler：打开工具栏--->Tools--->Options--->HTTPS

> 如下图配置：

> ![](http://oqpmmru7y.bkt.clouddn.com/fiddler_https_config.png)
> 
> 选中Capture HTTPS CONNECTS，因为我们要用fiddler获取手机客户端发出的https请求，所以中间的下拉菜单中选中**from remote clients only**。其他按照上图配置。

* 导出fiddler生成的https证书，并在手机上进行安装。

> 单击Actions--->选择 export root certificate to desktop--->将桌面的证书发送到手机上进行安装--->完成以后就可以在fiddler上抓取到app发送的https请求
>
> ![](http://oqpmmru7y.bkt.clouddn.com/FiddlerRoot.png)
> 
> 桌面上会出现如图所示的FiddlerRoot.cer文件，拷贝到手机后，通过设置--->安全--->安装证书，在手机上安装该证书。（注：不同手机型号，此操作步骤会有所不同）
>

* 测试结果：

> 经测试，在手机上安装证书的过程中`vivo`、`oppo`可直接安装，`魅族`则需要输入证书的存取密码（这个目前还没找到在哪里设置，有知道的小伙伴可以告诉我一下）。

*以上都是基于，fiddler可以抓取手机数据的基础上，如果你不知道怎么配置可参考：[http://jingyan.baidu.com/article/03b2f78c7b6bb05ea237aed2.html](http://jingyan.baidu.com/article/03b2f78c7b6bb05ea237aed2.html)*




