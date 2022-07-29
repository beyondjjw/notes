Ubuntu20.04/22.04 安装vmware 教程/完美解决安装失败
原因：

较新的内核版本在构建内核模块 VMMON 和 VMNET 方面存在问题。这将/可能发生在 ubuntu 20.04 以及更新版本中。
解决办法：

本文基于vmware 16.2.3 和 内核 5.15.0

如果不是该版本请下载在对应版本的替换文件

安装gcc 编译器

sudo apt install build-essential
1
下载替换文件，可直接访问下方网址，选择和自己系统和vmware版本对应的替换文件。

wget https://github.com/mkubecek/vmware-host-modules/archive/refs/tags/w16.2.3-k5.15.tar.gz
1
提取文件

tar -xzf workstation-15.5.1.tar.gz
1
进入目录

cd vmware-host-modules-w16.2.3-k5.15/
1
创建模块文件

tar -cf vmmon.tar vmmon-only
tar -cf vmnet.tar vmnet-only
1
2
将文件复制到对应目录

sudo cp -v vmmon.tar vmnet.tar /usr/lib/vmware/modules/source/
1
安装模块

sudo vmware-modconfig --console --install-all
1
输出：

结尾输出以下结果即为成功
如果不全部是done ，关闭bios的安全启动 然后重新启动电脑 然后再执行步骤7即可


Starting VMware services:
   Virtual machine monitor                                   done
   Virtual machine communication interfac                    done
   VM communication interface socket family                  done
   Blocking file system                                      done
   Virtual ethernet                                          done
   VMware Authentication Daemon                              done
   Shared Memory Available                                   done    

1
2
3
4
5
6
7
8
9
10
