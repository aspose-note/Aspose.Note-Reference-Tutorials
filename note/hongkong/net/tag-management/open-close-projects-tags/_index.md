---
title: 在 Aspose.Note 中開啟和關閉帶有標籤的項目
linktitle: 在 Aspose.Note 中開啟和關閉帶有標籤的項目
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 以程式設計方式操作 Microsoft OneNote 檔案。有效地打開和關閉帶有標籤的項目。
weight: 15
url: /zh-hant/net/tag-management/open-close-projects-tags/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Note 中開啟和關閉帶有標籤的項目

## 介紹

在本教程中，我們將學習如何使用 Aspose.Note for .NET 開啟和關閉帶有標籤的項目。 Aspose.Note 是一個功能強大的 API，可讓開發人員以程式設計方式處理 Microsoft OneNote 文件，從而實現處理文件中的文字、圖像和標籤等任務。

## 先決條件

在開始之前，請確保您已設定以下先決條件：

## 導入命名空間

```csharp
using System.IO;
using System.Linq;
```

現在讓我們將每個範例分解為多個步驟：

## 第 1 步：載入文檔

首先，我們需要將文件載入到Aspose.Note中。

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## 步驟 2：關閉項目 C 項

現在，讓我們關閉與「Project C」相關的所有複選框項目。

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## 步驟 3：儲存關閉的項目 C 註釋

使用關閉的「Project C」項目儲存修改後的文件。

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## 第 4 步：開啟項目 C 項

接下來，讓我們開啟與「Project C」相關的所有複選框項目。

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## 步驟 5：儲存開啟的項目 C 註釋

使用開啟的「Project C」項目儲存修改後的文件。

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

現在您已經學習如何使用 .NET 在 Aspose.Note 中開啟和關閉帶有標籤的項目。

## 結論

Aspose.Note for .NET 提供了一種以程式設計方式操作 OneNote 文件的便利方法。透過遵循本教學課程，您可以透過使用標籤開啟和關閉專案來有效管理專案。

## 常見問題解答

### Q1：Aspose.Note 是否相容於所有版本的 OneNote？

A1：Aspose.Note 支援 Microsoft OneNote 2010 及更高版本。

### Q2：我可以將Aspose.Note用於商業項目嗎？

 A2：是的，您可以將 Aspose.Note 用於個人和商業項目。訪問[這裡](https://purchase.aspose.com/buy)購買許可證。

### Q3：Aspose.Note 提供免費試用嗎？

A3：是的，您可以獲得免費試用[這裡](https://releases.aspose.com/).

### Q4：在哪裡可以找到 Aspose.Note 的文檔？

 A4：你可以找到文檔[這裡](https://reference.aspose.com/note/net/).

### Q5：在哪裡可以獲得 Aspose.Note 的支援？

 A5：如需支持，您可以造訪Aspose.Note[論壇](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
