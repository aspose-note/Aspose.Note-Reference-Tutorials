---
title: Aspose.Note テキストに中国語の数字リストを挿入
linktitle: Aspose.Note テキストに中国語の数字リストを挿入
second_title: Aspose.Note .NET API
description: Aspose.Note for .NET ドキュメントに中国語の数字リストを簡単に挿入する方法を学びます。このステップバイステップのガイドを使用して、文書の書式設定スキルを向上させてください。
type: docs
weight: 20
url: /ja/net/text-manipulation/insert-chinese-number-list/
---
## 導入
中国語の番号リストをドキュメントに組み込んで、Aspose.Note for .NET のスキルを強化したいと考えていますか?もしそうなら、あなたは正しい場所にいます！このチュートリアルでは、Aspose.Note for .NET を使用して中国語の数字リストを挿入するプロセスを説明します。この強力なライブラリを使用すると、OneNote ドキュメントをシームレスに操作できます。
## 前提条件
チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。
- C# プログラミングの基本的な知識。
-  Aspose.Note for .NET がインストールされています。ダウンロードできます[ここ](https://releases.aspose.com/note/net/).
## 名前空間のインポート
まず、必要な名前空間をプロジェクトにインポートします。
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## ステップ 1: OneNote ドキュメントを初期化する
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## ステップ 2: OneNote ページを初期化する
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## ステップ 3: テキスト スタイル設定を適用する
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## ステップ 4: アウトライン要素を作成する
次に、中国語の数字リストを使用して 3 つのアウトライン要素を作成しましょう。
### ステップ 4.1: 最初の要素
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### ステップ 4.2: 2 番目の要素
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### ステップ 4.3: 3 番目の要素
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## ステップ 5: アウトラインに要素を追加する
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## ステップ 6: ページにアウトラインを追加する
```csharp
page.AppendChildLast(outline);
```
## ステップ 7: ドキュメントにページを追加する
```csharp
doc.AppendChildLast(page);
```
## ステップ 8: OneNote ドキュメントを保存する
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
おめでとう！ .NET ライブラリを使用して、中国語の数字リストを Aspose.Note ドキュメントに挿入することができました。
## 結論
このチュートリアルでは、中国語の数字リストを Aspose.Note for .NET ドキュメントに組み込むプロセスを段階的に説明しました。これらのテクニックを使用して、ドキュメントの書式設定スキルを強化し、コンテンツをより魅力的なものにしましょう。
## よくある質問
### Q: 中国語の数字リストの書式をカスタマイズできますか?
 A: はい、パラメータを調整することで書式をカスタマイズできます。`NumberList`コンストラクタ。
### Q: Aspose.Note は .NET の最新バージョンと互換性がありますか?
A: はい、Aspose.Note は、.NET の最新バージョンをサポートするために定期的に更新されます。
### Q: 追加の例やドキュメントはどこで入手できますか?
A: 包括的な内容を確認してください[Aspose.Note ドキュメント](https://reference.aspose.com/note/net/).
### Q: Aspose.Note の一時ライセンスを取得するにはどうすればよいですか?
 A: 一時ライセンスを取得します。[ここ](https://purchase.aspose.com/temporary-license/).
### Q: Aspose.Note 関連の質問についてサポートを求めたり、相談したりできる場所はどこですか?
 A: にアクセスしてください。[Aspose.Note サポート フォーラム](https://forum.aspose.com/c/note/28)コミュニティサポートのために。