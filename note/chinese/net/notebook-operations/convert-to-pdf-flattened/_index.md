---
title: 在 Aspose Note .NET 中将笔记本转换为 PDF（扁平化）
linktitle: 在 Aspose Note .NET 中将笔记本转换为 PDF（扁平化）
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 轻松将 OneNote 笔记本转换为扁平 PDF。无缝保存您的内容。
weight: 15
url: /zh/net/notebook-operations/convert-to-pdf-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose Note .NET 中将笔记本转换为 PDF（扁平化）

## 介绍

您是否希望使用 Aspose Note .NET 将 OneNote 笔记本转换为扁平 PDF？您来对地方了！在本教程中，我们将逐步演示该过程。

## 先决条件

在我们开始之前，请确保您具备以下条件：

1.  Aspose.Note for .NET：确保您已下载并安装 Aspose.Note for .NET。如果没有，您可以从[这里](https://releases.aspose.com/note/net/).
2. Visual Studio：您需要在系统上安装 Visual Studio 来进行编码和编译。
3. OneNote 笔记本：准备好要转换为 PDF 的 OneNote 笔记本。

## 导入命名空间

首先，我们在 C# 代码中导入必要的命名空间：

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## 第 1 步：加载 OneNote 笔记本

```csharp
//文档目录的路径。
string dataDir = "Your Document Directory";

//加载 OneNote 笔记本
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

在此步骤中，我们使用以下命令加载 OneNote 笔记本`Notebook`Aspose.Note 提供的类。

## 第 2 步：通过拼合转换为 PDF

```csharp
//通过拼合将笔记本另存为 PDF
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

在这里，我们将加载的笔记本另存为 PDF，其中包含`Flatten`属性设置为`true`。此属性将所有内容（包括注释和图像）合并到 PDF 中。

## 第3步：打印成功消息

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

最后，我们打印一条成功消息以及 PDF 的保存路径。

## 结论

恭喜！您已使用 Aspose.Note for .NET 成功将 OneNote 笔记本转换为拼合 PDF。此过程可确保您的所有内容以 PDF 格式准确保存，从而更轻松地共享和分发。

## 常见问题解答

### Q1：我可以保留PDF中的交互元素吗？

A1：Aspose.Note 将内容（包括复选框或表单字段等交互式元素）扁平化到 PDF 中，使它们成为静态的。

### Q2：Aspose.Note支持将笔记本转换为其他格式吗？

A2：是的，Aspose.Note 支持将笔记本转换为各种格式，例如 PDF、HTML、图像等。

### Q3：我可以自定义转换选项吗？

A3：当然！ Aspose.Note 在转换过程中提供了广泛的自定义选项，允许您根据您的要求定制输出。

### Q4：有试用版吗？

 A4：是的，您可以免费试用 Aspose.Note[这里](https://releases.aspose.com/).

### Q5：如果遇到任何问题，我可以在哪里获得支持？

 A5：您可以通过以下地址寻求 Aspose 社区的支持：[Aspose.Note 论坛](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
