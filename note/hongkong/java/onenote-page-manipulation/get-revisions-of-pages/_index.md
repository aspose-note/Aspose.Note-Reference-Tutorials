---
title: 取得 OneNote 中頁面的修訂 - Aspose.Note
linktitle: 取得 OneNote 中頁面的修訂 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note Java 擷取 OneNote 文件中頁面的修訂版本。將其整合到您的 Java 應用程式中以實現高效的文件管理。
weight: 15
url: /zh-hant/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 取得 OneNote 中頁面的修訂 - Aspose.Note

## 介紹

在本教程中，我們將深入研究 Aspose.Note for Java 的功能，這是一個功能強大的程式庫，可讓您在 Java 應用程式中無縫地使用 Microsoft OneNote 檔案。具體來說，我們將重點放在如何檢索 OneNote 文件中頁面的修訂。在本指南結束時，您將具備有效提取頁面修訂的知識，包括上次修改時間、建立時間、標題、等級和作者等詳細資訊。

## 先決條件

在深入學習本教學之前，請確保您已設定以下先決條件：

### 安裝 Java 開發工具包 (JDK)

確保您的系統上安裝了 Java 開發工具包。您可以從 Oracle 網站下載並安裝它，或者如果您使用的是基於 Unix 的系統，則可以使用套件管理器。

### Java 函式庫的 Aspose.Note

從網站下載並安裝 Aspose.Note for Java 程式庫。你可以找到下載鏈接[這裡](https://releases.aspose.com/note/java/)。請按照文件中提供的安裝說明進行操作[這裡](https://reference.aspose.com/note/java/).

## 導入包

首先，將必要的套件匯入到您的 Java 專案中。這些套件將允許您利用 Aspose.Note for Java 提供的功能。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

現在，讓我們將提供的範例程式碼分解為多個步驟，以了解每個組件及其功能。

## 步驟1：設定文檔目錄

定義 OneNote 文件所在的目錄。

```java
String dataDir = "Your Document Directory";
```

## 第 2 步：載入文檔

將 OneNote 文件載入到 Aspose.Note 中。

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## 第 3 步：取得首頁

從文件中檢索第一頁。

```java
Page firstPage = doc.getFirstChild();
```

## 第 4 步：取得頁面修訂

取得頁面的修改歷史記錄。

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## 步驟5：遍歷頁面修訂

迭代頁面修訂清單並檢索相關資訊。

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

## 結論

在本教學中，我們探討如何使用 Aspose.Note for Java 擷取 OneNote 文件中頁面的修訂版本。透過遵循逐步指南並利用提供的範例程式碼，您可以輕鬆地將此功能整合到 Java 應用程式中，從而實現 OneNote 檔案的高效管理。

## 常見問題解答

### Q1：我可以使用Aspose.Note for Java建立新的OneNote文件嗎？

A1：是的，Aspose.Note for Java 為以程式設計方式建立、讀取和操作 OneNote 文件提供了全面的支援。

### Q2：Aspose.Note for Java 是否相容於不同版本的 OneNote 檔案？

A2：是的，Aspose.Note for Java 支援各種版本的 Microsoft OneNote 文件，確保不同環境之間的兼容性。

### Q3：匯出 OneNote 文件時可以自訂輸出格式嗎？

A3：當然，Aspose.Note for Java 可以靈活地將 OneNote 文件匯出為不同的格式，例如 PDF、HTML 和圖像，並提供自訂選項。

### Q4：Aspose.Note for Java 商業使用需要授權嗎？

A4：是的，Aspose.Note for Java 的商業用途需要有效的授權。您可以從 Aspose 網站取得許可證。

### Q5：如果我遇到問題或對 Aspose.Note for Java 有疑問，可以在哪裡尋求協助？

 A5： 如需支援和協助，您可以造訪 Aspose.Note 論壇[這裡](https://forum.aspose.com/c/note/28)，您可以在其中提出問題、分享經驗以及與其他使用者和專家互動。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
