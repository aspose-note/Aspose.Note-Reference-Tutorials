---
title: 將 OneNote 文件轉換為映像 - Java
linktitle: 將 OneNote 文件轉換為映像 - Java
second_title: Aspose.Note Java API
description: 學習使用 Aspose.Note for Java 將 OneNote 轉換為映像。按照簡單的步驟，載入文檔，初始化選項，然後另存為 PNG。
weight: 14
url: /zh-hant/java/onenote-document-loading/convert-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 OneNote 文件轉換為映像 - Java

## 介紹

在本教學中，我們將引導您完成使用 Aspose.Note for Java 將 OneNote 文件轉換為映像的過程。我們將把每個步驟分解為易於遵循的說明。

## 先決條件

在我們開始之前，請確保您具備以下條件：

1. 您的系統上安裝了 Java 開發工具包 (JDK)。
2.  Java 函式庫的 Aspose.Note。您可以從以下位置下載：[這裡](https://releases.aspose.com/note/java/).

## 導入包

首先，在 Java 程式碼中匯入必要的套件：

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

現在讓我們將提供的範例程式碼分解為多個步驟：

## 第 1 步：設定文檔目錄

定義 OneNote 文件所在的目錄：

```java
String dataDir = "Your Document Directory";
```

代替`"Your Document Directory"`以及 OneNote 文檔的路徑。

## 第 2 步：載入文檔

將 OneNote 文件載入到 Aspose.Note 中：

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

確保`"Sample1.one"`與您的 OneNote 文件的名稱相符。

## 步驟 3：初始化 ImageSaveOptions

初始化`ImageSaveOptions`物件指定保存格式：

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

在這裡，我們將文件儲存為 PNG 映像。如果需要，您可以選擇其他格式，例如 JPEG 或 BMP。

## 步驟 4：將文件另存為影像

將載入的文件儲存為圖片：

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

此行使用指定選項將文件另存為 PNG 映像。

## 步驟5：列印確認

列印一條訊息以確認文件已儲存：

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

此行通知您轉換成功以及已儲存的映像檔的位置。

## 結論

透過執行上述步驟，您可以使用 Aspose.Note for Java 輕鬆將 OneNote 文件轉換為映像。這是在 Java 應用程式中處理文件轉換的一種簡單而有效的方法。

## 常見問題解答

### Q1：我可以一次轉換多個 OneNote 文件嗎？

A1：是的，您可以循環遍歷文件清單並對每個文件執行轉換操作。

### Q2：Aspose.Note 是否支援除影像之外的其他輸出格式？

A2：是的，Aspose.Note 支援多種輸出格式，例如 PDF、HTML 和 Microsoft Word 格式。

### Q3：Aspose.Note 是否相容於所有版本的 OneNote 檔案？

A3：Aspose.Note 提供與在不同版本的 Microsoft OneNote 中建立的 OneNote 檔案的相容性。

### Q4：我可以自訂輸出影像的解析度嗎？

A4：是的，您可以使用Aspose.Note中的選項來調整解析度和其他參數。

### Q5：Aspose.Note 需要網路連線才能進行文件轉換嗎？

A5：不需要，Aspose.Note 在本地運行，無需網路連線。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
