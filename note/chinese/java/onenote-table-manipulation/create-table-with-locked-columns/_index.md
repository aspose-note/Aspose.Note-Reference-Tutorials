---
date: 2026-01-23
description: 了解如何在使用 Aspose.Note for Java 向 OneNote 添加表格时锁定列宽。一步一步的指南，包含代码、技巧和常见问题解答。
linktitle: How to Lock Column in OneNote Table – Aspose.Note
second_title: Aspose.Note Java API
title: 如何在 OneNote 表格中锁定列 – Aspose.Note
url: /zh/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 OneNote 表格中锁定列 – Aspose.Note

## 介绍
OneNote 是一个多功能的记笔记平台，Aspose.Note for Java 使在向 OneNote 添加表格时轻松 **锁定列** 宽度。 在本教程中，您将看到一个完整的实战示例，展示如何设置表格列宽、锁定该宽度以及自定义 OneNote 表格边框——只需几行 Java 代码。

## 快速答案
- **“锁定列”是什么意思？** 它固定列宽，使用户在 OneNote 中无法调整大小。  
- **哪个库提供此功能？** Aspose.Note for Java。  
- **运行示例是否需要许可证？** 免费试用可用于评估；生产环境需要商业许可证。  
- **锁定列后还能添加更多行吗？** 可以，您可以继续追加行；锁定的宽度仍然保持。  
- **支持哪个版本的 Java？** Java 6 及更高版本。

## 在 OneNote 表格中，“锁定列” 是什么？
锁定列是指为 `TableColumn` 对象分配固定宽度，并将其 `LockedWidth` 属性设置为 `true`。这可以防止最终用户意外调整大小，保持布局一致。

## 为什么在 OneNote 中锁定列宽？
- **一致的布局** – 您的笔记在每个设备上看起来相同。  
- **更好的可读性** – 长文本在可预测的列宽内换行。  
- **专业的外观** – 锁定列提供精致、类似报告的感觉。

## 先决条件
在开始之前，请确保以下内容已准备好：

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) 已在您的机器上安装。  
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) 库已下载并添加到项目的类路径中。

## 导入包
在您的 Java 项目中，导入使用 Aspose.Note 所需的包：

```java
import com.aspose.note.*;
import java.io.IOException;
```

## 步骤 1：设置项目
创建一个新的 Java 项目（或使用现有项目），并将 Aspose.Note JAR 文件添加到构建路径。确保项目使用已安装的 JDK 编译。

## 步骤 2：初始化 Document 和 Page 对象
我们首先创建一个全新的 `Document` 和一个用于放置表格的 `Page`。

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## 步骤 3：创建表格行和单元格
这里我们构建两行，每行只有一个单元格，包含一些示例文本。这演示了锁定列在短内容和长内容下的表现。

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## 步骤 4：创建并自定义表格
现在我们创建表格，**设置表格列宽**、**锁定列**，以及**自定义 OneNote 表格边框**。

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);               // customize onenote table borders
TableColumn col = new TableColumn();
col.setWidth(200);                           // set table column width
col.setLockedWidth(true);                    // onenote table locked width
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## 步骤 5：将表格添加到大纲和页面
我们现在将表格附加到 `OutlineElement`，并最终将其添加到页面——这就是 **add outline element java** 步骤。

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## 步骤 6：保存文档
将 OneNote 文件（`.one`）保存到您之前指定的目录。

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

恭喜！您已成功使用 Aspose.Note for Java **将表格添加到 OneNote**，实现了锁定列、固定宽度和自定义边框。

## 常见问题及解决方案
| 问题 | 解决方案 |
|-------|----------|
| 表格显示无边框 | 确保已调用 `table.setBordersVisible(true);`。 |
| 添加行后列宽发生变化 | 确认在追加行之前已设置 `col.setLockedWidth(true);` **before** 行被追加。 |
| 文件未保存 | 检查 `dataDir` 是否指向可写文件夹且以有效文件名结尾。 |

## 常见问题
**Q: Aspose.Note for Java 是否兼容所有 Java 版本？**  
A: 是的，它支持 Java 6 及更高版本，包括 Java 11 和 Java 17。

**Q: 我可以进一步自定义表格的外观吗？**  
A: 当然！您可以通过 `Table` 和 `TableCell` 属性修改边框样式、单元格内边距、背景颜色等。

**Q: 在购买前是否有试用版？**  
A: 有，您可以 [下载免费试用版](https://releases.aspose.com/) 来体验 Aspose.Note for Java 的功能。

**Q: 我在哪里可以找到更多支持或社区讨论？**  
A: 请访问 [Aspose.Note 论坛](https://forum.aspose.com/c/note/28) 获取支持和社区讨论。

**Q: 如何获取 Aspose.Note for Java 的临时许可证？**  
A: 请访问 [此链接](https://purchase.aspose.com/temporary-license/) 获取用于测试的临时许可证。

---

**最后更新：** 2026-01-23  
**已测试：** Aspose.Note for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}