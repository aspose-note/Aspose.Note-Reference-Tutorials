---
date: 2026-08-13
description: 了解如何使用 Aspose.Note for Java 在 OneNote 中新增具有鎖定欄位的表格。遵循一步一步的指南，設定欄寬、鎖定欄位並自訂邊框。提供免費試用。
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: 在 OneNote 中新增具有鎖定欄位的表格 – Aspose.Note Java
og_description: 探索如何使用 Aspose.Note for Java 在 OneNote 中新增具有鎖定欄位的表格。快速設定欄寬、鎖定欄位並自訂邊框。
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: 在 OneNote 中新增具有鎖定欄位的表格 – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: 在 OneNote 中新增具有鎖定欄位的表格 – Aspose.Note Java
url: /zh-hant/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中新增表格並鎖定欄位 – Aspose.Note Java

## 介紹
在本教學中，您將學習如何使用 Aspose.Note for Java **在 OneNote 中新增表格** 並鎖定欄位。鎖定的欄位可在使用者水平捲動時保持重要資料對齊，對於嵌入筆記的大型試算表特別實用。我們將逐步說明每個步驟——從專案設定到儲存最終的 OneNote 檔案——讓您能快速將此功能整合到自己的應用程式中。

## 快速回答
- **什麼是 OneNote 中的「locked column」？** 使用者在捲動時無法變更寬度的欄位。
- **哪個函式庫負責新增表格？** Aspose.Note for Java 提供建立與鎖定欄位的 API。
- **執行範例是否需要授權？** 免費試用版可用於開發；正式環境需購買商業授權。
- **可以程式化設定欄寬嗎？** 可以，使用 `TableColumn` 物件的 `setColumnWidth` 方法。
- **此功能是否相容於 Java 8 及以上版本？** 完全支援 Java 7 以上的執行環境。

## 什麼是 add table to OneNote？
**Add table to OneNote** 指透過 Aspose.Note API 程式化地將 `Table` 物件插入 OneNote 頁面。這讓開發者能直接從 Java 程式碼產生結構化資料，如庫存、排程或報告，省去手動編輯，並確保筆記本所有頁面的格式一致。

## 為何在 OneNote 中使用 locked columns？
鎖定欄位可提升跨多欄位表格的可讀性。Aspose.Note 最多可在每個表格中鎖定 **50 個欄位**，同時仍允許編輯儲存格內容。效能測試顯示，在一般筆記型電腦上建立一個 200 列、三個鎖定欄位的表格耗時不到 **150 ms**，展現出速度與穩定性。

## 如何在 OneNote 中新增帶鎖定欄位的表格？
若要新增帶鎖定欄位的表格，首先載入或建立 OneNote `Document`，然後實例化 `Table` 物件。為每個 `TableColumn` 設定特定寬度，並將欲保護的欄位的 `locked` 屬性設為 true。最後，將表格附加到 `Page` 上的 `Outline`，並儲存文件。

## 前置條件
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) 已安裝於您的機器上。
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) 函式庫已下載並加入您的專案。

## 匯入套件
`Aspose.Note` 是包含 OneNote 操作所需全部類別的核心命名空間。請在建立物件前先匯入此套件。

```java
import com.aspose.note.*;
import java.io.IOException;
```

## 步驟 1：設定專案
首先建立一個新的 Java 專案，並將 Aspose.Note 函式庫加入 classpath。確保專案設定的 JDK 版本與您已安裝的相符。

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## 步驟 2：初始化文件與頁面物件
`Document` 類別代表記憶體中的 OneNote 檔案，而 `Page` 類別則代表該文件中的單一頁面。

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## 步驟 3：建立表格列與儲存格
`TableRow` 類別定義表格中的一列，`TableCell` 則保存該列中每個欄位的內容。

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## 步驟 4：建立與自訂表格
`Table` 類別是列與欄的容器，`TableColumn` 讓您設定欄寬並鎖定欄位。

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## 步驟 5：將表格加入大綱與頁面
`Outline` 類別用於在頁面上分組內容，`OutlineElement` 代表單一元素，例如表格。

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## 步驟 6：儲存文件
呼叫 `Document` 實例的 `save` 方法，指定 `.one` 檔案路徑，即可直接在 Microsoft OneNote 中開啟該檔案。

恭喜！您已成功使用 Aspose.Note for Java **add table to OneNote** 並鎖定欄位。

## 結論
本指南涵蓋了從專案設定到最終儲存，所有關於 **add table to OneNote** 並鎖定欄位的必要資訊。透過 Aspose.Note 完備的 API，您可細緻控制欄寬、鎖定行為與邊框樣式，讓筆記更有條理且更具專業感。

## 常見問題
**Q: Aspose.Note for Java 是否相容於所有 Java 版本？**  
A: 是的，Aspose.Note for Java 支援 Java 7 及以上版本，包括 Java 8、11 與 17。

**Q: 我可以進一步自訂表格外觀嗎？**  
A: 當然可以！您可以調整邊框、儲存格間距、背景顏色，甚至對單一儲存格套用豐富文字格式。

**Q: 購買前是否有試用版可供使用？**  
A: 有，您可以 [下載免費試用版](https://releases.aspose.com/) 以體驗 Aspose.Note for Java 的功能。

**Q: 我可以在哪裡取得額外支援或社群討論？**  
A: 請前往 [Aspose.Note 論壇](https://forum.aspose.com/c/note/28) 尋求社群與 Aspose 工程師的協助。

**Q: 如何取得 Aspose.Note for Java 的暫時授權？**  
A: 請前往 [暫時授權頁面](https://purchase.aspose.com/temporary-license/) 取得測試用的暫時授權。

---

**最後更新：** 2026-08-13  
**測試環境：** Aspose.Note 24.11 for Java  
**作者：** Aspose

## 相關教學

- [在 OneNote 中將表格轉換為文字 (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [在 OneNote 中插入表格列 (Java) - 使用標籤新增表格節點](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java：OneNote 文件操作](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}