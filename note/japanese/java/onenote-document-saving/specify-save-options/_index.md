---
title: OneNote で保存オプションを指定する - Aspose.Note
linktitle: OneNote で保存オプションを指定する - Aspose.Note
second_title: Aspose.Note Java API
description: Aspose.Note for Java を使用して OneNote で保存オプションを指定する方法を学習します。ページのインデックス、カウント、圧縮設定を簡単にカスタマイズします。
type: docs
weight: 24
url: /ja/java/onenote-document-saving/specify-save-options/
---
## 導入

このチュートリアルでは、Aspose.Note for Java を使用して OneNote で保存オプションを指定する方法を学習します。 Aspose.Note は、開発者がプログラムで OneNote ドキュメントを作成、操作、変換できるようにする強力な Java ライブラリです。 Aspose.Note を使用すると、さまざまな保存オプションを簡単に制御して、要件に応じて出力をカスタマイズできます。

## 前提条件

始める前に、次の前提条件を満たしていることを確認してください。

1. Java プログラミング言語の基本的な知識。
2. JDK (Java Development Kit) がシステムにインストールされていること。
3.  Java ライブラリの Aspose.Note がインストールされています。からダウンロードできます[ここ](https://releases.aspose.com/note/java/).

## パッケージのインポート

まず、必要なパッケージを Java コードにインポートします。

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

この例を複数のステップに分けてみましょう。

## ステップ 1: OneNote ドキュメントをロードする

```java
//ドキュメントディレクトリへのパス。
String dataDir = "Your Document Directory";

//ドキュメントを Aspose.Note にロードします。
Document doc = new Document(dataDir + "Aspose.one");
```

この手順では、OneNote ドキュメントへのパスを指定し、それを`Document`物体。

## ステップ 2: PdfSaveOptions オブジェクトを初期化する

```java
// PdfSaveOptions オブジェクトを初期化する
PdfSaveOptions opts = new PdfSaveOptions();
```

ここでは、`PdfSaveOptions`ドキュメントを PDF として保存するためのオプションを指定するために使用されるオブジェクト。

## ステップ 3: ページインデックスとページ数を設定する

```java
//ページインデックスを設定する
opts.setPageIndex(2);

//ページ数を設定する
opts.setPageCount(3);
```

これらの行は、保存するページのインデックスとカウントを設定します。この例では、インデックス 2 から開始して合計 3 ページを保存しています。

## ステップ 4: 圧縮設定を指定する

```java
//必要に応じて圧縮を指定します
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

ここでは、PDF の画像圧縮設定を指定します。圧縮を JPEG 形式に設定し、JPEG 品質を 90% に指定します。

## ステップ 5: オプションを指定してドキュメントを保存する

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

最後に、指定したオプションを使用してドキュメントを保存します。出力 PDF は、指定されたオプションを使用して指定された場所に保存されます。

## 結論

このチュートリアルでは、Aspose.Note for Java を使用して OneNote で保存オプションを指定する方法を学習しました。保存オプションをカスタマイズすると、ページ インデックス、カウント、圧縮設定など、出力ドキュメントのさまざまな側面を制御できます。

## よくある質問

### Q1: Aspose.Note は大きな OneNote ドキュメントを処理できますか?

A1: はい、Aspose.Note は大きな OneNote ドキュメントを効率的に処理できるように設計されています。

### Q2: Aspose.Note は最新の Java バージョンと互換性がありますか?

A2: はい、Aspose.Note は最新の Java バージョンと互換性があります。

### Q3: Aspose.Note を使用して OneNote ドキュメントを他の形式に変換できますか?

A3: はい、Aspose.Note は、OneNote ドキュメントの PDF、DOCX、HTML などのさまざまな形式への変換をサポートしています。

### Q4: Aspose.Note は、OneNote ドキュメントの暗号化と復号化をサポートしていますか?

A4: はい、Aspose.Note は OneNote ドキュメントの暗号化と復号化のための API を提供します。

### Q5: Aspose.Note は商用利用に適していますか?

A5: はい、Aspose.Note はライセンスを購入することで商用目的で使用できます。