---
title: Aspose.Note のテキストに箇条書きを適用する
linktitle: Aspose.Note のテキストに箇条書きを適用する
second_title: Aspose.Note .NET API
description: Aspose.Note for .NET のテキストに箇条書きを適用して、OneNote ドキュメントを強化する方法を学びます。効果的なフォーマットを行うには、このステップバイステップのガイドに従ってください。
weight: 10
url: /ja/net/text-manipulation/apply-bullets-on-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note のテキストに箇条書きを適用する

## 導入
Aspose.Note for .NET を使用してテキストに箇条書きを適用するためのこのステップバイステップ ガイドへようこそ。 Aspose.Note は、開発者が .NET アプリケーションで Microsoft OneNote ファイルをシームレスに操作できるようにする強力なライブラリです。このチュートリアルでは、テキストに箇条書きを適用して、OneNote ドキュメントの視覚的な魅力を高めるプロセスを説明します。
## 前提条件
チュートリアルに入る前に、次の前提条件を満たしていることを確認してください。
- C# および .NET プログラミングの基本的な知識。
-  Aspose.Note for .NET ライブラリがインストールされています。ダウンロードできます[ここ](https://releases.aspose.com/note/net/).
## 名前空間のインポート
C# コードには、必要な名前空間を必ず含めてください。
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## ステップ 1: ドキュメントを設定する
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "Your Document Directory";
//Documentクラスのオブジェクトを作成する
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## ステップ 2: ページとアウトラインを初期化する
```csharp
// Pageクラスオブジェクトの初期化
Aspose.Note.Page page = new Aspose.Note.Page(doc);
//アウトラインクラスオブジェクトの初期化
Outline outline = new Outline(doc);
```
## ステップ 3: デフォルトのテキストスタイルを設定する
```csharp
//TextStyle クラス オブジェクトを初期化し、書式設定プロパティを設定します。
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## ステップ 4: 箇条書きを含むアウトライン要素を作成する
```csharp
//OutlineElement クラス オブジェクトを初期化して箇条書きを適用する
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
//他のアウトライン要素についても繰り返します
```
## ステップ 5: アウトライン要素をアウトラインに追加する
```csharp
//アウトライン要素を追加する
outline.AppendChildLast(outlineElem1);
//他のアウトライン要素についても繰り返します
```
## ステップ 6: ページにアウトラインを追加する
```csharp
//アウトラインノードの追加
page.AppendChildLast(outline);
```
## ステップ 7: ドキュメントにページを追加する
```csharp
//ページノードの追加
doc.AppendChildLast(page);
```
## ステップ 8: OneNote ドキュメントを保存する
```csharp
// OneNote ドキュメントを保存する
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## 結論
おめでとう！ Aspose.Note for .NET を使用してテキストに箇条書きを適用する方法を学習しました。この機能により、OneNote ドキュメントの書式設定が大幅に強化され、見た目がより魅力的になります。
## よくある質問
### リスト内の各項目に異なる箇条書きスタイルを適用できますか?
はい、箇条書きスタイルは、`NumberList`それぞれのプロパティ`OutlineElement`.
### Aspose.Note は Microsoft OneNote の最新バージョンと互換性がありますか?
Aspose.Note は Microsoft OneNote のさまざまなバージョンをサポートし、古いバージョンと新しいバージョンの両方との互換性を保証します。
### Aspose.Note を商用目的で使用できますか?
はい、商用プロジェクトで Aspose.Note for .NET を使用できます。ライセンスを取得するには、次のサイトにアクセスしてください[ここ](https://purchase.aspose.com/buy).
### Aspose.Note for .NET の試用版はありますか?
はい、無料トライアルをダウンロードできます[ここ](https://releases.aspose.com/).
### 追加のサポートやリソースはどこで入手できますか?
 Aspose.Note コミュニティ フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/note/28)サポートとディスカッションのため。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
