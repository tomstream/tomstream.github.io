---
layout: post
title: import caffe时出错：can not find module skimage.io
---

在Ubuntu下安装配置深度学习库caffe时，如果想使用python接口，按照官方文档说明，需要执行下面的sh命令来获取依赖库：
		
		for req in $(cat requirements.txt); do pip install $req; done

然而，由于一些网络环境的原因，有些依赖库不能使用pip工具成功安装，导致出现can not find module skimage.io错误。


在经过多番尝试后，我使用apt-get命令可以成功安装所有依赖库。
此时只要按照以下命令操作即可：

	sudo apt-get install python-numpy python-scipy python-matplotlib python-sklearn python-skimage python-h5py python-protobuf python-leveldb python-networkx python-nose python-pandas python-gflags Cython ipython 
	$ sudo apt-get update

在caffe-master目录下：

	make pycaffe

然后在命令行输入python;再输入import caffe就可以成功啦。

参考资料：
[import caffe时出错：can not find module skimage.io](http://blog.csdn.net/tsinghuahui/article/details/46790705)