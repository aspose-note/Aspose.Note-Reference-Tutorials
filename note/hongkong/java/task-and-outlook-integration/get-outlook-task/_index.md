---
date: 2026-04-01
description: 學習如何使用 Aspose.Note for Java 從 Outlook 提取任務至 OneNote。遵循此一步一步的指南，快速取得任務詳細資料。
keywords:
- how to extract tasks
- Aspose.Note Java
- Outlook task extraction
linktitle: 在 OneNote 中取得 Outlook 任務 - Aspose.Note
second_title: Aspose.Note Java API
title: 如何使用 Aspose.Note 在 OneNote 中提取 Outlook 任務
url: /zh-hant/java/task-and-outlook-integration/get-outlook-task/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中取得 Outlook 任務 - Aspose.Note

## 簡介
歡迎閱讀我們的完整指南，說明如何使用 Aspose.Note for Java 從 Outlook 中的 OneNote 筆記本 **提取任務**。無論您是建立遷移工具、產生報告，或只是需要同步任務資料，本教學都會一步一步帶領您，從載入 OneNote 檔案到讀取每個 Outlook 任務的屬性。完成後，您將擁有一段可直接使用的程式碼片段，您可以將其套用到自己的專案中。

## 快速解答
- **本教學涵蓋什麼內容？** 使用 Aspose.Note for Java 從 OneNote 文件中提取 Outlook 任務詳細資訊。  
- **使用哪個 API？** Aspose.Note Java 函式庫。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買商業授權。  
- **實作需要多久？** 環境設定完成後，大約需要 10‑15 分鐘。  
- **可以處理多本筆記本嗎？** 可以，只需對檔案進行迴圈，重複使用相同的邏輯。

## 什麼是任務提取？
任務提取是指讀取 Outlook 以 `NoteTask` 標籤形式儲存在 OneNote 頁面中的結構化任務資訊（例如截止日期、狀態和圖示）。這讓您能以程式方式存取任務中繼資料，而無需手動複製。

## 為何使用 Aspose.Note for Java？
- **不需 Microsoft Office** – 可在任何具備 Java 執行環境的平台上運行。  
- **完整保真度** – 保留所有 OneNote 元素，同時讓您直接存取標籤。  
- **高效能** – 針對大型筆記本與批次處理進行最佳化。  

## 先決條件
在開始之前，請確保您已準備好以下項目：

- **Java 開發環境** – 已安裝並設定 JDK 8 或更新版本。  
- **Aspose.Note 函式庫** – 從官方網站[此處](https://releases.aspose.com/note/java/)下載最新的 Java 套件。  
- **範例 OneNote 檔案** – 本教學使用 `Sample1.one`；您可替換為任何包含 Outlook 任務的筆記本。  

## 匯入套件
將所需的匯入語句加入您的 Java 類別。這些類別讓您能存取文件模型以及 Outlook 專屬的 `NoteTask` 標籤。

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```

## 步驟說明

### 步驟 1：設定文件目錄
定義存放 OneNote 檔案的資料夾。可使用絕對路徑或相對路徑，但請保持路徑字串整潔以提升可讀性。

```java
String dataDir = "Your Document Directory";
```

### 步驟 2：載入 OneNote 文件
透過指向 `.one` 檔案建立 `Document` 實例。Aspose.Note 會將檔案解析為類似 DOM 的結構，供您遍歷。

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### 步驟 3：取得所有 RichText 節點
Outlook 任務儲存在 `RichText` 元素內。取得每個 `RichText` 節點，以便檢查其標籤。

```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```

### 步驟 4：遍歷每個節點
對每個 `RichText` 節點進行迴圈，檢查其標籤，當遇到 `NoteTask` 時執行相應操作。以下程式碼會列印每個任務最有用的屬性。

```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Retrieve properties
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```

**小技巧：** 若您只需要部分屬性，可跳過其他屬性，以提升處理大型筆記本時的效能。

### 常見問題與解決方案
- **未找到任務：** 請確認 OneNote 頁面確實包含 Outlook 任務。它們會顯示為帶有小 Outlook 圖示的核取方塊。  
- **空值：** 某些任務欄位（例如 `CompletedTime`）若任務尚未完成可能為 `null`。在列印前先檢查是否為 `null`，以避免 `NullPointerException`。  
- **找不到檔案：** 確認 `dataDir` 以正確的路徑分隔符（`/` 或 `\\`）結尾，符合您的作業系統。  

## 結論
恭喜！您已學會使用 Aspose.Note Java API **從 OneNote 中的 Outlook 提取任務**。此方法讓您能完整程式化控制任務資料，並可整合至自訂報告工具、資料庫或其他業務工作流程。

## 常見問題

**Q: Aspose.Note 是否相容於所有版本的 OneNote？**  
A: Aspose.Note 支援 Microsoft OneNote 2010 及之後的版本。

**Q: 我可以將 Aspose.Note 用於個人與商業專案嗎？**  
A: 可以，Aspose.Note 可用於個人與商業專案。請前往[此處](https://purchase.aspose.com/buy)了解授權選項。

**Q: 是否提供 Aspose.Note 的免費試用？**  
A: 有，您可在[此處](https://releases.aspose.com/)取得免費試用。

**Q: 如何取得 Aspose.Note 的支援？**  
A: 前往 [Aspose.Note 論壇](https://forum.aspose.com/c/note/28)取得社群支援。若需額外協助，可考慮購買[臨時授權](https://purchase.aspose.com/temporary-license/)。

**Q: 是否有可供測試的 OneNote 範例文件？**  
A: 您可在 Aspose.Note 文件[此處](https://reference.aspose.com/note/java/)找到範例文件。

---

**最後更新：** 2026-04-01  
**測試環境：** Aspose.Note for Java 24.12 (latest at time of writing)  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}