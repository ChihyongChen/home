---
layout:     post
title:      "mysql数据库直接复制data里的文件夹不能正常使用解决办法"
subtitle:   "坑爹mysql"
date:       2019-06-16 20:26:00
author:     "陈志勇"
header-img: "img/post-bg-2015.jpg"
catalog: true 
tags:
    - Mysql
    - 专治疑难杂症
---

> “不断探索...... ”


当我们直接复制 mysql/data 下的数据库文件（如 test/ 文件夹）到新的mysql/data目录下，打开数据库管理软件或者phpmyadmin时，会提示找不到表，但是表名都可以正常显示

### 解决办法

复制 **mysql/data/** 文件夹下的 **ibdata1** 到新的 mysql/data 文件夹，注意：不是我们自己创建的数据库文件夹下
