---
title: 在 OneNote 中將筆記本轉換為平面圖像 - Aspose.Note
linktitle: 在 OneNote 中將筆記本轉換為平面圖像 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 將筆記本轉換為 OneNote 中的拼合圖。輕鬆地將所有元素保留在單一影像檔案中。
type: docs
weight: 13
url: /zh-hant/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---
## 介紹

在本教程中，我們將引導您完成使用 Aspose.Note for Java 在 OneNote 中將筆記本轉換為平面圖像的過程。這允許您將筆記本另存為圖像文件，確保所有元素都以單一圖像格式保留。

## 先決條件

在我們開始之前，請確保您具備以下條件：

1. 您的系統上安裝了 Java 開發工具包 (JDK)。
2. 下載 Aspose.Note for Java 函式庫並在您的 Java 專案中進行設定。您可以從以下位置下載該程式庫[這裡](https://releases.aspose.com/note/java/).
3. Java 程式設計的基礎知識。

## 導入包

首先，您需要從 Aspose.Note for Java 匯入必要的套件：

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## 第 1 步：設定文檔目錄

首先，定義筆記本檔案所在的目錄：

```java
String dataDir = "Your Document Directory";
```

代替`"Your Document Directory"`以及筆記本文件的路徑。

## 第 2 步：載入筆記本

接下來，使用以下命令載入筆記本文件`Notebook`班級：

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

確保更換`"test.onetoc2"`與您的筆記本文件的名稱。

## 第 3 步：設定影像儲存選項

現在，設定將筆記本儲存為影像的選項。我們將指定儲存格式為 PNG 並將解析度設為 400 DPI：

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

您可以根據您的要求調整解析度。

## 第四步：壓平筆記本

為了確保所有元素都被展平為單一影像，請設置`flatten`選項`true`:

```java
saveOptions.setFlatten(true);
```

這可確保產生的影像保持筆記本的佈局。

## 第5步：儲存影像

最後，將筆記本另存為平面影像：

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

代替`"ExportImageasFlattenedNotebook_out.png"`與您想要的輸出檔名。

## 結論

總之，使用 Aspose.Note for Java，您可以輕鬆地將筆記本轉換為 OneNote 中的平面影像。此過程可確保所有元素都以單一影像格式儲存，以便於輕鬆分享和檢視。

## 常見問題解答

### Q1：我可以調整輸出影像的解析度嗎？

 A1: 是的，您可以根據您的要求進行修改`setResolution`方法參數。

### Q2：Aspose.Note是否支援其他影像格式匯出？

A2: 是的，Aspose.Note 支援多種圖片格式，如 PNG、JPEG、BMP 等，用於匯出筆記本。

### Q3：我可以進一步自訂輸出影像嗎？

A3：是的，Aspose.Note 提供了豐富的選項用於自訂輸出影像，包括頁面大小、方向和品質設定。

### Q4：Aspose.Note for Java 有試用版嗎？

 A4：是的，您可以從以下位置取得免費試用版：[這裡](https://releases.aspose.com/).

### Q5：哪裡可以找到 Aspose.Note for Java 的支援？

 A5：您可以在 Aspose.Note 論壇上找到支援和資源[這裡](https://forum.aspose.com/c/note/28).