---
title: 使用 Aspose.Note 检索附加文件
linktitle: 使用 Aspose.Note 检索附加文件
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 从 Microsoft OneNote 文档中检索附加文件。按照步骤加载、获取节点并迭代附件。
type: docs
weight: 12
url: /zh/net/attachments/retrieve-attached-files/
---
## 介绍

在本教程中，我们将探讨如何使用 Aspose.Note for .NET 从文档中检索附加文件。 Aspose.Note 是一个功能强大的 API，允许开发人员以编程方式使用 Microsoft OneNote 文件。我们将把这个过程分解为简单的步骤，以便于遵循。

## 先决条件

在我们开始之前，请确保您具备以下条件：

-  Aspose.Note for .NET：确保您已安装 Aspose.Note for .NET。您可以从以下位置下载：[这里](https://releases.aspose.com/note/net/).

## 导入命名空间

首先，让我们导入使用 Aspose.Note 所需的命名空间：

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## 第 1 步：加载文档

```csharp
//文档目录的路径。
string dataDir = "Your Document Directory";

//将文档加载到 Aspose.Note 中。
Document oneFile = new Document(dataDir + "Sample1.one");
```

## 第 2 步：获取附加文件节点

```csharp
//获取附加文件节点的列表
IList<AttachedFile> nodes = oneFile.GetChildNodes<AttachedFile>();
```

## 第 3 步：遍历附加文件

```csharp
//遍历所有节点
foreach (AttachedFile file in nodes)
{
    //将附加文件加载到流对象
    using (Stream outputStream = new MemoryStream(file.Bytes))
    {
        //创建本地文件
        using (Stream fileStream = System.IO.File.OpenWrite(String.Format(dataDir + file.FileName)))
        {
            //复制文件流
            CopyStream(outputStream, fileStream);
        }
    }
}
```

## 结论

在本教程中，我们学习了如何使用 Aspose.Note for .NET 从文档中检索附加文件。通过执行这些简单的步骤，您可以将此功能无缝集成到您的 .NET 应用程序中。

## 常见问题解答

### Q1：Aspose.Note 是否兼容所有版本的 OneNote 文件？

A1：是的，Aspose.Note支持各种版本的Microsoft OneNote文件，确保跨不同平台的兼容性。

### Q2：我可以在本地保存检索到的附件之前修改它们吗？

A2：当然！您可以根据需要在应用程序中操作附加文件，然后再将它们保存在本地。

### Q3：Aspose.Note 为开发者提供支持吗？

A3：当然！ Aspose 提供了广泛的文档和专门的支持论坛，以帮助开发人员解决遇到的任何疑问或问题。

### Q4: 我可以在购买之前试用 Aspose.Note 吗？

A4：是的，您可以在做出购买决定之前免费试用 Aspose.Note 来探索其特性和功能。

### Q5：如何获得Aspose.Note的临时许可证？

A5：您可以向 Aspose 请求临时许可证，以在您的开发环境中评估 API 的全部功能。