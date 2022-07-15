# beyondcompare
今天打开beyond compare，提示密钥到期，无法打开，在网上找到答案，记录一下备忘。

解决方法：

在/Home/ .config/ bcompare文件夹下删除BCState.xml、BCState.xml.bak文件，重新启动beyond compare，可以正常使用了。

因为 .config文件夹被隐藏了，使用命令行进入到文件夹/Home/ .config/ bcompare，进行删除文件。

