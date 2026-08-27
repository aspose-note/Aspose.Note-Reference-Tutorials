---
date: 2026-01-15
description: 了解如何使用 Aspose.Note for Java 追蹤 OneNote 的變更並管理 OneNote 文件中的頁面修訂。包括修訂摘要範例以及如何修改修訂日期。
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote 變更追蹤 – 使用 Aspose.Note 管理頁面修訂
url: /zh-hant/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中處理頁面修訂 - Aspose.Note

## 簡介

OneNote 是一個強大的筆記組織工具，當您需要 **track changes onenote** 時，管理頁面修訂對於有效的協作至關重要。使用 Aspose.Note for Java，您可以以程式方式處理修訂、查看誰編輯了頁面，甚至調整時間戳記。本教學將帶您逐步完成從載入文件到更新修訂摘要的每個步驟。

## 快速解答
- **What does “track changes onenote” mean?** 它指的是監控誰在何時編輯 OneNote 頁面。
- **Which library is required?** Aspose.Note for Java。
- **Can I change the author or date of a revision?** 可以，使用 RevisionSummary API（`modify revision date`）。
- **Do I need a OneNote file beforehand?** 需要，必須先備有一個 `.one` 範例檔案。
- **Is a license needed for production?** 需要，商業使用必須擁有有效的 Aspose.Note 授權。

## 什麼是修訂摘要範例？

*revision summary* 提供關於頁面最近變更的中繼資料——作者名稱、最後修改時間以及其他細節。在本指南中，我們將取得並顯示這些資訊，然後示範如何 **modify revision date**。

## 為什麼要使用 Aspose.Note 追蹤 OneNote 變更？

- **Collaboration:** 協作：快速查看誰進行了最新編輯。
- **Auditing:** 稽核：保留可靠的變更歷史以符合合規要求。
- **Automation:** 自動化：將修訂處理整合到後端服務或遷移工具中。

## 前置條件

### Java Development Environment
確保您的系統已安裝 Java Development Kit（JDK）。

### Aspose.Note for Java Library
從 [here](https://releases.aspose.com/note/java/) 下載並安裝 Aspose.Note for Java 程式庫。

### OneNote Document
準備好一個 OneNote 範例文件以供測試。

## 匯入套件

在您的 Java 專案中，匯入使用 Aspose.Note for Java 所需的套件。

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

讓我們將提供的範例分解為多個步驟，以便清晰理解。

## 步驟 1：載入 OneNote 文檔

首先，載入 OneNote 文件並取得第一個子頁面。

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## 步驟 2：讀取頁面修訂摘要

讀取該頁面的內容修訂摘要。這就是顯示最後編輯者的 **revision summary example**。

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## 步驟 3：更新頁面修訂摘要

使用新作者與新修改日期更新頁面修訂摘要。此範例示範如何以程式方式 **modify revision date**。

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## 結論

以程式方式管理 OneNote 文件中的頁面修訂，可藉由 Aspose.Note for Java 簡化。依循本教學的步驟，您即可有效 **track changes onenote**、檢視修訂細節，甚至 **modify revision date** 以符合工作流程需求。

## 常見問題解答

### 問題1：我可以將 Aspose.Note for Java 與其他 Java 函式庫一起使用嗎？

回答： 可以，Aspose.Note for Java 可與其他 Java 程式庫整合，以增強功能。

### 問題2：Aspose.Note for Java 是否支援所有版本的 OneNote 文件？

回答： Aspose.Note for Java 支援多種 OneNote 文件版本，包括較舊的版本。

### 問題3：Aspose.Note for Java 是否適用於企業級應用？

回答： 絕對適合，Aspose.Note for Java 為企業級應用設計，具備強大功能與可擴充性。

### 問題4：我可以使用 Aspose.Note for Java 自訂頁面修訂嗎？

回答： 可以，您可依需求使用 Aspose.Note for Java 自訂頁面修訂。

### 問題5：我可以在哪裡獲得 Aspose.Note for Java 的支援？

回答： 您可從 [Aspose.Note forum](https://forum.aspose.com/c/note/28) 取得 Aspose.Note for Java 的支援。

---

**最後更新：** 2026-01-15  
**測試環境：** Aspose.Note for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}