---
title: 在Aspose.Note中获取图像信息
linktitle: 在Aspose.Note中获取图像信息
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 从 Microsoft OneNote 文件中提取图像信息。遵循我们的分步指南以实现高效开发。
weight: 13
url: /zh/net/images/get-info-of-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在Aspose.Note中获取图像信息

## 介绍

在 .NET 开发领域，Aspose.Note 提供了一组强大的工具来处理 Microsoft OneNote 文件。开发人员经常面临的一项常见任务是从这些笔记中嵌入的图像中提取信息。无论是获取尺寸、文件名还是修改时间，Aspose.Note 都简化了这个过程。

## 先决条件

在我们深入使用 Aspose.Note 提取图像信息之前，请确保您具备以下条件：

1. C# 基础知识：熟悉 C# 编程语言对于理解代码示例至关重要。
2. 安装了 Aspose.Note for .NET：确保您的开发环境中安装了 Aspose.Note 库。你可以下载它[这里](https://releases.aspose.com/note/net/).

## 导入命名空间

在开始之前，让我们导入必要的名称空间：

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## 第 1 步：加载文档

首先，将目标 OneNote 文档加载到 Aspose.Note 中：

```csharp
//文档目录的路径。
string dataDir = "Your Document Directory";

//将文档加载到 Aspose.Note 中。
Document oneFile = new Document(dataDir + "Aspose.one");
```

代替`"Your Document Directory"`以及 OneNote 文件的路径。

## 第2步：检索图像信息

接下来，从文档中检索所有图像节点：

```csharp
//获取所有Image节点
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

此代码片段获取加载的 OneNote 文档中的所有图像节点。

## 第 3 步：迭代图像

现在，让我们迭代每个图像节点以提取其元数据：

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

该循环打印出每个图像的各种属性，例如宽度、高度、原始尺寸、文件名和上次修改时间。

## 结论

借助 Aspose.Note for .NET，从 OneNote 文档中提取图像信息成为一个无缝过程。通过遵循本教程中概述的步骤，开发人员可以有效地从嵌入图像中检索元数据，从而使他们能够构建强大的应用程序。

## 常见问题解答

### Q1：Aspose.Note 是否兼容所有版本的 Microsoft OneNote？

A1：Aspose.Note 支持多种格式的 OneNote 文件，包括 .one、.onepkg 和 .onetoc2，确保不同版本之间的兼容性。

### Q2：我可以使用Aspose.Note修改图像属性吗？

A2：是的，Aspose.Note 允许您以编程方式操作图像属性，例如尺寸、文件名和修改时间。

### Q3：Aspose.Note 是否提供对 .NET Core 的支持？

A3：是的，Aspose.Note 提供对 .NET Core 的支持，使您的应用程序能够跨平台开发。

### Q4：Aspose.Note 有免费试用版吗？

A4：是的，您可以在购买之前免费试用 Aspose.Note 以探索其功能。

### 问题 5：我在哪里可以找到有关 Aspose.Note 的其他支持或帮助？

A5：如有任何疑问或帮助，您可以访问 Aspose.Note 论坛[这里](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
