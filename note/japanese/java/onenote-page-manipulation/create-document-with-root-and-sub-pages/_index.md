---
description: Aspose.Note for Java を使用して OneNote の PDF を保存し、サブページを追加する方法を学びましょう。ステップバイステップのガイドに従って、ノートを効率的に整理してください。
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: OneNoteのPDFを保存し、サブページを追加する方法
url: /ja/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote PDF の保存方法とサブページの追加

## はじめに

このチュートリアルでは、Aspose.Note for Java を使用して **OneNote PDF を保存** し、ルートページとサブページの両方を含むドキュメントを作成する方法をご紹介します。OneNote ノートブックを明確な階層構造で整理すれば、ナビゲーションが容易になり、PDF へのエクスポートにより、どこでも閲覧可能な形式でノートを共有できます。また、**サブページの追加** 方法も示すので、マルチレベルの構造を簡単に構築できます。

## クイック回答
- **主要キーワードは何を意味しますか？** Aspose.Note を使用して OneNote ノートブックを PDF にエクスポートすることを指します。  
- **使用している API はどれですか？** Aspose.Note for Java。  
- **階層ページを作成できますか？** はい – ページレベルを設定してルートページとサブページを構築できます。  
- **ライセンスは必要ですか？** 無料トライアルは利用可能ですが、本番環境では商用ライセンスが必要です。  
- **サポートされている出力形式は何ですか？** BMP、PDF、PNG など多数。

## 「OneNote PDF の保存方法」とは？

OneNote を PDF として保存すると、ノートブックのページが固定レイアウトのドキュメントに変換され、書式、画像、階層構造が保持されます。共有、アーカイブ、印刷に最適です。

## なぜサブページを追加するのか？

サブページを追加すると、関連コンテンツを親ページの下にグループ化でき、フォルダーのような構造が実現します。ノートの整理が向上し、検索が高速化され、PDF にエクスポートした際の閲覧体験も向上します。

## 前提条件

開始する前に、以下の前提条件を満たしていることを確認してください。

1. Java Development Kit (JDK): システムに JDK がインストールされていること。  
2. Aspose.Note for Java: [ウェブサイト](https://purchase.aspose.com/buy) からダウンロードしてインストール。  
3. 統合開発環境 (IDE): IntelliJ IDEA、Eclipse、NetBeans などの Java IDE を選択。

## パッケージのインポート

Java プロジェクトで必要なパッケージをインポートします:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## 手順 1: ドキュメントディレクトリの設定

OneNote ドキュメントを保存するディレクトリを定義します:

```java
String dataDir = "Your Document Directory";
```

## 手順 2: Document オブジェクトの作成

`Document` オブジェクトをインスタンス化します:

```java
Document doc = new Document();
```

## 手順 3: ページの作成

ページオブジェクトを初期化し、レベルを設定します。レベルを設定することで、ページがルートページかサブページかが決まります:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## 手順 4: ページへのノード追加

### 最初のページへのノード追加

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### 2 番目のページへのノード追加

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### 3 番目のページへのノード追加

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## 手順 5: ドキュメントへのページ追加

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## 手順 6: ドキュメントの保存

OneNote ドキュメントを PDF（この例では BMP）として保存します。`SaveFormat` を変更すれば PDF にエクスポートでき、「OneNote PDF の保存方法」の要件を満たします:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **プロのコツ:** PDF に直接エクスポートするには、`SaveFormat.Bmp` を `SaveFormat.Pdf` に置き換えてください。

おめでとうございます！Aspose.Note for Java を使用して、ルートページとサブページを持つ OneNote ドキュメントを作成し、**OneNote PDF の保存方法** を習得しました。

## なぜ重要なのか

- **階層的な整理:** ルートページとサブページにより、OneNote 内でフォルダー構造を模倣できます。  
- **シームレスな PDF エクスポート:** 整理された状態で PDF にエクスポートすれば、階層が保持され、最終ドキュメントが読みやすく共有しやすくなります。  
- **自動化:** このコードは大規模な Java アプリケーションに組み込めるため、構造化されたノートブックのバッチ作成が可能です。

## よくある落とし穴と回避策

| 問題 | 原因 | 解決策 |
|------|------|--------|
| ページが同じレベルに表示される | `setLevel` の値が誤っている | ルートページは `setLevel((byte) 1)`、サブページは `setLevel((byte) 2)`（またはそれ以上）を使用 |
| PDF 出力が空白になる | `SaveFormat.Pdf` が指定されていない、またはファイルパスが誤っている | ディレクトリが存在することを確認し、`SaveFormat.Pdf` を使用 |
| フォントが適用されない | フォント名が間違っている、またはシステムにフォントがインストールされていない | 使用するフォント（例: “David Transparent”）が実行環境にインストールされていることを確認 |

## FAQ

**Q: Aspose.Note for Java で複数レベルのサブページを作成できますか？**  
A: はい、`setLevel((byte) 3)` のようにより高いレベル番号を設定すれば、3 階層目以降のサブページも作成できます。

**Q: Aspose.Note for Java はさまざまな Java IDE と互換性がありますか？**  
A: もちろんです。IntelliJ IDEA、Eclipse、NetBeans など、Java 開発をサポートする IDE で動作します。

**Q: OneNote ドキュメント内のテキスト書式をカスタマイズできますか？**  
A: はい。`ParagraphStyle` を使用して、各 `RichText` 要素のフォント名、サイズ、色などを設定できます。

**Q: Aspose.Note for Java は BMP 以外の形式で保存できますか？**  
A: はい。PDF、PNG、JPEG、DOCX など多数の形式がサポートされています。`SaveFormat` 列挙体を変更してください。

**Q: Aspose.Note for Java のトライアル版はありますか？**  
A: はい、Aspose のウェブサイトから無料トライアルをダウンロードできます。

## 結論

OneNote ノートブックを明確な階層構造で整理し、PDF としてエクスポートすれば、ノートのアクセシビリティと共有性が向上します。上記の手順に従えば、**OneNote PDF の保存方法** と **サブページの追加** をプログラムで実現できます。

---

**最終更新日:** 2026-01-07  
**テスト環境:** Aspose.Note for Java 24.11 (最新)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}