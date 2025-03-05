---
title: 檢索 Aspose.Note 文字中的項目符號或編號列表
linktitle: 檢索 Aspose.Note 文字中的項目符號或編號列表
second_title: Aspose.Note .NET API
description: 透過我們有關檢索項目符號或編號清單的逐步指南來釋放 Aspose.Note for .NET 的潛力。提升您的 OneNote 文件操作技能！
type: docs
weight: 23
url: /zh-hant/net/text-manipulation/retrieve-bullet-number-list/
---
## 介紹
歡迎來到 Aspose.Note for .NET 的世界，這是一個強大且多功能的程式庫，使開發人員能夠輕鬆處理 OneNote 文件操作。在本教學中，我們將深入研究使用 Aspose.Note for .NET 擷取項目符號或編號清單的過程。無論您是經驗豐富的開發人員還是編碼愛好者，本指南都將為您提供在 Aspose.Note 中使用清單的複雜知識。
## 先決條件
在我們開始編碼之旅之前，請確保您具備以下先決條件：
-  Aspose.Note for .NET：確保您已安裝 Aspose.Note 函式庫。如果沒有，您可以從以下位置下載[.NET 文件的 Aspose.Note](https://reference.aspose.com/note/net/).
- 開發環境：在您的電腦上設定一個有效的開發環境，最好是 Microsoft Visual Studio。
- C# 基礎：熟悉 C#，因為本教學是用這種語言寫的。
## 導入命名空間
為了與 Aspose.Note for .NET 交互，您需要將必要的命名空間匯入到您的專案中。在程式碼開頭包含以下命名空間：
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
現在，讓我們逐步分解檢索項目符號或編號清單的過程：
## 第 1 步：設定您的文件目錄
```csharp
//文檔目錄的路徑。
string dataDir = "Your Document Directory";
```
代替`"Your Document Directory"`與您的 Aspose.Note 文件所在的實際路徑。
## 第 2 步：載入文檔
```csharp
//將文件載入到 Aspose.Note 中。
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
確保更換`"ApplyNumberingOnText.one"`與您的特定 OneNote 文件的名稱。
## 步驟 3：檢索節點集合
```csharp
//檢索輪廓元素的節點集合。
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
此步驟從已載入的文件中檢索大綱節點的集合。
## 第 4 步：迭代每個節點
```csharp
//迭代每個節點。
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        //繼續執行後續步驟...
    }
}
```
這個循環確保我們只處理包含數字列表的節點。
## 第 5 步：檢索字體訊息
```csharp
//檢索字體名稱
Console.WriteLine("Font Name: " + list.Font);
//檢索字體長度
Console.WriteLine("Font Length: " + list.Font.Length);
//檢索字體大小
Console.WriteLine("Font Size: " + list.FontSize);
//檢索字體顏色
Console.WriteLine("Font Color: " + list.FontColor);
//檢索格式
Console.WriteLine("Font format: " + list.Format);
//勾選粗體
Console.WriteLine("Is bold: " + list.IsBold);
//檢查斜體
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
這些程式碼行從數字列表中提取各種與字體相關的資訊。
## 結論
恭喜！您已成功學習如何使用 Aspose.Note for .NET 擷取項目符號或編號清單。當您繼續探索時，請參閱[文件](https://reference.aspose.com/note/net/)以獲得更深入的見解和功能。
## 常見問題解答
### 我可以將 Aspose.Note for .NET 與其他程式語言一起使用嗎？
Aspose.Note 主要支援 .NET，但該程式庫還有其他針對不同平台和語言量身定制的版本。
### Aspose.Note 與最新的 OneNote 格式相容嗎？
是的，Aspose.Note 支援多種 OneNote 格式，確保與最新版本的兼容性。
### 如何獲得 Aspose.Note 的臨時許可證？
訪問[這個連結](https://purchase.aspose.com/temporary-license/)獲得用於評估目的的臨時許可證。
### Aspose.Note 使用者可以使用哪些支援選項？
您可以探索並尋求幫助[Aspose.Note 論壇](https://forum.aspose.com/c/note/28)對於您可能遇到的任何疑問或問題。
### Aspose.Note for .NET 有免費試用版嗎？
是的，您可以存取 Aspose.Note for .NET 的免費試用版[這裡](https://releases.aspose.com/).