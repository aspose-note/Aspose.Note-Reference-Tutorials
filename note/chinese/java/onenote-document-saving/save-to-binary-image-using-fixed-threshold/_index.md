---
title: 在 OneNote 中使用固定阈值保存到二进制图像
linktitle: 在 OneNote 中使用固定阈值保存到二进制图像
second_title: Aspose.Note Java API
description: 使用 Aspose.Note Java 的固定阈值轻松将 Microsoft OneNote 文档保存为二进制图像。提升您的 OneNote 文件操作能力。
weight: 14
url: /zh/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中使用固定阈值保存到二进制图像

## 介绍

Aspose.Note for Java 是一个功能强大的 API，允许开发人员以编程方式使用 Microsoft OneNote 文件。在本教程中，我们将探讨如何使用固定阈值将文档保存为二进制图像。请按照以下步骤来实现此目的。

## 先决条件

在开始之前，请确保您具备以下条件：

1. 您的系统上安装了 Java 开发工具包 (JDK)。
2. 下载了 Java 库的 Aspose.Note。您可以从以下位置下载：[这里](https://releases.aspose.com/note/java/).
3. Java 编程的基础知识。

## 导入包

首先，将必要的包导入到您的 Java 文件中。

```java
import com.aspose.note.*;
import java.io.IOException;
```

## 第 1 步：加载文档

使用 Aspose.Note API 加载 OneNote 文档。

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 第 2 步：设置二值化选项

定义用于将文档保存为二进制图像的二值化选项。

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

## 第 3 步：设置图像保存选项

设置图像保存选项，包括颜色模式和二值化选项。

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## 步骤 4：保存文档

使用指定选项将文档另存为二进制图像。

```java
oneFile.save(dataDir, options);
```

## 结论

在本教程中，我们学习了如何在 Aspose.Note for Java 中使用固定阈值将文档保存为二进制图像。通过执行以下步骤，您可以轻松地以编程方式操作 OneNote 文件。

## 常见问题解答

### Q1：二值化的阈值可以调整吗？

 A1：是的，您可以根据您的要求调整阈值，通过修改`setBinarizationThreshold()`方法参数。

### Q2：Aspose.Note for Java 是否与所有版本的 Microsoft OneNote 兼容？

A2：Aspose.Note for Java 支持各种版本的 Microsoft OneNote，包括 2010、2013 和 2016。

### Q3：可处理的文件大小有限制吗？

A3：Aspose.Note for Java对可处理的文档大小没有限制，让您高效处理大文件。

### Q4：我可以同时转换多个 OneNote 文档吗？

A4：是的，您可以通过迭代每个文件并应用必要的操作来批量处理多个 OneNote 文档。

### Q5：Aspose.Note for Java 是否提供技术支持？

 A5：是的，可以通过以下方式获得技术支持：[Aspose.Note 论坛](https://forum.aspose.com/c/note/28)，您可以在这里提出问题并寻求专家的帮助。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
