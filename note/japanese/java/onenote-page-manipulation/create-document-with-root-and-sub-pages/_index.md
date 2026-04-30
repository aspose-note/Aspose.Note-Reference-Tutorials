---
date: 2026-04-30
description: Aspose.Note for Java を使用して、OneNote で **PDF として保存** し、サブページを追加する方法を学びましょう。ステップバイステップのガイドに従って、ノートを効率的に整理してください。
keywords:
- save onenote as pdf
- add sub pages onenote
- Aspose.Note Java
linktitle: OneNoteをPDFとして保存し、サブページを追加する方法
second_title: Aspose.Note Java API
title: OneNoteをPDFとして保存し、サブページを追加する方法
url: /ja/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote を PDF として保存し、サブページを追加する方法

## はじめに

このチュートリアルでは、Aspose.Note for Java を使用して、ルートページとサブページの両方を含むドキュメントを作成しながら、**how to save onenote as pdf** を発見できます。OneNote ノートブックを明確な階層で整理することでナビゲーションが容易になり、PDF にエクスポートすれば、ノートを普遍的に読み取れる形式で共有できます。また、**add sub pages onenote** スタイルでサブページを追加する方法も示すので、マルチレベルの構造を簡単に構築できます。

## クイック回答

- **What does “save onenote as pdf” mean?** Aspose.Note for Java を使用して OneNote ノートブックを PDF ファイルにエクスポートすることを指します。  
- **Which API is required?** 必要なクラスとメソッドは Aspose.Note for Java が提供します。  
- **Can I create hierarchical pages?** はい – ページレベルを設定してルートページとサブページを作成します。  
- **Do I need a license for production?** 無料トライアルは利用可能ですが、製品環境で使用するには商用ライセンスが必要です。  
- **Which formats can I export to?** PDF に加えて、BMP、PNG、JPEG、DOCX などにもエクスポートできます。

## OneNote を PDF として保存する方法

OneNote を PDF に保存すると、各ノートブックページが固定レイアウトのドキュメントに変換され、書式設定、画像、ページ階層が保持されます。元の構造をそのまま保ったまま、ノートを共有、アーカイブ、印刷するのに最適です。

## なぜ onenote にサブページを追加するのか？

サブページを追加すると、関連するコンテンツを親ページの下にグループ化でき、フォルダーのような構造を再現できます。これによりノートの整理が向上し、検索が高速化され、ノートブックを PDF にエクスポートした際の閲覧体験が向上します。

## 前提条件

開始する前に、以下の前提条件が揃っていることを確認してください。

1. **Java Development Kit (JDK)** – システムに JDK がインストールされていることを確認してください。  
2. **Aspose.Note for Java** – [website](https://purchase.aspose.com/buy) から Aspose.Note for Java をダウンロードしてインストールしてください。  
3. **Integrated Development Environment (IDE)** – IntelliJ IDEA、Eclipse、NetBeans などの Java IDE を選択してください。

## パッケージのインポート

Java プロジェクトで必要なパッケージをインポートすることから始めます。

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

## ステップ 1: ドキュメントディレクトリの設定

OneNote ドキュメントを保存するディレクトリを定義します。

```java
String dataDir = "Your Document Directory";
```

## ステップ 2: ドキュメントオブジェクトの作成

`Document` オブジェクトをインスタンス化します。

```java
Document doc = new Document();
```

## ステップ 3: ページの作成

ページオブジェクトを初期化し、レベルを設定します。レベルを設定することで、ページがルートページかサブページかが決まります。

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## ステップ 4: ページにノードを追加

### 最初のページにノードを追加

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

### 2 番目のページにノードを追加

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

### 3 番目のページにノードを追加

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

## ステップ 5: ドキュメントにページを追加

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## ステップ 6: ドキュメントを保存

OneNote ドキュメントを PDF（この例では BMP）として保存します。`SaveFormat` を変更することで PDF にエクスポートでき、“save onenote as pdf” の要件を満たします。

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Pro tip:** PDF に直接エクスポートするには、`SaveFormat.Bmp` を `SaveFormat.Pdf` に置き換えてください。

おめでとうございます！ルートページとサブページを持つ OneNote ドキュメントを正常に作成し、Aspose.Note for Java を使用して **how to save onenote as pdf** を学びました。

## なぜこれが重要か

- **Hierarchical organization:** ルートページとサブページを使用して、OneNote 内でフォルダー構造を模倣できます。  
- **Seamless PDF export:** 整理された後に PDF にエクスポートすると階層が保持され、最終ドキュメントが読みやすく共有しやすくなります。  
- **Automation:** このコードは大規模な Java アプリケーションに統合でき、構造化されたノートブックのバッチ作成を可能にします。

## よくある落とし穴と回避方法

| 問題 | 原因 | 解決策 |
|-------|-------|----------|
| ページが同じレベルに表示される | `setLevel` の値が不正 | ルートページには `setLevel((byte) 1)`、サブページには `setLevel((byte) 2)`（またはそれ以上）を使用してください。 |
| PDF 出力が空白に見える | `SaveFormat.Pdf` が欠如している、またはファイルパスが間違っている | ディレクトリが存在することを確認し、`SaveFormat.Pdf` を使用してください。 |
| フォントが適用されない | フォント名が間違っている、またはシステムにフォントがインストールされていない | フォント（例: “David Transparent”）がコード実行マシンにインストールされていることを確認してください。 |

## よくある質問

**Q: Aspose.Note for Java を使用して、複数レベルのサブページを作成できますか？**  
A: はい、より高いレベル番号を設定することで、より深い階層を作成できます（例: 第三レベルのサブページには `setLevel((byte) 3)` を使用）。

**Q: Aspose.Note for Java はさまざまな Java IDE と互換性がありますか？**  
A: もちろんです。IntelliJ IDEA、Eclipse、NetBeans、そして Java 開発をサポートするすべての IDE で動作します。

**Q: OneNote ドキュメントのテキスト書式をカスタマイズできますか？**  
A: はい。`ParagraphStyle` を使用して、各 `RichText` 要素のフォント名、サイズ、色、その他の属性を設定できます。

**Q: Aspose.Note for Java は BMP 以外の形式での保存をサポートしていますか？**  
A: はい。サポートされている形式には PDF、PNG、JPEG、DOCX などがあります。`SaveFormat` 列挙体を適切に変更してください。

**Q: Aspose.Note for Java のトライアル版は利用可能ですか？**  
A: はい、Aspose のウェブサイトから無料トライアルをダウンロードできます。

## 結論

明確な階層構造で OneNote ノートブックを整理し、PDF としてエクスポートすることで、ノートがよりアクセスしやすく共有しやすくなります。上記の手順に従うことで、Aspose.Note for Java を使用してプログラム的に **how to save onenote as pdf** と **add sub pages onenote** スタイルを実現できるようになりました。

---

**最終更新日:** 2026-04-30  
**テスト環境:** Aspose.Note for Java 24.11 (latest)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}