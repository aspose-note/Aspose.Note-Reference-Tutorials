---
title: 从 OneNote 文档中的表格中提取行文本 - Aspose.Note
linktitle: 从 OneNote 文档中的表格中提取行文本 - Aspose.Note
second_title: Aspose.Note Java API
description: 学习使用 Aspose.Note for Java 轻松从 OneNote 表格中提取行文本。请按照我们的分步指南进行无缝集成。
weight: 13
url: /zh/java/onenote-table-manipulation/extract-row-text-from-table/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 从 OneNote 文档中的表格中提取行文本 - Aspose.Note

## 介绍
欢迎来到这个关于使用 Aspose.Note for Java 从 OneNote 文档中的表格中提取行文本的综合教程。 Aspose.Note 是一个功能强大的 Java 库，使开发人员能够无缝地使用 Microsoft OneNote 文件。在本教程中，我们将逐步指导您完成该过程，演示如何有效地从 OneNote 文档的表格中提取行文本。
## 先决条件
在我们深入学习本教程之前，请确保您具备以下先决条件：
-  Aspose.Note for Java 库：确保您已安装 Aspose.Note for Java 库。您可以从[下载链接](https://releases.aspose.com/note/java/).
- Java 开发环境：确保您的计算机上设置了 Java 开发环境。
- OneNote 文档：准备一个示例 OneNote 文档（例如“Sample1.one”），其中包含要从中提取行文本的表。
## 导入包
在您的 Java 项目中，导入必要的 Aspose.Note 包。这可确保您能够访问使用 OneNote 文档所需的类和方法。
```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.RichText;
import com.aspose.note.Table;
import com.aspose.note.TableRow;
```
## 第1步：设置文档目录
```java
//文档目录的路径。
String dataDir = "Your Document Directory";
```
## 步骤 2：加载 OneNote 文档
```java
//将文档加载到 Aspose.Note 中。
Document document = new Document(dataDir + "Sample1.one", new LoadOptions());
```
## 第三步：获取表节点
```java
//获取表节点列表
List<Table> nodes = (List<Table>) document.getChildNodes(Table.class);
```
## 第 4 步：迭代表和行
```java
//设置行数
int rowCount = 0;
for (Table table : nodes) {
    //遍历表行
    for (TableRow row : table) {
        rowCount++;
        //检索文本
        List<RichText> textNodes = (List<RichText>) row.getChildNodes(RichText.class);
        StringBuilder text = new StringBuilder();
        for (RichText richText : textNodes) {
            text = text.append(richText.getText().toString());
        }
        //在输出屏幕上打印文本
        System.out.println(text);
    }
}
```
对 OneNote 文档中的每个表格重复这些步骤，您将成功提取行文本。
## 结论
恭喜！您已了解如何使用 Aspose.Note for Java 从 OneNote 文档中的表格中提取行文本。本教程为在 Java 应用程序中利用 Aspose.Note 的强大功能奠定了基础。
## 经常问的问题
### Aspose.Note 与最新版本的 Microsoft OneNote 兼容吗？
 Aspose.Note 支持各种 OneNote 版本，包括最新版本。请参阅[文档](https://reference.aspose.com/note/java/)有关兼容性详细信息。
### 我可以在购买前试用 Aspose.Note for Java 吗？
是的，您可以在以下网址探索 Aspose.Note 的免费试用版：[这个链接](https://releases.aspose.com/).
### 我在哪里可以找到额外的支持和帮助？
参观[Aspose.Note 论坛](https://forum.aspose.com/c/note/28)以获得社区支持和讨论。
### 如何获得 Aspose.Note 的临时许可证？
获得临时许可证[这个链接](https://purchase.aspose.com/temporary-license/).
### 使用 Aspose.Note for Java 有任何特定的系统要求吗？
有关详细的系统要求，请参阅文档。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
