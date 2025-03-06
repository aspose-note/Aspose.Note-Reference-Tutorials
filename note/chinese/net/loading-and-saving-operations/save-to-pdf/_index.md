---
title: 在 Aspose.Note 中保存为 PDF
linktitle: 在 Aspose.Note 中保存为 PDF
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 将 Microsoft OneNote 文档保存为 PDF 格式。包含 Letter 和 A4 页面布局代码示例的分步教程。
weight: 26
url: /zh/net/loading-and-saving-operations/save-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Note 中保存为 PDF

## 介绍

在本教程中，我们将探讨如何使用 Aspose.Note for .NET 将文档保存为 PDF 格式。 Aspose.Note 是一个功能强大的库，使开发人员能够以编程方式处理 Microsoft OneNote 文件。我们将介绍先决条件、导入命名空间，并提供将文档保存为各种页面布局的 PDF 的分步指南。

## 先决条件

在我们开始之前，请确保您具备以下条件：

- Visual Studio 安装在您的系统上。
- 下载并安装了 Aspose.Note for .NET 库。您可以从以下位置下载：[这里](https://releases.aspose.com/note/net/).
- C# 编程语言的基础知识。

## 导入命名空间

首先，让我们将必要的命名空间导入到我们的 C# 代码中：

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

现在我们已经满足了先决条件并导入了命名空间，让我们继续以不同的页面布局将文档保存为 PDF。

## 第 1 步：使用 Letter 页面设置保存为 PDF


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    //文档目录的路径。
    string dataDir = "Your Document Directory";

    //将文档加载到 Aspose.Note 中。
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    //保存文档。
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### 解释：

- 我们将 OneNote 文档加载到 Aspose.Note 中。
- 定义保存的 PDF 文件的目标路径。
- 使用以下命令将文档保存为 PDF`PdfSaveOptions`和`PageSettings`设置`Letter`.

## 步骤 2：使用无高度限制的 A4 页面设置保存为 PDF

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    //文档目录的路径。
    string dataDir = "Your Document Directory";

    //将文档加载到 Aspose.Note 中。
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    //保存文档。
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### 解释：

- 与上一步类似，我们将 OneNote 文档加载到 Aspose.Note 中。
- 定义保存的 PDF 文件的目标路径。
- 使用以下命令将文档保存为 PDF`PdfSaveOptions`和`PageSettings`设置`A4NoHeightLimit`.

## 结论

在本教程中，我们学习了如何使用 Aspose.Note for .NET 将文档保存为 PDF 格式。我们介绍了两种不同的页面布局：Letter 和 A4，没有高度限制。借助 Aspose.Note，开发人员可以轻松地以编程方式操作 OneNote 文件，从而为文档管理任务提供灵活性和效率。

## 常见问题解答

### Q1：Aspose.Note 可以处理复杂的 OneNote 文件吗？

A1：是的，Aspose.Note 支持各种特性和功能来有效处理复杂的 OneNote 文件。

### Q2：Aspose.Note适合商业项目吗？

 A2：当然可以，Aspose.Note 可以轻松地用于商业项目。您可以购买许可证[这里](https://purchase.aspose.com/buy).

### Q3：Aspose.Note 提供免费试用吗？

A3：是的，您可以通过免费试用版探索 Aspose.Note[这里](https://releases.aspose.com/).

### Q4：在哪里可以找到 Aspose.Note 的文档？

 A4：你可以找到详细的文档[这里](https://reference.aspose.com/note/net/).

### Q5: 需要进一步帮助吗？

 A5：请随时在 Aspose.Note 论坛上提出任何问题或寻求支持[这里](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
