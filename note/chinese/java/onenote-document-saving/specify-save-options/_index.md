---
title: 在 OneNote 中指定保存选项 - Aspose.Note
linktitle: 在 OneNote 中指定保存选项 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 在 OneNote 中指定保存选项。轻松自定义页面索引、计数和压缩设置。
type: docs
weight: 24
url: /zh/java/onenote-document-saving/specify-save-options/
---
## 介绍

在本教程中，我们将学习如何使用 Aspose.Note for Java 在 OneNote 中指定保存选项。 Aspose.Note 是一个功能强大的 Java 库，允许开发人员以编程方式创建、操作和转换 OneNote 文档。使用Aspose.Note，您可以轻松控制各种保存选项，以根据您的要求自定义输出。

## 先决条件

在开始之前，请确保您具备以下先决条件：

1. Java 编程语言的基础知识。
2. 系统上安装了 JDK（Java 开发工具包）。
3. 安装了 Java 库的 Aspose.Note。您可以从以下位置下载：[这里](https://releases.aspose.com/note/java/).

## 导入包

首先，在 Java 代码中导入必要的包：

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

让我们将该示例分解为多个步骤：

## 第1步：加载OneNote文档

```java
//文档目录的路径。
String dataDir = "Your Document Directory";

//将文档加载到 Aspose.Note 中。
Document doc = new Document(dataDir + "Aspose.one");
```

在这一步中，我们指定 OneNote 文档的路径并将其加载到`Document`目的。

## 步骤 2：初始化 PdfSaveOptions 对象

```java
//初始化 PdfSaveOptions 对象
PdfSaveOptions opts = new PdfSaveOptions();
```

在这里，我们初始化一个`PdfSaveOptions`对象，用于指定将文档另存为 PDF 的选项。

## 步骤 3：设置页面索引和计数

```java
//设置页面索引
opts.setPageIndex(2);

//设置页数
opts.setPageCount(3);
```

这些行设置要保存的页面的索引和计数。在此示例中，我们将从索引 2 开始保存页面，总共 3 个页面。

## 步骤 4：指定压缩设置

```java
//如果需要指定压缩
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

在这里，我们指定 PDF 的图像压缩设置。我们将压缩设置为 JPEG 格式，并将 JPEG 质量指定为 90%。

## 第 5 步：使用选项保存文档

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

最后，我们使用指定的选项保存文档。输出的 PDF 将使用给定选项保存在指定位置。

## 结论

在本教程中，我们学习了如何使用 Aspose.Note for Java 在 OneNote 中指定保存选项。通过自定义保存选项，您可以控制输出文档的各个方面，例如页面索引、计数和压缩设置。

## 常见问题解答

### Q1：Aspose.Note 可以处理大型 OneNote 文档吗？

A1：是的，Aspose.Note 旨在高效处理大型 OneNote 文档。

### Q2：Aspose.Note 与最新的 Java 版本兼容吗？

A2：是的，Aspose.Note 与最新的 Java 版本兼容。

### Q3：我可以使用Aspose.Note 将OneNote 文档转换为其他格式吗？

A3：是的，Aspose.Note 支持将 OneNote 文档转换为 PDF、DOCX 和 HTML 等各种格式。

### Q4：Aspose.Note是否支持OneNote文档的加密和解密？

A4：是的，Aspose.Note 提供了用于 OneNote 文档加密和解密的 API。

### Q5：Aspose.Note适合商业用途吗？

A5：是的，Aspose.Note可以通过购买许可证用于商业目的。