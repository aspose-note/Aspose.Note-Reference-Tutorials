---
title: 在 OneNote 中获取页面修订 - Aspose.Note
linktitle: 在 OneNote 中获取页面修订 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 在 OneNote 中检索页面修订。请遵循我们的分步指南，以有效跟踪更改。
weight: 14
url: /zh/java/onenote-page-manipulation/get-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中获取页面修订 - Aspose.Note

## 介绍

OneNote 是用于组织和管理笔记的强大工具，但有时您需要跟踪对页面所做的更改和修订。使用 Aspose.Note for Java，您可以轻松地以编程方式检索页面修订。在本教程中，我们将指导您完成使用 Aspose.Note for Java 在 OneNote 中获取页面修订的过程。

## 先决条件

在我们开始之前，请确保您具备以下先决条件：

### 1.Java开发工具包（JDK）

确保您的系统上安装了 Java 开发工具包 (JDK)。您可以从 Oracle 网站下载并安装 JDK。

### 2.Java 版 Aspose.Note

从以下地址下载并安装 Aspose.Note for Java[下载链接](https://releases.aspose.com/note/java/).

### 3. OneNote 文档示例

准备一个示例 OneNote 文档（`Sample1.one`），其中包含您要从中检索修订的页面。

## 导入包

首先，您需要从 Aspose.Note for Java 导入必要的包。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

现在，让我们将提供的示例分解为多个步骤：

## 第 1 步：设置文档目录

定义 OneNote 文档所在的目录路径。

```java
String dataDir = "Your Document Directory";
```

## 步骤 2：加载 OneNote 文档

使用加载 OneNote 文档`LoadOptions`启用加载历史记录。

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## 第 3 步：获取首页

从加载的文档中检索第一页。

```java
Page firstPage = document.getFirstChild();
```

## 第 4 步：迭代页面修订

迭代每个页面修订并检索相关信息，例如上次修改时间、创建时间、标题、级别和作者。

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## 结论

在本教程中，我们学习了如何使用 Aspose.Note for Java 在 OneNote 中检索页面修订。通过执行这些步骤，您可以以编程方式有效跟踪对 OneNote 页面所做的更改。

## 常见问题解答

### Q1: 我可以使用Aspose.Note for Java来修改页面修订吗？

A1：不，Aspose.Note for Java 目前支持检索页面修订，但不支持修改它们。

### Q2：Aspose.Note for Java 是否兼容不同版本的 OneNote 文档？

A2：是的，Aspose.Note for Java 支持各种版本的 OneNote 文档，让您可以无缝地处理不同的文件格式。

### Q3：Aspose.Note for Java 需要许可证才能使用吗？

A3：是的，您需要购买许可证才能在商业项目中使用Aspose.Note for Java。但是，您也可以获得用于评估目的的临时许可证。

### Q4：如果在使用 Aspose.Note for Java 时遇到任何问题，我可以寻求支持吗？

 A4：是的，您可以从Aspose.Note论坛寻求支持[这里](https://forum.aspose.com/c/note/28).

### Q5：Aspose.Note for Java 有免费试用版吗？

A5：是的，您可以从以下地址访问 Aspose.Note for Java 的免费试用版：[网站](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
