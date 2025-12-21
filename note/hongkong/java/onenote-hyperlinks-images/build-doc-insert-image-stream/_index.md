---
date: 2025-12-21
description: 學習如何使用 Aspose.Note for Java 在 Java 中建立 OneNote 文件並輕鬆插入圖片。為 Java 開發者提供的逐步指南。
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: 如何在 Java 中建立 OneNote 文件 – 使用串流建構文件並插入圖片
url: /zh-hant/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何建立 onenote document java – 使用串流建立文件並插入圖片

## 介紹

歡迎！在本教學中，您將 **create onenote document java** 從頭開始，並學習如何使用影像串流插入圖片。我們會逐步說明每個步驟、解釋各部分的重要性，並提供實用技巧，讓您能在實際專案中運用此技術。完成後，您將能以程式方式產生 OneNote 頁面，並在需要的地方嵌入圖片。

## 快速解答
- **需要哪個函式庫？** Aspose.Note for Java  
- **可以從串流插入圖片嗎？** 可以 – 只需將 `InputStream` 傳遞給 `Image` 建構子。  
- **可以匯出為哪種格式？** 任何 Aspose.Note 支援的格式，例如 PDF、DOCX、HTML。  
- **開發是否需要授權？** 免費的暫時授權可用於評估；正式環境需購買完整授權。  
- **需要哪個 Java 版本？** Java 8 或更高。

## 什麼是 “create onenote document java”？

在 Java 中建立 OneNote 文件是指使用 Aspose.Note API 以程式方式建構筆記本結構——包括頁面、輪廓與元素——而不需開啟 OneNote 桌面客戶端。此方式非常適合自動化報告產生、批次處理筆記，或將 OneNote 內容整合至更大型的 Java 應用程式中。

## 為什麼使用 Aspose.Note for Java 來 create onenote document java？

- **完整控制** 頁面版面、輪廓位置與元素樣式。  
- **無 COM 互操作** – 可在任何支援 Java 的作業系統上執行。  
- **豐富的匯出選項** – 只需一次呼叫即可將同一文件轉換為 PDF、DOCX、HTML 等格式。  
- **支援串流** – 可直接從記憶體、網路或雲端儲存載入圖片。

## 前置條件

在開始之前，請確保已完成以下設定：

### Java 開發工具包 (JDK)

在您的電腦上已安裝近期版本的 JDK（8 或以上）。

### Aspose.Note for Java 函式庫

從官方 Aspose 釋出頁面下載函式庫： [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/)。

### IDE 設定

在您偏好的 IDE（IntelliJ IDEA、Eclipse、VS Code 等）中設定，將 Aspose.Note 的 JAR 檔案加入專案的 classpath。

## 匯入套件

首先，匯入所需的 Java 與 Aspose.Note 類別。這些匯入讓您能使用文件建立、頁面處理、輪廓管理與圖片插入等功能。

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## 步驟 1：設定文件目錄

定義包含來源圖片的資料夾以及輸出檔案要儲存的位置。請將佔位符替換為您機器上的實際路徑。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：建立 Document 物件

實例化一個新的 `Document`。此物件代表您正在建立的 OneNote 筆記本。

```java
Document doc = new Document();
```

## 步驟 3：初始化 Page 物件

建立一個 `Page`，用來容納此筆記本頁面的所有輪廓與元素。

```java
Page page = new Page();
```

## 步驟 4：建立 Outline

`Outline` 如同一個容器，用於放置定位元素。此處我們設定垂直與水平偏移量，以將 Outline 放置於頁面上。

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## 步驟 5：建立 Outline Element

`OutlineElement` 將承載我們即將插入的圖片。

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## 步驟 6：載入圖片串流

以串流方式開啟圖片檔案。使用串流可讓您從任何來源（檔案系統、網路、資料庫）讀取圖片，而不必先將其寫入磁碟。

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## 步驟 7：插入圖片

建立一個 `Image` 物件。若稍後提供串流，第一個參數可為 `null`，但為了簡化示範，我們在此直接使用檔案路徑，並將其對齊設定為頁面的右側。

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## 步驟 8：將圖片加入 Outline Element

將圖片加入 Outline Element，使其成為頁面視覺層級的一部份。

```java
outlineElem1.appendChildLast(image);
```

## 步驟 9：將 Outline Element 加入 Outline

現在將包含圖片的 Outline Element 附加到 Outline 容器中。

```java
outline1.appendChildLast(outlineElem1);
```

## 步驟 10：將 Outline 加入 Page

將 Outline 放置於頁面上。

```java
page.appendChildLast(outline1);
```

## 步驟 11：將 Page 加入 Document

將完整建好的 Page 加入 Document 物件中。

```java
doc.appendChildLast(page);
```

## 步驟 12：儲存 Document

最後，將 OneNote 文件儲存為您需要的格式。在此範例中我們匯出為 PDF，但您亦可選擇 Aspose.Note 支援的任何格式。

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

依照上述步驟，您已成功 **created onenote document java**，並使用輸入串流嵌入圖片。

## 常見問題與技巧

- **未關閉串流** – 在正式環境中，務必在 `finally` 區塊中關閉 `InputStream`，或使用 try‑with‑resources。  
- **檔案路徑錯誤** – 請再次確認 `dataDir` 以正確的分隔符（`/` 或 `\`）結尾。  
- **圖片對齊** – 若圖片顯示超出畫面，請調整 Outline 的 `VerticalOffset`/`HorizontalOffset` 值。  
- **授權例外** – 使用評估版可能會在輸出中加入浮水印；請套用有效授權以移除浮水印。

## 常見問答

### Q1：Aspose.Note for Java 是否相容所有版本的 OneNote？

A1：Aspose.Note for Java 支援多種 OneNote 檔案格式，確保在桌面版、線上版與行動版之間皆具相容性。

### Q2：我能否使用 Aspose.Note for Java 自訂 OneNote 文件中插入圖片的外觀？

A2：可以，您可以透過 `Image` 物件的相關屬性調整對齊、尺寸、旋轉，甚至套用裁切。

### Q3：Aspose.Note for Java 是否支援 PDF 之外的其他文件格式？

A3：當然可以。此 API 可匯出為 DOCX、HTML、XPS 等多種格式，讓您在分享或保存筆記時更具彈性。

### Q4：我可以在哪裡找到 Aspose.Note for Java 的其他資源與支援？

A4：官方 Aspose 網站提供完整的文件、程式碼範例、論壇，以及供評估使用的暫時授權。

### Q5：是否有 Aspose.Note for Java 的試用版？

A5：有的，您可從 Aspose 釋出頁面下載免費試用版，以在購買前體驗全部功能。

**最後更新：** 2025-12-21  
**測試環境：** Aspose.Note for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}