# conda

-  conda 管理执行环境
`` conda create -n python35 python=3.5 anaconda``
这里安装的是相关的所有anaconda的包
(如果只是想要一个环境，用不到这些包可以执行conda create -n python35 python=3.5，这句代码只会安装几个基础包)

- To activate this environment, use

    ``$ conda activate python35``

- To deactivate an active environment, use

    ``$ conda deactivate``


``conda install -c conda-forge ta-lib``


ubuntu 安装TA-Lib
可能需要参考https://blog.csdn.net/vivian187/article/details/51750639安装编译器

wget http://prdownloads.sourceforge.net/ta-lib/ta-lib-0.4.0-src.tar.gz
tar xf ta-lib-0.4.0-src.tar.gz
cd ta-lib
./configure --prefix=/usr
make
sudo make install
pip install TA-Lib