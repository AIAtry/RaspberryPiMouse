# RaspberryPiMouse

[![Build Status](https://travis-ci.org/rt-net/RaspberryPiMouse.svg?branch=master)](https://travis-ci.org/rt-net/RaspberryPiMouse)

This repository has the source code and kernel objects
for the Raspberry Pi mouse.

## インストール

./utilディレクトリのシェルスクリプトを実行します。

```
$ git clone https://github.com/rt-net/RaspberryPiMouse.git
$ cd utils
###Raspbianの場合###
$ ./build_install.raspbian.bash
###Ubuntuの場合（ubuntu14とありますがUbuntu Linux 16.04でもインストール可能です）###
$ ./build_install.ubuntu14.bash
```


## How to install the device driver（マニュアルインストール）

```
$ git clone https://github.com/rt-net/RaspberryPiMouse.git
### check the kernel version
$ uname -r
4.1.6-v7+
###choose a directory based on your RPi and the kernel version
$ cd RaspberryPiMouse/lib/Pi2B+/4.1.6-v7+/
###install the kernel object
$ sudo insmod rtmouse.ko
```

## ドライバの導入の際の注意

以下の設定を確認ください。
raspi-configコマンドで設定します。

* SPI機能を「入」にする。

2017年1月現在、以下の設定は不要です。  
rtmouseをインストールして不具合が出た場合のみ以下の設定を追加で行ってください。

* Device Tree機能を「切」にする。

## 日経Linux連載

連載（Raspberry Piで始めるかんたんロボット製作）で上田氏が書いた
シェルスクリプトは下記にあります。

https://github.com/ryuichiueda/RPiM


## License

This repository is licensed under the GPLv3 License, see [LICENSE](./LICENSE).

このリポジトリはGPLv3ライセンスで公開されています。詳細は[LICENSE](./LICENSE)を確認してください。

### Includings

This repository contains the code of the repository shown below.

このリポジトリは以下に示すリポジトリのコードを一部含みます。

* [take-iwiw/DeviceDriverLesson](https://github.com/take-iwiw/DeviceDriverLesson)
  * BSD License
* [mcp3204.c in Raspberry Piで学ぶARMデバイスドライバープログラミング](http://www.socym.co.jp/support/s-940#ttlDownload)
  * GPL v2 License
