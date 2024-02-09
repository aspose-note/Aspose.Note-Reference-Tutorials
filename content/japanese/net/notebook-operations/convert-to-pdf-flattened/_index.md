---
title: Aspose Note .NET でノートブックを PDF (フラット化) に変換する
linktitle: Aspose Note .NET でノートブックを PDF (フラット化) に変換する
second_title: Aspose.Note .NET API
description: Aspose.Note for .NET を使用して、OneNote ノートブックをフラット化された PDF に簡単に変換する方法を学びます。コンテンツをシームレスに保存します。
type: docs
weight: 15
url: /ja/net/notebook-operations/convert-to-pdf-flattened/
---
## 導入

Aspose Note .NET を使用して、OneNote ノートブックをフラット化された PDF に変換したいと考えていますか?あなたは正しい場所にいます！このチュートリアルでは、プロセスを段階的に説明します。

## 前提条件

始める前に、以下のものがあることを確認してください。

1.  Aspose.Note for .NET: Aspose.Note for .NET をダウンロードしてインストールしていることを確認してください。そうでない場合は、から入手できます[ここ](https://releases.aspose.com/note/net/).
2. Visual Studio: コーディングとコンパイルのために、システムに Visual Studio がインストールされている必要があります。
3. OneNote ノートブック: PDF に変換する OneNote ノートブックを用意します。

## 名前空間のインポート

まずは、C# コードに必要な名前空間をインポートします。

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## ステップ 1: OneNote ノートブックをロードする

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "Your Document Directory";

// OneNote ノートブックをロードする
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

この手順では、次のコマンドを使用して OneNote ノートブックを読み込みます。`Notebook` Aspose.Note によって提供されるクラス。

## ステップ 2: フラット化を使用して PDF に変換する

```csharp
//ノートブックをフラット化して PDF として保存する
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

ここでは、読み込んだノートブックを PDF として保存します。`Flatten`に設定されたプロパティ`true`。このプロパティは、注釈や画像を含むすべてのコンテンツを PDF にフラット化します。

## ステップ 3: 成功メッセージを印刷する

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

最後に、成功メッセージと PDF が保存されるパスを出力します。

## 結論

おめでとう！ Aspose.Note for .NET を使用して、OneNote ノートブックをフラット化された PDF に変換することに成功しました。このプロセスにより、すべてのコンテンツが PDF 形式で正確に保存され、共有や配布が容易になります。

## よくある質問

### Q1: インタラクティブな要素を PDF に保存できますか?

A1: Aspose.Note は、チェックボックスやフォーム フィールドなどのインタラクティブな要素を含むコンテンツを PDF にフラット化し、静的にします。

### Q2: Aspose.Note はノートブックの他の形式への変換をサポートしていますか?

A2: はい、Aspose.Note は、PDF、HTML、画像などのさまざまな形式へのノートブックの変換をサポートしています。

### Q3: 変換オプションをカスタマイズできますか?

A3：もちろんです！ Aspose.Note には、変換プロセス中にカスタマイズ用の広範なオプションが用意されており、要件に応じて出力を調整できます。

### Q4: 体験版はありますか?

 A4: はい、Aspose.Note の無料トライアルを次のサイトから入手できます。[ここ](https://releases.aspose.com/).

### Q5: 問題が発生した場合はどこでサポートを受けられますか?

 A5: Aspose コミュニティからのサポートを求めることができます。[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28).