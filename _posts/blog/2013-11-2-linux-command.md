---
layout:     post
title:      linux脚本学习
category: blog
description: linux下批量替换文件内容的办法
---

## 批量替换文件内容
<pre>
grep -i "string1" -r /path | awk -F : '{print $1}' | sort | uniq | xargs sed -i 's/string1/string2/g'
</pre>

### grep
-i 表示忽略大小写
### awk

### sort
排序




