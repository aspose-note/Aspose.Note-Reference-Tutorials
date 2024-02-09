---
title: 從 Aspose.Note 中的範本產生文檔
linktitle: 從 Aspose.Note 中的範本產生文檔
second_title: Aspose.Note .NET API
description: 使用 Aspose.Note for .NET 輕鬆產生動態文件。遵循我們的逐步指南來建立個人化和資料驅動的文件。
type: docs
weight: 18
url: /zh-hant/net/text-manipulation/generate-document-from-template/
---
## 介紹
在不斷發展的文件建立領域，Aspose.Note for .NET 脫穎而出，成為輕鬆產生動態文件的強大工具。無論您是處理報告、發票還是個人化文檔，本教學都會引導您完成使用 Aspose.Note for .NET 從範本產生文檔的過程。
## 先決條件
在深入了解逐步指南之前，請確保您具備以下先決條件：
1.  Aspose.Note for .NET Library：從以下位置下載並安裝該程式庫：[.NET 文件的 Aspose.Note](https://reference.aspose.com/note/net/).
2. 文件範本：準備 OneNote 格式的範本文件（副檔名為 .one）。這將作為動態生成文件的基礎。
## 導入命名空間
確保在您的專案中包含必要的命名空間：
```csharp
    using System;
    using System.Collections.Generic;
    using System.IO;
```
現在，讓我們分解指南中的每個步驟。
## 第 1 步：定義您的文件目錄
```csharp
string dataDir = "Your Document Directory";
```
將「您的文件目錄」替換為您要儲存產生的文件的路徑。
## 第 2 步：建立包含替換值的字典
```csharp
var templateData = new Dictionary<string, string>
{
    { "Company", "Atlas Shrugged Ltd" },
    { "CandidateName", "John Galt" },
    { "JobTitle", "Chief Entrepreneur Officer" },
    { "Department", "Sales" },
    { "Salary", "123456 USD" },
    { "Vacation", "30" },
    { "StartDate", "29 Feb 2024" },
    { "YourName", "Ayn Rand" }
};
```
定義一個字典，其中鍵是模板中的佔位符，值是要替換它們的資料。

## 第三步：載入模板文檔
```csharp
var templateDocument = new Document(Path.Combine(dataDir, "JobOffer.one"));
```
將 OneNote 範本文件載入到 Aspose.Note 中。

## 步驟 4：用動態資料取代模板單字
```csharp
foreach (var paragraph in templateDocument.GetChildNodes<RichText>())
{
    foreach (var replacement in templateData)
    {
        paragraph.Replace($"${{{replacement.Key}}}", replacement.Value);
    }
}
```
迭代模板中的每個段落，用動態資料取代佔位符。

## 步驟5：儲存產生的文檔
```csharp
templateDocument.Save(Path.Combine(dataDir, "JobOffer_out.one"));
```
將動態產生的文件儲存到您指定的目錄中。

## 結論
恭喜！您已使用 Aspose.Note for .NET 成功產生了動態文件。此過程為無縫創建個人化和數據驅動的文件開闢了無限可能。

## 經常問的問題
### 我可以將 Aspose.Note for .NET 與其他文件格式一起使用嗎？
是的，Aspose.Note for .NET 主要處理 OneNote 文檔，但 Aspose 為不同格式提供了各種函式庫。
### Aspose.Note for .NET 是否有免費試用版？
是的，您可以透過免費試用來探索 Aspose.Note for .NET 的功能。訪問[這裡](https://releases.aspose.com/)了解更多。
### 如何獲得 Aspose.Note for .NET 支援？
參觀[Aspose.Note for .NET 論壇](https://forum.aspose.com/c/note/28)獲得社區和專家的幫助。
### Aspose.Note for .NET 是否有臨時授權？
是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/)用於測試和評估目的。
### 在哪裡可以找到 Aspose.Note for .NET 的綜合文件？
請參閱[文件](https://reference.aspose.com/note/net/)有關使用 Aspose.Note for .NET 的深入資訊。