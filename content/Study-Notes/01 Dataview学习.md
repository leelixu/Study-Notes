---
Title: 01 Dataview学习
C_time: 2023-06-28-23:49
Done_time: 2023-06-29-22:30
Status: Done
draft: true
Tag:
- #Obsidian
- #Dataview
---

原文：[Obsidian DataView 入门保姆级引导手册](https://zhuanlan.zhihu.com/p/614881764)

# DataView 查询语法

````text
```dataview
<QUERY-TYPE> <WITHOUT ID> <字段>(as "别名")
FROM <来源>
<WHERE> <条件表达式>
<SORT> <排序依据 排序方式>
<GROUP BY> <分组依据>
<LIMIT> <限定显示记录数>
<FLATTEN> <拆分表达式>
```
````

## 1 QUERY-TYPE说明

### 1.1 TABLE 表格

以表格的形式显示符合查询条件的文件清单和相关属性。

### 1.2 LIST 列表

以无序列表的形式显示符合查询条件的文件清单。

### 1.3 TASK 任务

仅以任务列表的形式显示符合查询条件的任务列表。

### 1.4 CALENDAR 日历

以日历视图的形式显示查询结果

## 2 字段说明

### 2.1 文件自带的属性

|文件属性|字段类型|属性说明|
|---|---|---|
|file.name|Text|文件名|
|file.folder|Text|所在文件夹|
|file.path|Text|完整路径 + 完整文件名|
|file.ext|Text|扩展名|
|file.link|Link|链接至本文件|
|file.size|Number|文件大小 (bytes)|
|file.ctime|Date Time|创建时间|
|file.cday|Date|创建日期|
|file.mtime|Date Time|最后修改时间|
|file.mday|Date|最后修改日期|
|file.tags|List|文中的 `#标签` 和 YAML 中的 tags|
|file.etags|List|文中的 `#标签` 和 YAML 中的 tags|
|file.inlinks|List|反向链接|
|file.outlinks|List|正向链接|
|file.tasks|List|文中的任务列表|
|file.lists|List|文中的列表 (包含任务列表)|
|file.frontmatter|List|文件中的 YAML 块内容|
|file.starred|Boolean|加星|

### 2.2 YAML自定义属性

例如：

```Text
学习笔记模版
---
Title: {{title}}
C_time: {{date}}-{{time}}
Done_time: NA
Status: Undone or Done
Tag:
- 
---
```

其中`:` 之前的为属性名，直接使用，不需要 `file.属性`，`:` 之后==必须接空格==。

### 2.3 属性的字段类型

|字段类型|表达方式|举例|
|---|---|---|
|Text|用 "" 括起来的字符|"这就是 Text 类型"|
|Number|由符号 + - 数字 0 ~ 9 和小数点 . 组成|-0.98|
|Boolean|只有 true 和 false 两个值，表示是与否|true|
|Date|由日期和时间组成，遵循ISO 8601标准  <br>格式为 YYYY-MM[-DDTHH:mm:ss.nnn+ZZ]|2021-04-18|
|Link|使用\[\[内部文件链接\]\]的链接|"\[\[内部文件链接\]\]"|
|List|有序/无序/任务列表|- 无序列表|

## 3 FROM 数据来源

### 3.1 Tags 标签

````text
```dataview
LIST
FROM #DataView 
```
````

### 3.2 Folders 文件夹

````text
```
TABLE
FROM "01 编程学习"
```
````

### 3.3 pecific Files 指定文件

````text
```dataview
TABLE
FROM "01 编程学习/python学习"
```
````

### 3.4 Links 链接

````text
```dataview
LIST
FROM outgoing([[python学习]]) 
```
````

### 3.5 Combing Sources 多重来源

即将 1、2、4 组合起来使用

````text
```dataview
TABLE
FROM "01 编程学习" and outgoing([[python学习]])
```
````

## 4 WHERE 过滤条件

### 4.1 Text 类条件

1. 包含指定文本


````text
```dataview
TABLE
FROM "02 其他学习"
where icontains(file.name,"dataview")
```
// contains(file.name,"obsidian") 大小写敏感
// icontains(file.name,"obsidian") 大小写不敏感
````

2. 不包含指定文本

````text
```dataview
TABLE
FROM "02 其他学习"
where !icontains(file.name,"dataview")
```
````

3. 以特定文本开头

````text
```dataview
TABLE
FROM "02 其他学习"
where startswith(file.name,"dataview")
```
````

4. 以特定文本结尾

````text
```dataview
TABLE
FROM "02 其他学习"
where endswith(file.name,"dataview")
```
````

5. 英文大小写转换

````text
```dataview
TABLE
FROM "02 其他学习"
where endswith(lower(file.name),"dataview") or
where endswith(upper(file.name),"dataview")
```
````

### 4.2 Number 类条件

1. 等于与不等于

````text
```dataview
TABLE
FROM "02 其他学习"
where number = 9
```
````

2. 大于或大于等于

````text
```dataview
TABLE
FROM "02 其他学习"
where number > 9 or 
where number >= 9
```
````

3. 小于或小于等于

````text
```dataview
TABLE
FROM "02 其他学习"
where number < 9 or 
where number <= 9
```
````

4. 数字的四则运算

````text
```dataview
TABLE
FROM "02 其他学习"
where number1 - number2 = 9 
```
````

### 4.3 Date类条件

1. 日期的格式化

````text
```dataview
TABLE WITHOUT ID
  file.link as "文件名称",
  dateformat(file.cday,"yyyy-MM-dd") as "创建日期",
  dateformat(file.ctime,"HH:mm: ss") as "创建时间",
  choice(file.starred, "是", "否") as "加星"
FROM "200-学习箱/210-知识库搭建"
WHERE file.cday <= date("2023-02-20")
```

//日期格式化通常只作为输出显示格式定义，不作为条件
````

2. 等于指定日期

````text
```dataview
TABLE WITHOUT ID
  file.link as "文件名称",
  dateformat(file.cday,"yyyy-MM-dd") as "创建日期",
  choice(file.starred, "是", "否") as "加星"
FROM "200-学习箱/210-知识库搭建"
WHERE file.cday = date("2023-02-19")
```
````

3. 大于等于指定日期

````text
```dataview
TABLE WITHOUT ID
  file.link as "文件名称",
  dateformat(file.cday,"yyyy-MM-dd") as "创建日期",
  choice(file.starred, "是", "否") as "加星"
FROM "200-学习箱/210-知识库搭建"
WHERE file.cday >= date("2023-02-19")
```
````

4. 小于等于指定日期

````text
```dataview
TABLE WITHOUT ID
  file.link as "文件名称",
  dateformat(file.cday,"yyyy-MM-dd") as "创建日期",
  choice(file.starred, "是", "否") as "加星"
FROM "200-学习箱/210-知识库搭建"
WHERE file.cday <= date("2023-02-20")
```
````

5. 常用的日期属性

````text
```dataview
TABLE WITHOUT ID
  file.link as "文件名称",
  dateformat(file.cday,"yyyy-MM-dd") as "创建日期",
  choice(file.starred, "是", "否") as "加星"
FROM "200-学习箱/210-知识库搭建"
WHERE file.cday.month = date(today).month
```

// year
// month
// day
// date (today)
// date (now)
// date (tomorrow)
// date (yesterday)
// date (sow)
// date (eow)
````

### 4.4 Boolean类条件

````text
```dataview
TABLE WITHOUT ID
  file.link as "文件名称",
  dateformat(file.cday,"yyyy-MM-dd") as "创建日期",
  choice(file.starred, "是", "否") as "加星"
FROM "02 其他学习"
WHERE file.starred
```
// file.starred---加星
// !file.starred--未加星

```dataview
TASK
WHERE !fullyCompleted
```
// 如果本级任务未完成，下级任务已完成，会将下级已完成的一起显示
// fullyCompleted and !fullyCompleted
````

Boolean 类字段的格式化，就是将 true、false 转换为更偏于用户阅读的是 / 否，或者是 yes / no

### 4.5 List类条件

````text
```dataview
TABLE WITHOUT ID
  file.link as "文件名称",
  dateformat(file.cday,"yyyy-MM-dd") as "创建日期",
  choice(file.starred, "是", "否") as "加星"
FROM "200-学习箱/210-知识库搭建"
WHERE contains(tags,"DataView")
```
````

### 4.6 Link类条件

````text
```dataview
TABLE WITHOUT ID
  file.link as "文件名称",
  dateformat(file.cday,"yyyy-MM-dd") as "创建日期",
  choice(file.starred, "是", "否") as "加星"
FROM "200-学习箱/210-知识库搭建"
WHERE contains(file.outlinks, [[内部文件链接]])
```
````

### 4.7 and 条件连接符

```text
<条件1> and <条件2>

1. 只满足<条件1>，不会被显示到查询结果中
2. 只满足<条件2>，不会被显示到查询结果中
3. 同时满足<条件1>和<条件2>，会显示到查询结果中
```

### 4.8 or条件连接符

```text
<条件1> or <条件2>

1. 只满足<条件1>，会被显示到查询结果中
2. 只满足<条件2>，会被显示到查询结果中
3. 同时满足<条件1>和<条件2>，会显示到查询结果中
```

### 4.9 ()定义条件优先级

```text
仅发生在需要同时运用 and 和 or 两个边接符时，才需要使用括号定义优先级

（<条件1> or <条件2>) and <条件3>

1. 只满足<条件1>，不会被显示到查询结果中
2. 只满足<条件2>，不会被显示到查询结果中
3. 只满足<条件3>，不会被显示到查询结果中
4. 同时满足<条件1>和<条件2>，不会显示到查询结果中
5. 同时满足<条件1>和<条件3>，会显示到查询结果中
6. 同时满足<条件2>和<条件3>，会显示到查询结果中
7. 同时满足<条件1>、<条件2>和<条件3>，会显示到查询结果中
仅发生在需要同时运用 and 和 or 两个边接符时，才需要使用括号定义优先级

（<条件1> and <条件2>) or <条件3>

1. 只满足<条件1>，不会被显示到查询结果中
2. 只满足<条件2>，不会被显示到查询结果中
3. 只满足<条件3>，会被显示到查询结果中
4. 同时满足<条件1>和<条件2>，会显示到查询结果中
5. 同时满足<条件1>和<条件3>，会显示到查询结果中
6. 同时满足<条件2>和<条件3>，会显示到查询结果中
7. 同时满足<条件1>、<条件2>和<条件3>，会显示到查询结果中
```
