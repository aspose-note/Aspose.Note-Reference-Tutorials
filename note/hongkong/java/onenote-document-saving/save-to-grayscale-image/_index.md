---
date: 2025-12-17
description: 了解如何使用 Aspose.Note for Java，將 OneNote 文件另存為灰階 PNG 圖像以匯出 OneNote。內容包括載入
  OneNote 文件及建立灰階圖像的步驟。
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: 如何將 OneNote 匯出為灰階圖像 – Aspose.Note
url: /zh-hant/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中儲存為灰階影像 - Aspose.Note

## 簡介

在本教學中，我們將示範 **如何匯出 OneNote**，透過將文件儲存為灰階影像，使用 Aspose.Note for Java。灰階影像是僅包含灰色階層的單色圖片，可用於列印、存檔或減少檔案大小。我們將說明載入 OneNote 文件、設定儲存選項以 **建立灰階影像**，最後 **將文件儲存為 PNG**。

## 快速解答
- **「如何匯出 OneNote」是什麼意思？** 它指的是以程式方式將 OneNote 檔案轉換為其他格式，例如影像。  
- **哪種格式最適合灰階輸出？** PNG 表現良好，因為它保留無損品質且支援灰階色彩模式。  
- **我需要授權嗎？** 在正式環境使用需擁有有效的 Aspose.Note 授權；測試時可使用臨時試用授權。  
- **需要哪個版本的 Java？** 建議使用 Java 8 或更高版本。  
- **我可以調整影像尺寸嗎？** 可以，在儲存前調整 `ImageSaveOptions` 的屬性，例如 `Resolution` 或 `PageSize`。  

## 「如何匯出 OneNote」是什麼？
匯出 OneNote 指的是以程式方式將 OneNote `.one` 檔案轉換為其他形式，例如 PDF、HTML 或影像。本指南聚焦於匯出為 **灰階 PNG** 影像，這在文件或列印工作流程中相當常見。

## 為什麼要將 OneNote 匯出為灰階影像？
- **減少檔案大小** – 灰階 PNG 通常比全彩影像更小。  
- **提升可讀性** – 在列印報告時，灰階往往能提供更清晰的對比度。  
- **相容性** – PNG 在瀏覽器、編輯器及行動裝置上廣受支援。  

## 前置條件

在開始之前，請確保您具備以下項目：

1. 已在系統上安裝 Java Development Kit (JDK)。  
2. Aspose.Note for Java 程式庫。您可從 [here](https://releases.aspose.com/note/java/) 下載。  
3. 具備 Java 程式設計的基本概念。  

## 匯入套件

開始之前，請匯入必要的套件：

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 步驟 1：載入 OneNote 文件

首先，**載入 OneNote 文件** 到 Aspose.Note。將 `"Your Document Directory"` 替換為本機資料夾的路徑，將 `"Aspose.one"` 替換為您的 OneNote 檔案名稱。

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 步驟 2：設定輸出路徑與選項

定義灰階影像的輸出路徑並指定儲存選項。我們將 `ColorMode` 設為 `GrayScale`，並使用 **將文件儲存為 PNG** 的格式。

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## 步驟 3：儲存文件

最後，使用先前設定的選項將文件儲存為灰階 PNG 影像。

```java
oneFile.save(dataDir, options);
```

## 常見問題與解決方案
- **FileNotFoundException** – 請確認 `dataDir` 指向正確的資料夾，且 `.one` 檔案確實存在。  
- **LicenseException** – 在呼叫 `save` 之前，請確保已套用有效的 Aspose.Note 授權。  
- **低解析度輸出** – 如有需要，可調整 `options.setResolution(300)` 以提升 DPI。  

## 常見問答

**Q1：我可以將灰階影像儲存為其他格式嗎？**  
A1：可以，只需在 `ImageSaveOptions` 建構函式中將 `SaveFormat` 參數改為 `Jpeg`、`Bmp` 等。

**Q2：Aspose.Note 是否相容所有版本的 OneNote 文件？**  
A2：Aspose.Note 支援 Microsoft OneNote 2010 及之後的版本。

**Q3：使用 Aspose.Note 是否需要授權？**  
A3：正式環境使用需擁有有效授權，但可取得臨時試用授權以進行評估。

**Q4：我可以在將文件儲存為影像前操作其他部分嗎？**  
A4：當然可以！Aspose.Note 提供完整的 API，讓您在匯出前編輯章節、頁面及內容。

**Q5：如果遇到問題，我該去哪裡尋求支援？**  
A5：您可於 Aspose.Note 論壇取得支援，請點擊 [here](https://forum.aspose.com/c/note/28)。

## 結論

您現在已學會 **如何匯出 OneNote**：透過載入 OneNote 檔案、設定儲存選項以 **建立灰階影像**，並 **將文件儲存為 PNG**。此技巧可輕鬆產生輕量、適合列印的視覺圖檔，從 OneNote 筆記本中提取。歡迎嘗試其他 `ColorMode` 設定或影像格式，以符合您的專案需求。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose  

---