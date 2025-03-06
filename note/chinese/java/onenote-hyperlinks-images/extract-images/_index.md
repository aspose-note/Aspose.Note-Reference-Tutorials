---
title: 使用 Java 从 OneNote 文档中提取图像
linktitle: 使用 Java 从 OneNote 文档中提取图像
second_title: Aspose.Note Java API
description: 了解如何使用 Java 和 Aspose.Note 库从 OneNote 文档中提取图像。请按照我们的分步指南进行无缝图像提取。
weight: 14
url: /zh/java/onenote-hyperlinks-images/extract-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 从 OneNote 文档中提取图像

## 介绍

在本教程中，我们将指导您在 Aspose.Note 库的帮助下完成使用 Java 从 OneNote 文档中提取图像的过程。

## 先决条件

在开始之前，请确保您具备以下条件：

1.  Java 开发工具包 (JDK)：确保您的系统上安装了 Java。您可以从以下位置下载并安装它[网站](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2. Aspose.Note 库：下载 Aspose.Note 库并将其包含在您的 Java 项目中。您可以从[下载链接](https://releases.aspose.com/note/java/).

## 导入包

首先，导入必要的包：

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## 第 1 步：加载文档

首先，使用 Aspose.Note 加载 OneNote 文档：

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## 第2步：获取所有图像

接下来，从文档中检索所有图像：

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## 第三步：提取图像

遍历图像列表并将每个图像保存到文件中：

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## 结论

使用 Java 从 OneNote 文档中提取图像可以通过 Aspose.Note 库无缝实现。通过遵循本教程中概述的步骤，您可以轻松地从文档中检索图像以进行进一步处理或分析。

## 常见问题解答

### Q1：我可以从受密码保护的 OneNote 文档中提取图像吗？

A1：是的，Aspose.Note 也支持从受密码保护的文档中提取图像。

### Q2：Aspose.Note 是否兼容不同版本的 Java？

A2：Aspose.Note兼容各个版本的Java，确保开发人员的灵活性。

### Q3：我可以在一次执行中从多个 OneNote 文档中提取图像吗？

A3：当然，您可以使用 Aspose.Note 迭代多个文档并从每个文档中提取图像。

### Q4：OneNote 文档有大小限制吗？

A4：Aspose.Note可以高效处理各种尺寸的文档，确保图像提取时对文档尺寸没有限制。

### Q5：Aspose.Note 是否支持提取除图像之外的其他类型的内容？

A5：是的，除了图像之外，Aspose.Note 还允许从 OneNote 文档中提取文本、附件和其他内容类型。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
