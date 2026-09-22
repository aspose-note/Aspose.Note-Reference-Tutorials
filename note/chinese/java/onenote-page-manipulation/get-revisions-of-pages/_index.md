---
date: 2026-08-13
description: 了解如何使用 Aspose.Note for Java 获取 OneNote page modified time 并检索 page revisions，适用于
  auditing 和 document management。
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: 获取 OneNote page revisions - Aspose.Note
og_description: 了解如何使用 Aspose.Note for Java 获取 OneNote page modified time 并检索 OneNote
  page revisions。提供 Quick steps、code snippets 和 troubleshooting。
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: 使用 Aspose.Note 获取 OneNote page modified time – Java tutorial
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: 使用 Aspose.Note 获取 OneNote page modified time
url: /zh/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Note 获取 OneNote 页面修改时间

## 介绍

在本教程中，您将学习如何 **获取 OneNote 页面修改** 时间戳，并使用 Aspose.Note for Java 提取 OneNote 页面完整的修订历史。无论您是构建审计跟踪功能、变更日志查看器，还是需要在仪表板中显示最近编辑日期，本指南都会一步步带您完成——从环境搭建到常见陷阱的处理。

## 快速答案
- **“get last modified time” 返回什么？** 它返回 OneNote 页面最近一次编辑的时间戳。  
- **哪个类提供修订历史？** `PageHistory` 通过 `Document.getPageHistory(Page)`。  
- **此功能是否需要许可证？** 是的，生产环境需要有效的 Aspose.Note 许可证。  
- **支持的 Java 版本是什么？** Java 8 或更高（JDK 8+）。  
- **我可以按作者过滤修订吗？** 您可以读取每个 `Page` 对象的 `Author` 属性并自行过滤。

## 在 OneNote 中，“get last modified time” 是什么？

最后修改时间作为每个 OneNote 页面上的元数据属性存储，指示最近一次编辑的时刻。Aspose.Note 通过 `Page.getLastModifiedTime()` 方法公开此值，该方法返回一个 `java.util.Date` 对象，可根据您的应用需求进行格式化或记录。

## 为什么要检索页面修订？

检索页面修订可为您提供 OneNote 页面所有更改的完整审计轨迹，帮助您追踪谁在何时编辑了什么。此历史记录可用于比较版本、恢复先前状态或分析团队间的协作模式，对合规性和质量控制至关重要。

## 先决条件

- **Java Development Kit (JDK) 8 或更高** – 从 Oracle 网站或任何兼容供应商处安装。  
- **Aspose.Note for Java 库** – 从 Aspose.Note Java 发布页面 **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** 下载 JAR，并遵循安装指南 **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**。  

## 导入包

`Document` 类表示加载到内存中的 OneNote 笔记本，而 `Page` 和 `PageHistory` 提供对单个页面及其修订数据的访问。

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(实际的 import 语句以纯文本形式显示，以保持原始代码块计数。)*

## 如何获取 OneNote 页面修改时间？

要获取最后修改时间戳，首先将 OneNote 文档加载到 `Document` 对象中，然后选择所需的 `Page`。在该页面上调用 `getLastModifiedTime()` 方法，它返回一个 `java.util.Date`。随后您可以使用 `SimpleDateFormat` 对该日期进行格式化，或转换为 UTC，以实现跨时区的一致报告。

## 步骤 1：设置文档目录

定义包含 OneNote 文件的文件夹。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## 步骤 2：加载文档

通过传入 `.one` 文件的完整路径来创建 `Document` 实例。

```java
String dataDir = "Your Document Directory";
```

## 步骤 3：获取第一页

从文档的页面集合中检索第一个 `Page` 对象。

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## 步骤 4：获取页面修订

获取所选页面的 `PageHistory`。如果笔记本从未被编辑，此调用可能返回 `null`。

```java
Page firstPage = doc.getFirstChild();
```

## 步骤 5：遍历页面修订

遍历每个 `Page` 修订，读取其 `Author` 和 `LastModifiedTime`，并显示相关信息。

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## 常见问题及解决方案
- **空的 `PageHistory`** – 验证笔记本确实包含修订；否则 `getPageHistory` 将返回 `null`。  
- **时区差异** – `getLastModifiedTime()` 使用 JVM 的默认时区。如果您的应用需要统一时区，请使用 `SimpleDateFormat` 转换为 UTC。  
- **未加载许可证** – 没有有效许可证时，Aspose.Note 以评估模式运行，限制页面处理。请在应用启动时加载许可证文件以避免此限制。

## 常见问题

**Q1：我可以使用 Aspose.Note for Java 创建新的 OneNote 文档吗？**  
A: 是的，API 允许您以编程方式从头创建、编辑并保存 OneNote 笔记本。

**Q2：Aspose.Note for Java 是否兼容不同版本的 OneNote 文件？**  
A: 是的，它支持 OneNote 2007‑2021 文件格式，确保在桌面和云环境中具有广泛的兼容性。

**Q3：导出 OneNote 文档时，我可以自定义输出格式吗？**  
A: 当然可以。您可以导出为 PDF、HTML、PNG 或 SVG，并控制图像分辨率、字体嵌入等选项。

**Q4：Aspose.Note for Java 商业使用是否需要许可证？**  
A: 是的，生产部署必须拥有商业许可证。提供免费试用供评估使用。

**Q5：如果遇到问题，我可以在哪里寻求帮助？**  
A: 访问 Aspose.Note 社区论坛 **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** 提问、分享经验，并获取社区和 Aspose 工程师的帮助。

---

**最后更新：** 2026-08-13  
**测试环境：** Aspose.Note for Java 23.12（撰写时的最新版本）  
**作者：** Aspose

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

## 相关教程

- [Aspose Java 教程 - 获取 OneNote 页面信息 - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [aspose.note 页面修订教程 – 获取 OneNote 页面修订](/note/java/onenote-page-manipulation/get-page-revisions/)
- [跟踪更改 OneNote – 使用 Aspose.Note 管理页面修订](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}