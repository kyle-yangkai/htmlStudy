本文主要讨论表格的布局及美化。首先我们通过表1来看HTML中表格包含哪些标签及属性。

![表1：表格标签及属性](https://github.com/kyle-yangkai/images/raw/master/20180707-html-%E8%A1%A8%E6%A0%BC%E5%B8%83%E5%B1%80/%E8%A1%A8%E6%A0%BC%E6%A0%87%E7%AD%BE%E5%8F%8A%E5%B1%9E%E6%80%A7.png)

其中有几个属性是我们常用来实现表格布局及美化的：

1. `rowspan`和`colspan`分别规定单元格横跨的行数和列数，其作用于标签`th`、`td`，这是改变表格布局的两个重要属性。

![图1：colspan和rowspan测试代码](https://github.com/kyle-yangkai/images/raw/master/20180707-html-%E8%A1%A8%E6%A0%BC%E5%B8%83%E5%B1%80/colspan%E5%92%8Crowspan.png)

以图1中代码为例，我们给不同的`td`分别设置了`rowspan`、`colspan`、`rowspan`和`colspan`属性，得到了图2的结果。（ps：`table`默认有`cellpadding`、`cellspacing`，因此可以看到单元格之间有空隙）

![图2：colspan和rowspan测试结果](https://github.com/kyle-yangkai/images/raw/master/20180707-html-%E8%A1%A8%E6%A0%BC%E5%B8%83%E5%B1%80/colspan%E5%92%8Crowspan%E7%BB%93%E6%9E%9C.png)

2. `frame`和`rules`分别规定外侧边框和内侧边框的显示部位。

![图3：frame和rules测试代码](https://github.com/kyle-yangkai/images/raw/master/20180707-html-%E8%A1%A8%E6%A0%BC%E5%B8%83%E5%B1%80/frame%E5%92%8Crules1.png)

以图2中代码为例，在图1代码基础上加入了`frame`和`rules`属性，得到图4结果。（ps：当`table`有设置`rules`属性时，`table`的`border-collapse`（css属性）默认值会变成`collapse`（单元格边框合并））

![图4：frame和rules测试结果](https://github.com/kyle-yangkai/images/raw/master/20180707-html-%E8%A1%A8%E6%A0%BC%E5%B8%83%E5%B1%80/frame%E5%92%8Crules1%E7%BB%93%E6%9E%9C.png)

其中`rules`属性值`groups`值得注意，它规定行组和列祖之间有边框。一般使用`co`l和`colgroup`来规定列祖，使用`thead`、`tbody`、`tfoot`来规定行组。

![图5：无col、tbody等标签测试代码](https://github.com/kyle-yangkai/images/raw/master/20180707-html-%E8%A1%A8%E6%A0%BC%E5%B8%83%E5%B1%80/frame%E5%92%8Crules2.png)

如果table中没有上述规定行组和列祖的标签时（如图5代码所示），表格不显示边框，测试结果如图6。

![图6：无col、tbody等标签测试结果](https://github.com/kyle-yangkai/images/raw/master/20180707-html-%E8%A1%A8%E6%A0%BC%E5%B8%83%E5%B1%80/frame%E5%92%8Crules2%E7%BB%93%E6%9E%9C.png)

![图7：有col、tbody等标签测试代码](https://github.com/kyle-yangkai/images/raw/master/20180707-html-%E8%A1%A8%E6%A0%BC%E5%B8%83%E5%B1%80/frame%E5%92%8Crules3.png)

如图7所示，如果代码中含有`col`、`tbody`等标签，会得到图8所示结果。由图可以看出行组能“穿透”合并的单元格，但是列祖不能。实际上是因为设置`body`这类标签时，`tbody`包含的部分会独立出来，而设置`col`这类标签只是在原来的基础上将列进行“分类”，并不会影响到原本的结构。

![图8：有col、tbody等标签测试结果](https://github.com/kyle-yangkai/images/raw/master/20180707-html-%E8%A1%A8%E6%A0%BC%E5%B8%83%E5%B1%80/frame%E5%92%8Crules3%E7%BB%93%E6%9E%9C.png)
