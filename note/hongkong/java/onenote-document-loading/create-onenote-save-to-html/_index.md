---
date: 2025-12-02
description: 了解如何在使用 Aspose.Note for Java 將 OneNote 儲存為 HTML 時匯出字型。本指南將示範如何以程式方式建立
  OneNote，並嵌入字型、CSS 與圖片。
language: zh-hant
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: 將 OneNote 儲存為 HTML 時如何匯出字型 – Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在將 OneNote 儲存為 HTML 時匯出字型 – Java

## Introduction

在本教學中，您將了解 **如何匯出字型**，當您 **將 OneNote 儲存為 HTML** 時，使用 Aspose.Note for Java。 我們將示範如何以程式方式建立 OneNote 文件、設定 HTML 儲存選項，並嵌入所需的字型檔案，使產生的 HTML 與原始 OneNote 頁面外觀完全相同。此方法在您需要以網頁友好格式保留 OneNote 內容的視覺忠實度時非常適用。

## Quick Answers
- **什麼程式庫負責匯出？** Aspose.Note for Java  
- **字型可以嵌入 HTML 嗎？** 是 – 設定 `ExportFonts` 為 `ExportEmbedded`  
- **生產環境需要授權嗎？** 商業使用需擁有有效的 Aspose.Note 授權  
- **支援哪個 Java 版本？** Java 8 或更高版本  
- **是否可以將資源儲存為獨立檔案？** 當然可以 – 依需求設定 `ResourceExportType`  

## What is “how to export fonts” in the context of OneNote HTML conversion?

在 OneNote HTML 轉換的情境下，「如何匯出字型」是什麼意思？

當您將 OneNote 筆記本轉換為 HTML 時，視覺外觀取決於 CSS、圖片，尤其是原始頁面使用的字型。**匯出字型** 意味著將字型檔案（例如 TTF）直接嵌入 HTML 套件，使瀏覽器能夠如同在 OneNote 中呈現的方式渲染文字，即使最終使用者本機未安裝這些字型。

## Why create OneNote programmatically and save it as HTML?

- **自動化：** 從 OneNote 產生報告、文件或知識庫文章，無需手動複製貼上。  
- **一致性：** 在不同裝置間保留版面配置、樣式與自訂字型。  
- **可移植性：** HTML 可在任何平台檢視——不需要 OneNote 客戶端。  

## Prerequisites

1. 已安裝 Java Development Kit (JDK) 8 或更新版本。  
2. Aspose.Note for Java 程式庫 – 從 [here](https://releases.aspose.com/note/java/) 下載。  
3. 用於載入的範例 OneNote 檔案（`.one`），或您也可以以程式方式建立新的檔案。  

## Import Packages

First, import the required classes into your Java project:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## How to Export Fonts While Saving OneNote as HTML?

以下是逐步指南，說明 **如何匯出字型** 以及其他資源。

### Step 1: Create a OneNote document programmatically  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

此行載入現有的 `.one` 檔案。若您需要 **以程式方式建立 OneNote**，可以實例化新的 `Document` 物件，並透過 API 新增章節/頁面（此處未示範，以免分散匯出字型的重點）。

### Step 2: Save to a memory stream with embedded fonts  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` 告訴 Aspose.Note **匯出字型** 直接至 HTML 套件。  
- `setFontFaceTypes(FontFaceType.Ttf)` 確保使用 TrueType 字型，具廣泛的瀏覽器相容性。  

### Step 3: Save as HTML with separate resource files (still exporting fonts)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

即使 CSS 與圖片已嵌入，若您偏好將資源分為獨立檔案以利快取，也可以將 `ResourceExportType` 改為 `ExportExternal`。關鍵步驟——**匯出字型**——仍保持不變。

### Step 4: Use callbacks to control where each resource is stored  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

`UserSavingCallbacks` 類別（您需要實作 `ICssSavingCallback`、`IImageSavingCallback` 與 `IFontSavingCallback`）讓您完整掌控資料夾結構，您可以將字型保留在專屬的 `fonts` 目錄中，同時正確 **匯出字型**。

## Common Issues & Tips

- **輸出缺少字型：** 請確認已設定 `setExportFonts(ResourceExportType.ExportEmbedded)`，且來源 OneNote 檔案確實使用了嵌入字型。  
- **HTML 檔案過大：** 嵌入字型會增加檔案大小。若擔心頻寬，可將 `ExportFonts` 改為 `ExportExternal`，並將字型放置於 CDN 上。  
- **回呼實作錯誤：** 請確保您的回呼類別正確寫入串流並關閉資源，以免檔案損毀。  

## Frequently Asked Questions

**Q: 我可以一次轉換多個 OneNote 文件為 HTML 嗎？**  
A: 可以，遍歷每個 `Document` 實例並套用相同的 `HtmlSaveOptions`。  

**Q: Aspose.Note for Java 是否支援除 HTML 之外的其他輸出格式？**  
A: 當然支援。您可以使用相應的儲存選項匯出為 PDF、DOCX、PNG、JPEG 等格式。  

**Q: 是否有 Aspose.Note for Java 的試用版？**  
A: 有，請從 [here](https://releases.aspose.com/) 下載免費試用版。  

**Q: 我可以從哪裡取得 Aspose.Note for Java 的支援？**  
A: 前往 [Aspose.Note forum](https://forum.aspose.com/c/note/28) 獲取社群與官方協助。  

**Q: 如何購買 Aspose.Note for Java 的授權？**  
A: 可於 [Aspose website](https://purchase.aspose.com/buy) 購買授權。  

## Conclusion

現在您已了解在使用 Aspose.Note for Java **將 OneNote 儲存為 HTML 時如何匯出字型**。透過設定 `HtmlSaveOptions`，並視需要使用回呼，您可以在網路上呈現 OneNote 頁面的完整外觀——包括自訂字型。歡迎嘗試不同的 `ResourceExportType` 設定，以符合您專案的效能與儲存需求。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-12-02  
**測試環境：** Aspose.Note for Java 24.12  
**作者：** Aspose  

---