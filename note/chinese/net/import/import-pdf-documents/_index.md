---
title: 将 PDF 文档导入 Aspose.Note
linktitle: 将 PDF 文档导入 Aspose.Note
second_title: Aspose.Note .NET API
description: 了解如何使用各种合并选项轻松将 PDF 文档导入 Aspose.Note for .NET 中以实现无缝集成。
weight: 10
url: /zh/net/import/import-pdf-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 PDF 文档导入 Aspose.Note

## 介绍

如今，可用的数字内容数量巨大，将 PDF 文档无缝集成到您的项目中至关重要。 Aspose.Note for .NET 提供了强大的功能来高效导入 PDF 文档。在本教程中，我们将探索如何使用 Aspose.Note for .NET 逐步导入 PDF 文档。

## 先决条件

在深入学习本教程之前，请确保您具备以下条件：

1.  Aspose.Note for .NET：从以下地址下载并安装库[这里](https://releases.aspose.com/note/net/).
2. C# 和 .NET Framework 的基础知识：了解 C# 编程语言和 .NET Framework 将很有帮助。

## 导入命名空间

确保导入必要的命名空间以访问 PDF 导入功能所需的类和方法：

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;

using Aspose.Note.Importing;

```

## 第 1 步：使用简单合并导入 PDF 文档

简单合并方法允许逐页导入多个 PDF 文档中的所有页面：

```csharp
public static void ImportSetOfFiles_SimpleMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    d.Import(Path.Combine(dataDir, "sampleText.pdf"))
     .Import(Path.Combine(dataDir, "sampleImage.pdf"))
     .Import(Path.Combine(dataDir, "sampleTable.pdf"));

    d.Save(Path.Combine(dataDir, "sample_SimpleMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## 步骤 2：使用结构化合并导入 PDF 文档

结构化合并导入 PDF 文档中的所有页面，同时将每个文档中的页面插入为顶级 OneNote 页面的子级：

```csharp
public static void ImportSetOfFiles_StructuredMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    foreach (var file in new[] { "sampleText.pdf", "sampleImage.pdf", "sampleTable.pdf" })
    {
        d.AppendChildLast(new Page()).Title = new Title() { TitleText = new RichText() { ParagraphStyle = ParagraphStyle.Default }.Append(file) };
        d.Import(Path.Combine(dataDir, file), new PdfImportOptions(), new MergeOptions() { InsertAt = int.MaxValue, InsertAsChild = true });
    }

    d.Save(Path.Combine(dataDir, "sample_StructuredMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## 步骤 3：使用单页合并导入 PDF 文档

单页合并将多个 PDF 文档的内容合并到单个 OneNote 页面上：

```csharp
public static void ImportSetOfFiles_SinglePageMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    var importOptions = new PdfImportOptions();
    var mergeOptions = new MergeOptions() { ImportAsSinglePage = true, PageSpacing = 100 };

    d.Import(Path.Combine(dataDir, "sampleText.pdf"), importOptions, mergeOptions)
     .Import(Path.Combine(dataDir, "sampleImage.pdf"), importOptions, mergeOptions)
     .Import(Path.Combine(dataDir, "sampleTable.pdf"), importOptions, mergeOptions);

    d.Save(Path.Combine(dataDir, "sample_SinglePageMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## 步骤 4：使用自定义合并导入 PDF 文档

自定义合并允许根据自定义标准将 PDF 文档中的页面分组为单个 OneNote 页面：

```csharp
public static void ImportSetOfFiles_CustomMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    var mergeOptions = new MergeOptions() { ImportAsSinglePage = true, PageSpacing = 100 };

    IEnumerable<Page> pages = PdfImporter.Import(Path.Combine(dataDir, "SampleGrouping.pdf"));
    while (pages.Any())
    {
        d.Merge(pages.Take(5), mergeOptions);
        pages = pages.Skip(5);
    }

    d.Save(Path.Combine(dataDir, "sample_CustomMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## 结论

使用 Aspose.Note 将 PDF 文档集成到您的 .NET 应用程序中是一个简单的过程，提供了根据您的项目要求定制的各种合并选项。无论您需要导入多个页面还是分层组织内容，Aspose.Note 都提供了无缝集成所需的工具。

## 常见问题解答

### Q1：我可以导入加密的PDF文档吗？

A1: 是的，Aspose.Note 支持导入加密的 PDF 文档。确保您提供所需的解密凭据。

### Q2：导入的PDF文件大小有限制吗？

A2：Aspose.Note 对于导入的 PDF 文件大小没有固有的限制。但是，请考虑大型 PDF 文件的系统资源和性能影响。

### Q3：我可以自定义导入的 PDF 内容的外观吗？

A3：是的，您可以使用 Aspose.Note 提供的各种选项自定义导入的 PDF 内容的外观，例如字体样式、颜色和布局调整。

### Q4：Aspose.Note 与.NET Core 兼容吗？

A4：是的，Aspose.Note 与 .NET Core 兼容，允许您将 PDF 导入功能集成到跨平台应用程序中。

### Q5：我在哪里可以找到额外的支持或资源？

 A5：如需更多支持、文档或社区帮助，请访问[Aspose.Note 论坛](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
