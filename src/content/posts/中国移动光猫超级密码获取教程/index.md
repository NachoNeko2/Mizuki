---
title: 中国移动光猫超级密码获取教程
published: 2026-03-28
description: 中国移动光猫超级密码获取教程
image: ./cover.jpg
tags: ["中国移动", "教程"]
category: 教程
draft: false
pinned: false
author: Fate命定指冠
lang: zh
sourceLink: https://dmm.ink/2024/10/04/h5-9telnet
---

## 前言
中国移动光猫超级密码获取教程（理论通用）,我用的H5-9

![](https://pic.fatetech.cc.cd/file/1774665095886_QQ%E6%88%AA%E5%9B%BE20260328101853.png)

话不多说开始教程
## 打开光猫的Telnet功能
在浏览器输入:
```
http://192.168.1.1/usr=CMCCAdmin&psw=aDm8H%MdA&cmd=1&telnet.gch
```
型号是PT924G，可以用以下方法打开Telnet
```
http://192.168.1.1/cgi-bin/abcdidfope94e0934jiewru8ew414.cgi
```

[![提示这个就证明开启成功](https://pic.fatetech.cc.cd/file/1774666883620_QQ%E6%88%AA%E5%9B%BE20260328101853.png "提示这个就证明开启成功")](https://pic.fatetech.cc.cd/file/1774666883620_QQ%E6%88%AA%E5%9B%BE20260328101853.png "提示这个就证明开启成功")

提示这个就证明开启成功

## 打开电脑的Telnet模式
在控制面板里面：程序-启用或关闭windows功能，开启Telnet功能等待完成即可。（找不到的话把图标改成类别）

[![](https://pic.fatetech.cc.cd/file/1774667216952_QQ%E6%88%AA%E5%9B%BE20260328110633.png)](https://pic.fatetech.cc.cd/file/1774667216952_QQ%E6%88%AA%E5%9B%BE20260328110633.png)

## 打开CMD
输入(字母和数字间要有一个空格)：```telnet 192.168.1.1```

然后账户为`CMCCAdmin`

密码为`aDm8H%MdA`

***你不会觉得默认的密码不对吧，我也觉得，可他就是对的，我也没办法。***


## 后面依次输入以下代码即可获取

```
sidbg 1 DB p DevAuthInfo
sidbg 1 DB decry /userconfig/cfg/db_user_cfg.xml
cd /tmp
vi debug-decry-cfg
/DevAuthInfo
```

## 最后

最后显示这个就完成了，图片指向的就是超级管理员密码了CMCCAdmin+数字+！

[![](https://pic.fatetech.cc.cd/file/1774668334380_QQ%E6%88%AA%E5%9B%BE20260328112511.png)](http://https://pic.fatetech.cc.cd/file/1774668334380_QQ%E6%88%AA%E5%9B%BE20260328112511.png)

## 高阶玩法：

下面命令可自定义修改超管账号和密码

```
sidbg 1 DB set DevAuthInfo 0 User CMCCAdmin
sidbg 1 DB set DevAuthInfo 0 Pass aDm8H%MdA
```
