---
date: 2026-01-20
description: 學習如何使用 Aspose.Note for Java 在 OneNote 中變更表格樣式並設定表格列的背景顏色。請依照逐步指南套用背景顏色、粗體文字，並儲存
  OneNote 文件。
linktitle: Change Table Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: 如何使用 Aspose.Note 更改 OneNote 中的表格樣式
url: /zh-hant/java/onenote-table-manipulation/change-table-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Note 在 OneNote 中變更表格樣式

## 介紹
如果您需要 **在 OneNote 筆記本中變更表格樣式**，Aspose.Note for Java 讓這件事變得輕而易舉。在本教學中，我們將完整示範從載入 OneNote 檔案、設定表格列背景顏色、套用粗體與斜體格式，直到最後儲存已更新的文件。完成後，您將熟悉 OneNote 表格格式化、了解如何為列設定背景色，並掌握如何以新樣式儲存 OneNote 文件。

## 快速答覆
- **哪個函式庫最適合 OneNote 表格樣式設定？** Aspose.Note for Java。  
- **我可以設定表格列的背景顏色嗎？** 可以，使用 `setRowStyle` 輔助方法。格中將文字設為粗體？** 在 `setRowStyle` 中設定 `bold` 旗標。  
- **儲存修改後的檔案需要什麼？** 呼叫 `document.save(...)` 並提供有效路徑。  
- **正式環境需要授權嗎？** 需要，必須購買商業授權。

## 什麼是 OneNote 中的「變更表格樣式」？
變更表格樣式即是調整列的顏色、文字格式以及整體外觀，使資料更易閱讀且視覺上更吸引人。Aspose.Note 提供流暢的 API，讓您以程式方式操作這些格式化** 功能，如背景顏色文字。發環境** – 已安裝 JDK 8 或以上版本。  
- **Aspose.Note for Java 函式庫** – 可從[下載頁面](https://releases.aspose.com/note/java/)取得。  
- **文件目錄** – 用於存放 `.one` 檔案的資料夾。  

## 匯入套件
在您的 Java 專案中，匯入操作 Aspose.Note 所需的套件：
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

## 步驟 1：設定文件
將 OneNote 文件載入 Aspose.Note，並取得表格節點清單。
```java
// Set up the document and get the list of table nodes
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```

## 步驟 2：設定列樣式
遍歷每個表格，為每一列設定樣式，並在標題列之後突顯第一列。此步驟示範 **設定表格列背景** 以及 **如何套用背景顏色**。
```java
// Set row styles for each table in the document
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Highlight first row after the head.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```

## setRowStyle 方法
此輔助方法會為列中的每個儲存格套用背景顏色、粗體與斜體格式。這裡實作了 **在 OneNote 中如何將文字設為粗體**。
```java
    private static void setRowStyle(TableRow row, Color highlightColor, boolean bold, boolean italic) {
        for (TableCell cell: row)
        {
            cell.setBackgroundColor(highlightColor);
            for (RichText node: cell.getChildNodes(RichText.class))
            {
                node.getParagraphStyle().setBold(bold);
                node.getParagraphStyle().setItalic(italic);
                for (TextRun run: node.getTextRuns())
                {
                    run.getStyle().setBold(bold);
                    run.getStyle().setItalic(italic);
                }
            }
        }
    }
```

## 步驟 3：儲存文件
完成表格樣式設定後，儲存已修改的文件。此步驟展示 **如何儲存 OneNote 文件** 並套用新格式。
```java
// Save the modified document
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```

## 結論
Aspose.Note for Java 簡化了操作 OneNote 檔案的流程。透過此函式庫，您可以輕鬆變更表格樣式、設定表格列背景顏色、套用粗體文字，並以幾行程式碼儲存 OneNote 文件。

## 常見問題
### 我可以在哪裡找到 Aspose.Note for Java 的文件說明？
請造訪[文件說明](https://reference.aspose.com/note/java/)取得完整指引。

### 如何取得 Aspose.Note for Java 的臨時授權？
請前往此[連結](https://purchase.aspose.com/temporary-license/)取得臨時授權。

### 是否提供 Aspose.Note for Java 的免費試用版？
是的，您可從[此處](https://releases.aspose.com/)下載免費試用版。

### 我可以在哪裡取得 Aspose.Note for Java 的支援？
加入[Aspose.Note 論壇](https://forum.aspose.com/c/note/28)向社群尋求協助。

### 我要如何購買 Aspose.Note for Java？
您可在[此處](https://purchase.aspose.com/buy)完成購買。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-01-20  
**測試環境：** Aspose.Note for Java 24.11  
**作者：** Aspose  

---