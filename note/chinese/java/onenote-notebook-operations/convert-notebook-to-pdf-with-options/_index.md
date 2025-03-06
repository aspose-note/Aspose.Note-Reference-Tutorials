---
title: 使用 OneNote 中的选项将笔记本转换为 PDF - Aspose.Note
linktitle: 使用 OneNote 中的选项将笔记本转换为 PDF - Aspose.Note
second_title: Aspose.Note Java API
description: 轻松自定义 OneNote 笔记本并将其导出为 PDF！ Aspose.Note for Java 处理繁重的工作。包括分步指南！ #OneNote #Java #Aspose
weight: 17
url: /zh/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 OneNote 中的选项将笔记本转换为 PDF - Aspose.Note

## 介绍

在本教程中，我们将深入研究如何使用 Aspose.Note for Java 将笔记本转换为 PDF，并提供可自定义的选项。 Aspose.Note 是一个功能强大的 Java API，允许开发人员以编程方式操作 Microsoft OneNote 文档。将笔记本转换为 PDF 格式是各种应用程序中的常见要求，而使用 Aspose.Note，此任务变得简化且高效。

## 先决条件

在我们开始之前，请确保您具备以下先决条件：

1. Java 开发工具包 (JDK)：确保您的系统上安装了 JDK。
2. Aspose.Note for Java：从以下位置下载并安装 Aspose.Note for Java：[下载链接](https://releases.aspose.com/note/java/).
3. IDE（集成开发环境）：选择您喜欢的 Java 开发 IDE。 IntelliJ IDEA、Eclipse 或 NetBeans 是流行的选择。

## 导入包

首先，您需要将必要的包导入到您的 Java 项目中。这些包提供了处理 OneNote 文档所需的类和方法。

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## 第 1 步：加载 OneNote 笔记本

要将笔记本转换为 PDF，您需要先加载 OneNote 笔记本。确保正确指定笔记本文件的路径。

```java
String dataDir = "Your Document Directory";
//加载 OneNote 笔记本
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## 步骤 2：指定 PDF 保存选项

Aspose.Note 提供了各种用于自定义 PDF 输出的选项。您可以指定页面分割算法、页眉/页脚设置等选项。

```java
//指定 PDF 保存选项
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## 步骤 3：将笔记本另存为 PDF

加载笔记本并指定保存选项后，就可以将笔记本另存为 PDF 文件了。

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
//保存笔记本
notebook.save(dataDir, notebookSaveOptions);
```

## 结论

在本教程中，我们探讨了如何使用 Aspose.Note for Java 将 OneNote 笔记本转换为 PDF 格式。通过遵循这些简单的步骤，您可以有效地处理 Java 应用程序中的文档转换。

---

## 常见问题解答

### Q1：我可以自定义 PDF 输出的外观吗？

A1：是的，Aspose.Note 提供了各种自定义 PDF 输出的选项，包括页眉/页脚设置、页面分割算法等。

### Q2：Aspose.Note 是否兼容所有版本的 OneNote？

A2：Aspose.Note支持Microsoft OneNote 2010及更高版本。

### Q3：Aspose.Note 提供免费试用吗？

 A3：是的，您可以从以下位置下载 Aspose.Note 的免费试用版：[这里](https://releases.aspose.com/).

### Q4：在哪里可以找到 Aspose.Note 的文档？

 A4：您可以找到 Aspose.Note 的综合文档[这里](https://reference.aspose.com/note/java/).

### Q5：如何获得 Aspose.Note 的支持？

 A5：如需任何技术帮助或疑问，您可以访问 Aspose.Note 支持论坛[这里](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
