---
title: 在 OneNote 中将笔记本转换为平面图像 - Aspose.Note
linktitle: 在 OneNote 中将笔记本转换为平面图像 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 将笔记本转换为 OneNote 中的拼合图像。轻松地将所有元素保留在单个图像文件中。
weight: 13
url: /zh/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中将笔记本转换为平面图像 - Aspose.Note

## 介绍

在本教程中，我们将指导您完成使用 Aspose.Note for Java 在 OneNote 中将笔记本转换为平面图像的过程。这允许您将笔记本另存为图像文件，确保所有元素都以单一图像格式保留。

## 先决条件

在我们开始之前，请确保您具备以下条件：

1. 您的系统上安装了 Java 开发工具包 (JDK)。
2. 下载 Aspose.Note for Java 库并在您的 Java 项目中进行设置。您可以从以下位置下载该库[这里](https://releases.aspose.com/note/java/).
3. Java 编程的基础知识。

## 导入包

首先，您需要从 Aspose.Note for Java 导入必要的包：

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## 第 1 步：设置文档目录

首先，定义笔记本文件所在的目录：

```java
String dataDir = "Your Document Directory";
```

代替`"Your Document Directory"`以及笔记本文件的路径。

## 第 2 步：加载笔记本

接下来，使用以下命令加载笔记本文件`Notebook`班级：

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

确保更换`"test.onetoc2"`与您的笔记本文件的名称。

## 第 3 步：设置图像保存选项

现在，设置将笔记本另存为图像的选项。我们将指定保存格式为 PNG 并将分辨率设置为 400 DPI：

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

您可以根据您的要求调整分辨率。

## 第四步：压平笔记本

为了确保所有元素都被展平为单个图像，请设置`flatten`选项`true`:

```java
saveOptions.setFlatten(true);
```

这可确保生成的图像保持笔记本的布局。

## 第5步：保存图像

最后，将笔记本另存为扁平图像：

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

代替`"ExportImageasFlattenedNotebook_out.png"`与您想要的输出文件名。

## 结论

总之，使用 Aspose.Note for Java，您可以轻松地将笔记本转换为 OneNote 中的扁平图像。此过程可确保所有元素都以单一图像格式保存，以便于轻松共享和查看。

## 常见问题解答

### Q1：我可以调整输出图像的分辨率吗？

 A1: 是的，您可以根据您的要求通过修改`setResolution`方法参数。

### Q2：Aspose.Note是否支持其他图像格式导出？

A2: 是的，Aspose.Note 支持多种图像格式，如 PNG、JPEG、BMP 等，用于导出笔记本。

### Q3：我可以进一步自定义输出图像吗？

A3：是的，Aspose.Note 提供了丰富的选项用于自定义输出图像，包括页面大小、方向和质量设置。

### Q4：Aspose.Note for Java 有试用版吗？

 A4：是的，您可以从以下位置获取免费试用版：[这里](https://releases.aspose.com/).

### Q5：哪里可以找到 Aspose.Note for Java 的支持？

 A5：您可以在 Aspose.Note 论坛上找到支持和资源[这里](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
