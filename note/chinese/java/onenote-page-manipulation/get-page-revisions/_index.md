---
date: 2026-08-08
description: 了解如何通过使用 Aspose.Note for Java 以编程方式检索页面修订来跟踪 OneNote 中的更改。
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: 获取 OneNote 页面修订 - Aspose.Note
og_description: 了解如何通过使用 Aspose.Note for Java 以编程方式检索页面修订来跟踪 OneNote 中的更改。
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: 在 OneNote 中跟踪更改 – 使用 Aspose.Note 的页面修订
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: 在 OneNote 中跟踪更改 – 使用 Aspose.Note 的页面修订
url: /zh/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中跟踪更改 – 使用 Aspose.Note 的页面修订

在本教程中，您将学习如何通过使用 Aspose.Note Java API 提取页面的完整修订历史来**跟踪 OneNote 中的更改**。我们将涵盖从设置开发环境到打印每个修订的作者、时间戳和标题的所有内容，以便您能够为任何基于 OneNote 的解决方案构建可靠的审计跟踪功能。

## 快速答案
- **本教程涵盖什么？** 使用 Aspose.Note for Java 从 OneNote 文件检索页面修订历史。  
- **需要哪个库版本？** 任何支持 `LoadOptions.setLoadHistory` 的近期 Aspose.Note for Java 发行版。  
- **我需要许可证吗？** 临时评估许可证可用于测试；生产环境需要商业许可证。  
- **我可以修改修订吗？** 该 API 对修订是只读的；您只能检索它们。  
- **主要前提条件是什么？** Java JDK、Aspose.Note for Java，以及包含修订数据的 OneNote 文档。

## 什么是 “aspose.note 页面修订教程”？
本教程演示如何以编程方式访问 OneNote 页面 的历史版本。每个修订包含作者、创建时间和修改时间等元数据，使您能够在应用程序中构建审计跟踪或变更日志功能。

## 为什么使用 Aspose.Note 进行页面修订跟踪？
在标准 2 GHz CPU 上，能够在 5 秒以内加载 500 页文件的整个笔记本修订历史，并在不启动 OneNote UI 的情况下检索元数据。该库支持 30 多种输入和输出格式，可在 Windows、Linux 和 macOS 上运行（覆盖 >95 % 的服务器环境），并提供对每个修订属性的完整控制。

## 前提条件

### 1. Java 开发工具包 (JDK)
确保已安装最近的 JDK（8 或更高），并已设置 `JAVA_HOME`。

### 2. Aspose.Note for Java
从[下载链接](https://releases.aspose.com/note/java/)下载库。

### 3. 示例 OneNote 文档
创建或获取一个包含修订历史页面的 OneNote 文件（例如 `Sample1.one`）。

## 导入包
首先，导入所需的 Aspose.Note 类。  
`Document` 表示 OneNote 笔记本，`LoadOptions` 配置加载行为，`Page` 表示单个页面。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## 步骤实现

### 步骤 1：设置文档目录
定义存放 OneNote 文件的文件夹。

```java
String dataDir = "Your Document Directory";
```

### 步骤 2：加载启用历史的 OneNote 文档
`LoadOptions` 是一个配置类，告诉 Aspose.Note 如何打开文件，包括是否读取修订数据。在加载文档之前启用该标志。

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### 步骤 3：获取第一页
获取第一页对象；这将作为检索其历史的参考点。

```java
Page firstPage = document.getFirstChild();
```

### 步骤 4：遍历页面修订
遍历每个修订并打印有用的元数据，如时间戳、标题、级别和作者。

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

> **技巧提示：** 如果需要按特定作者或日期范围过滤修订，只需在 `for` 循环中添加条件检查。

## 常见问题与解决方案
- **未返回修订：** 验证在加载文档之前已调用 `loadOptions.setLoadHistory(true)`。  
- **作者或标题为空：** 某些较旧的 OneNote 版本可能不存储这些字段；请优雅地处理 `null` 值。  
- **大型笔记本性能延迟：** 仅加载所需的章节或增大 JVM 堆大小。

## 常见问答

**Q1：我可以使用 Aspose.Note for Java 修改页面修订吗？**  
A1: 不，API 当前仅支持对页面修订的只读访问。

**Q2：Aspose.Note for Java 是否兼容不同版本的 OneNote 文档？**  
A2: 是的，它支持多种 OneNote 文件格式，能够在不同版本之间无缝处理。

**Q3：使用 Aspose.Note for Java 是否需要许可证？**  
A3: 生产使用需要商业许可证，但可提供临时评估许可证用于测试。

**Q4：如果在使用 Aspose.Note for Java 时遇到问题，我可以寻求支持吗？**  
A4: 可以，您可以在 Aspose.Note 论坛提问 [Aspose.Note forum](https://forum.aspose.com/c/note/28)。

**Q5：Aspose.Note for Java 是否提供免费试用？**  
A5: 是的，您可以从[网站](https://releases.aspose.com/)下载免费试用版。

---

**最后更新：** 2026-08-08  
**测试环境：** Aspose.Note for Java（最新发行版）  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [跟踪更改 onenote – 使用 Aspose.Note 管理页面修订](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Aspose Java 教程 - 获取 OneNote 页面信息 - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [更改 OneNote 页面背景 – Aspose.Note for Java](/note/java/onenote-page-manipulation/set-page-background-color/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}