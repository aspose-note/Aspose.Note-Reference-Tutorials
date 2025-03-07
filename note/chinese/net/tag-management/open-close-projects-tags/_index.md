---
title: 在 Aspose.Note 中打开和关闭带有标签的项目
linktitle: 在 Aspose.Note 中打开和关闭带有标签的项目
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 以编程方式操作 Microsoft OneNote 文件。有效地打开和关闭带有标签的项目。
weight: 15
url: /zh/net/tag-management/open-close-projects-tags/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Note 中打开和关闭带有标签的项目

## 介绍

在本教程中，我们将学习如何使用 Aspose.Note for .NET 打开和关闭带有标签的项目。 Aspose.Note 是一个功能强大的 API，允许开发人员以编程方式处理 Microsoft OneNote 文件，从而实现处理文档中的文本、图像和标签等任务。

## 先决条件

在开始之前，请确保您已设置以下先决条件：

## 导入命名空间

```csharp
using System.IO;
using System.Linq;
```

现在让我们将每个示例分解为多个步骤：

## 第 1 步：加载文档

首先，我们需要将文档加载到Aspose.Note中。

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## 步骤 2：关闭项目 C 项

现在，让我们关闭与“Project C”相关的所有复选框项目。

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## 步骤 3：保存关闭的项目 C 注释

使用关闭的“Project C”项目保存修改后的文档。

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## 第 4 步：打开项目 C 项

接下来，让我们打开与“Project C”相关的所有复选框项。

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## 步骤 5：保存打开的项目 C 注释

使用打开的“Project C”项目保存修改后的文档。

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

现在您已经学习了如何使用 .NET 在 Aspose.Note 中打开和关闭带有标签的项目。

## 结论

Aspose.Note for .NET 提供了一种以编程方式操作 OneNote 文档的便捷方法。通过遵循本教程，您可以通过使用标签打开和关闭项目来有效管理项目。

## 常见问题解答

### Q1：Aspose.Note 是否兼容所有版本的 OneNote？

A1：Aspose.Note 支持 Microsoft OneNote 2010 及更高版本。

### Q2：我可以将Aspose.Note用于商业项目吗？

 A2：是的，您可以将 Aspose.Note 用于个人和商业项目。访问[这里](https://purchase.aspose.com/buy)购买许可证。

### Q3：Aspose.Note 提供免费试用吗？

A3：是的，您可以获得免费试用[这里](https://releases.aspose.com/).

### Q4：在哪里可以找到 Aspose.Note 的文档？

 A4：你可以找到文档[这里](https://reference.aspose.com/note/net/).

### Q5：在哪里可以获得 Aspose.Note 的支持？

 A5：如需支持，您可以访问Aspose.Note[论坛](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
