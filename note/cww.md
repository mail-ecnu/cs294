# Homework 1


## install cuDNN

download at [Nvidia](https://developer.nvidia.com/rdp/cudnn-download), need a account. Download three.

- cuDNN Runtime Library for Ubuntu16.04 (Deb)
- cuDNN Developer Library for Ubuntu16.04 (Deb)
- cuDNN Code Samples and User Guide for Ubuntu16.04 (Deb)

How to install, link, [here](https://blog.csdn.net/m0_37924639/article/details/78785699)


进入CUDNN安装包所在目录，执行以下命令：

```
sudo dpkg -i runtime包.deb
sudo dpkg -i developer包.deb
sudo dpkg -i 代码sample包.deb
```
至此，CUDNN安装完成。

验证CUDA和CUDNN是否安装成功
CUDNN的code sample可以用来检查CUDNN和CUDA是否安装成功，执行以下命令：

```
sudo cp -r /usr/src/cudnn_samples_v7/ $HOME
cd $HOME/cudnn_samples_v7/mnistCUDNN
sudo make clean
sudo make
sudo ./mnistCUDNN
```

正常情况下执行以上代码会得到`Test passed!`的结果。如果在make步出错，那么可能gcc需要降级；如果出现CUDA driver version is insufficient for CUDA runtime version，那么或许你的显卡驱动安装失败，或许你之前安装过低版本的nvidia的显卡又没有删掉。

## Tensorflow

I cannot find tf version `1.10.5`, [here](https://github.com/berkeleydeeprlcourse/homework/issues/31)


install [mujoco-py](https://github.com/openai/mujoco-py)
