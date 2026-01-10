---
date: 2026-01-10
description: 了解如何使用 Aspose.Note for Java 獲取 OneNote 頁面的最後修改時間及檢索修訂版本。將此功能整合至您的 Java
  應用程式，以實現高效的文件管理。
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: 如何取得 OneNote 頁面的最後修改時間 – Aspose.Note
url: /zh-hant/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 取得 OneNote 頁面的修訂記錄 - Aspose.Note

## 介紹

在本教學中，您將 **取得頁面的最後修改時間**，並探索如何使用 Aspose.Note for Java 取得完整的修訂歷史。無論您是建置文件管理系統、審核變更，或只是需要顯示頁面最後編輯的時間，本指南都會示範如何以程式方式擷取這些資訊。

## 快速回答
- **「取得最後修改時間」會回傳什麼？** 回傳 OneNote 頁面最近一次編輯的時間戳記。  
- **哪個類別提供修訂歷史？** 透過 `Document.getPageHistory(Page)` 取得的 `PageHistory`。  
- **此功能需要授權嗎？** 需要，有效的 Aspose.Note 授權才能在正式環境使用。  
- **支援哪個 Java 版本？** Java 8 或更高版本（JDK 8+）。  
- **可以依作者過濾修訂嗎？** 您可以讀取每個 `Page` 物件的 `Author` 屬性，自行實作過濾條件。

## OneNote 中的「取得最後修改時間」是什麼？

**最後修改時間** 是每個頁面所儲存的中繼資料欄位，用來記錄該頁面最近一次變更的時間。Aspose.Note 透過 `Page.getLastModifiedTime()` 方法公開此值，讓您輕鬆顯示或記錄變更日期。

## 為什麼要取得頁面修訂？

- **稽核軌跡：** 保留誰在何時變更了什麼的紀錄。  
- **版本比較：** 建置可將兩個修訂並排比較的功能。  
- **使用者協作洞察：** 了解共享筆記本中的編輯模式。

## 前置條件

在開始之前，請確保您已具備以下項目：

### 已安裝 Java Development Kit (JDK)
從 Oracle 官方網站或您慣用的套件管理員安裝 JDK 8 或更新版本。

### Aspose.Note for Java 套件
從官方網站下載程式庫。您可以在 **[此處](https://releases.aspose.com/note/java/)** 取得下載連結。安裝說明請參考 **[此處](https://reference.aspose.com/note/java/)** 的文件。

## 匯入套件

首先，將必要的套件匯入您的 Java 專案。這些套件可讓您使用 Aspose.Note for Java 所提供的功能。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

接下來，我們將示範的程式碼分成多個步驟說明，以便了解每個元件及其功能。

## 如何取得 OneNote 頁面的最後修改時間

### 步驟 1：設定文件目錄
定義 OneNote 文件所在的目錄。

```java
String dataDir = "Your Document Directory";
```

### 步驟 2：載入文件
將 OneNote 文件載入 Aspose.Note。

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### 步驟 3：取得第一頁
從文件中取得第一頁。

```java
Page firstPage = doc.getFirstChild();
```

### 步驟 4：取得頁面修訂
取得該頁面的修訂歷史。

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### 步驟 5：遍歷頁面修訂
遍歷修訂清單，並取得相關資訊，包括 **最後修改時間**。

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

## 常見問題與解決方案
- **`PageHistory` 為 null：** 確認文件確實包含修訂；否則 `getPageHistory` 可能回傳 `null`。  
- **時區差異：** `getLastModifiedTime()` 會以系統預設時區回傳 `java.util.Date`，如有需要請自行轉換為 UTC。  
- **授權未載入：** 若未載入有效授權，Aspose.Note 會以評估模式運作，處理的頁面數量會受到限制。

## 常見問答

### Q1：我可以使用 Aspose.Note for Java 建立新的 OneNote 文件嗎？
A1：可以，Aspose.Note for Java 完整支援以程式方式建立、讀取與操作 OneNote 文件。

### Q2：Aspose.Note for Java 是否相容於不同版本的 OneNote 檔案？
A2：相容，Aspose.Note for Java 支援多種 Microsoft OneNote 檔案版本，確保在不同環境下皆可使用。

### Q3：匯出 OneNote 文件時，我可以自訂輸出格式嗎？
A3：當然可以，Aspose.Note for Java 提供將 OneNote 文件匯出為 PDF、HTML、影像等多種格式的彈性，且可自行設定匯出選項。

### Q4：Aspose.Note for Java 的商業使用是否需要授權？
A4：需要，商業使用必須取得有效的授權。您可於 Aspose 官方網站購買授權。

### Q5：如果遇到問題或有疑問，我該向哪裡尋求協助？
A5：您可前往 Aspose.Note 論壇 **[此處](https://forum.aspose.com/c/note/28)**，在那裡提問、分享經驗，並與其他使用者及專家互動。

---

**最後更新：** 2026-01-10  
**測試環境：** Aspose.Note for Java 23.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}