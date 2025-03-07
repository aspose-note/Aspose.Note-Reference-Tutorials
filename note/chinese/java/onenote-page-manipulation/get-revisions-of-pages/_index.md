---
title: 获取 OneNote 中页面的修订 - Aspose.Note
linktitle: 获取 OneNote 中页面的修订 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note Java 检索 OneNote 文档中页面的修订版本。将其集成到您的 Java 应用程序中以实现高效的文档管理。
weight: 15
url: /zh/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 获取 OneNote 中页面的修订 - Aspose.Note

## 介绍

在本教程中，我们将深入研究 Aspose.Note for Java 的功能，这是一个功能强大的库，使您能够在 Java 应用程序中无缝地使用 Microsoft OneNote 文件。具体来说，我们将重点关注如何检索 OneNote 文档中页面的修订。在本指南结束时，您将具备有效提取页面修订的知识，包括上次修改时间、创建时间、标题、级别和作者等详细信息。

## 先决条件

在深入学习本教程之前，请确保您已设置以下先决条件：

### 安装 Java 开发工具包 (JDK)

确保您的系统上安装了 Java 开发工具包。您可以从 Oracle 网站下载并安装它，或者如果您使用的是基于 Unix 的系统，则可以使用包管理器。

### Java 库的 Aspose.Note

从网站下载并安装 Aspose.Note for Java 库。你可以找到下载链接[这里](https://releases.aspose.com/note/java/)。按照文档中提供的安装说明进行操作[这里](https://reference.aspose.com/note/java/).

## 导入包

首先，将必要的包导入到您的 Java 项目中。这些包将允许您利用 Aspose.Note for Java 提供的功能。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

现在，让我们将提供的示例代码分解为多个步骤，以了解每个组件及其功能。

## 第1步：设置文档目录

定义 OneNote 文档所在的目录。

```java
String dataDir = "Your Document Directory";
```

## 第 2 步：加载文档

将 OneNote 文档加载到 Aspose.Note 中。

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## 第 3 步：获取首页

从文档中检索第一页。

```java
Page firstPage = doc.getFirstChild();
```

## 第 4 步：获取页面修订

获取页面的修改历史记录。

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## 第5步：遍历页面修订

迭代页面修订列表并检索相关信息。

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## 结论

在本教程中，我们探讨了如何使用 Aspose.Note for Java 检索 OneNote 文档中页面的修订版本。通过遵循分步指南并利用提供的示例代码，您可以轻松地将此功能集成到 Java 应用程序中，从而实现 OneNote 文件的高效管理。

## 常见问题解答

### Q1：我可以使用Aspose.Note for Java创建新的OneNote文档吗？

A1：是的，Aspose.Note for Java 为以编程方式创建、读取和操作 OneNote 文档提供了全面的支持。

### Q2：Aspose.Note for Java 是否兼容不同版本的 OneNote 文件？

A2：是的，Aspose.Note for Java 支持各种版本的 Microsoft OneNote 文件，确保不同环境之间的兼容性。

### Q3：导出 OneNote 文档时可以自定义输出格式吗？

A3：当然，Aspose.Note for Java 可以灵活地将 OneNote 文档导出为不同的格式，例如 PDF、HTML 和图像，并提供自定义选项。

### Q4：Aspose.Note for Java 商业使用需要许可证吗？

A4：是的，Aspose.Note for Java 的商业用途需要有效的许可证。您可以从 Aspose 网站获取许可证。

### Q5：如果我遇到问题或对 Aspose.Note for Java 有疑问，可以在哪里寻求帮助？

 A5： 如需支持和帮助，您可以访问 Aspose.Note 论坛[这里](https://forum.aspose.com/c/note/28)，您可以在其中提出问题、分享经验以及与其他用户和专家互动。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
