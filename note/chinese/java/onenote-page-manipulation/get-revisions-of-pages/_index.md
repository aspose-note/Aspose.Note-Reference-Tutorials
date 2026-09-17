---
date: 2026-01-10
description: 学习如何使用 Aspose.Note for Java 获取 OneNote 页面最后修改时间并检索修订版本。将其集成到您的 Java 应用程序中，实现高效的文档管理。
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: 如何获取 OneNote 页面最后修改时间 – Aspose.Note
url: /zh/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 获取 OneNote 页面修订 - Aspose.Note

## 介绍

在本教程中，您将**获取最后修改时间**（last modified time）以获取 OneNote 文档中页面的最后修改时间，并探索如何使用 Aspose.Note for Java 检索完整的修订历史。无论您是构建文档管理系统、审计更改，还是仅需显示页面的最近编辑时间，本指南都将向您展示如何以编程方式提取这些信息。

## 快速答案
- **“get last modified time” 返回什么？** OneNote 页面最近一次编辑的时间戳。  
- **哪个类提供修订历史？** 通过 `Document.getPageHistory(Page)` 的 `PageHistory`。  
- **此功能是否需要许可证？** 是的，生产环境需要有效的 Aspose.Note 许可证。  
- **支持的 Java 版本是什么？** Java 8 或更高（JDK 8+）。  
- **我可以按作者过滤修订吗？** 您可以读取每个 `Page` 对象的 `Author` 属性并自行过滤。

## 什么是 OneNote 中的 “get last modified time”？

**最后修改时间** 是随每个页面存储的元数据字段，记录页面最近一次更改的时间。Aspose.Note 通过 `Page.getLastModifiedTime()` 方法公开此值，便于显示或记录更改日期。

## 为什么检索页面修订？

- **审计轨迹：** 记录谁在何时更改了什么。  
- **版本比较：** 构建能够并排比较两个修订的功能。  
- **用户协作洞察：** 了解共享笔记本中的编辑模式。  

## 前提条件

在开始之前，请确保您具备以下条件：

### 已安装 Java Development Kit (JDK)

从 Oracle 网站或您喜欢的包管理器安装 JDK 8 或更高版本。

### Aspose.Note for Java 库

从官方网站下载库。您可以在 **[here](https://releases.aspose.com/note/java/)** 找到下载链接。请按照文档中的安装说明 **[here](https://reference.aspose.com/note/java/)** 进行操作。

## 导入包

首先，将必要的包导入您的 Java 项目。这些包将使您能够利用 Aspose.Note for Java 提供的功能。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

现在，让我们将提供的示例代码拆分为多个步骤，以了解每个组件及其功能。

## 如何获取 OneNote 页面最后修改时间

### 步骤 1：设置文档目录

定义 OneNote 文档所在的目录。

```java
String dataDir = "Your Document Directory";
```

### 步骤 2：加载文档

将 OneNote 文档加载到 Aspose.Note 中。

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### 步骤 3：获取第一页

从文档中检索第一页。

```java
Page firstPage = doc.getFirstChild();
```

### 步骤 4：获取页面修订

获取该页面的修订历史。

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### 步骤 5：遍历页面修订

遍历页面修订列表并检索相关信息，包括 **最后修改时间**。

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

## 常见问题及解决方案
- **空的 `PageHistory`：** 确保文档实际包含修订；否则 `getPageHistory` 可能返回 `null`。  
- **时区差异：** `getLastModifiedTime()` 返回系统默认时区的 `java.util.Date`。如有需要请转换为 UTC。  
- **许可证未加载：** 若未提供有效许可证，Aspose.Note 可能以评估模式运行，限制可处理的页面数量。

## 常见问答

### Q1：我可以使用 Aspose.Note for Java 创建新的 OneNote 文档吗？

A1：可以，Aspose.Note for Java 提供全面支持，可通过编程方式创建、读取和操作 OneNote 文档。

### Q2：Aspose.Note for Java 是否兼容不同版本的 OneNote 文件？

A2：是的，Aspose.Note for Java 支持多种 Microsoft OneNote 文件版本，确保在不同环境中的兼容性。

### Q3：导出 OneNote 文档时，我可以自定义输出格式吗？

A3：当然可以，Aspose.Note for Java 在将 OneNote 文档导出为 PDF、HTML、图像等不同格式时提供灵活的自定义选项。

### Q4：Aspose.Note for Java 商业使用是否需要许可证？

A4：是的，商业使用 Aspose.Note for Java 需要有效许可证。您可以从 Aspose 网站获取许可证。

### Q5：如果我在使用 Aspose.Note for Java 时遇到问题或有疑问，在哪里可以寻求帮助？

A5：如需支持和帮助，您可以访问 Aspose.Note 论坛 **[here](https://forum.aspose.com/c/note/28)**，在此提问、分享经验并与其他用户和专家互动。

---

**最后更新：** 2026-01-10  
**测试环境：** Aspose.Note for Java 23.12（撰写时的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}