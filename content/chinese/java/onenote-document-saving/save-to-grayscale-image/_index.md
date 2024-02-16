---
title: 在 OneNote 中保存到灰度图像 - Aspose.Note
linktitle: 在 OneNote 中保存到灰度图像 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 在 OneNote 中将文档另存为灰度图像。以编程方式轻松操作 Microsoft OneNote 文档。
type: docs
weight: 17
url: /zh/java/onenote-document-saving/save-to-grayscale-image/
---
## 介绍

在本教程中，我们将探讨如何使用 Aspose.Note for Java 在 OneNote 中将文档另存为灰度图像。灰度图像是单色图像，其中颜色信息仅由灰色阴影表示。 Aspose.Note 是一个功能强大的 Java API，允许以编程方式操作 Microsoft OneNote 文档。

## 先决条件

在我们开始之前，请确保您具备以下条件：

1. 您的系统上安装了 Java 开发工具包 (JDK)。
2.  Java 库的 Aspose.Note。您可以从以下位置下载：[这里](https://releases.aspose.com/note/java/).
3. 对 Java 编程有基本的了解。

## 导入包

首先，导入必要的包：

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 第 1 步：加载文档

首先，将文档加载到 Aspose.Note 中。代替`"Your Document Directory"`以及文档目录的路径和`"Aspose.one"`与您的 OneNote 文档的名称。

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 第2步：设置输出路径和选项

定义灰度图像的输出路径并指定保存选项。我们将颜色模式设置为灰度。

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## 第 3 步：保存文档

最后，使用指定的选项将文档另存为灰度图像。

```java
oneFile.save(dataDir, options);
```

## 结论

恭喜！您已成功学习如何使用 Aspose.Note for Java 在 OneNote 中将文档另存为灰度图像。这对于需要灰度图像的各种应用非常有用。

## 常见问题解答

### Q1：我可以将灰度图像保存为其他格式吗？

 A1: 是的，可以。只需更改`SaveFormat`中的参数`ImageSaveOptions`构造函数到您想要的格式。

### Q2：Aspose.Note 是否兼容所有版本的 OneNote 文档？

A2：Aspose.Note支持Microsoft OneNote 2010及以上版本。

### Q3：Aspose.Note 需要许可证才能使用吗？

A3：是的，您需要有效的许可证才能在生产环境中使用 Aspose.Note。但是，您可以获得用于测试目的的临时许可证。

### 问题 4：在将文档保存为图像之前，我可以对其进行其他操作吗？

A4：当然！ Aspose.Note 提供了多种以编程方式编辑 OneNote 文档的功能。

### Q5：如果遇到问题，我可以在哪里寻求支持？

A5：您可以在 Aspose.Note 论坛上找到支持[这里](https://forum.aspose.com/c/note/28).