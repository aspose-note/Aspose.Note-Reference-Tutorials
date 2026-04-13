---
date: 2026-04-13
description: .NET と Aspose.Note を使用して、画像ストリームで OneNote ドキュメントに画像を追加する方法を学びましょう。このステップバイステップガイドでは、ストリームから画像を読み込み、アウトラインに画像を追加し、ファイルを保存する手順を解説しています。
keywords:
- add image to onenote
- how to insert image
- load image from stream
- append image to outline
- image stream .net
linktitle: Aspose.Note を使用して画像ストリームで OneNote に画像を追加
second_title: Aspose.Note .NET API
title: Aspose.Note を使用して画像ストリームで OneNote に画像を追加
url: /ja/net/images/insert-image-using-image-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note を使用した画像ストリームで OneNote に画像を追加する

## はじめに

このチュートリアルでは、**画像を OneNote に追加する方法**を学びます。画像をストリームから読み込み、Aspose.Note for .NET を使用してアウトラインに追加します。レポートツール、ノートアプリ、ドキュメント自動化など、プログラムで画像を挿入することで OneNote ファイルがより魅力的で実用的になります。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.Note for .NET（無料トライアル利用可能）。  
- **サポートされている .NET バージョンはどれですか？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6 以上。  
- **ストリームから画像を読み込めますか？** はい – `FileStream` または任意の `Stream` 実装を使用します。  
- **画像の配置を制御するにはどうすればよいですか？** `Alignment` プロパティを設定します（例: `HorizontalAlignment.Right`）。  
- **生成されるファイル形式は何ですか？** Microsoft OneNote で開くことができる OneNote（`.one`）ファイルです。

## OneNote に画像を追加するとは？

OneNote ファイルに画像を追加することは、ページのコンテンツ階層内に視覚要素を直接埋め込むことを意味します。Aspose.Note では `Document`、`Page`、`Outline`、`OutlineElement` などのオブジェクトを使用します。`Image` オブジェクトを `OutlineElement` に挿入することで、画像は OneNote ページのレイアウトの一部となります。

## 画像挿入に Aspose.Note を使用する理由

- **Office のインストールは不要** – サーバー上で OneNote ファイルを生成または変更できます。  
- **レイアウトを完全に制御** – 画像を必要な場所に正確に配置、サイズ変更、位置決めできます。  
- **ストリーム対応** – 任意の `Stream` と連携でき、クラウドストレージやメモリのみのシナリオに最適です。  
- **クロスプラットフォーム** – Windows、Linux、macOS の .NET ランタイムと互換性があります。

## 前提条件

1. **開発環境** – Visual Studio 2022 または任意の .NET 対応 IDE。  
2. **Aspose.Note ライブラリ** – 公式サイトからダウンロードしてください [here](https://releases.aspose.com/note/net/)。  
3. **画像ファイル** – 埋め込みたい画像（JPG、PNG、BMP、GIF、または TIFF）を少なくとも1枚用意してください。  
4. **基本的な C# の知識** – ファイル操作やオブジェクト指向コードに慣れていること。

## 名前空間のインポート
まず、Aspose.Note のクラスと標準 .NET I/O ユーティリティにアクセスできる名前空間をインポートします。

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Now let’s walk through the process step‑by‑step.

### 手順 1: Document オブジェクトの初期化
OneNote ファイルを保持する新しい `Document` インスタンスを作成します。

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

### 手順 2: Page オブジェクトの作成
OneNote ファイルは 1 つ以上のページで構成されます。ここではコンテンツをホストする新しいページを作成します。

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### 手順 3: Outline と OutlineElement オブジェクトの初期化
Outline はリッチコンテンツ（テキスト、画像、テーブル）のコンテナです。`OutlineElement` は実際に項目を保持する子要素です。

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```

### 手順 4: ストリームから画像を読み込む
`FileStream`（または任意の `Stream`）を使用して画像ファイルを読み込み、`Image` オブジェクトを作成します。ここが **load image from stream** キーワードが活きるポイントです。

```csharp
using (FileStream fs = File.OpenRead(dataDir + "image.jpg"))
{
    Aspose.Note.Image image1 = new Aspose.Note.Image(doc, "Penguins.jpg", fs)
    {
        Alignment = HorizontalAlignment.Right
    };
    outlineElem1.AppendChildLast(image1);
}
```

### 手順 5: Image を OutlineElement に追加する
画像は現在 `OutlineElement` の一部です。この手順は **append image to outline** 機能を示しています。

```csharp
outlineElem1.AppendChildLast(image1);
```

### 手順 6: OutlineElement を Outline に追加する
ここで、画像を含む要素を Outline コンテナに添付します。

```csharp
outline1.AppendChildLast(outlineElem1);
```

### 手順 7: Outline を Page に追加する
画像を含む Outline がページに追加されます。

```csharp
page.AppendChildLast(outline1);
```

### 手順 8: Page を Document に追加する
ページの準備ができたら、ドキュメント階層に挿入します。

```csharp
doc.AppendChildLast(page);
```

### 手順 9: Document を保存する
最後に、OneNote ファイルをディスクに保存します。生成されたファイルは Microsoft OneNote で開くことができます。

```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```

## よくある問題と解決策

| 問題 | 発生原因 | 修正 |
|-------|----------------|-----|
| **画像が表示されない** | 画像が追加される前にストリームが閉じられました。 | （示されているように）`AppendChildLast` 呼び出しの周りに `using` ブロックを保持してください。 |
| **配置が正しくない** | `Alignment` プロパティが設定されていない、または後で上書きされています。 | `Image` 作成時に `Alignment` を設定するか、追加前に `image1.Alignment` を変更してください。 |
| **サポートされていない画像形式** | Aspose.Note が認識しない形式の画像を読み込もうとしています。 | 画像を JPG、PNG、BMP、GIF、または TIFF に変換してください。 |
| **ファイルパスエラー** | `dataDir` が存在しないフォルダーを指しています。 | `Path.Combine` を使用し、実行前にフォルダーが存在することを確認してください。 |

## よくある質問

**Q: この方法で単一のドキュメントに複数の画像を挿入できますか？**  
A: はい。各画像について *Load Image from Stream* と *Append Image to OutlineElement* の手順を繰り返すだけです。

**Q: Aspose.Note は JPG 以外の画像形式もサポートしていますか？**  
A: もちろんです。PNG、BMP、GIF、TIFF すべてがサポートされています。

**Q: 挿入した画像の配置やサイズをカスタマイズできますか？**  
A: はい。`Alignment` に加えて、`Image` オブジェクトの `Width`、`Height`、`Scale` プロパティを設定できます。

**Q: Aspose.Note はすべての .NET バージョンと互換性がありますか？**  
A: .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5、.NET 6 以上で動作します。

**Q: Aspose.Note の追加リソースやサポートはどこで見つけられますか？**  
A: 包括的なドキュメント、フォーラム、サポートは [Aspose Forum](https://forum.aspose.com/c/note/28) で見つけられます。

---

**最終更新日:** 2026-04-13  
**テスト済み:** Aspose.Note 24.11 for .NET  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}