---
title: 在 OneNote 中创建具有锁定列的表 - Aspose.Note
linktitle: 在 OneNote 中创建具有锁定列的表 - Aspose.Note
second_title: Aspose.Note Java API
description: 使用 Aspose.Note for Java 增强您的 OneNote 体验。了解如何使用分步指南创建具有锁定列的表。立即下载免费试用版！
type: docs
weight: 12
url: /zh/java/onenote-table-manipulation/create-table-with-locked-columns/
---
## 介绍
OneNote 是一个用于组织信息的强大工具，Aspose.Note for Java 通过提供无缝方式创建具有锁定列的表来增强其功能。在本教程中，我们将指导您完成使用 Aspose.Note for Java 在 OneNote 中创建具有锁定列的表的过程。
## 先决条件
在开始之前，请确保您具备以下先决条件：
- [Java 开发工具包 (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)安装在您的机器上。
- [用于 Java 的 Aspose.Note](https://downloads.aspose.com/note/java)库已下载并添加到您的项目中。
## 导入包
在您的 Java 项目中，导入使用 Aspose.Note 所需的包：
```java
import com.aspose.note.*;
import java.io.IOException;
```
## 第 1 步：设置您的项目
首先创建一个新的 Java 项目并将 Aspose.Note 库添加到类路径中。确保您的项目配置为使用 JDK。
## 第 2 步：初始化文档和页面对象
```java
//文档目录的路径。
String dataDir = "Your Document Directory";
//创建Document类的对象
Document doc = new Document();
//初始化Page类对象
Page page = new Page();
```
## 第 3 步：创建表格行和单元格
```java
//初始化TableRow类对象
TableRow row1 = new TableRow();
//初始化TableCell类对象并设置文本内容
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
//初始化TableRow类对象
TableRow row2 = new TableRow();
//初始化TableCell类对象并设置文本内容
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## 第 4 步：创建并自定义表格
```java
//初始化Table类对象
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
//添加行
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## 第5步：将表格添加到大纲和页面
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
//添加表节点
outlineElem.appendChildLast(table);
//添加轮廓元素节点
outline.appendChildLast(outlineElem);
//添加轮廓节点
page.appendChildLast(outline);
//添加页面节点
doc.appendChildLast(page);
```
## 第 6 步：保存文档
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
恭喜！您已使用 Aspose.Note for Java 在 OneNote 中成功创建了带有锁定列的表。
## 结论
在本教程中，我们探索了利用 Aspose.Note for Java 通过创建具有锁定列的表来增强 OneNote 体验的过程。此功能为您的笔记添加了新的组织和结构层。
## 常见问题解答
### Aspose.Note for Java 是否与所有 Java 版本兼容？
是的，Aspose.Note for Java 与 Java 6 及更高版本兼容。
### 我可以进一步自定义表格的外观吗？
绝对地！ Aspose.Note for Java 提供了广泛的自定义表格选项，例如调整边框、单元格间距等。
### 购买前是否有试用版？
是的你可以[下载免费试用版](https://releases.aspose.com/)探索 Aspose.Note for Java 的功能。
### 我在哪里可以找到其他支持或社区讨论？
参观[Aspose.Note 论坛](https://forum.aspose.com/c/note/28)用于支持和社区讨论。
### 如何获得 Aspose.Note for Java 的临时许可证？
访问[这个链接](https://purchase.aspose.com/temporary-license/)获得用于测试目的的临时许可证。