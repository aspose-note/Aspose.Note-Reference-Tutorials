---
title: Aspose.Note for .NET によるダーク テーマの変換
linktitle: Aspose.Note のテキストにダーク テーマを適用する
second_title: Aspose.Note .NET API
description: Aspose.Note for .NET を使用して OneNote ドキュメントを変換します。洗練されたダークテーマを簡単に適用します。今すぐダウンロードして、メモ取りのエクスペリエンスを強化してください。
type: docs
weight: 11
url: /ja/net/text-manipulation/apply-dark-theme-text/
---
## 導入
Aspose.Note for .NET のテキストにダーク テーマを適用するためのステップバイステップ ガイドへようこそ。 Aspose.Note は、開発者がプログラムで Microsoft OneNote ファイルを操作できるようにする強力な .NET API です。このチュートリアルでは、テキストにダーク テーマを適用することで、OneNote ドキュメントに洗練されたモダンな外観を与える方法を説明します。
## 前提条件
チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。
-  Aspose.Note for .NET: Aspose.Note for .NET がインストールされていることを確認してください。そうでない場合は、からダウンロードできます。[Aspose.Note ドキュメント](https://reference.aspose.com/note/net/).
- 開発環境: Visual Studio など、好みの .NET 開発環境をセットアップします。
- ドキュメント ディレクトリ: OneNote ドキュメントが配置されるディレクトリを準備します。
## 名前空間のインポート
.NET プロジェクトで、Aspose を使用するために必要な名前空間をインポートします。注:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## ステップ 1: OneNote ドキュメントをロードする
次のコードを使用して、OneNote ドキュメントを Aspose.Note に読み込みます。
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "Your Document Directory";
//ドキュメントを Aspose.Note にロードします。
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## ステップ 2: 背景色の設定
各ページの背景色を黒に設定します。
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## ステップ 3: テキストの色を調整する
見やすくするために、テキストのフォントの色を白に調整します。
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## ステップ 4: ドキュメントを保存する
変更した OneNote ドキュメントを PDF として保存します。
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## 結論
おめでとう！ Aspose.Note ドキュメント内のテキストにダーク テーマを適用することに成功しました。このシンプルかつ効果的な機能強化により、OneNote ファイルの外観がより洗練されたものになります。
## よくある質問
### OneNote ドキュメントの特定のセクションにダーク テーマを適用できますか?
はい、コードをカスタマイズして、ドキュメント内の特定のページまたはセクションをターゲットにすることができます。
### Aspose.Note は PDF 以外のエクスポート形式をサポートしていますか?
絶対に！ Aspose.Note は、画像や Microsoft Word などのさまざまなエクスポート形式をサポートしています。
### Aspose.Note が処理できるドキュメント サイズに制限はありますか?
Aspose.Note はさまざまなサイズのドキュメントを処理でき、そのパフォーマンスは効率化のために最適化されています。
### ダークテーマを適用した後、元のテーマに戻すことはできますか?
はい、コードを変更して、好みに応じてテーマを切り替えることができます。
### Aspose.Note 関連のクエリのサポートはどこで受けられますか?
サポートが必要な場合は、次のサイトにアクセスしてください。[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28)または、[ドキュメンテーション](https://reference.aspose.com/note/net/).