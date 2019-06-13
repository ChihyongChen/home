---
layout:     post
title:      "加速访问Github"
subtitle:   "快就完事了"
date:       2019-06-13 23:55:00
author:     "陈志勇"
header-img: "img/post-bg-2015.jpg"
catalog: true
tags:
    - 加速
    - Github
---

> “天下武功，唯快不破...... ”

转自https://blog.csdn.net/u011275684/article/details/79655038

访问GitHub经常很慢，通过**绕过dns解析，在本地直接绑定host**，该方法也可加速其他因为CDN被屏蔽导致访问慢的网站。 

在本地host文件中添加映射，步骤如下：

1、用文本编辑器打开C:\Windows\System32\drivers\etc\hosts

2、打开 http://tool.chinaz.com/dns(查询域名映射关系工具)

3、查询 github.global.ssl.fastly.net 和 assets-cdn.github.com 两个地址

4、多查几次，选择一个稳定，延迟(TTL)较低的 ip 按如下方式添加到host文件 

如将下列信息添加到host文件中

# github

151.101.109.194  github.global.ssl.fastly.net

185.199.111.153 assets-cdn.github.com

5、保存文件，重新打开浏览器

有时候改完hosts文件没立即生效，需要刷新DNS缓存

windows下刷新DNS的方法：

打开CMD

输入ipconfig /flushdns

Linux下刷新DNS的方法：

输入指令：sudo /etc/init.d/networking restart 即可。

然后，你关闭浏览器再访问github就起飞了。





