---
title: 在 OneNote 中撰寫表格 - Aspose.Note
linktitle: 在 OneNote 中撰寫表格 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 以程式設計方式在 OneNote 中撰寫表格。高效率文件建立的逐步指南。
type: docs
weight: 11
url: /zh-hant/java/onenote-table-manipulation/compose-table/
---
## 介紹
在當今競爭激烈的商業環境中，有效的溝通和協作是成功的關鍵因素。 Aspose.Note for Java 提供了一個強大的解決方案，用於以程式設計方式建立和操作 OneNote 文件。在本教學中，我們將探討如何使用 Aspose.Note for Java 在 OneNote 中撰寫表格。請按照下面的逐步指南來增強您的文件建立過程。
## 先決條件
在深入學習本教程之前，請確保您符合以下先決條件：
- Java 程式設計的基礎知識。
- 安裝了 Java 函式庫的 Aspose.Note。您可以從以下位置下載：[這裡](https://releases.aspose.com/note/java/).
- 為 Java 開發而設定的整合開發環境 (IDE)。
## 導入包
確保導入必要的套件來啟動您的專案。將以下導入語句加入您的 Java 類別：
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.stream.StreamSupport;
```
## 步驟1：設定文檔目錄
```java
String dataDir = "Your Document Directory";
```
確保將「您的文件目錄」替換為您要儲存 OneNote 文件的實際路徑。
## 第 2 步：撰寫標題
```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```
為您的文件建立引人注目的標題。根據需要調整字體大小、粗細和對齊方式。
## 第 3 步：建立頁面和大綱
```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```
設定新頁面和大綱，然後將先前建立的標題新增至大綱。
## 第 4 步：新增摘要文本
```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```
包括簡短的摘要文字以提供表格的上下文。
## 第5步：撰寫表格
```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
//其餘步驟涉及設定表結構、標題行和新增空白行。
//具體實作請參考提供的程式碼。
```
建構表結構並填入相關資訊。提供的程式碼包括為「聯絡人」欄位新增欄位、標題行、空白行和範本內容。
## 第 6 步：儲存文檔
```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```
使用指定的檔案名稱和目錄路徑儲存已撰寫的文件。
## 結論
恭喜！您已使用 Aspose.Note for Java 在 OneNote 中成功編寫了一個表格。本教學課程示範了逐步過程，使您能夠以程式設計方式增強文件建立功能。
## 經常問的問題
### Q：在哪裡可以找到 Aspose.Note for Java 文件？
你可以參考文檔[這裡](https://reference.aspose.com/note/java/).
### Q：如何下載 Aspose.Note for Java？
您可以從以下位置下載：[這個連結](https://releases.aspose.com/note/java/).
### Q：有免費試用嗎？
是的，您可以免費試用[這裡](https://releases.aspose.com/).
### Q：在哪裡可以獲得 Aspose.Note for Java 的支援？
造訪支援論壇[這裡](https://forum.aspose.com/c/note/28).
### Q：我可以獲得臨時許可證嗎？
是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).