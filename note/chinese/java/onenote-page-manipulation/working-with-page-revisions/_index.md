---
date: 2026-01-15
description: 学习如何使用 Aspose.Note for Java 跟踪 OneNote 的更改并管理页面修订。包括修订摘要示例以及如何修改修订日期。
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: 跟踪更改 OneNote – 使用 Aspose.Note 管理页面修订
url: /zh/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中处理页面修订 - Aspose.Note

## 介绍

OneNote 是一个用于组织笔记的强大工具，当您需要 **track changes onenote** 时，管理页面修订对于有效协作至关重要。使用 Aspose.Note for Java，您可以以编程方式处理修订，查看谁编辑了页面，甚至调整时间戳。本教程将带您逐步完成从加载文档到更新修订摘要的每一步。

## 快速回答
- **What does “track changes onenote” mean?** 它指的是监控谁在何时编辑了 OneNote 页面。
- **Which library is required?** Aspose.Note for Java.
- **Can I change the author or date of a revision?** 是的，使用 RevisionSummary API（`modify revision date`）。
- **Do I need a OneNote file beforehand?** 是的，需要一个示例 `.one` 文件。
- **Is a license needed for production?** 是的，商业使用需要有效的 Aspose.Note 许可证。

## 什么是修订摘要示例？

*revision summary* 提供有关页面最近更改的元数据——作者名称、最后修改时间以及其他细节。在本指南中，我们将检索并显示这些信息，然后演示如何 **modify revision date**。

## 为什么使用 Aspose.Note 进行 track changes onenote？

- **Collaboration:** 快速查看谁进行了最新编辑。
- **Auditing:** 为合规保留可靠的更改历史。
- **Automation:** 将修订处理集成到后端服务或迁移工具中。

## 前提条件

### Java 开发环境
确保系统已安装 Java Development Kit（JDK）。

### Aspose.Note for Java 库
从 [here](https://releases.aspose.com/note/java/) 下载并安装 Aspose.Note for Java 库。

### OneNote 文档
准备好用于测试的示例 OneNote 文档。

## 导入包

在您的 Java 项目中，导入使用 Aspose.Note for Java 所需的包。

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

让我们将提供的示例拆分为多个步骤，以便清晰理解。

## 步骤 1：加载 OneNote 文档

首先，加载 OneNote 文档并获取第一个子页面。

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## 步骤 2：读取页面修订摘要

读取页面的内容修订摘要。这是 **revision summary example**，显示谁最后编辑了页面。

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## 步骤 3：更新页面修订摘要

使用新作者和新的修改日期更新页面修订摘要。这演示了如何以编程方式 **modify revision date**。

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## 结论

使用 Aspose.Note for Java 可以简化对 OneNote 文档中页面修订的编程管理。通过遵循本教程中概述的步骤，您可以有效地 **track changes onenote**，查看修订详情，甚至 **modify revision date** 以适应您的工作流程。

## 常见问题

### Q1：我可以将 Aspose.Note for Java 与其他 Java 库一起使用吗？

A: 可以，Aspose.Note for Java 可以与其他 Java 库集成，以增强功能。

### Q2：Aspose.Note for Java 是否支持所有版本的 OneNote 文档？

A: Aspose.Note for Java 支持包括旧版本在内的多种 OneNote 文档版本。

### Q3：Aspose.Note for Java 是否适用于企业级应用？

A: 当然，Aspose.Note for Java 旨在通过强大的功能和可扩展性满足企业级应用的需求。

### Q4：我可以使用 Aspose.Note for Java 自定义页面修订吗？

A: 可以，您可以使用 Aspose.Note for Java 根据需求自定义页面修订。

### Q5：我在哪里可以获得 Aspose.Note for Java 的支持？

A: 您可以从 [Aspose.Note forum](https://forum.aspose.com/c/note/28) 获取 Aspose.Note for Java 的支持。

---

**最后更新：** 2026-01-15  
**测试环境：** Aspose.Note for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}