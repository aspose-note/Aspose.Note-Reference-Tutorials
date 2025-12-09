---
date: 2025-12-02
description: 學習如何使用 Aspose.Note for Java 在 Java 中建立帶有標題的 OneNote 頁面。本指南展示如何設定 OneNote
  頁面的標題以及自訂標題字型。
linktitle: How to Create OneNote Page with Title - Java
second_title: Aspose.Note Java API
title: 如何使用 Java 建立帶標題的 OneNote 頁面
url: /zh-hant/java/onenote-document-loading/create-onenote-doc-page-title/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Java 建立 OneNote 頁面標題

## 介紹

如果您需要 **以程式方式建立 OneNote 頁面**，Aspose.Note for Java 讓這件事變得相當簡單。於本教學中，您將學會如何產生 OneNote 檔案、設定頁面標題，甚至自訂標題的字型——全部透過 Java 程式碼完成。完成後，您將擁有一個可直接在任何 Java 應用程式中使用的 OneNote 文件。

## 快速回答
- **需要哪個函式庫？** Aspose.Note for Java。  
- **可以自訂標題字型嗎？** 可以——使用 `ParagraphStyle` 來定義字型名稱、大小與顏色。  
- **支援哪個 Java 版本？** 任意 JDK 8 以上（API 向下相容）。  
- **開發時需要授權嗎？** 免費試用版可用於測試；正式上線需購買授權。  
- **輸出檔案儲存在哪裡？** 由 `dataDir` 變數自行定義路徑。

## 什麼是一頁 OneNote 的標題？
OneNote 頁面標題是顯示在每頁頂部的標頭，通常包含頁面名稱、建立日期與時間。以程式方式設定此標題，可協助您建立結構一致、條理分明的筆記本。

## 為什麼要以程式方式設定 OneNote 頁面標題？
- **自動化：** 產生報告或會議記錄時無需手動編輯。  
- **一致性：** 在所有頁面上強制執行命名規則。  
- **整合性：** 可將 OneNote 與其他系統（如 CRM、專案管理工具）結合。

## 前置作業

- **Java Development Kit (JDK)** – 版本 8 或以上。  
- **Aspose.Note for Java** – 從官方網站 **[此處](https://releases.aspose.com/note/java/)** 下載。  
- **IDE** – IntelliJ IDEA、Eclipse 或 NetBeans（自行選擇）。

## 匯入套件

首先，匯入 Aspose.Note 函式庫中所需的類別。

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

### 步驟 1：設定文件目錄  
定義產生的 OneNote 檔案要儲存的位置。

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

### 步驟 2：建立 Document 物件  
實例化新的 `Document`——這代表您即將建立的 OneNote 檔案。

```java
// Create an object of the Document class
Document doc = new Document();
```

### 步驟 3：初始化 Page 物件  
建立一個 `Page` 物件，用來放置標題與其他內容。

```java
// Initialize Page class object
Page page = new Page();
```

### 步驟 4：設定預設文字樣式  
定義一個預設的 `ParagraphStyle`，將套用於標題文字。這裡就是 **自訂 OneNote 標題字型** 的地方。

```java
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

### 步驟 5：設定頁面標題屬性  
在此 **設定 OneNote 頁面標題** 的細節——標題文字、日期與時間。可依需求自行修改字串內容。

```java
// Set page title properties
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

### 步驟 6：將標題指派給頁面  
現在我們 **將標題加入 OneNote**，透過把 `Title` 物件與 `Page` 連結。

```java
page.setTitle(title);
```

### 步驟 7：將頁面加入文件  
把已設定好的頁面加入文件結構中。

```java
doc.appendChildLast(page);
```

### 步驟 8：儲存 OneNote 文件  
指定輸出檔名並儲存筆記本。至此 **java 建立 onenote 檔案** 的流程完成。

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// Save OneNote document
doc.save(dataDir);
```

## 常見問題與技巧

| 問題 | 解決方案 |
|------|----------|
| **檔案路徑無效** | 確認 `dataDir` 以正確的分隔符 (`/` 或 `\\`) 結尾，且資料夾已存在。 |
| **標題未顯示** | 檢查 `ParagraphStyle` 是否已套用至每個 `RichText` 元素。 |
| **授權例外** | 測試時使用試用授權；正式部署前請套用正式授權。 |
| **日期顯示錯誤月份** | Java 的月份是從 0 開始計算；`cal.set(2018, 04, 03)` 其實設定的是 5 月，請自行調整。 |

## 常見問答

**Q: Aspose.Note for Java 是否相容不同的 Java 版本？**  
A: 是的，函式庫支援 Java 8 以上，讓您在各種環境中都能使用。

**Q: 我可以自訂頁面標題的字型樣式與大小嗎？**  
A: 當然可以！如步驟 4 所示，使用 `ParagraphStyle` 即可設定任意字型名稱、大小與顏色。

**Q: 要如何在頁面上加入更多內容（例如段落、圖片）？**  
A: 建立額外的 `RichText` 或 `Image` 物件，設定樣式後以 `page.appendChildLast(yourObject)` 加入 `Page`。

**Q: 是否有 Aspose.Note for Java 的試用版？**  
A: 有，您可從 Aspose 官方網站下載免費試用版，以評估所有功能。

**Q: 若遇到問題，該向哪裡尋求支援？**  
A: 前往 [Aspose.Note 論壇](https://forum.aspose.com/c/note/28) 取得社群協助，或向 Aspose 提交支援票。

---

**最後更新：** 2025-12-02  
**測試環境：** Aspose.Note for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}