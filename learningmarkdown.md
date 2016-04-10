# Markdown入门

## 目录
---

* [关于 Markdown](.#关于-markdown)
  - [第一个 Markdown 文档](article/about/helloworld.md)
  - [Hello.md](article/about/hello.md)
* [语法](article/syntax/readme.md)
  - [段落与换行](article/syntax/paragraphs-and-line-breaks.md)
  - [标题](article/syntax/headers.md)
  - [引用](article/syntax/blockquotes.md)
  - [列表](article/syntax/lists.md)
  - [代码](article/syntax/code.md)
  - [分隔线](article/syntax/horizontal-rule.md)
  - [超链接](article/syntax/links.md)
  - [图片](article/syntax/images.md)
  - [强调](article/syntax/emphasis.md)
  - [字符转义](article/syntax/blackslash-escapes.md)
* [扩展语法](article/extension/readme.md)
  - [删除线](article/extension/strikethrougn.md)
  - [代码块和语法高亮](article/extension/code-blocks-and-highlighting.md)
  - [表格](article/extension/table.md)
  - [Task List](article/extension/task-list.md)
* [编辑器与扩展](article/tools/readme.md)
  - [MarkdownPad](article/tools/markdownpad.md)
  - [Texts](article/tools/texts.md)
  - [MarkPad](article/tools/markpad.md)
  - [MdCharm](article/tools/mdcharm.md)
  - [Markdown Edit](article/tools/markdown-edit.md)
  - [CuteMarkEd](article/tools/cutemarked.md)
  - [Haroopad](article/tools/haroopad.md)
  - [Mou](article/tools/mou.md)
  - [MacDown](article/tools/macdown.md)
  - [Markdown Pro](article/tools/markdown-pro.md)
  - [ReText](article/tools/retext.md)
  - [sublime-markdown-extended](article/tools/sublime-markdown-extended.md)
  - [Atom Markdown Preview](article/tools/atom-markdown-preview.md)
  - [IDEA Markdown](article/tools/idea-markdown.md)
  - [Cmd Markdown](article/tools/cmd-markdown.md)
  - [StackEdit](article/tools/stackedit.md)
  - [Dillinger](article/tools/dillinger.md)
* [格式转换](article/convert/readme.md)
  - [HTML](article/convert/html.md)
  - [PDF](article/convert/pdf.md)
  - [Word](article/convert/word.md)

## 关于 Markdown
---

### 介绍

[Wiki: Markdown](http://zh.wikipedia.org/wiki/Markdown "Wiki: Markdown")

>Markdown 是一种轻量级标记语言，创始人为约翰·格鲁伯（John Gruber）。它允许人们“使用易读易写的纯文本格式编写文档，然后转换成有效的 XHTML（或者 HTML）文档”。这种语言吸收了很多在电子邮件中已有的纯文本标记的特性。

### 为什么选择 Markdown

+ 它基于纯文本，方便修改和共享；
+ 几乎可以在所有的文本编辑器中编写；
+ 有众多编程语言的实现，以及应用的相关扩展；
+ 在 [GitHub](https://github.com/) 等网站中有很好的应用；
+ 很容易转换为 HTML 文档或其他格式；
+ 适合用来编写文档、记录笔记、撰写文章。

### 兼容 HTML

Markdown 完全兼容 HTML 语法，可以直接在 Markdown 文档中插入 HTML 内容：

```html
<table>
  <tr>
    <td>1</td>
    <td>2</td>
  </tr>
  <tr>
    <td>3</td>
    <td>4</td>
  </tr>
</table>
```

这段代码会变成下面的样子：

<table>
  <tr>
    <td>1</td>
    <td>2</td>
  </tr>
  <tr>
    <td>3</td>
    <td>4</td>
  </tr>
</table>


## 第一个 Markdown 文档
----

### Hello.md

打开你熟悉的文本编辑器（如 [Sublime Text](http://www.sublimetext.com/)），新建一个 'hello.md' 文件，写入下面的内容，并保存：

```markdown
Hello
====

I like [Google](https://www.google.com/)
```

>'.md' 和 '.markdown' 都是被普遍支持的扩展名，不过 '.md' 更加简单和方便。

它转换为 HTML 文档后，应该和 [Hello.md](hello.html) 差不多：

![Hello.md](learningmarkdown-images/hello.png 'Hello.md')

>要了解将 Markdown 转换为 HTML 或其他格式，可以参考 [格式转换](../convert/readme.md) 。



## 语法
-------
### 段落与换行

1\. 段落的前后必须是空行：

空行指的是行内什么都没有，或者只有空白符（空格或制表符）

相邻两行文本，如果中间没有空行
会显示在一行中（换行符被转换为空格）

2\. 如果需要在段落内加入换行（`<br>`）：

可以在前一行的末尾加入至少两个空格  
然后换行写其它的文字

3\. Markdown 中的多数区块都需要在两个空行之间。


### 标题

#### 1. Setext 形式

```markdown
H1
====

H2
----
```

H1
====

H2
----

>`=` 和 `-` 的数量是没有限制的。通常的做法是使其和标题文本的长度相同，这样看起来比较舒服。或者可以像我一样，用四个 `-` 或 `=`。  
>Setext 形式只支持 `h1` 和 `h2` 两种标题。

#### 2. atx 形式

① 可以用对称的 `#` 包括文本：

```markdown
####H4####

#####H5#####
```

####H4

#####H5

② 也可以只在左边使用 `#`：

```markdown
####H4

#####H5
```

####H4

#####H5

③ 成对的 `#` 左侧和只在左边使用的 `#` 左侧都不可以有任何空白，但其内侧可以使用空白。

```markdown
 ###左侧使用了空格###

#### 内侧使用了空格
```

 ###左侧使用了空格###

#### 内侧使用了空格

>在这一点上，可能各种 Markdown 的实现会有不同的结果，不过仍然需要我们遵守语法规则。


### 引用

#### 1. 引用内容

在段落或其他内容前使用 `>` 符号，就可以将这段内容标记为 '引用' 的内容（`<blockquote>`）：

```markdown
>引用内容
```

>引用内容

#### 2. 多行引用

```markdown
>多行引用
>可以在每行前加 `>`
```

>多行引用
>可以在每行前加 `>`

```markdown
>如果仅在第一行使用 `>`，
后面相邻的行即使省略 `>`，也会变成引用内容
```

>如果仅在第一行使用 `>`，
后面相邻的行即使省略 `>`，也会变成引用内容

```markdown
>如果引用内容需要换行，  
>可以在行尾添加两个空格
>
>或者在引用内容中加一个空行
```

>如果引用内容需要换行，  
>可以在行尾添加两个空格
>
>或者在引用内容中加一个空行

3. 嵌套引用
----

```markdown
>也可以在引用中
>>使用嵌套的引用
```

>也可以在引用中
>>使用嵌套的引用

4. 其他 Markdown
----

```markdown
>在引用中可以使用使用其他任何 *Markdown* 语法
```

>在引用中可以使用使用其他任何 *Markdown* 语法


### 列表

#### 无序列表

```markdown
* 可以使用 `*` 作为标记
+ 也可以使用 `+`
- 或者 `-`
```

* 可以使用 `*` 作为标记
+ 也可以使用 `+`
- 或者 `-`

#### 有序列表

```markdown
1. 有序列表以数字和 `.` 开始；
3. 数字的序列并不会影响生成的列表序列；
4. 但仍然推荐按照自然顺序（1.2.3...）编写。
```

1. 有序列表以数字和 `.` 开始；
3. 数字的序列并不会影响生成的列表序列；
4. 但仍然推荐按照自然顺序（1.2.3...）编写。

#### 嵌套的列表

```markdown
1. 第一层
  + 1-1
  + 1-2
2. 无序列表和有序列表可以随意相互嵌套
  1. 2-1
  2. 2-2
```

1. 第一层
  + 1-1
  + 1-2
2. 无序列表和有序列表可以随意相互嵌套
  1. 2-1
  2. 2-2

#### 语法和用法

1. 无序列表项的开始是：符号 空格；
2. 有序列表项的开始是：数字 `.` 空格；
3. 空格至少为一个，多个空格将被解析为一个；
4. 如果仅需要在行前显示数字和 `.`：

```markdown
05\. 可以使用：数字\. 来取消显示为列表
```

05\. 可以使用：数字\\. 来取消显示为列表

>`\*` 的语法专门用来显示 Markdown 语法中使用的特殊字符，参考 [字符转义](blackslash-escapes.md)
