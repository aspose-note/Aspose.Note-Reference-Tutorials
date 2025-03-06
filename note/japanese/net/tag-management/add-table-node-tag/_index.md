---
title: Aspose.Note にタグ付きのテーブル ノードを追加する
linktitle: Aspose.Note にタグ付きのテーブル ノードを追加する
second_title: Aspose.Note .NET API
description: Aspose.Note for .NET でタグ付きのテーブルを追加する方法を学びます。プログラムによるドキュメント操作スキルを強化します。
weight: 11
url: /ja/net/tag-management/add-table-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note にタグ付きのテーブル ノードを追加する

## 導入

このチュートリアルでは、Aspose.Note for .NET を使用してタグを持つテーブル ノードを追加するプロセスを説明します。これを実現するには、以下の手順に従ってください。

## 名前空間のインポート

開始する前に、Aspose を使用するために必要な名前空間をインポートしてください。注:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## 前提条件

続行する前に、次の前提条件が設定されていることを確認してください。

1. インストール: Aspose.Note for .NET ライブラリを次のサイトからダウンロードしてインストールします。[ここ](https://releases.aspose.com/note/net/).
2. ライセンス: ライセンスを取得するか、[仮免許](https://purchase.aspose.com/temporary-license/)図書館を利用するために。
3. 開発環境: Visual Studio など、互換性のある開発環境をセットアップします。

## ステップ 1: ドキュメントとページのオブジェクトを初期化する

まず、のインスタンスを作成します。`Document`クラスと初期化`Page`物体：

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## ステップ 2: テーブル、行、セル オブジェクトを作成する

を初期化します`Table`, `TableRow`、 そして`TableCell`オブジェクト:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## ステップ 3: コンテンツをセルに挿入する

を使用してコンテンツをセルに追加します。`AppendChildLast`方法：

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## ステップ 4: テーブル ノードを初期化する

を初期化します`Table`指定されたプロパティを持つオブジェクト:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## ステップ 5: テーブルに行を追加する

行ノードをテーブルに追加します。

```csharp
table.AppendChildLast(row);
```

## ステップ 6: テーブルノードにタグを追加する

テーブル ノードのタグを含めます。

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## ステップ 7: テーブル ノードをアウトライン要素に追加する

を作成します`Outline`そして`OutlineElement`テーブルノードを追加するには:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## ステップ 8: ドキュメントを保存する

OneNote ドキュメントを保存します。

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

これらの手順を実行すると、Aspose.Note for .NET を使用してタグを持つテーブル ノードが正常に追加されるはずです。

## 結論

このチュートリアルでは、Aspose.Note for .NET でタグを使用してテーブル ノードを追加するプロセスについて説明しました。これらの手順に従うと、OneNote ドキュメントをプログラムで効率的に操作でき、ドキュメント管理機能が強化されます。

## よくある質問

### Q1: Aspose.Note は、.NET のすべてのバージョンと互換性がありますか?

A1: Aspose.Note for .NET は、.NET Core および .NET Standard を含む .NET Framework バージョン 2.0 以降をサポートします。

### Q2: ライセンスを購入する前に、Aspose.Note を試すことはできますか?

 A2: はい、Aspose.Note の無料トライアルを次のサイトから入手できます。[ここ](https://releases.aspose.com/).

### Q3: Aspose.Note の一時ライセンスを取得するにはどうすればよいですか?

 A3: 一時ライセンスは以下から取得できます。[このリンク](https://purchase.aspose.com/temporary-license/)、有効期限は 30 日間です。

### Q4: Aspose.Note はドキュメントの暗号化をサポートしていますか?

A4: はい、Aspose.Note は、データのセキュリティを確保するために OneNote ドキュメントの暗号化をサポートしています。

### Q5: Aspose.Note ユーザーはテクニカル サポートを利用できますか?

 A5: はい、技術サポートは Aspose フォーラムを通じて提供されます。[ここ](https://forum.aspose.com/c/note/28)、専門家に支援を求めることができます。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
