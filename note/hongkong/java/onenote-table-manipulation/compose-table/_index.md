---
date: 2026-01-23
description: 學習如何使用 Aspose.Note for Java 以程式方式向 OneNote 添加表格。一步一步的指南，助您高效建立文件。
linktitle: How to add table to OneNote with Aspose.Note for Java
second_title: Aspose.Note Java API
title: 如何使用 Aspose.Note for Java 在 OneNote 中加入表格
url: /zh-hant/java/onenote-table-manipulation/compose-table/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Note for Java 在 OneNote 中新增表格

## 介紹
在本教學中，您將學習如何使用 Aspose.Note for Java **在 OneNote 中新增表格**，讓您能以程式方式建立豐富且結構化的文件，提升協作與報告效果。Aspose.Note 提供強大的 API，讓您在不需手動編輯的情況下建構 OneNote 頁面、大綱與表格。

## 快速解答
- **本教學涵蓋什麼內容？** 使用 Aspose.Note for Java 在 OneNote 中新增表格。  
- **需要多少時間？** 基本實作大約需要 10‑15 分鐘。  
- **需要授權嗎？** 免費試用可用於評估；正式上線需購買商業授權。  
- **支援哪個 Java 版本？** Java 8 及以上。  
- **可以自訂表格樣式嗎？** 可以——您可透過 API 修改字型、顏色與儲存格邊框。  

## 前置條件
在開始本教學之前，請確保您已具備以下前置條件：
- 具備 Java 程式設計的基本知識。  
- 已安裝 Aspose.Note for Java 程式庫。您可從 [此處](https://releases.aspose.com/note/java/) 下載。  
- 已設定好用於 Java 開發的整合開發環境 (IDE)。  

## 匯入套件
確保匯入必要的套件以啟動您的專案。將以下 import 陳述加入您的 Java 類別中：

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.stream.StreamSupport;
```

## 步驟 1：設定文件目錄
將 `"Your Document Directory"` 替換為您想儲存 OneNote 文件的實際路徑。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：組成標題
為您的文件建立醒目的標題。根據需要調整字型大小、粗體與對齊方式。

```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```

## 步驟 3：建立頁面與大綱
設定新頁面與大綱，然後將先前建立的標題加入大綱中。

```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```

## 步驟 4：加入摘要文字
加入簡短的摘要文字，以提供表格的背景說明。

```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```

## 步驟 5：在 OneNote 中新增表格
組成表格結構並填入相關資訊。提供的程式碼包括新增欄位、標題列、空白列，以及「Contacts」欄的範本內容。

```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
// Remaining steps are involved in setting up the table structure, header row, and adding empty rows.
// Refer to the provided code for detailed implementation.
```

## 步驟 6：儲存文件
使用指定的檔名與目錄路徑儲存您組成的文件。

```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```

## 結論
恭喜！您已成功使用 Aspose.Note for Java **在 OneNote 中新增表格**。本教學示範了逐步流程，讓您能以程式方式提升文件建立的能力。

## 常見問題
### Q: 在哪裡可以找到 Aspose.Note for Java 的文件說明？
您可參考文件 [此處](https://reference.aspose.com/note/java/)。

### Q: 如何下載 Aspose.Note for Java？
您可從 [此連結](https://releases.aspose.com/note/java/) 下載。

### Q: 是否提供免費試用？
是的，您可在 [此處](https://releases.aspose.com/) 取得免費試用。

### Q: 在哪裡可以取得 Aspose.Note for Java 的支援？
請前往支援論壇 [此處](https://forum.aspose.com/c/note/28)。

### Q: 我可以取得臨時授權嗎？
是的，您可在 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

---

**最後更新：** 2026-01-23  
**測試環境：** Aspose.Note for Java (latest release)  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}