---
date: 2026-04-01
description: 学习如何使用 Aspose.Note for Java 将 Outlook 中的任务提取到 OneNote。按照本分步指南快速获取任务详情。
keywords:
- how to extract tasks
- Aspose.Note Java
- Outlook task extraction
linktitle: 在 OneNote 中获取 Outlook 任务 - Aspose.Note
second_title: Aspose.Note Java API
title: 如何使用 Aspose.Note 在 OneNote 中提取 Outlook 任务
url: /zh/java/task-and-outlook-integration/get-outlook-task/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中获取 Outlook 任务 - Aspose.Note

## 介绍
欢迎阅读我们关于使用 Aspose.Note for Java 从 OneNote 笔记本中 **提取 Outlook 任务** 的完整指南。无论您是构建迁移工具、生成报告，还是仅需同步任务数据，本教程将逐步演示每个环节——从加载 OneNote 文件到读取每个 Outlook 任务的属性。完成后，您将拥有一段可直接使用的代码片段，能够根据自己的项目进行适配。

## 快速回答
- **本教程涵盖什么内容？** 使用 Aspose.Note for Java 从 OneNote 文档中提取 Outlook 任务详情。  
- **使用哪个 API？** Aspose.Note Java 库。  
- **是否需要许可证？** 免费试用可用于开发；生产环境需商业许可证。  
- **实现需要多长时间？** 环境搭建好后大约 10‑15 分钟。  
- **可以处理多个笔记本吗？** 可以——只需遍历文件并复用相同逻辑。

## 什么是任务提取？
任务提取是指读取 Outlook 以 `NoteTask` 标签形式存储在 OneNote 页面中的结构化任务信息（如截止日期、状态和图标）。这使得可以通过编程方式访问任务元数据，而无需手动复制。

## 为什么使用 Aspose.Note for Java？
- **无需 Microsoft Office** – 在任何具备 Java 运行时的平台上均可运行。  
- **完整保真** – 在保留所有 OneNote 元素的同时，直接访问标签。  
- **高性能** – 针对大型笔记本和批处理进行优化。  

## 前置条件
在开始之前，请确保已准备好以下内容：

- **Java 开发环境** – 已安装并配置 JDK 8 或更高版本。  
- **Aspose.Note 库** – 从官方站点[此处](https://releases.aspose.com/note/java/)下载最新的 Java 包。  
- **示例 OneNote 文件** – 本教程使用 `Sample1.one`；您可以替换为任何包含 Outlook 任务的笔记本。

## 导入包
在 Java 类中添加所需的导入。这些类可让您访问文档模型以及 Outlook 特定的 `NoteTask` 标签。

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```

## 步骤指南

### 步骤 1：设置文档目录
定义存放 OneNote 文件的文件夹。可以使用绝对路径或相对路径，但请保持路径字符串整洁以提升可读性。

```java
String dataDir = "Your Document Directory";
```

### 步骤 2：加载 OneNote 文档
通过指向 `.one` 文件创建 `Document` 实例。Aspose.Note 会将文件解析为类似 DOM 的结构，供您遍历。

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### 步骤 3：获取所有 RichText 节点
Outlook 任务存储在 `RichText` 元素中。检索所有 `RichText` 节点，以便检查其标签。

```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```

### 步骤 4：遍历每个节点
遍历每个 `RichText` 节点，检查其标签，并在遇到 `NoteTask` 时进行处理。下面的代码会打印每个任务的最有用属性。

```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Retrieve properties
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```

**技巧提示：** 如果只需要部分属性，可跳过其余属性，以提升处理大型笔记本时的性能。

### 常见问题与解决方案
- **未找到任务：** 确认 OneNote 页面实际包含 Outlook 任务。它们表现为带有小 Outlook 图标的复选框。  
- **空值：** 某些任务字段（如 `CompletedTime`）在任务未完成时可能为 `null`。在打印前检查 `null`，以防止 `NullPointerException`。  
- **文件未找到：** 确认 `dataDir` 以适合您操作系统的路径分隔符（`/` 或 `\\`）结尾。

## 结论
恭喜！您已经学习了如何使用 Aspose.Note Java API 从 OneNote 中 **提取 Outlook 任务**。此方法让您能够全面以编程方式控制任务数据，便于与自定义报表工具、数据库或其他业务工作流集成。

## 常见问题

**Q: Aspose.Note 是否兼容所有版本的 OneNote？**  
A: Aspose.Note 支持 Microsoft OneNote 2010 及更高版本。

**Q: 我可以在个人和商业项目中使用 Aspose.Note 吗？**  
A: 可以，Aspose.Note 可用于个人和商业项目。访问[此处](https://purchase.aspose.com/buy)了解许可选项。

**Q: Aspose.Note 是否提供免费试用？**  
A: 是的，您可以在[此处](https://releases.aspose.com/)获取免费试用。

**Q: 如何获取 Aspose.Note 的支持？**  
A: 前往 [Aspose.Note 论坛](https://forum.aspose.com/c/note/28)获取社区支持。若需进一步帮助，可考虑购买[临时许可证](https://purchase.aspose.com/temporary-license/)。

**Q: 是否有可用于测试的 OneNote 示例文档？**  
A: 您可以在 Aspose.Note 文档的[此处](https://reference.aspose.com/note/java/)找到示例文档。

**最后更新：** 2026-04-01  
**测试环境：** Aspose.Note for Java 24.12（撰写时的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}