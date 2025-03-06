---
title: 使用 Java 从 OneNote 获取图像信息
linktitle: 使用 Java 从 OneNote 获取图像信息
second_title: Aspose.Note Java API
description: 使用 Java 从 OneNote 文档中提取图像信息！获取图像尺寸、文件名等。包括简单的步骤和代码示例。 #OneNote #Java #Aspose
weight: 15
url: /zh/java/onenote-hyperlinks-images/get-image-info/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 从 OneNote 获取图像信息

## 介绍

在 Java 开发领域，从各种文档格式中提取信息是一项常见任务。 OneNote 是一种流行的笔记平台，通常在文本旁边包含图像。使用 Java 以编程方式从 OneNote 文件中检索图像信息可以简化文档处理工作流程。在本教程中，我们将深入研究如何使用 Aspose.Note for Java 从 OneNote 文档中提取图像详细信息。

## 先决条件

在我们深入实施之前，请确保您具备以下先决条件：

### 1.Java开发工具包（JDK）

确保您的系统上安装了 Java 开发工具包 (JDK)。您可以从以下位置下载并安装最新的 JDK[甲骨文网站](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2.Java 库的 Aspose.Note

下载 Aspose.Note for Java 库并将其包含在您的项目中。您可以从以下位置获取该库：[下载页面](https://releases.aspose.com/note/java/).

### 3.OneNote文档

准备包含图像的示例 OneNote 文档。该文档将用于以编程方式提取图像信息。

## 导入包

首先，从 Aspose.Note for Java 导入必要的包：

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

让我们将上面的代码分解为逐步说明：

## 第1步：设置文档目录

```java
String dataDir = "Your Document Directory";
```

代替`"Your Document Directory"`以及 OneNote 文档的路径。

## 第 2 步：加载文档

```java
Document doc = new Document(dataDir + "Sample1.one");
```

使用 Aspose.Note for Java 库加载 OneNote 文档。确保您提供文档的正确路径。

## 第3步：获取所有图像

```java
List<Image> list = doc.getChildNodes(Image.class);
```

从加载的 OneNote 文档中检索所有图像。

## 步骤 4：打印图像总数

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

打印文档中找到的图像总数。

## 第五步：遍历并打印图像信息

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

遍历图像列表并打印详细信息，例如每个图像的宽度、高度、原始尺寸、文件名和上次修改时间。

## 结论

按照本教程中概述的步骤，您可以在 Aspose.Note for Java 库的帮助下，使用 Java 有效地从 OneNote 文档中检索图像信息。将此功能集成到您的应用程序中可以自动执行与文档处理相关的任务，从而提高效率和生产力。

## 常见问题解答

### Q1：Aspose.Note for Java 可以处理除 OneNote 之外的其他文档格式吗？

A1：是的，Aspose.Note for Java 支持各种文档格式，包括 OneNote、PDF 和 Microsoft Word。

### Q2：Aspose.Note for Java 适合个人和商业用途吗？

A2：是的，您可以将 Aspose.Note for Java 用于个人和商业目的。

### Q3：Aspose.Note for Java 提供技术支持吗？

 A3：是的，可以通过 Aspose 论坛获得技术支持：[这里](https://forum.aspose.com/c/note/28).

### Q4：我可以在购买前试用 Aspose.Note for Java 吗？

 A4：是的，您可以从以下位置探索 用于 Java 的 Aspose.Note 的免费试用版：[Aspose.Note for Java](https://releases.aspose.com/note/java/).

### Q5：如何获得 Aspose.Note for Java 的临时许可证？
 
 A5：您可以从以下机构获取临时许可证：[临时牌照/](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
