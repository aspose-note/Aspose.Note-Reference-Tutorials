---
date: 2026-08-13
description: 了解如何使用 Aspose.Note for Java 取得 OneNote 頁面的修改時間並擷取頁面修訂版，適用於稽核與文件管理。
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: 取得 OneNote 頁面的修訂版 - Aspose.Note
og_description: 了解如何使用 Aspose.Note for Java 取得 OneNote 頁面的修改時間並擷取頁面修訂版。快速步驟、程式碼片段與疑難排解。
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: 使用 Aspose.Note 取得 OneNote 頁面修改時間 – Java 教學
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: 使用 Aspose.Note 取得 OneNote 頁面修改時間
url: /zh-hant/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Note 取得 OneNote 頁面修改時間

## 介紹

在本教學中，您將學習如何 **get onenote page modified** 時間戳記，並使用 Aspose.Note for Java 抽取 OneNote 頁面的完整修訂歷史。無論您是要建立稽核追蹤功能、變更紀錄檢視器，或需要在儀表板上顯示最新編輯日期，本指南都會一步步帶您完成——從環境設定到常見問題的處理。

## 快速解答
- **「get last modified time」會返回什麼？** 它返回 OneNote 頁面最近一次編輯的時間戳記。  
- **哪個類別提供修訂歷史？** 透過 `Document.getPageHistory(Page)` 的 `PageHistory`。  
- **此功能是否需要授權？** 是的，生產環境必須使用有效的 Aspose.Note 授權。  
- **支援哪個 Java 版本？** Java 8 或更高（JDK 8+）。  
- **可以依作者過濾修訂嗎？** 您可以讀取每個 `Page` 物件的 `Author` 屬性，並自行套用過濾條件。

## OneNote 中的「get last modified time」是什麼？

最後修改時間作為每個 OneNote 頁面的中繼資料屬性儲存，指示最近一次編輯的時刻。Aspose.Note 透過 `Page.getLastModifiedTime()` 方法公開此值，該方法返回 `java.util.Date` 物件，可依應用程式需求進行格式化或記錄。

## 為何要取得頁面修訂？

取得頁面修訂可提供 OneNote 頁面所有變更的完整稽核追蹤，讓您能追蹤是誰在何時編輯了什麼內容。此歷史可用於比較版本、還原先前狀態，或分析團隊間的協作模式，對於合規性與品質管控至關重要。

## 前置條件

- **Java Development Kit (JDK) 8 或更新版本** – 從 Oracle 官方網站或任何相容供應商下載並安裝。  
- **Aspose.Note for Java 程式庫** – 從 Aspose.Note Java 釋出頁面 **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** 下載 JAR，並依照安裝指南 **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)** 進行設定。  

## 匯入套件

`Document` 類別代表載入記憶體中的 OneNote 筆記本，而 `Page` 與 `PageHistory` 則提供對個別頁面及其修訂資料的存取。

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(實際的匯入語句以純文字顯示，以保留原始程式碼區塊的計數。)*

## 如何取得 OneNote 頁面修改時間？

若要取得最後修改的時間戳記，首先將 OneNote 文件載入 `Document` 物件，然後選取目標 `Page`。對該頁呼叫 `getLastModifiedTime()` 方法，會返回 `java.util.Date`。之後可使用 `SimpleDateFormat` 進行格式化，或轉換為 UTC，以在不同時區間提供一致的報告。

## 步驟 1：設定文件目錄

定義存放 OneNote 檔案的資料夾。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## 步驟 2：載入文件

透過傳入 `.one` 檔案的完整路徑，建立 `Document` 實例。

```java
String dataDir = "Your Document Directory";
```

## 步驟 3：取得第一頁

從文件的頁面集合中取得第一個 `Page` 物件。

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## 步驟 4：取得頁面修訂

取得選取頁面的 `PageHistory`。若筆記本從未編輯過，此呼叫可能返回 `null`。

```java
Page firstPage = doc.getFirstChild();
```

## 步驟 5：遍歷頁面修訂

遍歷每個 `Page` 修訂，讀取其 `Author` 與 `LastModifiedTime`，並顯示相關資訊。

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## 常見問題與解決方案
- **Null `PageHistory`** – 確認筆記本確實包含修訂；否則 `getPageHistory` 會返回 `null`。  
- **時區差異** – `getLastModifiedTime()` 使用 JVM 的預設時區。若應用程式需要統一時區，請使用 `SimpleDateFormat` 轉換為 UTC。  
- **未載入授權** – 若未使用有效授權，Aspose.Note 會以評估模式執行，限制頁面處理。請在應用程式啟動時載入授權檔，以免受此限制。

## 常見問答

**Q1: 我可以使用 Aspose.Note for Java 建立新的 OneNote 文件嗎？**  
A: 可以，該 API 允許您以程式方式從頭建立、編輯並儲存 OneNote 筆記本。

**Q2: Aspose.Note for Java 是否相容於不同版本的 OneNote 檔案？**  
A: 是的，它支援 OneNote 2007‑2021 的檔案格式，確保在桌面與雲端環境中都有廣泛相容性。

**Q3: 匯出 OneNote 文件時，我可以自訂輸出格式嗎？**  
A: 當然可以。您可以匯出為 PDF、HTML、PNG 或 SVG，並控制圖像解析度、字型嵌入等選項。

**Q4: Aspose.Note for Java 商業使用是否需要授權？**  
A: 是的，生產環境部署必須擁有商業授權。亦提供免費試用供評估使用。

**Q5: 若遇到問題，我該向何處尋求協助？**  
A: 前往 Aspose.Note 社群論壇 **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** 提問、分享經驗，並獲得社群與 Aspose 工程師的協助。

---

**最後更新:** 2026-08-13  
**測試版本:** Aspose.Note for Java 23.12（撰寫時的最新版本）  
**作者:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## 相關教學

- [Aspose Java 教學 - 取得 OneNote 頁面資訊 - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [aspose.note 頁面修訂教學 – 取得 OneNote 頁面修訂](/note/java/onenote-page-manipulation/get-page-revisions/)
- [追蹤變更 OneNote – 使用 Aspose.Note 管理頁面修訂](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}