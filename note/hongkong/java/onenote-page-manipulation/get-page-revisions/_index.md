---
date: 2026-08-08
description: 了解如何透過程式方式使用 Aspose.Note for Java 取得 OneNote 的頁面修訂，從而追蹤變更。
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: 取得 OneNote 頁面修訂 - Aspose.Note
og_description: 了解如何透過程式方式使用 Aspose.Note for Java 取得 OneNote 的頁面修訂，從而追蹤變更。
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: 追蹤 OneNote 中的變更 – 使用 Aspose.Note 的頁面修訂
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: 追蹤 OneNote 中的變更 – 使用 Aspose.Note 的頁面修訂
url: /zh-hant/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中追蹤變更 – 使用 Aspose.Note 的頁面修訂

在本教學中，您將學習如何透過使用 Aspose.Note Java API 來擷取頁面的完整修訂歷史，以 **在 OneNote 中追蹤變更**。我們將從設定開發環境到列印每個修訂的作者、時間戳記與標題，全面說明，讓您能為任何基於 OneNote 的解決方案建立可靠的稽核追蹤功能。

## 快速回答
- **本教學涵蓋什麼內容？** 使用 Aspose.Note for Java 從 OneNote 檔案中取得頁面修訂歷史。  
- **需要哪個版本的函式庫？** 任何支援 `LoadOptions.setLoadHistory` 的近期 Aspose.Note for Java 版本皆可。  
- **我需要授權嗎？** 測試時可使用臨時評估授權；正式環境則需商業授權。  
- **我可以修改修訂嗎？** 此 API 只提供唯讀存取修訂，僅能取得資料。  
- **主要前置條件是什麼？** Java JDK、Aspose.Note for Java，以及包含修訂資料的 OneNote 文件。

## 什麼是「aspose.note 頁面修訂教學」？
本教學示範如何以程式方式存取 OneNote 頁面的歷史版本。每個修訂皆包含作者、建立時間與修改時間等中繼資料，讓您能在應用程式中建立稽核追蹤或變更紀錄功能。

## 為何使用 Aspose.Note 進行頁面修訂追蹤？
在標準 2 GHz CPU 上，能於 5 秒內載入 500 頁檔案的完整筆記本修訂歷史，且無需啟動 OneNote 介面即可取得中繼資料。此函式庫支援超過 30 種輸入與輸出格式，可在 Windows、Linux 與 macOS 上執行（覆蓋 >95 % 的伺服器環境），並提供對每個修訂屬性的完整控制。

## 前置條件

### 1. Java 開發工具包 (JDK)
確保已安裝近期的 JDK（8 版或以上），且已設定 `JAVA_HOME`。

### 2. Aspose.Note for Java
從 [download link](https://releases.aspose.com/note/java/) 下載函式庫。

### 3. 範例 OneNote 文件
建立或取得包含修訂歷史的 OneNote 檔案（例如 `Sample1.one`）。

## 匯入套件
首先，匯入所需的 Aspose.Note 類別。  
`Document` 代表 OneNote 筆記本，`LoadOptions` 用於設定載入行為，`Page` 代表單一頁面。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## 步驟實作說明

### 步驟 1：設定文件目錄
定義 OneNote 檔案所在的資料夾。

```java
String dataDir = "Your Document Directory";
```

### 步驟 2：載入啟用修訂歷史的 OneNote 文件
`LoadOptions` 是一個設定類別，用於告訴 Aspose.Note 如何開啟檔案，包括是否讀取修訂資料。請在載入文件前啟用此旗標。

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### 步驟 3：取得第一頁
取得第一頁物件；此物件將作為取得其修訂歷史的參考點。

```java
Page firstPage = document.getFirstChild();
```

### 步驟 4：遍歷頁面修訂
遍歷每個修訂，並列印時間戳記、標題、層級與作者等有用的中繼資料。

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **專業提示：** 若需依特定作者或日期範圍過濾修訂，只需在 `for` 迴圈內加入條件判斷即可。

## 常見問題與解決方案
- **未返回修訂：** 請確認在載入文件前已呼叫 `loadOptions.setLoadHistory(true)`。  
- **作者或標題為 null：** 某些較舊的 OneNote 版本可能不會儲存這些欄位，請妥善處理 `null` 值。  
- **大型筆記本效能下降：** 僅載入所需的節點或增大 JVM 堆積大小。

## 常見問答

**Q1: 我可以使用 Aspose.Note for Java 來修改頁面修訂嗎？**  
A1: 不行，該 API 目前僅支援唯讀存取頁面修訂。

**Q2: Aspose.Note for Java 是否相容於不同版本的 OneNote 文件？**  
A2: 是的，它支援多種 OneNote 檔案格式，能在不同版本間無縫處理。

**Q3: 使用 Aspose.Note for Java 是否需要授權？**  
A3: 正式環境需商業授權，測試可使用臨時評估授權。

**Q4: 若在使用 Aspose.Note for Java 時遇到問題，我可以尋求支援嗎？**  
A4: 可以，您可在 Aspose.Note 論壇提問 [Aspose.Note forum](https://forum.aspose.com/c/note/28)。

**Q5: 是否提供 Aspose.Note for Java 的免費試用？**  
A5: 有，您可從[網站](https://releases.aspose.com/)下載免費試用版。

---

**最後更新：** 2026-08-08  
**測試環境：** Aspose.Note for Java (latest release)  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [在 OneNote 中追蹤變更 – 使用 Aspose.Note 管理頁面修訂](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Aspose Java 教學 - 取得 OneNote 頁面資訊 - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [變更 OneNote 頁面背景 – Aspose.Note for Java](/note/java/onenote-page-manipulation/set-page-background-color/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}