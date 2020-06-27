# MarkDwon功能演示
```markdown
# 标题H1

## 标题H2

### 标题H3

#### 标题H4

##### 标题H5

###### 标题H5

# 字符效果和横线等

~~删除线~~ 

<s>删除线（开启识别HTML标签时）</s>

*斜体字*  

**粗体** 

***粗斜体***

上标：X<sub>2</sub>，下标：O<sup>2</sup>

# 引用文本

> 引用的行内混合  引用：如果想要插入空白换行`即<br />标签`，在插入处先键入两个以上的空格然后回车即可

# 锚点与链接 Links
[普通链接](#)  
[普通链接带标题](# "普通链接带标题")  
直接链接：<#>  
[锚点链接][anchor-id]  

# 多语言代码高亮
行内代码 Inline code  
执行命令：`npm install marked`

# 缩进风格
即缩进四个空格，也做为实现类似 `<pre>` 预格式化文本 ( Preformatted Text ) 的功能。
    <?php
        echo "Hello world!";
    ?>

# 预格式化文本：

    | First Header  | Second Header |
    | ------------- | ------------- |
    | Content Cell  | Content Cell  |
    | Content Cell  | Content Cell  |
```

# JS代码
```javascript
function test() {
	console.log("Hello world!");
}
```

# HTML 代码
```html
<!DOCTYPE html>
<html>
    <head>
        <mate charest="utf-8" />
    </body>
</html>
```
# 图片

# 列表 Lists

```markdown
## 无序列表（减号）
- 列表一
- 列表二
- 列表三

## 无序列表（星号）
* 列表一
* 列表二
* 列表三

## 无序列表（加号和嵌套）
+ 列表一
+ 列表二
    + 列表二-1
    + 列表二-2
    + 列表二-3
+ 列表三
    * 列表一
    * 列表二
    * 列表三

## 有序列表
1. 第一行
2. 第二行
3. 第三行

## GFM task list

- [x] GFM task list 1
- [x] GFM task list 2
- [ ] GFM task list 3
    - [ ] GFM task list 3-1
    - [ ] GFM task list 3-2
    - [ ] GFM task list 3-3
- [ ] GFM task list 4
    - [ ] GFM task list 4-1
    - [ ] GFM task list 4-2

# 绘制表格
| 标题1 | 标题2   | 长长的标题3 | title 4 |
| ----- | --------- | ----------- | ------- |
| 内容1 | content 2 |             |         |
| 行3  | line3     | column 3    |         |

# 特殊符号

&copy; &  &uml; &trade; &iexcl; &pound;
&amp; &lt; &gt; &yen; &euro; &reg; &plusmn; &para; &sect; &brvbar; &macr; &laquo; &middot;

X&sup2; Y&sup3; &frac34; &frac14;  &times;  &divide;   &raquo;

18&ordm;C  &quot;  &apos;

# 反斜杠

# 科学公式

# 分页符

# 绘制流程图

# 绘制序列图
```