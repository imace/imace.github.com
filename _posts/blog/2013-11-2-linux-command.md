---
layout:     post
title:      linux脚本学习
category: blog
description: linux下批量替换文件内容的办法
---

## 批量替换文件内容
<pre>
sed -i "s/oldstring/newstring/g" `grep oldstring -rl yourdir`
</pre>

如果不写最后的那个g，s/oldstring/newstring 将只替换每一行开头的字符串







