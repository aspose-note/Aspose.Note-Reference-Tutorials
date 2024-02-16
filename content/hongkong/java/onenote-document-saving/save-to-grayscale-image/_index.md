---
title: 在 OneNote 中儲存到灰階影像 - Aspose.Note
linktitle: 在 OneNote 中儲存到灰階影像 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 在 OneNote 中將文件儲存為灰階影像。以程式設計方式輕鬆操作 Microsoft OneNote 文件。
type: docs
weight: 17
url: /zh-hant/java/onenote-document-saving/save-to-grayscale-image/
---
## 介紹

在本教學中，我們將探討如何使用 Aspose.Note for Java 在 OneNote 中將文件儲存為灰階影像。灰階影像是單色影像，其中顏色資訊僅由灰色陰影表示。 Aspose.Note 是一個功能強大的 Java API，允許以程式設計方式操作 Microsoft OneNote 文件。

## 先決條件

在我們開始之前，請確保您具備以下條件：

1. 您的系統上安裝了 Java 開發工具包 (JDK)。
2.  Java 函式庫的 Aspose.Note。您可以從以下位置下載：[這裡](https://releases.aspose.com/note/java/).
3. 對 Java 程式設計有基本的了解。

## 導入包

首先，導入必要的套件：

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 第 1 步：載入文檔

首先，將文件載入到 Aspose.Note 中。代替`"Your Document Directory"`以及文檔目錄的路徑和`"Aspose.one"`與您的 OneNote 文件的名稱。

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 步驟2：設定輸出路徑和選項

定義灰階影像的輸出路徑並指定儲存選項。我們將顏色模式設定為灰階。

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## 第 3 步：儲存文檔

最後，使用指定的選項將文件另存為灰階影像。

```java
oneFile.save(dataDir, options);
```

## 結論

恭喜！您已成功學習如何使用 Aspose.Note for Java 在 OneNote 中將文件儲存為灰階影像。這對於需要灰階影像的各種應用非常有用。

## 常見問題解答

### Q1：我可以將灰階影像儲存為其他格式嗎？

 A1: 是的，可以。只需更改`SaveFormat`中的參數`ImageSaveOptions`建構函數到您想要的格式。

### Q2：Aspose.Note 是否相容於所有版本的 OneNote 文件？

A2：Aspose.Note支援Microsoft OneNote 2010以上版本。

### Q3：Aspose.Note 需要許可證才能使用嗎？

A3：是的，您需要有效的許可證才能在生產環境中使用 Aspose.Note。但是，您可以獲得用於測試目的的臨時許可證。

### 問題 4：在將文件儲存為影像之前，我可以對其進行其他操作嗎？

A4：當然！ Aspose.Note 提供了多種以程式設計方式編輯 OneNote 文件的功能。

### Q5：如果遇到問題，我可以在哪裡尋求支援？

A5：您可以在 Aspose.Note 論壇上找到支持[這裡](https://forum.aspose.com/c/note/28).