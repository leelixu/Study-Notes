---
Title: 02 Markdown学习
C_time: 2023-06-29-22:35
Done_time: NA
Status: Done
draft: false
Tag:
- #Markdown
---

## [Home](index)

原文：[Markdown 官方教程](https://markdown.com.cn/basic-syntax/)

[Markdown 的创建者编写的原始指南](https://daringfireball.net/projects/markdown/)

[Obsidian中文教程 - Obsidian Publish](https://publish.obsidian.md/chinesehelp/01+2021%E6%96%B0%E6%95%99%E7%A8%8B/2021%E5%B9%B4%E6%96%B0%E6%95%99%E7%A8%8B)

# 一 Markdown 基本介绍

Markdown 是一种轻量级的标记语言，可用于在纯文本文档中添加格式化元素。Markdown 由 John Gruber 于 2004 年创建，如今已成为世界上最受欢迎的标记语言之一。

1. 专注于文字内容；
2. 纯文本，易读易写，可以方便地纳入版本控制；
3. 语法简单，没有什么学习成本，能轻松在码字的同时做出美观大方的排版。

Markdown语法的优点：

1. Markdown 无处不在
2. Markdown 是纯文本可移植的
3. Markdown 是独立于平台的
4. Markdown 能适应未来的变化

# 二 Markdown 基本语法

## 1 Markdown 标题

要创建标题，请在单词或短语前面添加井号 (`#`) 。`#` 的数量代表了标题的级别。

```text
# 一级标题
## 二级标题
### 三级标题
......
```

## 2 Markdown 段落

要创建段落，请使用空白行将一行或多行文本进行分隔。

```text
我是一段文本

我是另一段文本

我是第三段文本
```

## 3 Markdown 换行

在一行的末尾添加两个或多个空格，然后按回车键,即可创建一个换行。

```text
我是一段文本。
我是另一段文本  
我是第三段文本  
```

## 4 Markdown 强调

通过将文本设置为粗体或斜体来强调其重要性。

### 4.1 粗体（Bold）

要加粗文本，请在单词或短语的前后各添加两个星号（asterisks）或下划线（underscores）。

```text
我是**粗体文字**
```

效果：

我是**粗体文字**

### 4.2 斜体（Italic）

要用斜体显示文本，请在单词或短语前后添加一个星号（asterisk）或下划线（underscore）。

```text
我是*斜体文字*
```

效果：

我是*斜体文字*

### 4.3 粗体（Bold）和斜体（Italic）

要同时用粗体和斜体突出显示文本，请在单词或短语的前后各添加三个星号或下划线。

```text
我是***粗斜体文字***
```

效果：

我是***粗斜体文字***

## 5 Markdown 引用

### 5.1 单个段落引用

要创建块引用，请在段落前添加一个 `>` 符号。

```text
>我是引用文字
```

效果：

>我是引用文字

### 5.2 多个段落的块引用

可以包含多个段落。为段落之间的空白行添加一个 `>` 符号。

```text
>我是引用文字
>
>我是另一段引用文字
```

效果：

>我是引用文字
>
>我是另一段引用文字

### 5.3 嵌套块引用

块引用可以嵌套。在要嵌套的段落前添加一个 `>>` 符号。

```text
>我是引用文字
>>我是嵌套引用文字
```

效果：

>我是引用文字
>>我是嵌套引用文字

### 5.4 带有其它元素的块引用

块引用可以包含其他 Markdown 格式的元素。但是并非所有元素都可以使用。

```text
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.
```

效果：

> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.

## 6 Markdown 列表

可以将多个条目组织成有序或无序列表。

### 6.1 有序列表

要创建有序列表，请在每个列表项前添加数字并紧跟一个英文句点。数字不必按数学顺序排列，但是列表应当以数字 1 起始。

```text
1. 第一段文字
2. 第二段文字
3. 第三段文字
```

效果：

1. 第一段文字
2. 第二段文字
3. 第三段文字

### 6.2 无序列表

要创建无序列表，请在每个列表项前面添加破折号 (-)、星号 (\*) 或加号 (+) 。缩进一个或多个列表项可创建嵌套列表。

```text
- 第一段文字
- 第二段文字
- 第三段文字
```

效果：

- 第一段文字
- 第二段文字
- 第三段文字

### 6.3 在列表中嵌套其他元素

要在保留列表连续性的同时在列表中添加另一种元素，请将该元素缩进四个空格或一个制表符，如下例所示：

#### 段落

```text
*   This is the first list item.
*   Here's the second list item.

    I need to add another paragraph below the second list item.

*   And here's the third list item.
```

效果：

*   This is the first list item.
*   Here's the second list item.

    I need to add another paragraph below the second list item.

*   And here's the third list item.

#### 引用块

```text
*   This is the first list item.
*   Here's the second list item.

    > A blockquote would look great below the second list item.

*   And here's the third list item.
```

效果：

*   This is the first list item.
*   Here's the second list item.

    > A blockquote would look great below the second list item.

*   And here's the third list item.

#### 代码块

```text
1.  Open the file.
2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.
```

效果：

1.  Open the file.
2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.

#### 图片

```text
1.  Open the file containing the Linux mascot.
2.  Marvel at its beauty.

    ![[linux_tux.png]]

3.  Close the file.
```

效果：

1.  Open the file containing the Linux mascot.
2.  Marvel at its beauty.

    ![[linux_tux.png]]

3.  Close the file.

#### 列表

```text
1. First item
2. Second item
3. Third item
    - Indented item
    - Indented item
4. Fourth item
```

效果：

1. First item
2. Second item
3. Third item
    - Indented item
    - Indented item
4. Fourth item

## 7 Markdown 代码

### 7.1 对于单词或短语

要将单词或短语表示为代码，请将其包裹在反引号 (`` ` ``) 中。

```text
At the command prompt, type `nano`.
```

效果：

At the command prompt, type `nano`.

### 7.2 转义反引号

如果你要表示为代码的单词或短语中包含一个或多个反引号，则可以通过将单词或短语包裹在双反引号(` `` `)中。

```text
``Use `code` in your Markdown file.``
```

效果：

``Use `code` in your Markdown file.``

### 7.3 代码块

要创建代码块，请将代码块的每一行缩进至少四个空格或一个制表符，或者在代码块之前和之后的行上使用三个反引号（(` ``` `）或三个波浪号（\~\~~）

````text
```
    <html>
      <head>
      </head>
    </html>
```
或者
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````

效果：

    <html>
      <head>
      </head>
    </html>

或者

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

## 8 Markdown分隔线

要创建分隔线，请在单独一行上使用三个或多个星号 (`***`)、破折号 (`---`) 或下划线 (`___`) ，并且不能包含其他内容。

```
***

---

_________________
```

以上三个分隔线的渲染效果看起来都一样：

效果：

***

---

_________________

## 9 Markdown 链接

链接文本放在中括号内，链接地址放在后面的括号中，链接title可选。

超链接Markdown语法代码：`[超链接显示名](超链接地址 "超链接title")`

```text
这是一个链接 [Markdown语法](https://markdown.com.cn)。
```

效果：

这是一个链接 [Markdown语法](https://markdown.com.cn)。

#### 9.1 给链接增加 Title

链接title是当鼠标悬停在链接上时会出现的文字，这个title是可选的，它放在圆括号中链接地址后面，跟链接地址之间以空格分隔。

```text
这是一个链接 [Markdown语法](https://markdown.com.cn "最好的markdown教程")。
```

效果：

这是一个链接 [Markdown语法](https://markdown.com.cn "最好的markdown教程")。

#### 9.2 网址和Email地址

使用尖括号可以很方便地把URL或者email地址变成可点击的链接。

```text
<https://markdown.com.cn>
<fake@example.com>
```

效果：

<https://markdown.com.cn>
<fake@example.com>

#### 9.3 带格式化的链接

强调链接, 在链接语法前后增加星号。 要将链接表示为代码，请在方括号中添加反引号。

```
I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code).
```

效果：

I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code).

#### 9.4 引用类型链接

引用样式链接是一种特殊的链接，它使URL在Markdown中更易于显示和阅读。参考样式链接分为两部分：与文本保持内联的部分以及存储在文件中其他位置的部分，以使文本易于阅读。

##### 链接的第一部分格式

引用类型的链接的第一部分使用两组括号进行格式设置。第一组方括号包围应显示为链接的文本。第二组括号显示了一个标签，该标签用于指向您存储在文档其他位置的链接。

尽管不是必需的，可以在第一组和第二组括号之间包含一个空格。第二组括号中的标签不区分大小写，可以包含字母，数字，空格或标点符号。

以下示例格式对于链接的第一部分效果相同：

- `[hobbit-hole][1]`
- `[hobbit-hole] [1]`


##### 链接的第二部分格式

引用类型链接的第二部分使用以下属性设置格式：

1. 放在括号中的标签，其后紧跟一个冒号和至少一个空格（例如`[label]:`）。
2. 链接的URL，可以选择将其括在尖括号中。
3. 链接的可选标题，可以将其括在双引号，单引号或括号中。

以下示例格式对于链接的第二部分效果相同：

- `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle`
- `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"`
- `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit lifestyles'`
- `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle (Hobbit lifestyles)`
- `[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"`
- `[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> 'Hobbit lifestyles'`
- `[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit lifestyles)`

可以将链接的第二部分放在Markdown文档中的任何位置。有些人将它们放在出现的段落之后，有些人则将它们放在文档的末尾（例如尾注或脚注）。

## 10 Markdown 图片

#### 10.1 插入图片

要添加图像，请使用感叹号 (`!`), 然后在方括号增加替代文本，图片链接放在圆括号里，括号里的链接后可以增加一个可选的图片标题文本。

插入图片Markdown语法代码：`![图片alt](图片链接 "图片title")`。

```
![这是图片](linux_tux.png "图片")
```

效果：

![这是图片](linux_tux.png)

#### 10.2 链接图片

给图片增加链接，请将图像的Markdown 括在方括号中，然后将链接添加在圆括号中。

```
[![这是图片](linux_tux.png "图片")](https://markdown.com.cn)
```

效果：

[![这是图片](linux_tux.png "图片")](https://markdown.com.cn)

## 11 Markdown 转义字符

要显示原本用于格式化 Markdown 文档的字符，请在字符前面添加反斜杠字符 \\ 。

```
\* Without the backslash, this would be a bullet in an unordered list.
```

效果：

\* Without the backslash, this would be a bullet in an unordered list.

#### 可做转义的字符

以下列出的字符都可以通过使用反斜杠字符从而达到转义目的。

|Character|Name|
|---|---|
|\\|backslash|
|`|backtick (see also escaping backticks in code)|
|*|asterisk|
|_|underscore|
|{ }|curly braces|
|[ ]|brackets|
|( )|parentheses|
|#|pound sign|
|+|plus sign|
|-|minus sign (hyphen)|
|.|dot|
|!|exclamation mark|
|\||pipe (see also escaping pipe in tables)|

## 12 Markdown 内嵌HTML标签

对于 Markdown 涵盖范围之外的标签，都可以直接在文件里面用 HTML 本身。如需使用 HTML，不需要额外标注这是 HTML 或是 Markdown，只需 HTML 标签添加到 Markdown 文本中即可。

#### 行级內联标签

HTML 的行级內联标签如 `<span>`、`<cite>`、`<del>` 不受限制，可以在 Markdown 的段落、列表或是标题里任意使用。依照个人习惯，甚至可以不用 Markdown 格式，而采用 HTML 标签来格式化。例如：如果比较喜欢 HTML 的 `<a>` 或 `<img>` 标签，可以直接使用这些标签，而不用 Markdown 提供的链接或是图片语法。当你需要更改元素的属性时（例如为文本指定颜色或更改图像的宽度），使用 HTML 标签更方便些。

HTML 行级內联标签和区块标签不同，在內联标签的范围内， Markdown 的语法是可以解析的。

```
This **word** is bold. This <em>word</em> is italic.
```

渲染效果如下:

This **word** is bold. This _word_ is italic.

#### 区块标签

区块元素──比如 `<div>`、`<table>`、`<pre>`、`<p>` 等标签，必须在前后加上空行，以便于内容区分。而且这些元素的开始与结尾标签，不可以用 tab 或是空白来缩进。Markdown 会自动识别这区块元素，避免在区块标签前后加上没有必要的 `<p>` 标签。

例如，在 Markdown 文件里加上一段 HTML 表格：

```
This is a regular paragraph.

<table>
    <tr>
        <td>Foo</td>
    </tr>
</table>

This is another regular paragraph.
```

请注意，Markdown 语法在 HTML 区块标签中将不会被进行处理。例如，你无法在 HTML 区块内使用 Markdown 形式的`*强调*`

# 三 Markdown 拓展语法

## 1 Markdown 表格

### 1.1 表格使用

要添加表，请使用三个或多个连字符（`---`）创建每列的标题，并使用管道（`|`）分隔每列。您可以选择在表的任一端添加管道。

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
```

呈现的输出如下所示：

|Syntax|Description|
|---|---|
|Header|Title|
|Paragraph|Text|

单元格宽度可以变化，如下所示。呈现的输出将看起来相同。

```
| Syntax | Description |
| --- | -------------------- |
| Header | Title |
| Paragraph | Text |
```

### 1.2 表格对齐

可以通过在标题行中的连字符的左侧，右侧或两侧添加冒号（`:`），将列中的文本对齐到左侧，右侧或中心。

```
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |
```

呈现的输出如下所示：

|Syntax|Description|Test Text|
| :---        |    :----:   |          ---: |
|Header|Title|Here’s this|
|Paragraph|Text|And more|

### 1.3 格式化表格中的文字

可以在表格中设置文本格式。例如，您可以添加链接，代码（仅反引号（`` ` ``）中的单词或短语，而不是代码块）和强调。但是不能添加标题，块引用，列表，水平规则，图像或HTML标签。

## 2 Markdown 脚注

脚注使您可以添加注释和参考，而不会使文档正文混乱。当您创建脚注时，带有脚注的上标数字会出现在您添加脚注参考的位置。读者可以单击链接以跳至页面底部的脚注内容。

要创建脚注参考，请在方括号（`[^1]`）内添加插入符号和标识符。标识符可以是数字或单词，但不能包含空格或制表符。标识符仅将脚注参考与脚注本身相关联-在输出中，脚注按顺序编号。

在括号内使用另一个插入符号和数字添加脚注，并用冒号和文本（`[^1]: My footnote.`）。您不必在文档末尾添加脚注。您可以将它们放在除列表，块引号和表之类的其他元素之外的任何位置。

```
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.
```

呈现的输出如下所示：


Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

## 3 Markdown 标题编号

许多Markdown处理器支持标题的自定义ID - 一些Markdown处理器会自动添加它们。添加自定义ID允许您直接链接到标题并使用CSS对其进行修改。要添加自定义标题ID，请在与标题相同的行上用大括号括起该自定义ID。

```
### My Great Heading {#custom-id}
```

#### 链接到标题ID (#headid)

通过创建带有数字符号（`#`）和自定义标题ID的[标准链接]((/basic-syntax/links.html)，可以链接到文件中具有自定义ID的标题。

|Markdown|HTML|预览效果|
|---|---|---|
|`[Heading IDs](#heading-ids)`|`<a href="#heading-ids">Heading IDs</a>`|[Heading IDs](https://markdown.com.cn/extended-syntax/heading-ids.html#heading-ids)|

其他网站可以通过将自定义标题ID添加到网页的完整URL（例如`[Heading IDs](https://markdown.com.cn/extended-syntax/heading-ids.html#headid)`）来链接到标题。

## 4 Markdown 定义列表

一些Markdown处理器允许您创建术语及其对应定义的_定义列表_。要创建定义列表，请在第一行上键入术语。在下一行，键入一个冒号，后跟一个空格和定义。

```
First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.
```

HTML看起来像这样：

```
<dl>
  <dt>First Term</dt>
  <dd>This is the definition of the first term.</dd>
  <dt>Second Term</dt>
  <dd>This is one definition of the second term. </dd>
  <dd>This is another definition of the second term.</dd>
</dl>
```

呈现的输出如下所示：

<dl>
  <dt>First Term</dt>
  <dd>This is the definition of the first term.</dd>
  <dt>Second Term</dt>
  <dd>This is one definition of the second term. </dd>
  <dd>This is another definition of the second term.</dd>
</dl>

## 5 Markdown 删除线

可以通过在单词中心放置一条水平线来删除单词。结果看起来~~像这样~~。此功能使您可以指示某些单词是一个错误，要从文档中删除。若要删除单词，请在单词前后使用两个波浪号`~~`。

```
~~世界是平坦的。~~ 我们现在知道世界是圆的。
```

呈现的输出如下所示：

~~世界是平坦的。~~ 我们现在知道世界是圆的。

## 6 Markdown 任务列表语法

任务列表使您可以创建带有复选框的项目列表。在支持任务列表的Markdown应用程序中，复选框将显示在内容旁边。要创建任务列表，请在任务列表项之前添加破折号`-`和方括号`[ ]`，并在`[ ]`前面加上空格。要选择一个复选框，请在方括号`[x]`之间添加 x 。

```
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
```

呈现的输出如下所示：

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

## 7 Markdown 使用 Emoji 表情

有两种方法可以将表情符号添加到Markdown文件中：将表情符号复制并粘贴到Markdown格式的文本中，或者键入_emoji shortcodes_。

#### 复制和粘贴表情符号

在大多数情况下，您可以简单地从[Emojipedia](https://emojipedia.org/) 等来源复制表情符号并将其粘贴到文档中。许多Markdown应用程序会自动以Markdown格式的文本显示表情符号。从Markdown应用程序导出的HTML和PDF文件应显示表情符号。

**Tip:** 如果您使用的是静态网站生成器，请确保将HTML页面编码为UTF-8。.

#### 使用表情符号简码

一些Markdown应用程序允许您通过键入表情符号短代码来插入表情符号。这些以冒号开头和结尾，并包含表情符号的名称。

```
去露营了！ :tent: 很快回来。

真好笑！ :joy:
```

呈现的输出如下所示：

去露营了！ ⛺很快回来。

真好笑！ 😂

Note: 注意：您可以使用此[表情符号简码列表](https://gist.github.com/rxaviers/7360908)，但请记住，表情符号简码因应用程序而异。有关更多信息，请参阅Markdown应用程序的文档。

[[表情符号简码列表]]

# 四 Markdown 高级语法

[Markdown语法及原理从入门到高级](https://www.zhihu.com/tardis/zm/art/99319314?source_id=1005)

## 1 更改字体、大小、颜色

```text
<font face="黑体">我是黑体字</font>
<font face="微软雅黑">我是微软雅黑</font>
<font face="STCAIYUN">我是华文彩云</font>
<font color=red>我是红色</font>
<font color=#008000>我是绿色</font>
<font color=Blue>我是蓝色</font>
<font size=5>我是尺寸</font>
<font face="黑体" color=green size=5>我是黑体，绿色，尺寸为5</font>
```

效果如下：

<font face="黑体">我是黑体字</font>
<font face="微软雅黑">我是微软雅黑</font>
<font face="STCAIYUN">我是华文彩云</font>
<font color=red>我是红色</font>
<font color=#008000>我是绿色</font>
<font color=Blue>我是蓝色</font>
<font size=5>我是尺寸</font>
<font face="黑体" color=green size=5>我是黑体，绿色，尺寸为5</font>

## 2 为文字添加背景色

由于 style 标签和标签的 style 属性不被支持，所以这里只能是借助 table, tr, td 等表格标签的 bgcolor 属性来实现背景色。故这里对于文字背景色的设置，只是将那一整行看作一个表格，更改了那个格子的背景色（bgcolor）。 语法：

```text
<table><tr><td bgcolor=yellow>背景色yellow</td></tr></table>
```

效果如下

<table><tr><td bgcolor=yellow>背景色yellow</td></tr></table>

## 3 设置文字居中

```text
<center>文字居中</center>
<p align="left">文字左对齐</p>
<p align="right">文字右对齐</p>
```

效果如下：
<center>文字居中</center>
<p align="left">文字左对齐</p>
<p align="right">文字右对齐</p>

## 4 加入上下标

使用HTML中下标下标的语法即可, 语法：

```text
H<sub>2</sub>O  CO<sub>2</sub>
爆米<sup>TM</sup>
```

效果如下：

H<sub>2</sub>O  CO<sub>2</sub>
爆米<sup>TM</sup>

## 5 LaTeX 公式

[Latex 数学公式](https://publish.obsidian.md/csj-obsidian/0+-+Obsidian/Markdown/Markdown%E8%B6%85%E7%BA%A7%E6%95%99%E7%A8%8B+Obsidian%E7%89%88#16.+Latex+%E6%95%B0%E5%AD%A6%E5%85%AC%E5%BC%8F)

Markdown还有一大优势就是可以支持 LaTeX 的公式。 \$ 表示行内公式 \$$ 表示整行公式 访问 [MathJax](https://link.zhihu.com/?target=https%3A//math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference) 参考更多使用方法。

这里说一个常用的，很多时候，我们在做笔记时候，需要画箭头，然后在箭头上需要写字，这里就可以用LaTeX公式来实现：

```text
$ X\stackrel{F}{\longrightarrow}Y $
```

效果如下： $ X\stackrel{F}{\longrightarrow}Y $

LaTeX 支持多种箭号，内容很丰富,这里就不一一列举了，大家可以参见[Latex各种箭号符号](https://link.zhihu.com/?target=https%3A//blog.csdn.net/J__Max/article/details/86549124)。

[[Latex各种箭号符号]]

## 6 嵌入

### 6.1 嵌入音频

- 格式：
    - **`<audio controls="controls" preload="none" src="音频链接地址"></audio>`**
- 示例：

```html
<audio controls="controls" preload="none" src="https://www.ldoceonline.com/media/english/exaProns/p008-001803372.mp3?version=1.2.37"></audio>
```

- 效果：

<audio controls="controls" preload="none" src="https://www.ldoceonline.com/media/english/exaProns/p008-001803372.mp3?version=1.2.37"></audio>

### 6.2 嵌入视频

- **格式：**

```html
<video width="600" height="420" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  <source src="movie.webm" type="video/webm">  
</video>
```

- **说明：**
    - width ( 宽度 ) height ( 高度 ) ，可以自己设置，直接输入数字即可，单位默认是 px(像素)  
        也可以使用 **百分比**  
        **`width=100%`** 代表水平撑满整个窗口  
        **`height=50%`** 代表垂直撑满半个窗口
    - **Video标签** 支持的视频格式 ：MP4 ogg webm

### 6.3 嵌入页面

- **格式：** **`<iframe width=600 height=400 src="页面链接地址" scrolling="auto" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>`**

```html
<iframe width=600 height=400 src="https://www.runoob.com/html/html-tutorial.html" scrolling="auto" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
```

- **效果**

<iframe width=600 height=400 src="https://publish.obsidian.md/csj-obsidian/0+-+Obsidian/Markdown/Markdown%E8%B6%85%E7%BA%A7%E6%95%99%E7%A8%8B+Obsidian%E7%89%88#15.2%20%E5%B5%8C%E5%85%A5%E8%A7%86%E9%A2%91" scrolling="auto" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

- iframe标签 除了嵌入页面，也可以嵌入**在线视频**，主流的视频网站都会提供**嵌入代码**
    
    - 具体可以看这个 [iframe视频嵌入教程](https://www.wolai.com/wolai/go85vJpt3wDwrid7DfCZcE)
    - **B站** 的视频，得在 **`//`** 前面补充 **`http:`**
    - 不是所有的 编辑器和笔记软件 都支持这个
- 示例：

```html
<iframe width=600 height=400 src="http://player.bilibili.com/player.html?aid=20190823&bvid=BV1yW411s7og&cid=32964980&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
```

- 宽高设置和前面的 **video** 一样

## 7 Mermaid 流图

[Mermaid](https://publish.obsidian.md/csj-obsidian/0+-+Obsidian/Markdown/Markdown%E8%B6%85%E7%BA%A7%E6%95%99%E7%A8%8B+Obsidian%E7%89%88#17.+Mermaid)

[什么是 Mermaid？](https://publish.obsidian.md/csj-obsidian/0+-+Obsidian/Mermaid/%E4%BB%80%E4%B9%88%E6%98%AF+Mermaid%EF%BC%9F)

### 7.1 什么是 Mermaid？

- **Mermaid** 可以让你通过书写 文本+ 代码，来绘制图像，实现文字与逻辑的**可视化**
    - 其原理是：通过 [**Mermaid-js 官网**](https://mermaid-js.github.io/ "Mermaid官网") 及其所提供的 [编译器](https://mermaid-js.github.io/mermaid-live-editor "Mermaid在线编译器")
    - 它是一个基于 **JavaScript** 的图表绘制工具，可以在 Markdown 快速且动态地，创建和修改图表。
- **Mermaid** 可以让你专注于书写，不被其他因素影响(节点大小、节点之间的距离、箭头长度等)
    - 传统的图表绘制软件，制图较为耗时，且难以在原来的基础上进行维护与修改
    - 过多的选择不见得是好事，这点在 [为什么要使用Markdown](https://publish.obsidian.md/csj-obsidian/0+-+Obsidian/Markdown/Markdown%E8%B6%85%E7%BA%A7%E6%95%99%E7%A8%8B+Obsidian%E7%89%88#%E4%B8%BA%E4%BB%80%E4%B9%88%E8%A6%81%E4%BD%BF%E7%94%A8%20Markdown) 中也提到过
- **Mermaid** 让图像与思维的联系更为紧密，书写时具有很强的逻辑性。即便不看图，单看源码，一样条理清晰

如何使用Mermaid？

- 在前期的学习中，可以试着仿照其他由绘图软件制作的图
- 熟悉了 **Mermaid** 语法后，要尽量避免这样的刻意 **“模仿”**
- Mermaid 是让你在书写中培养思维逻辑，并让它可视化，要让自己主动去写，去思考

### 7.2 Mermaid 流图

#### 7.2.1 关键字与方向

关键字和方向，是最基本的。你得告诉 **Mermaid**，你要画的是个什么图，图的走向是什么？

- 使用 `关键字`，声明图的**类型**
- 使用 `方向`，声明图的**方向**(走向)