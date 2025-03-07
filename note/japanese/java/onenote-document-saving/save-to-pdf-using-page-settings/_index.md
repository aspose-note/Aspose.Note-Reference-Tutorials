---
title: OneNote のページ設定を使用して PDF に保存 - Aspose.Note
linktitle: OneNote のページ設定を使用して PDF に保存 - Aspose.Note
second_title: Aspose.Note Java API
description: Aspose.Note ライブラリを使用して Java で OneNote ドキュメントを PDF に保存する方法を学びます。さまざまなページ設定のコード例を含むステップバイステップのガイド。
weight: 19
url: /ja/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote のページ設定を使用して PDF に保存 - Aspose.Note

## 導入

このチュートリアルでは、Aspose.Note for Java でさまざまなページ設定を使用して OneNote ドキュメントを PDF 形式で保存する方法を学習します。レターページ設定で保存する方法と、高さ制限なしの A4 ページ設定で保存する 2 つの方法について説明します。

## 前提条件

始める前に、次の前提条件が満たされていることを確認してください。

1. Java Development Kit (JDK) がシステムにインストールされています。
2. Aspose.Note for Java ライブラリがダウンロードされ、Java プロジェクトに組み込まれます。
3. Java プログラミング言語の基本的な理解。

## パッケージのインポート

プロジェクトで Aspose.Note for Java を使用するために必要なパッケージがインポートされていることを確認してください。 import ステートメントは次のとおりです。

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## レターページ設定を使用して PDF に保存

### ステップ 1: ドキュメントをロードする

まず、OneNote ドキュメントを Aspose.Note に読み込みます。

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### ステップ 2: 宛先パスを定義する

PDF ファイルの宛先パスを指定します。

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### ステップ 3: ドキュメントを保存する

レターページ設定を使用してドキュメントを保存します。

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## 高さ制限なしの A4 ページ設定を使用して PDF に保存

### ステップ 1: ドキュメントをロードする

同様に、OneNote ドキュメントを Aspose.Note に読み込みます。

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### ステップ 2: 宛先パスを定義する

PDF ファイルの宛先パスを指定します。

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### ステップ 3: ドキュメントを保存する

高さ制限なしの A4 ページ設定でドキュメントを保存します。

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

これらの手順を実行すると、さまざまなページ設定を使用して OneNote ドキュメントを PDF に保存できます。

## 結論

このチュートリアルでは、Aspose.Note for Java ライブラリを使用して OneNote ドキュメントを PDF 形式で保存する方法を説明しました。ステップバイステップのガイドに従うことで、この機能を Java アプリケーションに簡単に統合できます。

## よくある質問

### Q1: ページ設定をさらにカスタマイズできますか?

A1: はい、Aspose.Note for Java を使用して、要件に応じてページ設定をカスタマイズできます。

### Q2: Aspose.Note は PDF 以外の他の出力形式をサポートしていますか?

A2: はい、Aspose.Note は画像や HTML などのさまざまな出力形式をサポートしています。

### Q3: Aspose.Note は、OneNote ファイルのさまざまなバージョンと互換性がありますか?

A3: はい、Aspose.Note は、.one や .onetoc2 などのさまざまなバージョンの OneNote ファイルをサポートしています。

### Q4: 複数の OneNote ファイルを 1 回の実行で PDF に変換できますか?

A4: はい、Aspose.Note for Java を使用して複数の OneNote ファイルをバッチ処理できます。

### Q5: テスト目的で利用できる試用版はありますか?

A5: はい、Web サイトから Aspose.Note for Java の無料トライアルを入手できます。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
