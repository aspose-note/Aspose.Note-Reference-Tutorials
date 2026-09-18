---
date: 2026-01-12
description: 了解如何使用 Aspose.Note for Java 修改 OneNote 頁面歷史記錄、更改 OneNote 頁面標題，以及刪除 OneNote
  頁面歷史記錄。
linktitle: Modify Page History in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: 如何使用 Aspose.Note 修改 OneNote 頁面歷史
url: /zh-hant/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Note 修改 OneNote 頁面歷史

在本教學中，您將了解 **如何程式化修改 OneNote** 文件，透過操作頁面歷史。我們將示範如何載入 OneNote 檔案、編輯其歷史項目、變更頁面標題，最後儲存更新後的筆記本——全部使用 Aspose.Note for Java API。無論您是需要清理舊版修訂，或是重新命名頁面，以下步驟都提供完整、可投入生產的解決方案。

## 快速答覆
- **「頁面歷史」在 OneNote 中是什麼意思？**  
  它是儲存在 OneNote 檔案內的先前頁面版本的集合。  
- **我可以刪除特定的歷史項目嗎？**  
  可以，使用 `PageHistory` 物件的 `removeRange` 或 `removeItem` 方法。  
- **變更頁面標題屬於歷史操作的一部分嗎？**  
  當然——每個歷史項目都有自己的標題，您可以修改它。  
- **執行此程式碼需要授權嗎？**  
  測試時可使用臨時評估授權；正式環境則需完整授權。  
- **支援哪個 Java 版本？**  
  Aspose.Note for Java 支援 JDK 8 及以上版本。

## 前置條件

在開始之前，請確保您已具備以下條件：

1. **Java Development Kit (JDK)** – 已在您的機器上安裝 JDK 8 或更新版本。  
2. **Aspose.Note for Java library** – 從 [download page](https://releases.aspose.com/note/java/) 下載。  
3. **範例 OneNote 文件** – 例如可安全修改的 `Sample1.one`。

## 匯入套件

首先，匯入您需要的類別。以下程式碼區塊必須保持原樣。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## 步驟指南

### 步驟 1：載入 OneNote 文件

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### 步驟 2：取得第一個頁面及其歷史

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### 步驟 3：刪除一段歷史項目

如果您需要 **刪除 OneNote 頁面歷史** 項目，請呼叫 `removeRange`。此範例會移除第一筆項目。

```java
pageHistory.removeRange(0, 1);
```

### 步驟 4：取代歷史項目

您可以使用全新的 `Page` 物件取代現有的歷史項目。

```java
pageHistory.set_Item(0, new Page());
```

### 步驟 5：變更歷史頁面的標題

在特定修訂中想要 **變更 OneNote 頁面標題** 時，變更標題是常見需求。

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### 步驟 6：新增歷史項目

將全新頁面加入歷史集合中。

```java
pageHistory.addItem(new Page());
```

### 步驟 7：在特定位置插入頁面

在索引 1 處插入頁面，將現有項目往後移動。

```java
pageHistory.insertItem(1, new Page());
```

### 步驟 8：儲存已修改的筆記本

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## 為何要修改 OneNote 頁面歷史？

- **版本控制：** 只保留相關的修訂，捨棄雜訊草稿。  
- **一致性：** 統一所有歷史版本的頁面標題，以提升導覽體驗。  
- **效能：** 較小的歷史集合可減少檔案大小並提升載入速度。

## 常見陷阱與技巧

- **索引超出範圍：** 在呼叫 `removeRange` 或 `insertItem` 前，務必先檢查集合大小。  
- **標題為 null：** 某些歷史頁面可能沒有標題，呼叫 `getTitle()` 時需防止 `null`。  
- **儲存位置：** 確認輸出路徑 (`ModifyPageHistory_out.one`) 可寫入，否則會拋出 `IOException`。

## 常見問答

**Q: 我可以將 Aspose.Note for Java 與其他 Java 框架一起使用嗎？**  
A: 可以，Aspose.Note for Java 相容於多種 Java 框架，如 Spring、Hibernate 等。

**Q: Aspose.Note for Java 是否相容於不同版本的 OneNote 檔案？**  
A: Aspose.Note for Java 支援處理舊版與新版的 OneNote 檔案。

**Q: Aspose.Note for Java 需要額外的相依性嗎？**  
A: 不需要，Aspose.Note for Java 為獨立庫，無需額外相依性。

**Q: 我能同時對多個 OneNote 檔案執行批次修改嗎？**  
A: 可以，Aspose.Note for Java 提供 API 能有效處理批次修改。

**Q: 是否有 Aspose.Note for Java 的社群論壇可供提問？**  
A: 有，您可以前往 [Aspose.Note 論壇](https://forum.aspose.com/c/note/28) 取得協助或諮詢相關問題。

---

**最後更新：** 2026-01-12  
**測試環境：** Aspose.Note for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}