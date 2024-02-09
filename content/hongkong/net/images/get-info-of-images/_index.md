---
title: 在Aspose.Note中獲取圖像信息
linktitle: 在Aspose.Note中獲取圖像信息
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 從 Microsoft OneNote 檔案中提取映像資訊。遵循我們的逐步指南以實現高效開發。
type: docs
weight: 13
url: /zh-hant/net/images/get-info-of-images/
---
## 介紹

在 .NET 開發領域，Aspose.Note 提供了一組強大的工具來處理 Microsoft OneNote 檔案。開發人員經常面臨的一項常見任務是從這些筆記中嵌入的圖像中提取資訊。無論是取得尺寸、檔案名稱或修改時間，Aspose.Note 都簡化了這個過程。

## 先決條件

在我們深入使用 Aspose.Note 提取圖像資訊之前，請確保您具備以下條件：

1. C# 基礎知識：熟悉 C# 程式語言對於理解程式碼範例至關重要。
2. 安裝了 Aspose.Note for .NET：確保您的開發環境中安裝了 Aspose.Note 函式庫。你可以下載它[這裡](https://releases.aspose.com/note/net/).

## 導入命名空間

在開始之前，讓我們導入必要的名稱空間：

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## 第 1 步：載入文檔

首先，將目標 OneNote 文件載入到 Aspose.Note 中：

```csharp
//文檔目錄的路徑。
string dataDir = "Your Document Directory";

//將文件載入到 Aspose.Note 中。
Document oneFile = new Document(dataDir + "Aspose.one");
```

代替`"Your Document Directory"`以及 OneNote 檔案的路徑。

## 第2步：檢索影像資訊

接下來，從文件中檢索所有影像節點：

```csharp
//取得所有Image節點
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

此程式碼片段取得載入的 OneNote 文件中的所有影像節點。

## 第 3 步：迭代圖像

現在，讓我們迭代每個圖像節點以提取其元資料：

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

此循環列印出每個影像的各種屬性，例如寬度、高度、原始尺寸、檔案名稱和上次修改時間。

## 結論

借助 Aspose.Note for .NET，從 OneNote 文件中提取圖像資訊成為一個無縫過程。透過遵循本教程中概述的步驟，開發人員可以有效地從嵌入圖像中檢索元數據，從而使他們能夠建立強大的應用程式。

## 常見問題解答

### Q1：Aspose.Note 是否相容於所有版本的 Microsoft OneNote？

A1：Aspose.Note 支援多種格式的 OneNote 文件，包括 .one、.onepkg 和 .onetoc2，確保不同版本之間的相容性。

### Q2：我可以使用Aspose.Note修改圖片屬性嗎？

A2：是的，Aspose.Note 允許您以程式設計方式操作影像屬性，例如尺寸、檔案名稱和修改時間。

### Q3：Aspose.Note 是否提供對 .NET Core 的支援？

A3：是的，Aspose.Note 提供對 .NET Core 的支持，使您的應用程式能夠跨平台開發。

### Q4：Aspose.Note 有免費試用版嗎？

A4：是的，您可以在購買之前免費試用 Aspose.Note 以探索其功能。

### Q5：我可以在哪裡找到有關 Aspose.Note 的其他支援或協助？

 A5：如有任何疑問或協助，您可以造訪 Aspose.Note 論壇[這裡](https://forum.aspose.com/c/note/28).