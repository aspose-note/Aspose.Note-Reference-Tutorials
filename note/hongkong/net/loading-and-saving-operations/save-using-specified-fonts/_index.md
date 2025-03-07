---
title: 在 Aspose.Note 中使用指定字體儲存
linktitle: 在 Aspose.Note 中使用指定字體儲存
second_title: Aspose.Note .NET API
description: 了解如何在 Aspose.Note for .NET 中儲存具有指定字型的文件。輕鬆自訂字體設置，以實現一致的文件格式。
weight: 28
url: /zh-hant/net/loading-and-saving-operations/save-using-specified-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Note 中使用指定字體儲存

## 介紹

在本教程中，我們將學習如何在 Aspose.Note for .NET 中使用指定字體儲存文件。我們將逐步探索實現這一目標的不同方法。

## 先決條件

在我們開始之前，請確保您具備以下條件：

1.  Aspose.Note for .NET：確保您已安裝 Aspose.Note for .NET。您可以從以下位置下載：[這裡](https://releases.aspose.com/note/net/).

2. 開發環境：您需要為.NET 開發設定一個開發環境。

## 導入命名空間

首先，讓我們導入必要的名稱空間：

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## 第 1 步：使用預設字體名稱儲存

在此步驟中，我們將使用指定的預設字型名稱來儲存文件。

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    //文檔目錄的路徑。
    string dataDir = "Your Document Directory";

    //將文件載入到 Aspose.Note 中。
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    //使用指定的預設字型將文件另存為 PDF。
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## 步驟 2：使用檔案中的預設字體儲存

接下來，讓我們使用從文件加載的預設字體來保存文件。

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    //文檔目錄的路徑。
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    //將文件載入到 Aspose.Note 中。
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    //使用從文件載入的預設字型將文件另存為 PDF。
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## 步驟 3：使用 Stream 中的預設字型儲存

最後，讓我們使用從流加載的預設字體來保存文件。

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    //文檔目錄的路徑。
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    //將文件載入到 Aspose.Note 中。
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    //使用從流程載入的預設字體將文件另存為 PDF。
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## 結論

在本教學中，我們探討如何在 Aspose.Note for .NET 中使用指定字型儲存文件。透過執行以下步驟，您可以根據您的要求自訂字體設置，確保文件的格式符合您的要求。

## 常見問題解答

### Q1: 我可以使用任何字體在Aspose.Note中儲存文件嗎？

A1: 是的，您可以指定任何字型來儲存文件。只需確保字體檔案可存取並正確加載即可。

### Q2：Aspose.Note 是否相容於不同的文件格式？

A2：Aspose.Note 主要適用於 OneNote 文檔，但提供了儲存為各種格式（包括 PDF）的選項。

### Q3：儲存文件時字體遺失如何處理？

A3：Aspose.Note 提供了使用預設字體的選項，以防指定字體遺失，確保文件格式一致。

### Q4：Aspose.Note 支援在輸出文件中嵌入字型嗎？

A4：是的，Aspose.Note 允許嵌入字體，以確保文件的可移植性和跨不同平台的一致渲染。

### Q5：我可以在哪裡獲得有關 Aspose.Note 的進一步協助？

 A5： 如需進一步協助或技術支持，您可以訪問[Aspose.Note 論壇](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
