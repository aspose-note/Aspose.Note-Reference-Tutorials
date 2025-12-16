---
date: 2025-12-08
description: Aspose.Note を使用して Java で OneNote ドキュメントを作成する際の段落スタイル設定とアウトライン要素の追加方法を学びます。OneNote
  を PDF にエクスポートし、OneNote ファイルを手軽に生成できます。
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: JavaでOneNoteドキュメントを作成する際に段落スタイルを設定する
url: /ja/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでOneNoteドキュメントを作成する際の段落スタイル設定

## Introduction

今日のスピーディな開発環境では、プログラムから **set paragraph style** を行えることが、洗練された OneNote ファイルを作成する上で不可欠です。このチュートリアルでは、シンプルなリッチテキストで OneNote ドキュメントを生成し、カスタム段落書式を適用し、最後に Aspose.Note for Java を使用して **export OneNote to PDF** する手順をステップバイステップで紹介します。レポートエンジン、自動ノート取得ソリューション、ドキュメント変換サービスの構築を検討している方でも、ここで紹介する手法を使えば、**generate OneNote files** を思い通りの外観で作成できます。

## Quick Answers
- **What does “set paragraph style” mean?** フォント、サイズ、カラー、その他の書式を段落単位で適用することです。  
- **Can I export the result to PDF?** はい – チュートリアルの最後で OneNote ファイルを PDF として保存します。  
- **Do I need a license for Aspose.Note?** 無料トライアルで評価は可能ですが、本番環境ではライセンスが必要です。  
- **Which IDEs are supported?** 任意の Java IDE が使用可能です – Eclipse、IntelliJ IDEA、NetBeans など。  
- **How long does the implementation take?** 基本的なドキュメントでおおよそ 10‑15 分程度です。

## What is “set paragraph style” in Aspose.Note?
段落スタイルの設定とは、`ParagraphStyle` オブジェクト（フォント名、サイズ、カラー等）を構成し、それを `RichText` ノードに付与することを指します。これにより、OneNote ページ内のテキスト表示を完全にコントロールできます。

## Why set paragraph style when generating OneNote files?
- **Consistent branding:** 企業のフォントやカラーを自動的に適用できます。  
- **Readability:** 大きめのフォントや特定のカラーでアクセシビリティを向上させます。  
- **Export fidelity:** 後で **convert OneNote PDF** した際に、書式付きテキストが正しく保持されます。  

## Prerequisites

開始する前に、以下を用意してください。

1. **Java Development Kit (JDK) 1.8+** – 最近の JDK であれば問題ありません。  
2. **Aspose.Note for Java** – 最新の JAR を [Aspose.Note ダウンロードページ](https://releases.aspose.com/note/java/) から取得してください。  
3. **IDE** (Eclipse、IntelliJ IDEA、または NetBeans) – サンプルのコンパイルと実行に使用します。  

> **Pro tip:** Maven で依存関係を追加するか、IDE で JAR を手動で参照して、Aspose.Note JAR をプロジェクトのクラスパスに追加してください。

## Import Packages

まず、必要なクラスをインポートします。このブロックは変更しません。

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> `ParagraphStyle` クラスは、チュートリアル後半で **set paragraph style** を行うための鍵となります。

## Step‑by‑Step Guide

以下に各操作の簡潔な手順を示します。コードブロックは元のサンプルと同一で、説明文のみ日本語に置き換えています。

### Step 1: Set Document Directory
生成されたファイルの保存先ディレクトリを定義します。

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` を、マシン上の絶対パスまたは相対パスに置き換えてください。

### Step 2: Initialize Document Object
OneNote ファイル全体を表すルート `Document` を作成します。

```java
Document doc = new Document();
```

### Step 3: Initialize Page Object
OneNote ファイルは 1 つ以上のページで構成されます。ここでは単一ページから開始します。

```java
Page page = new Page();
```

### Step 4: Initialize Outline Object
アウトラインはアウトライン要素（セクション相当）のコンテナとして機能します。

```java
Outline outline = new Outline();
```

### Step 5: Initialize OutlineElement Object
ここでリッチテキストを保持する **outline element** を追加します。

```java
OutlineElement outlineElem = new OutlineElement();
```

### Step 6: Set Text Style (Set Paragraph Style)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

`ParagraphStyle` インスタンスでフォント、サイズ、カラーを定義し、以降のテキストノードに **set paragraph style** を適用します。

### Step 7: Initialize RichText Object

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

`RichText` ノードを作成し、シンプルな文字列を挿入、先ほど定義したスタイルを付与します。

### Step 8: Add RichText Node to OutlineElement

```java
outlineElem.appendChildLast(text);
```

これでスタイル付きテキストがアウトライン要素内に配置されました。

### Step 9: Add OutlineElement Node to Outline

```java
outline.appendChildLast(outlineElem);
```

アウトラインにテキストを保持する要素が追加されました。

### Step 10: Add Outline Node to Page

```java
page.appendChildLast(outline);
```

ページ上にアウトラインを配置します。

### Step 11: Add Page Node to Document

```java
doc.appendChildLast(page);
```

ドキュメントに単一ページが追加され、スタイル付きテキストが完成します。

### Step 12: Save the Document (Export OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

`save` メソッドで OneNote ファイルを保存すると同時に **export OneNote PDF** も実行できます。ネイティブ形式が必要な場合は `SaveFormat.One` を使用して `.one` として保存してください。

## Common Issues & Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **File not found** | `dataDir` が存在しないフォルダーを指しています。 | ディレクトリが存在することを確認するか、`new File(dataDir).mkdirs();` でプログラムから作成してください。 |
| **Blank PDF** | 保存前にコンテンツが追加されていません。 | `RichText` ノードが正しく追加され、スタイルが設定されているか確認してください。 |
| **Unsupported font** | システムにフォントがインストールされていません。 | `"Arial"` など一般的なフォントを使用するか、プロジェクトにフォントを埋め込んでください。 |

## Frequently Asked Questions

**Q: Aspose.Note はテーブルや画像などの複雑な書式にも対応していますか？**  
A: はい、API はテーブル、画像、ハイパーリンク、その他高度なレイアウト機能をサポートしています。

**Q: **convert OneNote PDF** を元の OneNote ファイルに戻すことは可能ですか？**  
A: 直接的な変換機能は提供されていませんが、PDF の内容を抽出し、API を使って OneNote ドキュメントを再構築することはできます。

**Q: ライブラリは Linux/macOS 環境でも動作しますか？**  
A: 完全にプラットフォームに依存しません。JDK がインストールされていれば問題なく動作します。

**Q: 複数ページや複数アウトラインはどうやって追加しますか？**  
A: 追加の `Page` や `Outline` オブジェクトを作成し、単一ページの例と同様に `Document` に Append すれば実現できます。

**Q: もっとサンプルはどこで見られますか？**  
A: 公式の Aspose.Note ドキュメントと [サポートフォーラム](https://forum.aspose.com/c/note/28) に多数のコード例が掲載されています。

## Conclusion

これで **set paragraph style**、**add outline element**、そして Aspose.Note for Java を使用した **export OneNote PDF** の手順が理解できました。作成段階でスタイル付きテキストを組み込むことで、最終的なドキュメントがプロフェッショナルに仕上がり、後続の **convert OneNote PDF** 操作でも書式が保持されます。画像、テーブル、カスタムメタデータなどを追加して、プロジェクトの要件に合わせて拡張してください。

---

**最終更新日:** 2025-12-08  
**テスト環境:** Aspose.Note for Java 24.11 (latest release)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}