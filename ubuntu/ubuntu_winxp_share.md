在Liunx操作系统上，安装了virtualBox,然后在virtualBox中安装了一个XP系统，但是我想在XP下访问Linux下的一些目录，然后阅读里面的文件。
- 1.  首先是安装VirtualBox,这个在Ubuntu下很简单，在software center中查找VirtualBox后，安装就可以的了。

- 2. 安装windows操作系统，这个跟平时我们安装的一样。

- 3. 安装增强包 点击进入xp后你会发现鼠标在主机和xp之间不能随便移动，而要需要按右边的Crtl切换出来，比较不方便。其实只需要安装了 VirtualBox增强包就行了。安装后VirtualBox就可以像普通的应用程序窗口那样，在主机和虚拟系统之间自由切换了。打开虚拟机，点击菜单“ 设备(Devices)“ ->安装增强功能(Install Guest Additions)，你的WindowsXP就会弹出一个安装界面，会叫你安装VirtualBox Guest Additions。如果点击没有反应的话，先选择"设备"-> CD/DVD Devices，勾选VirtualBox Guest Additions，然后再点击菜单“ 设备“ ->安装增强功能，然后一路next下去就行了。这样你的鼠标就可以在主机和虚拟机之间自由移动。

- 4. 创建目录共享

- 4.1 在虚拟机的菜单" 设备(Devices)"-->"(Shared Folder)分配数据空间"中新建，然后选择你所要共享的文件夹,

- 4.2 选择打开虚拟机，在我的电脑上单击右键，选择映射网络驱动器。

       驱动器，这个地方的字母是选在你windows中没有出现过的盘符，就是说你选择的盘符没有被占用。

       文件夹就是这个格式：\\VBOXSVR\Documents(这里的documents就是你想要共享的目录)

- 4.3 然后在我的电脑中就可以看到另外一个盘符了，实现与linux共享了。