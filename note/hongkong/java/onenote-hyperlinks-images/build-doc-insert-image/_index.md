---
date: 2025-12-20
description: 學習如何使用 Aspose.Note for Java 為 OneNote 添加相片。一步一步的指南，教您以程式方式建立 OneNote
  文件並插入圖像。
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: 如何使用 Java 向 OneNote 添加圖片 – 建立文件並插入圖片
url: /zh-hant/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Java 向 OneNote 添加圖片 – 建立文件並插入圖像

## 簡介

在本教學中，您將學習如何使用 Aspose.Note Java API **向 OneNote 添加圖片**。我們將一步步示範如何從頭建立 OneNote 文件、插入圖像，並將結果儲存為 PDF。無論您是要建構報表工具、自動化筆記，或僅需以程式方式嵌入圖形，本指南都提供清晰、實作的步驟。

## 快速問答

- **需要哪個函式庫？** Aspose.Note for Java.  
- **可以插入任何圖像格式嗎？** 支援 JPEG、PNG、BMP、GIF 等多種格式。  
- **有哪些輸出格式可用？** 您可以儲存為 OneNote、PDF、XPS、HTML 等。  
- **正式環境需要授權嗎？** 是的，非試用使用必須購買商業授權。  
- **程式碼是否跨平台？** 當然 – Java 可在 Windows、Linux 與 macOS 上執行。

## 什麼是「向 OneNote 添加圖片」？

向 OneNote 添加圖片是指以程式方式將圖像檔嵌入 OneNote 頁面，使其與文字、大綱或其他元素一起顯示。Aspose.Note API 抽象化了 OneNote 檔案格式，讓您專注於內容本身，而不必處理底層的 XML 結構。

## 為什麼使用 Java 向 OneNote 添加圖片？

- **自動化：** 自動產生帶有螢幕截圖的會議記錄。  
- **一致性：** 確保每頁皆遵循相同的版面與品牌風格。  
- **整合性：** 可直接將其他系統的資料（例如圖表）合併至 OneNote 筆記本。  
- **跨平台：** Java 讓您在任何伺服器或桌面環境上執行相同程式碼。

## 先決條件

在開始之前，請確保您已具備以下項目：

1. **Java Development Kit (JDK)** – 任意近期版本（8 或以上）。  
2. **Aspose.Note for Java 函式庫** – 從[網站](https://releases.aspose.com/note/java/)下載。  
3. **IDE** – IntelliJ IDEA、Eclipse，或您偏好的任何 Java 相容編輯器。

## 匯入套件

開始在您的 Java 原始檔案中匯入必要的類別：

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## 步驟說明

### 步驟 1：設定文件

建立一個全新的 OneNote 文件與頁面容器，以放置內容。

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### 步驟 2：初始化大綱

*大綱* 如同容器，用於放置文字與圖像等元素。我們將其偏移量設為 0，使內容從左上角開始。

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### 步驟 3：載入並對齊圖像

載入欲嵌入的圖片，並將其對齊至頁面的右側。這就是實際 **向 OneNote 添加圖片** 的地方。

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### 步驟 4：將圖像附加至大綱元素

將圖像包裹在 `OutlineElement` 中。此步驟將視覺物件與文件的大綱層級結合。

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### 步驟 5：組合文件結構

將大綱元素加入大綱，接著將大綱附加至頁面，最後將頁面加入文件。

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### 步驟 6：儲存 OneNote 文件

將文件寫入磁碟。本範例匯出為 PDF，但您也可以透過變更 `SaveFormat`，將其儲存為原生 OneNote 檔案（`.one`）。

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## 常見問題與解決方案

| 問題 | 發生原因 | 解決方法 |
|------|----------|----------|
| **圖片未顯示** | 檔案路徑錯誤或格式不支援。 | 確認 `dataDir` 指向正確的資料夾，並使用支援的圖像類型（JPEG、PNG 等）。 |
| **文件儲存為空白 PDF** | 大綱偏移量設定不正確。 | 確保已呼叫 `setVerticalOffset(0)` 與 `setHorizontalOffset(0)`，或調整偏移量以將內容放置於頁面範圍內。 |
| **儲存時發生 IOException** | 目標資料夾不存在或缺乏寫入權限。 | 事先建立資料夾，或以具備相應權限的方式執行程式。 |

## 常見問答

**Q1：在哪裡可以找到 Aspose.Note for Java 的文件說明？**  
A1：您可在[此處](https://reference.aspose.com/note/java/)取得文件說明。

**Q2：如何下載 Aspose.Note for Java？**  
A2：您可從[下載頁面](https://releases.aspose.com/note/java/)下載 Aspose.Note for Java。

**Q3：Aspose.Note for Java 是否提供免費試用？**  
A3：是的，您可從[網站](https://releases.aspose.com/)取得免費試用。

**Q4：在哪裡可以取得 Aspose.Note for Java 的支援？**  
A4：請前往 [Aspose.Note 論壇](https://forum.aspose.com/c/note/28)取得支援。

**Q5：我可以取得 Aspose.Note for Java 的臨時授權嗎？**  
A5：可以，您可在[此處](https://purchase.aspose.com/temporary-license/)申請臨時授權。

---

**最後更新：** 2025-12-20  
**測試環境：** Aspose.Note for Java 24.12（最新）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}