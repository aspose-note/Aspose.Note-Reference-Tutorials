---
date: 2025-12-09
description: Aspose.Note for Java を使用して、Java で書式設定されたリッチテキストを含む OneNote を PDF に保存する方法を学びましょう。シームレスなドキュメント自動化のためのステップバイステップガイドをご覧ください。
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: Javaでフォーマットされたリッチテキスト付きOneNoteをPDFとして保存
url: /ja/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java でリッチテキスト書式付き OneNote を PDF として保存

## はじめに

リッチテキストの書式を保持したまま **OneNote を PDF に保存** したい場合は、こちらのチュートリアルが最適です。本稿では OneNote ドキュメントの作成、カスタスタイルの適用、そして Aspose.Note for Java を使用した直接 PDF へのエクスポート手順を解説します。最後まで読めば、任意の Java プロジェクトに組み込んで OneNote → PDF 変換を自動化できる再利用可能なコードスニペットが手に入ります。

## クイック回答
- **このチュートリアルで学べることは？** スタイル付きテキストを持つ OneNote ドキュメントを作成し、PDF として保存する方法。  
- **必要なライブラリは？** Aspose.Note for Java（公式サイトからダウンロード可）。  
- **ライセンスは必要？** テスト用の一時ライセンスで動作しますが、本番環境では正式ライセンスが必要です。  
- **使用できる IDE は？** 任意の Java IDE（IntelliJ IDEA、Eclipse、NetBeans など）。  
- **出力形式は変更できる？** はい、Aspose.Note は PDF、HTML、PNG など複数の形式に対応しています。

## 「save onenote as pdf」とは？
OneNote を PDF に保存するとは、OneNote のページ構造（テキスト、画像、書式設定）を静的な PDF ファイルに変換し、OneNote がなくても任意のプラットフォームで閲覧できるようにすることを指します。

## なぜ Java でリテキストを書式設定するのか？
Java で直接リッチテキストの書式（フォント、色、スタイル）を適用できれば、手作業の編集なしにプロフェッショナルな文書を生成でき、ブランドガイドラインに合わせた統一感のある出力が可能になります。

## 前提条件

1. **Java Development Kit (J)** – バージョン 8 以上のいずれか。  
2. **Aspose.Note for Java JAR** – [ダウンロードリンク](https://releases.aspose.com/note/java/) から取得。  
3. **IDE** – IntelliJ IDEA、Eclipse、またはお好みのエディタ。

## パッケージのインポート

まず、Java プロジェクトに必要なパッケージをインポートします。Java ファイルの先頭に以下のインポート文を追加してください。

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## 手順 1: ドキュメントとページの設定

`Document` と `Page` オブジェクトを初期化します。

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## 手順 2: 書式付きタイトルの作成

書式付きテキストでタイトルを作成します。

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## 手順 3: 書式付きリッチテキストの作成

さまざまな書式スタイルを持つリッチテキストを作成します。

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## 手順 4: ページとドキュメントへの要素追加

タイトルとリッチテキストをページに追加し、アウトライン要素も設定します。

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## 手順 5: ドキュメントの保存

作成した OneNote ドキュメントを PDF として保存します。

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## よくある問題と対策

| 問題 | 対策 |
|------|------|
| **ファイルが見つからない** | `dataDir` が実在するフォルダーを指しているか、書き込み権限があるか確認してください。 |
| **フォントが見つからない** | 参照しているフォント（例: *Calibri*）がホストマシンにインストールされていることを確認してください。 |
| **ライセンスが適用されていない**Document` を作成する前に Aspose のライセンスをロードし、評価版の透かしが表示されないようにしてください。 |

## FAQ

**Q: フォントスタイルをさらにカスタマイズできますか？**  
A: はい、`Text` や `ParagraphStyle` クラスを使用して下線、取り消し線、テキスト配置などの追加プロパティを調整できます。

**Q: Aspose.Note for Java はすべての Java IDE と互換性がありますか？**  
A: もちろんです。標準的な Java 開発をサポートしている IDE であれば、Aspose.Note JAR をクラスパスに追加すれば利用可能です。

**Q: この機能をウェブアプリケーションに組み込めますか？**  
A: はい、サーブレットベースや Spring Boot アプリケーションでも同じコードが動作し、サーバー側で動的に OneNote → PDF 変換を実行できます。

**Q: Aspose.Note for Java の使用にはライセンスが必要ですか？**  
A: 本番環境での使用には商用ライセンスが必要です。評価・テスト用に一時ライセンスを利用できます。

**Q: Aspose.Note for Java は OneNote 以外のドキュメント形式もサポートしていますか？**  
A: はい、PDF、HTML、PNG、JPEG など多数のエクスポート形式に対応しており、OneNote ページを必要な形式に柔軟に変換できます。

## 結論

本ガイドでは、Aspose.Note for Java を使用してリッチテキスト書式を適用しながら **OneNote を PDF として保存** する方法を示しました。ステップバイステップの手順に従うことで、洗練された OneNote ドキュメントの作成と PDF への自動変換を任意の Java ソリューションに組み込むことができます。

---

**最終更新日:** 2025-12-09  
**テスト環境:** Aspose.Note for Java 24.11（執筆時点での最新バージョン）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}