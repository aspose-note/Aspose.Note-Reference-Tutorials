---
date: 2026-01-10
description: 學習 Aspose.Note 的 Java 頁面修訂教學——使用 Aspose.Note 以程式方式擷取 OneNote 頁面修訂。請遵循我們的逐步指南。
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Aspose.Note 頁面修訂教學 – 在 OneNote 中取得頁面修訂
url: /zh-hant/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中取得頁面修訂 - Aspose.Note

OneNote 是一個功能強大的筆記平台，當您需要稽核變更時，**aspose.note page revisions tutorial** 會向您展示如何僅透過少量 Java 程式碼即取得修訂歷史。在本指南中，我們將逐步說明您需要的所有操作——從環境設定到列印每個修訂的詳細資訊——讓您輕鬆追蹤編輯、作者貢獻與時間戳記。

## 快速回答
- **本教學涵蓋什麼內容？** 使用 Aspose.Note for Java 從 OneNote 檔案中擷取頁面修訂歷史。  
- **需要哪個版本的函式庫？** 任何支援 `LoadOptions.setLoadHistory` 的近期 Aspose.Note for Java 版本皆可。  
- **是否需要授權？** 測試時可使用臨時評估授權；正式上線則需商業授權。  
- **我可以修改修訂嗎？** 修訂的 API 為唯讀；只能取得。  
- **主要前置條件是什麼？** Java JDK、Aspose.Note for Java，以及含有修訂資料的 OneNote 文件。

## 什麼是「aspose.note page revisions tutorial」？
本教學示範如何以程式方式存取 OneNote 頁面的歷史版本。每個修訂都包含作者、建立時間與修改時間等中繼資料，讓您能在應用程式中建立稽核追蹤或變更紀錄功能。

## 為什麼使用 Aspose.Note 來追蹤頁面修訂？
- **無 UI 依賴** – 完全以程式碼運作，適合後端服務。  
- **跨平台** – Java 可在 Windows、Linux 與 macOS 上執行。  
- **完整控制** – 無需手動開啟 OneNote，即可取得每筆修訂屬性。  
- **效能** – 讀取歷史已最佳化，即使大型筆記本亦能快速處理。

## 前置條件

### 1. Java Development Kit (JDK)
確保已安裝近期的 JDK（8 版或以上），且已設定 `JAVA_HOME`。

### 2. Aspose.Note for Java
從 [download link](https://releases.aspose.com/note/java/) 下載函式庫。

### 3. 範例 OneNote 文件
建立或取得包含修訂歷史之 OneNote 檔案（例如 `Sample1.one`）。

## 匯入套件
首先，匯入所需的 Aspose.Note 類別。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## 步驟實作說明

### 步驟 1：設定文件目錄
定義 OneNote 檔案所在的資料夾路徑。

```java
String dataDir = "Your Document Directory";
```

### 步驟 2：載入啟用歷史的 OneNote 文件
啟用 `LoadOptions` 旗標以取得修訂資料。

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### 步驟 3：取得第一頁
取得第一頁物件；此物件將作為取得其歷史的參考點。

```java
Page firstPage = document.getFirstChild();
```

### 步驟 4：遍歷頁面修訂
遍歷每筆修訂，並列印時間戳記、標題、層級與作者等有用的中繼資料。

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
- **未返回修訂**：確認在載入文件前已呼叫 `loadOptions.setLoadHistory(true)`。  
- **作者或標題為 null**：某些較舊的 OneNote 版本可能不會儲存這些欄位，請妥善處理 `null` 值。  
- **大型筆記本效能下降**：僅載入所需的節點或增大 JVM 堆積大小。

## 常見問答

**Q1：我可以使用 Aspose.Note for Java 來修改頁面修訂嗎？**  
A1：不行，API 目前僅支援唯讀存取頁面修訂。

**Q2：Aspose.Note for Java 是否相容於不同版本的 OneNote 文件？**  
A2：是的，它支援多種 OneNote 檔案格式，能在不同版本間無縫處理。

**Q3：使用 Aspose.Note for Java 是否需要授權？**  
A3：正式環境需購買商業授權，測試時可使用臨時評估授權。

**Q4：若在使用 Aspose.Note for Java 時遇到問題，我可以尋求支援嗎？**  
A4：可以，您可在 Aspose.Note 論壇 [here](https://forum.aspose.com/c/note/28) 提問。

**Q5：Aspose.Note for Java 是否提供免費試用？**  
A5：有，您可從 [website](https://releases.aspose.com/) 下載免費試用版。

---

**最後更新：** 2026-01-10  
**測試環境：** Aspose.Note for Java（最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}