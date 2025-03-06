---
title: 使用 Aspose.Note 撰写表格
linktitle: 使用 Aspose.Note 撰写表格
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 编写包含富文本内容的结构化表格。轻松增强文档的组织性和可读性。
weight: 11
url: /zh/net/table-manipulation/compose-tables/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Note 撰写表格

## 介绍

表格是文档的基本组成部分，可实现信息的结构化呈现。 Aspose.Note for .NET 提供了强大的工具来轻松地编写表格。在本教程中，我们将指导您完成使用 Aspose.Note 创建具有富文本内容的表格的过程。

## 先决条件

在使用 Aspose.Note for .NET 深入研究表组成之前，请确保您满足以下先决条件：

1. 环境设置：确保您拥有使用 .NET Framework 或 .NET Core 设置的合适的开发环境。
2. 安装：从以下位置下载并安装 Aspose.Note for .NET[网站](https://releases.aspose.com/note/net/).
3. 基础知识：熟悉 C# 编程和文档操作的基本概念。

## 导入命名空间

在开始组合表之前，请确保导入必要的命名空间：

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

让我们将提供的示例分解为可管理的步骤：

## 第 1 步：设置文档目录

在构建表格之前，定义保存文档的目录。

```csharp
string dataDir = "Your Document Directory";
```

## 第 2 步：创建标题文本

使用特定样式定义标题文本，例如字体大小和粗体。

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## 第 3 步：创建页面和大纲

初始化页面和大纲以构建内容。

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## 第 4 步：添加摘要文本

在表格前添加摘要文本。

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## 第5步：创建表

初始化表以按行和列组织数据。

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## 第 6 步：添加标题行

使用包含列标题的标题行填充表。

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## 步骤 7：添加空行

插入空行以准备数据插入。

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## 第 8 步：添加联系信息

使用模板内容填充“联系人”列。

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## 第9步：保存文档

保存组成的表格文档。

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## 第10步：确认

确认文档撰写成功。

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## 结论

在本教程中，我们探索了如何使用 Aspose.Note for .NET 编写具有富文本内容的表格。通过遵循这些分步说明，您可以在文档中高效地创建结构化表格，从而增强可读性和组织性。

## 常见问题解答

### Q1：我可以自定义表格元素的样式吗？
   
A1: 是的，您可以自定义各个方面，例如字体大小、颜色和对齐方式，以满足您的要求。

### Q2：Aspose.Note 与其他.NET 库兼容吗？
   
A2：Aspose.Note 与其他 .NET 库无缝集成，为文档操作提供了广泛的灵活性。

### Q3：Aspose.Note 支持将表格导出为不同格式吗？
   
A3：当然，Aspose.Note 允许您将表格导出为各种格式，包括 PDF、DOCX 和 HTML。

### 问题 4：我可以使用外部源的数据动态填充表吗？
   
A4：是的，您可以通过从数据库、API 或用户输入获取数据来动态填充表。

### Q5：Aspose.Note 用户可以获得技术支持吗？
   
A5：是的，Aspose 通过其论坛和专用支持渠道提供全面的技术支持。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
