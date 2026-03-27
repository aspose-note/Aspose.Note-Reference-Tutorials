---
date: 2026-01-12
description: 了解如何使用 Aspose.Note for Java 還原 OneNote 頁面並恢復先前的 OneNote 版本。請遵循此一步步指南，以實現高效的文件管理。
linktitle: How to Roll Back OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: 如何還原 OneNote - Aspose.Note
url: /zh-hant/java/onenote-page-manipulation/roll-back-to-previous-page-version/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何回滾 OneNote - Aspose.Note

## Introduction

如果您正在尋找一種清晰、程式化的方式來 **如何回滾 OneNote** 頁面，當錯誤發生時，您來對地方了。在本教學中，我們將示範如何使用 Aspose.Note for Java 將 OneNote 頁面還原至較早的狀態。無論您是構建自動化筆記管理工具，或是需要為協作筆記本提供安全網，回滾頁面都有助於保持內容的準確與可信。

## Quick Answers
- **「回滾」在 OneNote 中是什麼意思？** 將頁面還原至其歷史中先前儲存的版本。  
- **哪個 API 處理回滾？** Aspose.Note for Java 中的 `PageHistory` 類別。  
- **我需要授權嗎？** 生產環境使用需具備有效的 Aspose.Note 授權。  
- **我可以選擇任意先前的版本嗎？** 可以——您可以從頁面的歷史清單中挑選任意條目。  
- **此方法對大型筆記本安全嗎？** 絕對安全；此操作僅針對單一頁面執行，無需將整本筆記本載入記憶體。

## 如何回滾 OneNote 頁面版本
以下是一個簡潔的逐步指南，說明如何執行回滾。每一步都附有簡短說明，讓您了解 *為何* 這麼做，而不只是 *輸入什麼*。

## Prerequisites

在深入程式碼之前，請確保您已準備好以下項目：

### Java Development Environment Setup
1. **安裝 Java Development Kit (JDK)：** 從 Oracle 官方網站或您偏好的套件管理器取得最新的 JDK。  
2. **設定環境變數：** 設定 `JAVA_HOME` 並更新 `PATH`，使 `java` 與 `javac` 指令可在命令列中使用。  
3. **加入 Aspose.Note for Java：** 從[網站](https://purchase.aspose.com/buy)下載程式庫，並將 JAR 檔加入專案的 classpath。

## Import Packages

若要操作 OneNote 檔案，請匯入必要的 Aspose.Note 類別：

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Step 1: Load OneNote Document
```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```
我們首先指向存放 `.one` 檔案的資料夾，並將其載入 `Document` 物件。

## Step 2: Get Page History
```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```
`PageHistory` 讓您取得所選頁面的所有已儲存版本，從而具備 **還原先前 OneNote 版本** 的功能。

## Step 3: Remove Current Page
```java
document.removeChild(page);
```
透過移除目前的頁面，我們為欲還原的版本騰出空間。

## Step 4: Append Previous Page Version
```java
document.appendChildLast(pageHistory.get_Item(pageHistory.size() - 1));
```
此處我們選取最新的歷史條目（您可更改索引以針對任意較舊的版本），並將其重新加入文件中。

## Step 5: Save Document
```java
document.save(dataDir + "RollBackToPreviousPageVersion_out.one");
```
最後，將修改後的筆記本儲存。輸出檔案現在已包含回滾的頁面。

## Restore Previous OneNote Version
`PageHistory` 與 `appendChildLast` 的結合，使您僅需幾行程式碼即可 **還原先前 OneNote 版本**。在手動復原不可行的自動化工作流程中，這特別實用。

## Common Issues & Tips
- **歷史記錄為空：** 若 `pageHistory.size()` 回傳 0，表示該頁面沒有已儲存的版本——請確認 OneNote 已啟用版本功能。  
- **索引超出範圍：** 請記得歷史清單是從零開始。調整索引（`size() - 1`）以定位您需要的確切版本。  
- **效能：** 僅處理單一頁面可避免載入整本筆記本至記憶體，即使對大型檔案亦能保持快速執行。

## Conclusion

您現在已掌握使用 Aspose.Note for Java 進行 **如何回滾 OneNote** 頁面的完整、可投入生產的解決方案。透過 `PageHistory`，您能安全地還原筆記本頁面的任何先前狀態，確保資料完整性，並讓最終使用者在協作環境中充滿信心。

## Frequently Asked Questions

**Q1：我可以回滾頁面的多個版本嗎？**  
A：可以，您可以存取整個頁面歷史，並依需求回滾至任意先前的版本。

**Q2：Aspose.Note 是否支援除 Java 之外的其他程式語言？**  
A：支援，Aspose.Note 提供多種程式語言的函式庫，包括 .NET、C++ 與 Python。

**Q3：Aspose.Note 與所有版本的 OneNote 相容嗎？**  
A：Aspose.Note 支援多種 OneNote 格式，確保與大多數文件版本相容。

**Q4：我可以使用 Aspose.Note 自動化 OneNote 的其他工作嗎？**  
A：當然可以，Aspose.Note 提供廣泛的功能，可程式化地新增、刪除與修改內容。

**Q5：是否有 Aspose.Note 的社群論壇或支援服務？**  
A：有，您可前往 [Aspose.Note 論壇](https://forum.aspose.com/c/note/28)取得社群支援，或聯絡 Aspose 客戶服務以獲得協助。

---

**Last Updated:** 2026-01-12  
**Tested With:** Aspose.Note for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}