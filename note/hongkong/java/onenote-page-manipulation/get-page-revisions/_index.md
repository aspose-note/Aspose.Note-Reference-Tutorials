---
title: 在 OneNote 中取得頁面修訂 - Aspose.Note
linktitle: 在 OneNote 中取得頁面修訂 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 在 OneNote 中擷取頁面修訂。請遵循我們的逐步指南，以有效追蹤變更。
type: docs
weight: 14
url: /zh-hant/java/onenote-page-manipulation/get-page-revisions/
---
## 介紹

OneNote 是用於組織和管理筆記的強大工具，但有時您需要追蹤頁面所做的變更和修訂。使用 Aspose.Note for Java，您可以輕鬆地以程式設計方式檢索頁面修訂。在本教學中，我們將引導您完成使用 Aspose.Note for Java 在 OneNote 中取得頁面修訂的過程。

## 先決條件

在我們開始之前，請確保您具備以下先決條件：

### 1.Java開發工具包（JDK）

確保您的系統上安裝了 Java 開發工具包 (JDK)。您可以從 Oracle 網站下載並安裝 JDK。

### 2.Java 版 Aspose.Note

從以下地址下載並安裝 Aspose.Note for Java[下載連結](https://releases.aspose.com/note/java/).

### 3. OneNote 文件範例

準備一個範例 OneNote 文件（`Sample1.one`），其中包含您要從中檢索修訂的頁面。

## 導入包

首先，您需要從 Aspose.Note for Java 匯入必要的套件。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

現在，讓我們將提供的範例分解為多個步驟：

## 第 1 步：設定文檔目錄

定義 OneNote 文件所在的目錄路徑。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：載入 OneNote 文檔

使用載入 OneNote 文檔`LoadOptions`啟用載入歷史記錄。

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## 第 3 步：取得首頁

從已載入的文檔中檢索第一頁。

```java
Page firstPage = document.getFirstChild();
```

## 第 4 步：迭代頁面修訂

迭代每個頁面修訂並檢索相關信息，例如上次修改時間、創建時間、標題、級別和作者。

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

## 結論

在本教學中，我們學習如何使用 Aspose.Note for Java 在 OneNote 中擷取頁面修訂。透過執行這些步驟，您可以以程式設計方式有效追蹤對 OneNote 頁面所做的變更。

## 常見問題解答

### Q1: 我可以使用Aspose.Note for Java來修改頁面修訂嗎？

A1：不，Aspose.Note for Java 目前支援檢索頁面修訂，但不支援修改它們。

### Q2：Aspose.Note for Java 是否相容於不同版本的 OneNote 文件？

A2：是的，Aspose.Note for Java 支援各種版本的 OneNote 文檔，讓您可以無縫地處理不同的文件格式。

### Q3：Aspose.Note for Java 需要授權才能使用嗎？

A3：是的，您需要購買許可證才能在商業專案中使用Aspose.Note for Java。但是，您也可以獲得用於評估目的的臨時許可證。

### Q4：如果在使用 Aspose.Note for Java 時遇到任何問題，我可以尋求支援嗎？

 A4：是的，您可以從Aspose.Note論壇尋求支持[這裡](https://forum.aspose.com/c/note/28).

### Q5：Aspose.Note for Java 有免費試用版嗎？

A5：是的，您可以從以下地址存取 Aspose.Note for Java 的免費試用版：[網站](https://releases.aspose.com/).