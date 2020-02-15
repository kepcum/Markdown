# 参考资料
[菜鸟教程Markdown](https://www.runoob.com/markdown/md-tutorial.html "菜鸟教程Markdown")  
[MarkDown中国](http://www.markdown.cn/ "MarkDown中国")

Markdown基本规则
======

# 标题

## 大标题
	这是一个大标题，也是一级标题
	===

## 中标题
	这是一个中标题，也是二级标题
	-----

## 多级标题
	# 一级标题
	## 二级标题
	### 三级标题
	#### 四级标题
	##### 五级标题
	###### 六级标题

# 段落格式

## 换行
在后面加两个空格，加回车即可换行  
换行成功！
  
也可使用空行来换行

换行成功（但多了一个空行）。

## 字体

*斜体文字*  
_斜体文字_  
**粗体文字**  
__粗体文字__  
***粗斜体文字***  
___粗斜体文字___ <br>

## 分隔线
	可以使用三个以上的星号
***
	可以使用三个以上隔开的减号。（如果连续则表示二级标题）
- - - 

## 删除线
	如果要在文字上添加删除线，可在文字两端添加两个波浪线~~  
	好像并没有效果，emmm
~~添加删除线~~  

## 下划线
可以通过HTML的`<u>`标签来实现  
<u>带下划线的文字</u>

## 脚注
	[^要注明的文字]
	好像并没有效果，emmm  
我的梦想[^1]  
[^1]： 成为最有钱的程序员

# 列表

## 无序列表
	使用星号、加号、减号后跟空格作为列表标记  
* 第一项  
+ 第二项  
- 第三项

## 有序列表
	使用数字并加上"."号来标记  
1. 第一项（不仔细瞧真瞧不出来）  
2. 第二项
3. 第三项

### 列表嵌套
	只需在子列表中添加四个空格(一个TAB键)即可  
1. 第一项
	* 第一项嵌套的第一个元素
	* 第一项嵌套的第二个元素
2. 第二项
	* 第二项嵌套的第一个元素
	* 第二项嵌套的第二个元素

# 区块
	Markdown区块引用是在段落开头使用`>`符号，然后后面紧跟一个空格符号。
> 区块引用示例  
> dream
	
	区块引用是可以嵌套的，一个`>`符号表示最外层，两个`>`是第一层嵌套，以此类推
> 最外层  
>> 第一层嵌套  
>>> 第二层嵌套    

>> 第一层嵌套结束  

> 最外层嵌套结束

## 区块中使用列表
> 区块中使用列表  

> 1. 第一项  
> 2. 第二项  
> * 第一项  
> * 第二项


## 列表中使用区块
* 第一项  
	> 我的梦想  
	> 成为最有钱的程序员  
* 第二项

# 代码
	如果是段落上一个函数或片段的代码可以用反引号把它包起来（`）,例如  
	`printf()`函数
## 代码区块
代码区块使用四个空格，或者一个制表符（Tab键）。

	string name = "kepcum";
	string sex = "M";
	cout<<"name: "<<name<<endl<<"sex: "<<sex<<endl;

也可以用```包裹一段代码并指定一种语言（也可以不指定）：  

```cpp
string name = "kepcum";
string sex = "M";
cout<<"name: "<<name<<endl<<"sex: "<<sex<<endl;  
好像不能换行啊，emmm
```

# 链接
链接的使用格式如下：

	[链接名称]（链接地址）
	或者
	<链接地址>

例如：这是一个链接[kepcum's github](https://github.com/kepcum "kepcum的github")  

或者直接使用链接地址，例如：<https://github.com/kepcum>

## 高级链接

	链接地址也可以用变量代替，文档末尾附带变量地址：
这个链接用1做网址变量[Baidu][1]  
这个链接用kepcum的github做网址变量[kepcum's github][kepcum的github]  
然后在文档，末尾为变量赋值(网址)  
[1]: https://www.baidu.com/  
[kepcum的github]:https://github.com/kepcum

# 图片
	Markdown图片格式如下：
	![图片名]（链接 "可选标题"）
![百度's logo](https://www.baidu.com/img/baidu_logo.gif "百度Logo")

当然，你也可以像网址那样对图片网址使用变量：  
然后在文档的结尾处对变量赋值。

![BAIDU][BAIDU's Logo]  
[BAIDU's Logo]:https://www.baidu.com/img/baidu_logo.gif

## 为图片指定宽度和高度
	可以使用img标签为图片指定宽度和高度
<img src="https://www.baidu.com/img/baidu_logo.gif" width="50%">

# Markdown表格
	使用 "|" 来分隔不同的单元格，使用 "-" 来分隔表头和其它行。
	语法格式如下：  
	|  表头   | 表头  |  
	|  ----  | ----  |  
	| 单元格  | 单元格 |  
	| 单元格  | 单元格 |

|  表头   | 表头  |  
|  ----  | ----  |  
| 单元格  | 单元格 |  
| 单元格  | 单元格 |


	我们可以设置表格的对齐方式
	-:设置内容和标题栏居右对齐。
	:-设置内容和标题栏居左对齐。  
	:-:设置内容和标题栏居中对齐。

| 左对齐 | 右对齐 | 居中对齐 |  
| :--  | --: | :--: |  
| 单元 | 单元 | 单元 |  
| 单元 | 单元 | 单元 |

# Markdown高级技巧
## 支持HTML元素
	不在Markdown涵盖范围之内的标签，可以直接在文档里面用HTML编写。
	目前支持的HTML元素有：<kbd> <b> <i> <em> <sup> <sub> <br>等，如
使用<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Del</kbd> 重启电脑。

## 转义
	使用反斜杠("\")转义特殊字符:
**文本加粗**  
\*\*显示正常星号\*\*

markdown需要在以下符号前加上反斜杠来帮助插入普通符号：  
	
	\	反斜杠
	`	反引号
	*	星号
	_	下划线
	{}	花括号
	[]	方括号
	()	小括号
	#	井字号
	+	加号
	-	减号
	.	英语句点
	!	感叹号

## 公式
	当你需要在编辑器中插入公式时，可以使用两个美元符号$$包裹Tex或LaTex格式的数学公式来实现。  
	提交后，问答和文章页会根据需要加载Mathjax对数学公式进行渲染。

$$  
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix}   
\mathbf{i} & \mathbf{j} & \mathbf{k} \\  
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\  
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\  
\end{vmatrix}  
$$tep1}{\style{visibility:hidden}{(x+1)(x+1)}}  
$$
