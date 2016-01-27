``` html
<div style="width:200px; white-space:nowrap;overflow:hidden;text-overflow:ellipsis; border:1px solid red">试试看试试看试试看试试看试试看试试看试试看试试看试试看试试看试试看</div>  
```

语法：
text-overflow : clip | ellipsis
参数：
clip : 　不显示省略标记（...），而是简单的裁切
（clip这个参数是不常用的！）
ellipsis : 　当对象内文本溢出时显示省略标记（...）
说明：
设置或检索是否使用一个省略标记（...）标示对象内文本的溢出。
请您注意，text-overflow:ellipsis属性在FF中是没有效果的。
示例：
div { text-overflow : clip; }
text-overflow是一个比较特殊的样式，我们可以用它代替我们通常所用的标题截取函数，而且这样做对搜索引擎更加友好，如：标题文件有50 个汉字，而我们的列表可能只有300px的宽度。如果用标题截取函数，则标题不是完整的，如果我们用CSS样式text- overflow:ellipsis，输出的标题是完整的，只是受容器大小的局限不显示出来罢了。
text-overflow属性仅是注解，当文本溢出时是否显示省略标记。并不具备其它的样式属性定义。我们想要实现溢出时产生省 略号的效果。还必须定义：强制文本在一行内显示（white-space:nowrap）及溢出内容为隐藏（overflow:hidden）。只有这样 才能实现溢出文本显示省略号的效果。
 
 
有的时候的某段文本太长了，会影响整个的布局，很多人用动态语言来解决这个问题，但必须区分中文和英文，因为中文相当于两个英文字符长度，这样不仅繁琐，而且加重了服务器的负担。其实，我们完全可以使用CSS完美解决这个问题，

``` css
.p1{
text-align: center;
color:#C8CFD6;
height:34px;
text-overflow: -o-ellipsis-lastline;overflow: hidden;text-overflow: ellipsis;display: -webkit-box;-webkit-line-clamp: 2;-webkit-box-orient: vertical;
}
```
