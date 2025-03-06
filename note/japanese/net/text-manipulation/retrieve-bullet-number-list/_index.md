---
title: Aspose.Note テキストの箇条書きまたは番号リストを取得する
linktitle: Aspose.Note テキストの箇条書きまたは番号リストを取得する
second_title: Aspose.Note .NET API
description: 箇条書きまたは番号リストの取得に関するステップバイステップのガイドを使用して、Aspose.Note for .NET の可能性を解き放ちます。 OneNote ドキュメントの操作スキルを向上させましょう。
weight: 23
url: /ja/net/text-manipulation/retrieve-bullet-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note テキストの箇条書きまたは番号リストを取得する

## 導入
Aspose.Note for .NET の世界へようこそ。これは、開発者が OneNote ドキュメントの操作を簡単に処理できるようにする、堅牢で多用途のライブラリです。このチュートリアルでは、Aspose.Note for .NET を使用して箇条書きまたは番号リストを取得するプロセスを詳しく説明します。経験豊富な開発者であっても、コーディング愛好家であっても、このガイドは、Aspose.Note でのリストの操作の複雑さをナビゲートするための知識を提供します。
## 前提条件
このコーディング作業に着手する前に、次の前提条件が満たされていることを確認してください。
-  Aspose.Note for .NET: Aspose.Note ライブラリがインストールされていることを確認してください。そうでない場合は、からダウンロードできます。[Aspose.Note for .NET ドキュメント](https://reference.aspose.com/note/net/).
- 開発環境: 作業可能な開発環境 (できれば Microsoft Visual Studio) をマシン上にセットアップします。
- C# の基本知識: このチュートリアルは C# 言語で書かれているため、C# に慣れてください。
## 名前空間のインポート
Aspose.Note for .NET と対話するには、必要な名前空間をプロジェクトにインポートする必要があります。コードの先頭に次の名前空間を含めます。
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
ここで、箇条書きリストまたは番号リストを取得するプロセスを段階的に見てみましょう。
## ステップ 1: ドキュメント ディレクトリを設定する
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "Your Document Directory";
```
交換する`"Your Document Directory"`Aspose.Note ドキュメントが配置されている実際のパスに置き換えます。
## ステップ 2: ドキュメントをロードする
```csharp
//ドキュメントを Aspose.Note にロードします。
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
必ず交換してください`"ApplyNumberingOnText.one"`特定の OneNote ドキュメントの名前を付けます。
## ステップ 3: ノードのコレクションを取得する
```csharp
//アウトライン要素のノードのコレクションを取得します。
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
このステップでは、ロードされたドキュメントからアウトライン ノードのコレクションを取得します。
## ステップ 4: 各ノードを反復処理する
```csharp
//各ノードを反復処理します。
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        //次の手順に進みます...
    }
}
```
このループにより、数値リストを含むノードのみを処理することが保証されます。
## ステップ 5: フォント情報を取得する
```csharp
//フォント名の取得
Console.WriteLine("Font Name: " + list.Font);
//フォントの長さを取得する
Console.WriteLine("Font Length: " + list.Font.Length);
//フォントサイズを取得する
Console.WriteLine("Font Size: " + list.FontSize);
//フォントの色の取得
Console.WriteLine("Font Color: " + list.FontColor);
//取得形式
Console.WriteLine("Font format: " + list.Format);
//太字にチェックを入れる
Console.WriteLine("Is bold: " + list.IsBold);
//斜体をチェックする
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
これらのコード行は、数値リストからさまざまなフォント関連の情報を抽出します。
## 結論
おめでとう！ Aspose.Note for .NET を使用して箇条書きリストまたは番号リストを取得する方法を学習しました。探索を続けるときは、以下を参照してください。[ドキュメンテーション](https://reference.aspose.com/note/net/)より詳細な洞察と機能が得られます。
## よくある質問
### Aspose.Note for .NET を他のプログラミング言語で使用できますか?
Aspose.Note は主に .NET をサポートしていますが、さまざまなプラットフォームや言語に合わせて調整された他のバージョンのライブラリもあります。
### Aspose.Note は最新の OneNote 形式と互換性がありますか?
はい、Aspose.Note は幅広い OneNote 形式をサポートし、最新バージョンとの互換性を保証します。
### Aspose.Note の一時ライセンスを取得するにはどうすればよいですか?
訪問[このリンク](https://purchase.aspose.com/temporary-license/)評価目的で一時ライセンスを取得します。
### Aspose.Note ユーザーはどのようなサポート オプションを利用できますか?
を探索して支援を求めることができます。[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28)発生する可能性のある質問や問題については、
### Aspose.Note for .NET の無料試用版はありますか?
はい、Aspose.Note for .NET の無料試用版にアクセスできます。[ここ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
