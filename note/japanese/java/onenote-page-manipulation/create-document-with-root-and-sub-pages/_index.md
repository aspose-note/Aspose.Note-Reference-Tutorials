---
title: OneNote でルート ページとサブ ページを含むドキュメントを作成する
linktitle: OneNote でルート ページとサブ ページを含むドキュメントを作成する
second_title: Aspose.Note Java API
description: Aspose.Note for Java を使用して、OneNote でルート ページとサブ ページを含むドキュメントを作成します。ステップバイステップのガイドに従って、メモを効率的に整理してください。
weight: 11
url: /ja/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote でルート ページとサブ ページを含むドキュメントを作成する

## 導入

このチュートリアルでは、Aspose.Note for Java を使用して OneNote でルート ページとサブ ページを含むドキュメントを作成するプロセスを説明します。これらの手順に従うことで、OneNote ドキュメントを階層構造で効率的に整理できるようになります。

## 前提条件

始める前に、次の前提条件を満たしていることを確認してください。

1. Java Development Kit (JDK): システムに JDK がインストールされていることを確認してください。
2. Aspose.Note for Java: 次の場所から Aspose.Note for Java をダウンロードしてインストールします。[Webサイト](https://purchase.aspose.com/buy).
3. 統合開発環境 (IDE): IntelliJ IDEA、Eclipse、NetBeans などの Java IDE を選択します。

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。

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

## ステップ 1: ドキュメント ディレクトリを設定する

OneNote ドキュメントを保存するディレクトリを定義します。

```java
String dataDir = "Your Document Directory";
```

## ステップ 2: ドキュメント オブジェクトを作成する

インスタンス化する`Document`物体：

```java
Document doc = new Document();
```

## ステップ 3: ページを作成する

ページ オブジェクトを初期化し、そのレベルを設定します。

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## ステップ 4: ページにノードを追加する

### 最初のページにノードを追加する

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

### ページ目へのノードの追加

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

### ページ目へのノードの追加

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

## ステップ 5: ドキュメントにページを追加する

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## ステップ 6: ドキュメントを保存する

OneNote ドキュメントを保存します。

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    //例外を処理する
}
```

おめでとう！ Aspose.Note for Java を使用して、OneNote でルート ページとサブ ページを含むドキュメントが正常に作成されました。

## 結論

OneNote ドキュメントを階層構造で整理することは、管理とナビゲーションを向上させるために不可欠です。 Aspose.Note for Java を使用すると、ルート ページとサブ ページを含むドキュメントを効率的に作成でき、メモに明確で整理されたレイアウトを提供できます。

## よくある質問

### Q1: Aspose.Note for Java を使用して複数レベルのサブページを作成できますか?

A1: はい、各ページに適切なレベルを設定することで、複数のレベルのサブページを作成できます。

### Q2: Aspose.Note for Java はさまざまな Java IDE と互換性がありますか?

A2: はい、Aspose.Note for Java は、IntelliJ IDEA、Eclipse、NetBeans などの一般的な Java IDE と互換性があります。

### Q3: OneNote ドキュメント内のテキストの書式設定をカスタマイズできますか?

A3: はい、Aspose.Note for Java のリッチ テキスト機能を使用して、フォント、色、サイズ、その他の書式設定オプションをカスタマイズできます。

### Q4: Aspose.Note for Java は、さまざまな形式でのドキュメントの保存をサポートしていますか?

A4: はい、Aspose.Note for Java は、BMP、PDF、PNG などのさまざまな形式でのドキュメントの保存をサポートしています。

### Q5: Aspose.Note for Java の試用版はありますか?

A5: はい、Aspose.Note for Java の無料試用版を Web サイトからダウンロードできます。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
