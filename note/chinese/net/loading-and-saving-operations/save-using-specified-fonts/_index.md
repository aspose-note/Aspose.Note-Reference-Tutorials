---
title: 在 Aspose.Note 中使用指定字体保存
linktitle: 在 Aspose.Note 中使用指定字体保存
second_title: Aspose.Note .NET API
description: 了解如何在 Aspose.Note for .NET 中保存具有指定字体的文档。轻松自定义字体设置，以实现一致的文档格式。
type: docs
weight: 28
url: /zh/net/loading-and-saving-operations/save-using-specified-fonts/
---
## 介绍

在本教程中，我们将学习如何在 Aspose.Note for .NET 中使用指定字体保存文档。我们将逐步探索实现这一目标的不同方法。

## 先决条件

在我们开始之前，请确保您具备以下条件：

1.  Aspose.Note for .NET：确保您已安装 Aspose.Note for .NET。您可以从以下位置下载：[这里](https://releases.aspose.com/note/net/).

2. 开发环境：您需要为.NET 开发设置一个开发环境。

## 导入命名空间

首先，让我们导入必要的名称空间：

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## 第 1 步：使用默认字体名称保存

在此步骤中，我们将使用指定的默认字体名称保存文档。

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    //文档目录的路径。
    string dataDir = "Your Document Directory";

    //将文档加载到 Aspose.Note 中。
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    //使用指定的默认字体将文档另存为 PDF。
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## 步骤 2：使用文件中的默认字体保存

接下来，让我们使用从文件加载的默认字体保存文档。

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    //文档目录的路径。
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    //将文档加载到 Aspose.Note 中。
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    //使用从文件加载的默认字体将文档另存为 PDF。
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## 步骤 3：使用 Stream 中的默认字体保存

最后，让我们使用从流加载的默认字体保存文档。

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    //文档目录的路径。
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    //将文档加载到 Aspose.Note 中。
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    //使用从流加载的默认字体将文档另存为 PDF。
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## 结论

在本教程中，我们探讨了如何在 Aspose.Note for .NET 中使用指定字体保存文档。通过执行以下步骤，您可以根据您的要求自定义字体设置，确保文档的格式符合您的要求。

## 常见问题解答

### Q1: 我可以使用任何字体在Aspose.Note中保存文档吗？

A1: 是的，您可以指定任何字体来保存文档。只需确保字体文件可访问并正确加载即可。

### Q2：Aspose.Note 是否兼容不同的文档格式？

A2：Aspose.Note 主要适用于 OneNote 文档，但提供了保存为各种格式（包括 PDF）的选项。

### Q3：保存文档时字体丢失如何处理？

A3：Aspose.Note 提供了使用默认字体的选项，以防指定字体丢失，确保文档格式一致。

### Q4：Aspose.Note 支持在输出文档中嵌入字体吗？

A4：是的，Aspose.Note 允许嵌入字体，以确保文档的可移植性和跨不同平台的一致渲染。

### Q5：我可以在哪里获得有关 Aspose.Note 的进一步帮助？

 A5： 如需进一步帮助或技术支持，您可以访问[Aspose.Note 论坛](https://forum.aspose.com/c/note/28).