路径指文件存放的位置，在网页中利用路径可以引用文件，插入图像、视频等。表示路径的方法有两种：相对路径，绝对路径。以下讨论均是在HTML环境下进行。

## 相对路径

相对路径是指目标相对于当前文件的路径，网页结构设计中多采用这种方法来表示目标的路径。相对路径有多种表示方法，其表示的意义不尽相同。表示方法如下：

**./：代表文件所在的目录（可以省略不写）**

**../：代表文件所在的父级目录**

**../../ ：代表文件所在的父级目录的父级目录**

**/ ：代表文件所在的根目录**

值得注意的是，（**/ ：代表文件所在的根目录**）其实可以理解成项目内部的绝对路径。

![图1：项目结构目录](https://github.com/kyle-yangkai/images/raw/master/20180705-html-%E7%9B%B8%E5%AF%B9%E8%B7%AF%E5%BE%84%E4%B8%8E%E7%BB%9D%E5%AF%B9%E8%B7%AF%E5%BE%84/%E9%A1%B9%E7%9B%AE%E7%9B%AE%E5%BD%95%E7%BB%93%E6%9E%84.png)

以图1所示项目目录结构为例，如果要在test.html中引入000.css，可以有以下写法：

1. <link  href="./css/css1/000.css"/> (./可以省略)

2. <link href="/html/css/css1/000.css"/>

3. <link href="../html/css/css1/000.css"/>

## 绝对路径

绝对路径是指完整的网址，假设图一中项目的网站域名为www.test.com，那么000.css的绝对路径应该是https://www.test.com/HelloHBuilder/html/css/css1/000.css。

**相对路径与绝对路径的优缺点**

![图2：相对路径与绝对路径的优缺点](https://github.com/kyle-yangkai/images/raw/master/20180705-html-%E7%9B%B8%E5%AF%B9%E8%B7%AF%E5%BE%84%E4%B8%8E%E7%BB%9D%E5%AF%B9%E8%B7%AF%E5%BE%84/%E4%B8%8D%E5%90%8C%E8%B7%AF%E5%BE%84%E4%BC%98%E7%BC%BA%E7%82%B9.jpg)
