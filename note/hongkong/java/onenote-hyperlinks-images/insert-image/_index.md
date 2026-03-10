---
date: 2025-12-21
description: 學習如何使用 Java 及 Aspose.Note for Java 為 OneNote 文件加入圖片。跟隨我們的逐步指南插入圖片，並可選擇將
  OneNote 另存為 PDF。
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: 如何使用 Java 向 OneNote 添加圖片
url: /zh-hant/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 文件中使用 Java 插入圖片

## 簡介

在本教學中，我們將探討如何使用 Java 以及 Aspose.Note for Java 在 OneNote 文件中插入圖片。Aspose.Note for Java 是一個功能強大的程式庫，允許開發人員以程式方式操作 Microsoft OneNote 檔案，支援建立、讀取及操作 OneNote 文件等各種功能。

## 快速解答
- **使用 Java 向 OneNote 添加圖片的最簡單方法是什麼？**  
  使用 Aspose.Note for Java 的 `Image` 類別並將其附加到頁面上。
- **在正式環境使用是否需要授權？**  
  是的，正式部署需要商業授權。
- **我可以為圖片設定自訂尺寸嗎？**  
  當然可以——對 `Image` 物件呼叫 `setWidth()` 與 `setHeight()`。
- **在加入圖片後，能否將 OneNote 檔案另存為 PDF？**  
  可以，呼叫 `save(..., SaveFormat.Pdf)` 即可 **將 OneNote 另存為 PDF**。
- **支援哪個版本的 Java？**  
  Aspose.Note for Java 支援 JDK 8 及以上版本。

## 如何使用 Java 向 OneNote 添加圖片？

在深入程式碼之前，我們先簡要說明為何需要以程式方式在 OneNote 中嵌入圖片。無論是產生會議記錄、製作自動化報告，或是建構文件流程，插入圖片都能為筆記提供純文字無法呈現的視覺資訊。使用 Aspose.Note for Java，您可完全在程式碼中完成此操作，無需開啟 OneNote 使用者介面。

## 先決條件

在開始之前，請確保已完成以下先決條件的設定：

### 1. Java Development Kit (JDK)

確保您的系統已安裝 Java Development Kit（JDK）。您可從 Oracle 官方網站下載並安裝 JDK。

### 2. Aspose.Note for Java 程式庫

依照[文件說明](https://reference.aspose.com/note/java/)下載並設定 Aspose.Note for Java 程式庫。

## 匯入套件

首先在 Java 專案中匯入必要的套件。這些套件包括 Aspose.Note 程式庫及其他所需的相依性。

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

讓我們將在 OneNote 文件中插入圖片的過程分解為多個步驟：

## 步驟 1：載入 OneNote 文件

首先，載入您欲插入圖片的 OneNote 文件。

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## 步驟 2：取得頁面

取得文件中您想要插入圖片的頁面。

```java
Page page = oneFile.getFirstChild();
```

## 步驟 3：載入圖片

載入您想要插入至 OneNote 文件的圖片。

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## 步驟 4：自訂圖片屬性（可選）

您也可以依需求自訂圖片的大小、位置與對齊方式。這裡即是以 **Java 方式設定圖片尺寸** 的地方。

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## 步驟 5：將圖片加入頁面

將圖片加入 OneNote 文件的頁面中。

```java
page.appendChildLast(image);
```

## 步驟 6：儲存文件

儲存已修改的文件，包含插入的圖片。您亦可在此階段 **將 OneNote 另存為 PDF**。

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## 結論

在本教學中，我們學會了如何使用 Java 以及 Aspose.Note for Java 程式庫在 OneNote 文件中插入圖片。依循此步驟指南，即可輕鬆以程式方式將圖片納入 OneNote 文件中。

## 常見問題

### Q1：我可以使用此方法在單一 OneNote 文件中插入多張圖片嗎？

A1：可以，您只需對每張圖片重複本教學中說明的步驟，即可在同一 OneNote 文件中插入多張圖片。

### Q2：Aspose.Note for Java 是否相容於所有版本的 OneNote？

A2：Aspose.Note for Java 支援處理 Microsoft OneNote 2010 及之後版本所建立的 OneNote 檔案。

### Q3：我可以在 OneNote 文件中插入不同格式的圖片，例如 PNG 或 GIF 嗎？

A3：可以，Aspose.Note for Java 支援插入多種格式的圖片，包括 PNG、JPEG、GIF 等。

### Q4：是否提供 Aspose.Note for Java 的試用版供測試？

A4：可以，您可從官方網站下載 Aspose.Note for Java 的免費試用版以進行評估。

### Q5：如何取得 Aspose.Note for Java 的技術支援？

A5：您可前往專屬於 Aspose.Note 產品的[論壇](https://forum.aspose.com/c/note/28)取得技術支援。

---

**最後更新：** 2025-12-21  
**測試環境：** Aspose.Note for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}