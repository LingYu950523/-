# 第五天
html发明者是李爵士

前端的核心：HTML+URL+HTTP


```html 
<!DOCTYPE html>   html起手式
```  

```html 
<html></html>   根标签，后面语言属性lang一般为zh-CN
``` 

（标签后面可以跟属性值）

```html 
<head></head> <body></body>   是head标签的字标签
``` 

```html 
<meta>   用于设置网页的元数据，一共有五种属性（自闭合）
``` 

```html 
<title></title>   网页在边栏显示的名称
``` 

今天重点讲述```<body></body>```里面的

* 章节标签：

1. h1~h6 标题
2. section 章节
3. article 文章
4. p 段落
5. header 顶部
6. footer 底部
7. main 主要内容
8. aside 分支内容
9. div 区域划分
    
* 全局属性（所有标签都会有的属性）：

1. class 给标签做标记，不同的标记值用空格隔开（有多个标记值时，style里面需要用.style的方式来表示标记值）
2. contenteditable 可以让内容变为可编辑的
3. hidden 隐藏任意标签
4. display block 让标签内容显示出来
5. id 不到万不得已不要用，因为没办法保证其唯一性
6. style 标签中的style属性优先级比css要高，但js会覆盖html的属性值
7. tabindex 用来控制页面响应tab按键的顺序，从1开始，等于0是最后一个，等于-1永远不会被tab选中
8. title 可以在鼠标停留时显示具体内容

* 内容标签
1. ol+li ol全称是ordered list，li全称是list item
2. dl+dt+dd dl加加号可以打出整个结构，dl全称是description list，dt的全称是description term，dd的全称是description data，
3. pre html默认将空白合并为一个空格，pre可以将合并的内容全部展示出来
4. code 可以字体默认是等宽的，方便代码对齐，一般与上面的pre一起使用
5. hr 水平分割线
6. br 换行
7. a 超链接，href、target属性
8. em 起强调作用，默认样式是斜体，语气的强调
9. strong 加粗，语义的强调
10. quote 和 blockquote 是内联引用还是行外块引用

## 默认样式

Chrome检查 -> elements -> style -> user agent stylesheet
查看浏览器默认样式

默认样式可以被css覆盖


