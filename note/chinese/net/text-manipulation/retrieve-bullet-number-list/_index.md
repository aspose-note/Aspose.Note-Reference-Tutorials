---
title: 检索 Aspose.Note 文本中的项目符号或编号列表
linktitle: 检索 Aspose.Note 文本中的项目符号或编号列表
second_title: Aspose.Note .NET API
description: 通过我们有关检索项目符号或编号列表的分步指南来释放 Aspose.Note for .NET 的潜力。提升您的 OneNote 文档操作技能！
weight: 23
url: /zh/net/text-manipulation/retrieve-bullet-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 检索 Aspose.Note 文本中的项目符号或编号列表

## 介绍
欢迎来到 Aspose.Note for .NET 的世界，这是一个强大且多功能的库，使开发人员能够轻松处理 OneNote 文档操作。在本教程中，我们将深入研究使用 Aspose.Note for .NET 检索项目符号或编号列表的过程。无论您是经验丰富的开发人员还是编码爱好者，本指南都将为您提供在 Aspose.Note 中使用列表的复杂知识。
## 先决条件
在我们开始编码之旅之前，请确保您具备以下先决条件：
-  Aspose.Note for .NET：确保您已安装 Aspose.Note 库。如果没有，您可以从以下位置下载[.NET 文档的 Aspose.Note](https://reference.aspose.com/note/net/).
- 开发环境：在您的计算机上设置一个有效的开发环境，最好是 Microsoft Visual Studio。
- C# 基础知识：熟悉 C#，因为本教程是用这种语言编写的。
## 导入命名空间
为了与 Aspose.Note for .NET 交互，您需要将必要的命名空间导入到您的项目中。在代码开头包含以下命名空间：
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
现在，让我们逐步分解检索项目符号或编号列表的过程：
## 第 1 步：设置您的文档目录
```csharp
//文档目录的路径。
string dataDir = "Your Document Directory";
```
代替`"Your Document Directory"`与您的 Aspose.Note 文档所在的实际路径。
## 第 2 步：加载文档
```csharp
//将文档加载到 Aspose.Note 中。
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
确保更换`"ApplyNumberingOnText.one"`与您的特定 OneNote 文档的名称。
## 步骤 3：检索节点集合
```csharp
//检索轮廓元素的节点集合。
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
此步骤从加载的文档中检索大纲节点的集合。
## 第 4 步：迭代每个节点
```csharp
//迭代每个节点。
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        //继续执行后续步骤...
    }
}
```
这个循环确保我们只处理包含数字列表的节点。
## 第 5 步：检索字体信息
```csharp
//检索字体名称
Console.WriteLine("Font Name: " + list.Font);
//检索字体长度
Console.WriteLine("Font Length: " + list.Font.Length);
//检索字体大小
Console.WriteLine("Font Size: " + list.FontSize);
//检索字体颜色
Console.WriteLine("Font Color: " + list.FontColor);
//检索格式
Console.WriteLine("Font format: " + list.Format);
//勾选粗体
Console.WriteLine("Is bold: " + list.IsBold);
//检查斜体
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
这些代码行从数字列表中提取各种与字体相关的信息。
## 结论
恭喜！您已成功学习如何使用 Aspose.Note for .NET 检索项目符号或编号列表。当您继续探索时，请参阅[文档](https://reference.aspose.com/note/net/)以获得更深入的见解和功能。
## 常见问题解答
### 我可以将 Aspose.Note for .NET 与其他编程语言一起使用吗？
Aspose.Note 主要支持 .NET，但该库还有针对不同平台和语言量身定制的其他版本。
### Aspose.Note 与最新的 OneNote 格式兼容吗？
是的，Aspose.Note 支持多种 OneNote 格式，确保与最新版本的兼容性。
### 如何获得 Aspose.Note 的临时许可证？
访问[这个链接](https://purchase.aspose.com/temporary-license/)获得用于评估目的的临时许可证。
### Aspose.Note 用户可以使用哪些支持选项？
您可以探索并寻求帮助[Aspose.Note 论坛](https://forum.aspose.com/c/note/28)对于您可能遇到的任何疑问或问题。
### Aspose.Note for .NET 有免费试用版吗？
是的，您可以访问 Aspose.Note for .NET 的免费试用版[这里](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
