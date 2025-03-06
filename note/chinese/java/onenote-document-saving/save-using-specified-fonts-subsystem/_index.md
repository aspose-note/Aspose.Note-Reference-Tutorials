---
title: 在 OneNote 中使用指定字体子系统保存
linktitle: 在 OneNote 中使用指定字体子系统保存
second_title: Aspose.Note Java API
description: 了解如何通过 Aspose.Note 在 Java 中使用指定字体子系统保存 OneNote 文档。轻松确保跨平台的字体表示一致。
weight: 22
url: /zh/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中使用指定字体子系统保存

## 介绍

Aspose.Note for Java 提供了处理 OneNote 文档的强大功能。处理此类文档时的一项常见要求是确保正确维护字体，尤其是当文档要导出或保存为不同格式（如 PDF）时。本教程将指导您完成保存 OneNote 文档的过程，同时指定字体子系统，确保在不同平台上一致且准确地表示文本。

## 先决条件

在我们深入学习本教程之前，请确保您已设置以下先决条件：

### 1.Java开发工具包（JDK）

确保您的系统上安装了 Java 开发工具包 (JDK)。您可以从以下位置下载：[这里](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html)如果你还没有。

### 2.Java 库的 Aspose.Note

下载并设置 Aspose.Note for Java 库。您可以从[网站](https://releases.aspose.com/note/java/).

## 导入包

确保在您的 Java 项目中导入必要的包：

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

现在让我们将每个示例分解为多个步骤，以便更好地理解该过程。

## 步骤 1：使用文档字体子系统和默认字体名称保存

此步骤演示如何使用指定的默认字体名称将文档保存为 PDF 格式。

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    //将文档加载到 Aspose.Note 中。
    Document oneFile = new Document("missing-font.one");

    //指定默认字体。
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    //将文档另存为 PDF。
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

在这一步中：
- OneNote 文档是使用 Aspose.Note 加载的。
- 默认字体指定为“Times New Roman”。
- 文档以指定字体保存为 PDF 格式。

## 步骤 2：使用文档字体子系统和文件中的默认字体进行保存

此步骤演示如何使用从文件加载的默认字体以 PDF 格式保存文档。

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    //将文档加载到 Aspose.Note 中。
    Document oneFile = new Document("missing-font.one");

    //指定字体文件的路径。
    String fontFile = "geo_1.ttf";

    //指定文件中的默认字体。
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    //将文档另存为 PDF。
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

在这一步中：
- 加载字体文件“geo_1.ttf”。
- 默认字体是从加载的字体文件中指定的。
- 文档以指定字体保存为 PDF 格式。

## 步骤 3：使用文档字体子系统和流中的默认字体进行保存

此步骤演示如何使用从流加载的默认字体以 PDF 格式保存文档。

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    //将文档加载到 Aspose.Note 中。
    Document oneFile = new Document("missing-font.one");

    //指定字体文件的路径。
    String fontFile = "geo_1.ttf";

    //将字体文件作为流加载。
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        //指定流中的默认字体。
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        //将文档另存为 PDF。
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

在这一步中：
- 字体文件“geo_1.ttf”作为流加载。
- 默认字体是从加载的流中指定的。
- 文档以指定字体保存为 PDF 格式。

## 结论

在本教程中，我们学习了如何使用 Aspose.Note 在 Java 中使用指定字体子系统保存 OneNote 文档。通过执行这些步骤，您可以在导出或保存文档时确保跨不同平台的字体表示一致。

## 常见问题解答

### Q1：我可以为文档的不同部分指定不同的字体吗？

A1：是的，您可以使用 Aspose.Note for Java 为文档的不同部分指定不同的字体。

### Q2：Aspose.Note 是否兼容所有版本的 OneNote？

A2：Aspose.Note支持各种版本的OneNote，确保不同环境下的兼容性。

### Q3：保存文档时字体丢失如何处理？

A3：Aspose.Note提供了指定默认字体的选项，以便在文档保存过程中有效处理丢失的字体。

### Q4：我可以自定义字体属性，例如大小和样式吗？

A4：是的，您可以使用 Aspose.Note for Java 自定义字体属性，例如大小、样式和颜色。

### Q5：Aspose.Note for Java 有试用版吗？

A5：是的，您可以从网站上获得 Aspose.Note for Java 的免费试用版。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
