---
date: 2026-01-10
description: 学习 Aspose.Note 页面修订教程（Java）——使用 Aspose.Note 以编程方式检索 OneNote 页面修订。请按照我们的分步指南操作。
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Aspose.Note 页面修订教程 – 在 OneNote 中获取页面修订
url: /zh/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中获取页面修订 - Aspose.Note

OneNote 是一个强大的记笔记平台，当您需要审计更改时，**aspose.note page revisions tutorial** 精确展示了如何仅用几行 Java 代码提取修订历史。在本指南中，我们将逐步讲解您需要的所有内容——从环境设置到打印每个修订的详细信息——让您轻松跟踪编辑、作者贡献和时间戳。

## 快速答案
- **教程涵盖什么内容？** 使用 Aspose.Note for Java 从 OneNote 文件中检索页面修订历史。  
- **需要哪个库版本？** 任何支持 `LoadOptions.setLoadHistory` 的近期 Aspose.Note for Java 发行版。  
- **我需要许可证吗？** 临时评估许可证可用于测试；生产环境需要商业许可证。  
- **我可以修改修订吗？** API 对修订是只读的；只能检索它们。  
- **主要前提条件是什么？** Java JDK、Aspose.Note for Java，以及包含修订数据的 OneNote 文档。

## 什么是 “aspose.note page revisions tutorial”？
本教程演示了如何以编程方式访问 OneNote 页面 的历史版本。每个修订包含作者、创建时间和修改时间等元数据，使您能够在应用程序中构建审计追踪或变更日志功能。

## 为什么使用 Aspose.Note 进行页面修订跟踪？
- **无 UI 依赖** – 完全在代码中运行，适合后端服务。  
- **跨平台** – Java 可在 Windows、Linux 和 macOS 上运行。  
- **完全控制** – 在不手动打开 OneNote 的情况下检索每个修订属性。  
- **性能** – 加载历史已优化，即使是大型笔记本也能快速处理。

## 前提条件

### 1. Java 开发工具包 (JDK)
确保已安装近期的 JDK（8 或更高），并已设置 `JAVA_HOME`。

### 2. Aspose.Note for Java
从 [download link](https://releases.aspose.com/note/java/) 下载库。

### 3. 示例 OneNote 文档
创建或获取一个包含修订历史页面的 OneNote 文件（例如 `Sample1.one`）。

## 导入包
首先，导入所需的 Aspose.Note 类。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## 步骤实现

### 步骤 1：设置文档目录
定义 OneNote 文件所在的文件夹。

```java
String dataDir = "Your Document Directory";
```

### 步骤 2：启用历史的 OneNote 文档
启用 `LoadOptions` 标志以提取修订数据。

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### 步骤 3：获取第一页
获取第一页对象；它将作为检索历史的参考点。

```java
Page firstPage = document.getFirstChild();
```

### 步骤 4：遍历页面修订
遍历每个修订并打印有用的元数据，如时间戳、标题、层级和作者。

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
- **未返回修订：** 确认在加载文档之前调用了 `loadOptions.setLoadHistory(true)`。  
- **作者或标题为 null：** 某些旧版 OneNote 可能不存储这些字段；请优雅地处理 `null` 值。  
- **大型笔记性能延迟：** 仅加载所需的章节或增大 JVM 堆大小。

## 常见问答

**Q1: 我可以使用 Aspose.Note for Java 修改页面修订吗？**  
A1: 不可以，API 当前仅支持对页面修订的只读访问。

**Q2: Aspose.Note for Java 是否兼容不同版本的 OneNote 文档？**  
A2: 是的，它支持多种 OneNote 文件格式，可在不同版本之间无缝处理。

**Q3: 使用 Aspose.Note for Java 是否需要许可证？**  
A3: 生产环境需要商业许可证，测试可使用临时评估许可证。

**Q4: 在使用 Aspose.Note for Java 时遇到问题，我可以寻求支持吗？**  
A4: 可以，您可以在 Aspose.Note 论坛 [here](https://forum.aspose.com/c/note/28) 提问。

**Q5: 是否提供 Aspose.Note for Java 的免费试用？**  
A5: 是的，您可以从 [website](https://releases.aspose.com/) 下载免费试用。

---
**最后更新：** 2026-01-10  
**测试环境：** Aspose.Note for Java（最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}