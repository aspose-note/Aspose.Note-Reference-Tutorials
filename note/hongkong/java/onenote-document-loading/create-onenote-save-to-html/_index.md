---
date: 2026-02-07
description: 學習如何在使用 Aspose.Note for Java 將 OneNote 儲存為 HTML 時匯出字型。本指南將向您展示如何以程式方式建立
  OneNote 並嵌入字型、CSS 與圖片。
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: 如何在將 OneNote 儲存為 HTML 時匯出字型 – Java
url: /zh-hant/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在將 OneNote 儲存為 HTML 時匯出字型 – Java

## 簡介

在本教學中，您將了解 **如何匯出字型**，當您 **將 OneNote 儲存為 HTML** 時，使用 Aspose.Note for Java。我們將示範如何以程式方式建立 OneNote 文件、設定 HTML 儲存選項，並嵌入所需的字型檔案，使產生的 HTML 與原始 OneNote 頁面外觀完全相同。當您需要在網頁友好的格式中保留 OneNote 內容的視覺忠實度時，此方法非常適合。

## 快速答覆
- **哪個函式庫負責匯出？** Aspose.Note for Java  
- **字型可以嵌入到 HTML 中嗎？** 可以 – 設定 `ExportFonts` 為 `ExportEmbedded`  
- **商業使用需要授權嗎？** 需要有效的 Aspose.Note 授權才能用於商業用途  
- **支援哪個 Java 版本？** Java 8 或更高版本  
- **可以將資源儲存為獨立檔案嗎？** 當然可以 – 依需求設定 `ResourceExportType`  

## 「匯出字型」在 OneNote HTML 轉換中的意義是什麼？

當您將 OneNote 筆記本轉換為 HTML 時，視覺外觀取決於 CSS、圖片，尤其是原始頁面使用的字型。**匯出字型** 意味著將字型檔案（例如 TTF）直接嵌入 HTML 套件，使瀏覽器即使在使用者本機未安裝該字型，也能呈現與 OneNote 完全相同的文字外觀。

## 為什麼要以程式方式建立 OneNote 並儲存為 HTML？

- **自動化：** 從 OneNote 產生報告、文件或知識庫文章，免除手動複製貼上。  
- **一致性：** 在不同裝置間保留版面配置、樣式與自訂字型。  
- **可攜性：** HTML 可在任何環境檢視，無需 OneNote 客戶端。  

## 先決條件

1. 已安裝 Java Development Kit (JDK) 8 或更新版本。  
2. Aspose.Note for Java 程式庫 – 從 [here](https://releases.aspose.com/note/java/) 下載。  
3. 一個範例 OneNote 檔案（`.one`）以供載入，或可程式方式建立新檔案。  

## 匯入套件

首先，將所需的類別匯入您的 Java 專案：

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

## 如何在將 OneNote 儲存為 HTML 時匯出字型？

以下是一個逐步指南，說明如何 **匯出字型** 以及其他資源。

### 步驟 1：以程式方式建立 OneNote 文件  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

此行會載入現有的 `.one` 檔案。若您需要 **以程式方式建立 OneNote**，可以實例化新的 `Document` 物件，並透過 API 新增章節/頁面（此處未示範，以免分散匯出字型的重點）。

### 步驟 2：以嵌入字型的方式儲存至記憶體串流  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` 告訴 Aspose.Note **匯出字型** 直接至 HTML 套件中。  
- `setFontFaceTypes(FontFaceType.Ttf)` 確保使用 TrueType 字型，具廣泛的瀏覽器相容性。

### 步驟 3：以分離資源檔案的方式儲存為 HTML（仍匯出字型）  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

即使 CSS 與圖片已嵌入，若您希望以分離檔案以利快取，也可以將 `ResourceExportType` 改為 `ExportExternal`。關鍵部分——**匯出字型**——仍保持不變。

### 步驟 4：使用回呼函式控制每個資源的儲存位置  

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

`UserSavingCallbacks` 類別（您需要實作 `ICssSavingCallback`、`IImageSavingCallback` 與 `IFontSavingCallback`）讓您完整掌控資料夾結構，您可以將字型放在專屬的 `fonts` 目錄中，同時正確 **匯出字型**。

## 如何在將 OneNote 轉換為 HTML 時嵌入自訂字型

嵌入自訂字型可確保 HTML 的呈現與原始 OneNote 版面相符，即使在未安裝該字型的裝置上亦如此。透過將 `ExportEmbedded` 與 `FontFaceType.Ttf` 結合，TrueType 檔案會以 base‑64 編碼直接插入產生的 CSS 中，省去外部字型託管的需求。

## 使用 ResourceExportType 控制資源匯出

`ResourceExportType` 讓您決定 CSS、圖片與字型是儲存在 HTML 檔案 **內部**（`ExportEmbedded`）還是另存為 **外部** 檔案（`ExportExternal`）。若需要單一檔案解決方案，選擇 `ExportEmbedded`；若想利用瀏覽器快取大型資產，則使用 `ExportExternal`。

## 以程式方式建立 OneNote 以供 HTML 匯出

若從零開始，您可以完全以程式碼建立 OneNote 文件，加入章節、頁面與豐富文字，然後套用前述相同的 `HtmlSaveOptions`。這樣即可實現端對端自動化：從資料產生到帶有嵌入自訂字型的完整樣式化 HTML 輸出。

## 常見問題與技巧

- **輸出中缺少字型：** 確認已設定 `setExportFonts(ResourceExportType.ExportEmbedded)`，且來源 OneNote 檔案確實使用了嵌入字型。  
- **HTML 檔案過大：** 嵌入字型會增加檔案大小。若頻寬受限，可將 `ExportFonts` 改為 `ExportExternal`，並將字型託管於 CDN。  
- **回呼實作錯誤：** 確保您的回呼類別正確寫入串流並關閉資源，以免檔案損毀。  

## 常見問答

**Q: 我可以一次轉換多個 OneNote 文件為 HTML 嗎？**  
A: 可以，對每個 `Document` 實例迴圈，套用相同的 `HtmlSaveOptions`。

**Q: Aspose.Note for Java 是否支援除 HTML 之外的其他輸出格式？**  
A: 當然支援。您可以使用相應的儲存選項匯出為 PDF、DOCX、PNG、JPEG 等格式。

**Q: 是否提供 Aspose.Note for Java 的試用版？**  
A: 有，請從 [here](https://releases.aspose.com/) 下載免費試用版。

**Q: 我可以從哪裡取得 Aspose.Note for Java 的支援？**  
A: 前往 [Aspose.Note forum](https://forum.aspose.com/c/note/28) 取得社群與官方協助。

**Q: 我要如何購買 Aspose.Note for Java 的授權？**  
A: 可於 [Aspose website](https://purchase.aspose.com/buy) 購買授權。

## 結論

現在您已了解如何在使用 Aspose.Note for Java **將 OneNote 儲存為 HTML** 時 **匯出字型**。透過設定 `HtmlSaveOptions`，並視需要使用回呼函式，您可以在網路上呈現 OneNote 頁面的完整外觀——包括自訂字型。歡迎嘗試不同的 `ResourceExportType` 設定，以符合您專案的效能與儲存需求。

---

**最後更新：** 2026-02-07  
**測試環境：** Aspose.Note for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}