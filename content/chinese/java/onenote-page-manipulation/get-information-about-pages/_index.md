---
title: 获取有关 OneNote 中页面的信息 - Aspose.Note
linktitle: 获取有关 OneNote 中页面的信息 - Aspose.Note
second_title: Aspose.Note Java API
description: 揭开 OneNote 文档中的页面秘密！使用 Aspose.Note 提取修订版本、创建时间等。包含分步指南和代码！ #OneNote #Java #Aspose
type: docs
weight: 12
url: /zh/java/onenote-page-manipulation/get-information-about-pages/
---
## 介绍

在本教程中，我们将指导您完成使用 Aspose.Note for Java 提取 OneNote 中页面信息的过程。 Aspose.Note 是一个功能强大的 API，允许您以编程方式处理 Microsoft OneNote 文档。无论您需要访问页面修订、创建时间、标题还是作者，Aspose.Note 都可以通过其直观的界面简化任务。

## 先决条件

在我们开始之前，请确保您具备以下条件：

1. Java 开发工具包 (JDK)：确保您的系统上安装了 JDK。
2.  Aspose.Note for Java：下载并安装 Aspose.Note for Java 库。您可以从[网站](https://purchase.aspose.com/buy).
3. 示例 OneNote 文档：准备一个示例 OneNote 文档，您将使用它来检索信息。

## 导入包

首先，您需要导入必要的包以便在 Java 项目中使用 Aspose.Note。

```java
import java.io.IOException;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## 第1步：加载OneNote文档

首先使用 Aspose.Note 加载 OneNote 文档。

```java
String dataDir = "Your Document Directory";
//将文档加载到Aspose.Note中
LoadOptions options = new LoadOptions();
Document doc = new Document(dataDir + "Sample1.one", options);
```

代替`"Your Document Directory"`以及 OneNote 文档的路径。

## 第2步：检索页面信息

接下来，检索有关 OneNote 文档中页面的信息。

```java
//获取页面修订
List<Page> pages = doc.getChildNodes(Page.class);

//遍历页面列表
for (Page pageRevision : pages) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
}
```

此代码片段会迭代文档中的每个页面，并打印出每个页面的上次修改时间、创建时间、标题、级别和作者等信息。

## 结论

在本教程中，您学习了如何使用 Aspose.Note for Java 检索有关 OneNote 中页面的信息。通过执行上述步骤，您可以将 Aspose.Note 无缝集成到您的 Java 应用程序中，以从 OneNote 文档中提取有价值的数据。

## 常见问题解答

### Q1：我可以使用Aspose.Note for Java编辑OneNote文档吗？

A1：是的，Aspose.Note 提供了一套全面的功能，用于以编程方式编辑和操作 OneNote 文档。

### Q2：Aspose.Note 是否兼容所有版本的 OneNote？

A2：Aspose.Note支持各种版本的OneNote，确保不同环境下的兼容性。

### Q3：我可以使用Aspose.Note 将OneNote 文档转换为其他格式吗？

A3：当然可以，Aspose.Note 可以让您轻松地将 OneNote 文档转换为 PDF、HTML 和图像等格式。

### Q4：Aspose.Note 是否为开发者提供技术支持？

A4：是的，Aspose 提供专门的技术支持来帮助开发人员解决使用 Aspose.Note 时遇到的任何问题。

### Q5：Aspose.Note for Java 有试用版吗？

 A5：是的，您可以从以下位置下载 Aspose.Note for Java 的免费试用版：[这里](https://releases.aspose.com/).