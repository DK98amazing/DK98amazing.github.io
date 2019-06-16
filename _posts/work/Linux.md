---
layout: post
title: Linux：Linux学习
category: Linux
tags: [Linux]
keywords: Linux
---

## 新版本特性

新版本值得关注的亮点有哪些：

**内存dump命令**

jmap -dump:live,format=b,file=heap.hprof pid

**wireshark抓包命令**

tcpdump -i eth0 dst/src host 192.39.45.66

**Linux 命令**

	
	1. 顯示日期和時間：    date
	2. 显示日历的指令：    cal
	3. 简单好用的计算器：    bc    /    scale=number
	4. 数据同步写入磁盘：    sync
	5. 改变文件的所属群组：    chgrp
	6. 改变文件拥有者：    chown
	7. 改变文件的权限：    chmod
	8. 显示当前所在目录：    pwd
	9. 建立新目录：    mkdir
	10. 删除『空』的目录：    rmdir
	11. 档案与目录的显示：    ls
	12. 复制档案或目录：    cp
	13. 移除档案或目录：    rm
	14. 移动档案与目录，或更名：    mv
	15. 取得路径的文件名与目录名：    basename    dirname
	16. 由第一行开始显示档案内容：     cat
	17. 从最后一行开始显示档案内容：    tac
	18. 只看头几行：    head
	19. 只看尾几行：    tail
	20. 寻找特定档案：    locate    find
	21. 压缩文件和读取压缩文件：    gzip    zcat   tar
	22. 文件重命名或移动：  mv

	压缩
	tar –cvf jpg.tar *.jpg //将目录里所有jpg文件打包成tar.jpg
	tar –czf jpg.tar.gz *.jpg   //将目录里所有jpg文件打包成jpg.tar后，并且将其用gzip压缩，生成一个gzip压缩过的包，命名为jpg.tar.gz
	tar –cjf jpg.tar.bz2 *.jpg //将目录里所有jpg文件打包成jpg.tar后，并且将其用bzip2压缩，生成一个bzip2压缩过的包，命名为jpg.tar.bz2
	tar –cZf jpg.tar.Z *.jpg   //将目录里所有jpg文件打包成jpg.tar后，并且将其用compress压缩，生成一个umcompress压缩过的包，命名为jpg.tar.Z
	rar a jpg.rar *.jpg //rar格式的压缩，需要先下载rar for Linux
	zip jpg.zip *.jpg //zip格式的压缩，需要先下载zip for linux

	解压
	tar –xvf file.tar //解压 tar包
	tar -xzvf file.tar.gz //解压tar.gz
	tar -xjvf file.tar.bz2   //解压 tar.bz2
	tar –xZvf file.tar.Z   //解压tar.Z
	unrar e file.rar //解压rar
	unzip file.zip //解压zip
	
	1、*.tar 用 tar –xvf 解压
	2、*.gz 用 gzip -d或者gunzip 解压
	3、*.tar.gz和*.tgz 用 tar –xzf 解压
	4、*.bz2 用 bzip2 -d或者用bunzip2 解压
	5、*.tar.bz2用tar –xjf 解压
	6、*.Z 用 uncompress 解压
	7、*.tar.Z 用tar –xZf 解压
	8、*.rar 用 unrar e解压
	9、*.zip 用 unzip 解压