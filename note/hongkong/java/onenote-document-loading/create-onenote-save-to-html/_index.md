---
title: 建立 OneNote 文件並儲存為 HTML - Java
linktitle: 建立 OneNote 文件並儲存為 HTML - Java
second_title: Aspose.Note Java API
description: 了解使用 Aspose.Note for Java 建立 OneNote 文件並將其儲存為 HTML。整合到 Java 應用程式中以進行編程式 OneNote 檔案處理。

type: docs
weight: 18
url: /zh-hant/java/onenote-document-loading/create-onenote-save-to-html/
---
## 介紹

Aspose.Note for Java 是一個功能強大的函式庫，可讓開發人員以程式設計方式使用 Microsoft OneNote 檔案。在本教程中，我們將探索如何使用 Aspose.Note for Java 建立 OneNote 文件並將其儲存為 HTML 格式。

## 先決條件

在我們開始之前，請確保您具備以下條件：

1. 您的系統上安裝了 Java 開發工具包 (JDK)。
2.  Java 函式庫的 Aspose.Note。您可以從以下位置下載：[這裡](https://releases.aspose.com/note/java/).
3. Java 程式設計的基礎知識。

## 導入包

首先，將必要的套件匯入到您的 Java 專案中：

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

## 第 1 步：建立 OneNote 文檔對象

```java
Document document = new Document("Path_to_your_sample_one_file");
```

這段程式碼初始化了一個`Document`透過載入範例 OneNote 檔案來取得物件。

## 第 2 步：另存為 HTML 到記憶體流

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

在這裡，我們設定 HTML 保存選項並將文件保存到記憶體流。

## 步驟 3： 另存為 HTML，資源位於單獨的文件中

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

此步驟將文件另存為 HTML，並將 CSS、字體和圖像等資源保存在單獨的文件中。

## 步驟 4： 儲存為 HTML 到記憶體流，並透過回調來節省資源

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

在這裡，我們使用回調將文件作為 HTML 保存到記憶體流中以處理資源節省。

## 結論

恭喜！您已經學習如何使用 Aspose.Note for Java 建立 OneNote 文件並將其儲存為 HTML 格式。現在，您可以將此功能整合到 Java 應用程式中，以程式設計方式處理 OneNote 檔案。

## 常見問題解答

### Q1：我可以一次將多個 OneNote 文件轉換為 HTML 嗎？

A1：是的，您可以循環遍歷多個文件並迭代應用儲存過程。

### Q2：Aspose.Note for Java 是否支援 HTML 以外的其他輸出格式？

A2：是的，Aspose.Note for Java 支援各種輸出格式，包括 PDF、DOCX 和影像格式。

### Q3：Aspose.Note for Java 有試用版嗎？

A3：是的，您可以從以下位置下載免費試用版：[這裡](https://releases.aspose.com/).

### 問題 4：在哪裡可以獲得 Aspose.Note for Java 的支援？

 A4：您可以從以下機構獲得支持[Aspose.Note 論壇](https://forum.aspose.com/c/note/28).

### Q5：如何購買 Aspose.Note for Java 的授權？

 A5：您可以從以下位置購買許可證：[阿斯普斯網站](https://purchase.aspose.com/buy).