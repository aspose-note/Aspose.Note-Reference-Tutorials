---
title: 在Aspose.Note文本中插入中文数字列表
linktitle: 在Aspose.Note文本中插入中文数字列表
second_title: Aspose.Note .NET API
description: 了解如何在 Aspose.Note for .NET 文档中轻松插入中文数字列表。通过此分步指南提高您的文档格式化技能。
type: docs
weight: 20
url: /zh/net/text-manipulation/insert-chinese-number-list/
---
## 介绍
您是否希望通过将中文数字列表合并到文档中来增强您的 Aspose.Note for .NET 技能？如果是这样，那么您来对地方了！在本教程中，我们将引导您完成使用 Aspose.Note for .NET 插入中文数字列表的过程。这个强大的库允许您无缝地操作 OneNote 文档。
## 先决条件
在我们深入学习本教程之前，请确保您具备以下先决条件：
- C# 编程基础知识。
- 已安装 Aspose.Note for .NET。你可以下载它[这里](https://releases.aspose.com/note/net/).
## 导入命名空间
首先，将必要的命名空间导入到您的项目中：
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 步骤1：初始化OneNote文档
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## 步骤2：初始化OneNote页面
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## 第 3 步：应用文本样式设置
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## 第 4 步：创建轮廓元素
现在，让我们用中文数字列表创建三个大纲元素：
### 步骤 4.1：第一个元素
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### 步骤 4.2：第二个元素
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### 步骤 4.3：第三个元素
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## 第 5 步：将元素附加到大纲中
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## 第 6 步：将大纲附加到页面
```csharp
page.AppendChildLast(outline);
```
## 第 7 步：将页面附加到文档
```csharp
doc.AppendChildLast(page);
```
## 步骤 8：保存 OneNote 文档
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
恭喜！您已使用 .NET 库成功将中文数字列表插入到 Aspose.Note 文档中。
## 结论
在本教程中，我们介绍了将中文数字列表合并到 Aspose.Note for .NET 文档中的分步过程。增强您的文档格式化技能，并通过这些技术使您的内容更具吸引力。
## 常见问题解答
### 问：我可以自定义中文号码列表的格式吗？
答：是的，您可以通过调整参数中的参数来自定义格式`NumberList`构造函数。
### 问：Aspose.Note 与最新版本的.NET 兼容吗？
答：是的，Aspose.Note 会定期更新以支持最新版本的 .NET。
### 问：在哪里可以找到其他示例和文档？
答：全面探索[Aspose.Note 文档](https://reference.aspose.com/note/net/).
### 问：如何获得 Aspose.Note 的临时许可证？
答：获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).
### 问：我可以在哪里寻求帮助或讨论与 Aspose.Note 相关的问题？
答：访问[Aspose.Note 支持论坛](https://forum.aspose.com/c/note/28)以获得社区支持。