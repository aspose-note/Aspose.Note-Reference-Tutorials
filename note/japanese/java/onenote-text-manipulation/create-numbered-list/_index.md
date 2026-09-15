---
date: 2026-03-05
description: Aspose.Note for Java を使用して番号付きリストを作成しながら OneNote を PDF として保存する方法を学びます。デフォルトのテキストスタイルの設定と番号付けのカスタマイズ手順が含まれています。
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: OneNote を PDF に保存 – Aspose.Note で番号付きリストを作成
url: /ja/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote を PDF として保存 – Aspose.Note で番号付きリストを作成

## はじめに
Aspose.Note for Java は、Java 開発者が **OneNote を PDF として保存** し、番号付きリストなどの高度な書式設定でドキュメントを強化できるようにします。このチュートリアルでは、デフォルトのテキストスタイルの設定から番号書式のカスタマイズまで、OneNote を PDF にエクスポートしてプロフェッショナルな外観にするための全工程をご案内します。

## クイック回答
- **このチュートリアルの内容は何ですか？** OneNote で番号付きリストを作成し、Aspose.Note for Java を使用してファイルを PDF として保存します。  
- **対象の主要キーワードは何ですか？** *save onenote as pdf*  
- **ライセンスは必要ですか？** 無料トライアルが利用可能です。商用利用には商用ライセンスが必要です。  
- **必要な Java バージョンは？** JDK 8 以降。  
- **実装にかかる時間は？** 基本的なリストで約 10〜15 分です。

## 「OneNote を PDF として保存」とは？
OneNote を PDF として保存すると、リッチテキストの OneNote ページがポータブルで固定レイアウトのドキュメントに変換され、OneNote がインストールされていない環境でもプラットフォーム間で共有できます。これは、アーカイブ、レポート作成、または OneNote をインストールしていないユーザーへのコンテンツ配布に特に有用です。

## エクスポート前に番号付きリストを作成する理由
番号付きリストは構造と可読性を高め、エクスポートされた PDF を洗練されたレポートのように見せます。Aspose.Note を使用すれば、**番号書式をカスタマイズ** したり、フォントや行間を設定したりでき、元の OneNote のレイアウトを保持したまま調整できます。

## 前提条件
- Java Development Kit (JDK) がマシンにインストールされていること。  
- Aspose.Note for Java ライブラリを [here](https://releases.aspose.com/note/java/) からダウンロードすること。  

## パッケージのインポート
まず、必要なクラスをインポートして OneNote オブジェクトと PDF 変換を操作できるようにします。

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```

## 番号付きリストで OneNote を PDF として保存する方法
以下は、**リスト要素の作成**、**デフォルトテキストスタイルの設定**、そして最終的に **OneNote を PDF にエクスポート** する手順を示すステップバイステップガイドです。

### 手順 1: Document、Page、Outline オブジェクトの初期化
まず、OneNote の基本構造を作成します。これにより **add outline element java** の使用例も示されます。

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **プロのコツ:** `dataDir` パスは絶対パスで保持するか、`System.getProperty("user.dir")` を使用してパス問題を回避してください。

### 手順 2: デフォルトテキストスタイルの設定
一貫したスタイルにより、リスト全体の外観が統一されます。

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### 手順 3: Outline 要素の作成（番号付きリスト）
ここでは `NumberList` を使用して **番号書式をカスタマイズ** します。パターン `"{0})"` は “1)”、 “2)” などを生成します。

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **重要な理由:** 各 `OutlineElement` に `NumberList` を付与することで、番号スタイル、フォント、サイズを完全に制御できます。

### 手順 4: Outline 要素を Outline に追加
これで個々のリスト項目を単一の Outline にまとめます。

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### 手順 5: Outline を Page に添付
Outline は OneNote ページの階層構造の一部になります。

```java
page.appendChildLast(outline);
```

### 手順 6: ドキュメントを PDF として保存
最後に、**OneNote を PDF として保存** します。出力ファイルには定義通りの番号付きリストが含まれます。

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

上記のコードを実行すると、指定したディレクトリに `CreateNumberedList_out.pdf` という名前の PDF が生成され、番号付きリストの書式が保持されます。

## よくある問題と解決策
| 問題 | 解決策 |
|-------|----------|
| **PDF が空です** | `doc.appendChildLast(page);` が `doc.save()` の前に呼び出されていることを確認してください。 |
| **番号が表示されません** | `NumberList` のパターンと `NumberFormat` が正しく設定されているか確認してください。 |
| **ファイルが見つからないエラー** | `dataDir` を絶対パスで使用するか、事前にディレクトリを作成してください。 |
| **フォントが一致しません** | コードを実行するマシンにフォント（例: Arial）をインストールしてください。 |

## よくある質問
### Q: OneNote のリストで番号書式をカスタマイズできますか？
A: もちろんです！Aspose.Note for Java が提供する `NumberList` クラスを使用して番号書式をカスタマイズできます。

### Q: Aspose.Note for Java のトライアル版は利用可能ですか？
A: はい、無料トライアルを [here](https://releases.aspose.com/) からダウンロードできます。

### Q: Aspose.Note for Java のサポートはどのように受けられますか？
A: コミュニティサポートは [Aspose.Note for Java forum](https://forum.aspose.com/c/note/28) をご覧ください。

### Q: Aspose.Note for Java の詳細なドキュメントはどこで見つけられますか？
A: 包括的な情報は [documentation](https://reference.aspose.com/note/java/) を参照してください。

### Q: Aspose.Note for Java のライセンスはどのように購入できますか？
A: ライセンスは [here](https://purchase.aspose.com/buy) から購入できます。

## 結論
このチュートリアルでは、Aspose.Note for Java を使用してクリーンな番号付きリストを作成しながら **OneNote を PDF として保存** する方法を示しました。デフォルトのテキストスタイルを設定し、番号書式をカスタマイズし、ステップバイステップの手順に従うことで、OneNote ページから迅速かつ確実にプロフェッショナルな PDF を生成できます。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2026-03-05  
**テスト環境:** Aspose.Note for Java 24.11  
**作者:** Aspose  

---