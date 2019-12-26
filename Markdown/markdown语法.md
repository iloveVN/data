# 标题
用 Markdown 书写时，只需要在文本前面加上『# 』即可创建一级标题。同理，创建二级标题、三级标题等只需要增加『# 』个数即可，Markdown 共支持六级标题。如下所示：
```
	# 一级标题
	## 二级标题
	### 三级标题
	#### 四级标题
	##### 五级标题
	###### 六级标题
```

**这些标题可以被当做锚点进行跳转，例如：**
[跳转到标题](#标题)
```
	[title](#要跳转的标签名)
```

## 段落（使用的是Tab键）
段落的前后要有空行，所谓的空行是指没有文字内容。若想在段内强制换行的方式是使用两个以上空格加上回车（引用中换行省略回车）。

		我使用的是Tab键，创建的段落，然后结尾不用使用空格就可以换行
		这样我就换行了
	
还有一个是我自己的理解，我们正常的写如果不在结尾处添加两个空格例如我正在写的直接回车
我们会发现其实还是在一行中，只有我们在结尾处添加了两个空格然后再回车  
这样就会另起一行了。


## 引用
Markdown 标记区块引用和 email 中用 『>』的引用方式类似，只需要在整个段落的第一行最前面加上 『>』, 同时展示了可以在引用块中使用其他的Markdown语法

> ## 这里写数据
> 
>> + 这里是第一层
>> + 这里是第二层
>
> return shell_exec(`echo $input | $markdown_script`);


## 代码区块
这里我们使用的是git模板也是最常用的即：

```java
public static void main(String[] args){
	System.out.println("你好")
}
```

```xml
	可以根据不同的文本类型，在第一个```之后添加其语法类型
```

## 强调

*斜体* _斜体_  
**加粗**  __加粗__  
***三个是斜体加粗*** ___斜体加粗___  
~~删除~~  
**~~文本~~*混合*** 效果

### 转义
对于 Markdown 中的语法符号，前面加反斜线\即可显示符号本身  
\\ 反斜线  
\` 重音号  	  
\* 星号   
\_ 下划线   
\{\} \[\] \(\) 括号  
\# 井号  
\+ 加号  
\- 减号  
\. 句点  
\! 惊叹号  



## 列表
### 无序列表
使用*、+、或-标记无序列表

- -无序1
- -无序2

+ +无序1
+ +无序2

* *无序1
* *无序2


### 有序列表
有序列表的标记方式是将上述的符号换成数字,并辅以.，如：

1. 有序1
2. 有序2


## 分割线
分割线最常使用就是三个或以上*，还可以使用-和_.

----
我是分割线  

****
我是分割线
____
有没有影响

## 链接和图片
链接可以由两种形式生成: 行内式和参考式

### 行内式
[younghz的Markdown库](https:://github.com/younghz/Markdown "Markdown")。

### 参考式
```
参考式的这种写法是没有错的，只是我们使用的是GitHub式的MarkDown风格，导致这样语法无效。  
所以我们最好使用行内式就可以了
[younghz的Markdown库1][1]
[younghz的Markdown库2][2]
[1]:https:://github.com/younghz/Markdown "Markdown"
[2]:https:://github.com/younghz/Markdown "Markdown"
```

**图片的用法和链接的用法是一致的，区别仅仅在于需要在链接式的前面加上[!]**
![图片](/images/2018-02-04_123955.png "title") 

在这里用/开头表示本机图片，同时也可以引用网络地址。

### 自动链接
除了我们看到的上面两种，还有一种直接引用的，使用`<url>`的样式，只是这种看起来不方便,  
同时这种写法也只能去获取网络资源，不能适用于本地资源
<https:://github.com/younghz/Markdown>
<https://f12.baidu.com/it/u=4146956204,1424258428&fm=173&app=49&f=JPEG?w=640&h=476&s=33A8F70742425EFE101BEA6D03007049&access=215967316>


## 任务列表
这种语法也仅仅只是GitHub风格的MarkDown语法能够使用
- [x] 学习
- [ ] 学习
1. [ ]  写博客
2. [x]  不写博客


## HTML标签

	Markdown 中可以直接书写大部分 HTML 标签。其中在 HTML 的区块类型标签<div>、<table>、
	<pre>、<p> 等内的，Markdown 语法会失效，在 HTML 行内型标签<span>、<cite>、<del> 等
	内，Markdown 语法仍然有效。需要注意的是，在 HTML 标签内，书写特殊字符 < 和 & 仍然需要
	用它们的替代形式 &lt; 和 &amp;表示。在 Markdown 中，也能用 < 和 & 的这种特殊形式。

	MarkDown语法不支持标签中使用`**`加粗，可以使用html标签`<strong>`来加粗

This is <a href="http://cn.bing.com/images/search?q=markdown&amp;go=Submit+Query">Markdown</a>  regular paragraph. 
1 < 3 & 5
2 &lt; 4 &amp; 6
<table border="1">
    <tr>
        <td><strong>count</strong> 1 </td>
    	<td><strong>count</strong> 2 &lt; 4 &amp; 6</td>
		<td>**加粗无效**</td>
    </tr>
</table>
This is <em><strong>another regular</strong> paragraph</em>.

<span>**加粗**</span>


## 表格
	表格只能用在Extra Markdown或Github Markdown中。用竖线|和连字符-表示，
	竖线用于分隔表格中的不同列，连字符用于分开表头和表格主体，
	连字符添加冒号:还可以控制单元格对齐方式。书写时，竖线没有对齐要求，
	行首行尾的竖线可以省略，表头下需要至少三个连字符分隔。

	表格内容可以包含 Mardown 行内格式，不能添加引用、列表、多行文本，
	可以包含代码行，不能用代码块。若要书写竖线，需要用反斜线转义\|
	（cnblogs编辑器支持有问题）。

| 默认左对齐 | 左对齐 | 中对齐 | 右对齐 |
| ------    | :--- | :---: | ---: | 
 头尾的竖线可以省略 | 对齐 | 对齐 | 对齐  
| **加粗** | `int a;` | 竖线 \| | 链接[Google](www.google.com) |



## 支持 Tex 公式(这个就做了解)

	在 Markdown 中添加 Tex 公式有两种方式：请求外部服务器生成或者本地生成

	外部服务器生成方式是发送 Tex 公式到外部服务器，然后服务器会将 Tex 公式的图片发送回来，这种方式不能处理复杂的 Tex 语法。使用 HTML <img>标签，将 Tex 公式写在 <img>标签的 url 链接的参数里。如：
	Google Chart服务器

	<img src="http://chart.googleapis.com/chart?cht=tx&chl=\Large x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}">


	forkosh服务器

	<img src="http://www.forkosh.com/mathtex.cgi? \Large x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}">


	本地生成方式将 Tex 解析脚本插入到 HTML 文件的<head>标签中，在 HTML 文件渲染的过程中生成 Tex 公式，当网页中 Tex 公式比较多时速度会变慢。推荐使用 MathJax 引擎来实现，通过将下列 JS 脚本嵌入到生成的 HTML 文件<head>标签中，就能解析 Tex 公式了。Markdown 文件不应包含 <script> 标签，一般是通过修改 Markdown 编辑器的设置来自动添加。

	<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
	行间公式（$$Tex$$）：$$x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}$$
	x=−b±b2−4ac−−−−−−−√2a

	行内公式（$Tex$或\\(Tex\\)）：\\(x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}\\)
	x=−b±b2−4ac√2a
	csdn 的 Markdown 编辑器默认支持 Tex 公式，cnblogs 需要在博客“选项”中选中“启用数学公式支持”，MarkdownPad2 需要在Tools > Options > Advanced > HTML Head Editor中添加 MathJax 引擎，在F6预览中显示 Tex 公式。