---
layout:     post
title:      github网站的目录结构
category: blog
description: github网站的目录结构
---

## github网站的基本结构
<pre>
.
|-- _config.yml
|-- _includes
|-- _layouts
|   |-- default.html
|   `-- post.html
|-- _posts
|   |-- 2007-10-29-why-every-programmer-should-play-nethack.textile
|   `-- 2009-04-26-barcamp-boston-4-roundup.textile
|-- _site
`-- index.html
</pre>

###_config.yml
文件是用来储存一些配置文件。这些配置文件可以在命令行以参数的形式加进去，但是写入配置文件就不需要记忆复杂得参数了。  

###_includes
文件是包含一些_layouts中模板文件的重叠部分，（相当于头文件得形式，在模板中用liquid标签{% include file.ext %}即可添加_includes文件夹下的file.ext文件）  

###_layouts文件
是存储模板文件的。文件是YAML的前置语法，一个post接一个post的原则。liquid标签{{ content }}就是用来嵌入内容的。  

###_posts文件
就是你的动态文件夹。不过文件名必须严格按照年-月-日-标题.markup的形式。永久链接是可变的，但是每个post的数据和markup语言都是由文件名决定的。  

###_site文件
这里保存的是由jekyll生成的静态页面文件，所以最好将此文件加入.gitignore中。 
 

###index.html和其他html/markdown/textfile   
  
只要文件是YAML的前置语法，就会被Jekyll转化为站点中的post  
其他文件或者文件夹
每一个除了上述的文件都会在如你所愿进行转换，比如css文件夹,favicon.ico等等。

###本地运行Jekyll
jekyll --server --baseurl /blog

打开浏览器

http://localhost:4000/blog/index.html
