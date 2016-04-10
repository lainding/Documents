# Markdown入门

## 目录
---

* [关于 Markdown](#关于-markdown)
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
