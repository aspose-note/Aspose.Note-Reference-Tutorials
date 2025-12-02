---
date: 2025-12-02
description: Aspose.Note for Java を使用して Java でタイトル付きの OneNote ページを作成する方法を学びます。このガイドでは、OneNote
  ページのタイトルを設定し、タイトルのフォントをカスタマイズする方法を示します。
language: ja
linktitle: How to Create OneNote Page with Title - Java
second_title: Aspose.Note Java API
title: タイトル付きOneNoteページの作成方法 - Java
url: /java/onenote-document-loading/create-onenote-doc-page-title/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote ページをタイトル付きで作成する方法 - Java

## Introduction

プログラムで **OneNote ページを作成する方法** が必要な場合、Aspose.Note for Java を使用すれば簡単に実現できます。このチュートリアルでは、OneNote ファイルの生成、ページタイトルの設定、さらにはタイトルのフォントをカスタマイズする方法を Java コードから学びます。最後まで実行すれば、任意の Java アプリケーションに組み込める使用可能な OneNote ドキュメントが手に入ります。

## Quick Answers
- **必要なライブラリは？** Aspose.Note for Java。
- **タイトルのフォントをカスタムできますか？** はい – `ParagraphStyle` を使用してフォント名、サイズ、色を定義します。
- **対応している Java バージョンは？** JDK 8 以上（API は下位互換です）。
- **開発用にライセンスは必要ですか？** テスト用の無料トライアルで動作しますが、本番環境ではライセンスが必要です。
- **出力はどこに保存されますか？** `dataDir` 変数でパスを指定します。

## What is a OneNote Page Title?
OneNote ページタイトルは、各ページの上部に表示されるヘッダーです。通常、ページ名、作成日、時間が含まれます。プログラムでこのタイトルを設定することで、一貫性のある構造化されたノートブックを作成できます。

## Why Set OneNote Page Title Programmatically?
- **Automation:** 手動編集なしでレポートや会議ノートを生成。  
- **Consistency:** すべてのページで命名規則を統一。  
- **Integration:** OneNote を CRM やプロジェクト管理ツールなど他システムと連携。

## Prerequisites

- **Java Development Kit (JDK)** – バージョン 8 以上。  
- **Aspose.Note for Java** – 公式サイト **[here](https://releases.aspose.com/note/java/)** からダウンロード。  
- **IDE** – IntelliJ IDEA、Eclipse、または NetBeans（お好みで）。

## Import Packages

まず、Aspose.Note ライブラリから必要なクラスをインポートします。

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

### Step 1: Set Up Document Directory  
生成した OneNote ファイルを保存する場所を定義します。

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

### Step 2: Create Document Object  
新しい `Document` をインスタンス化します。これが作成する OneNote ファイルを表します。

```java
// Create an object of the Document class
Document doc = new Document();
```

### Step 3: Initialize Page Object  
タイトルとコンテンツを保持する `Page` オブジェクトを作成します。

```java
// Initialize Page class object
Page page = new Page();
```

### Step 4: Set Default Text Style  
タイトルテキストに適用するデフォルトの `ParagraphStyle` を定義します。ここで **OneNote タイトルフォントをカスタマイズ** します。

```java
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

### Step 5: Set Page Title Properties  
ここで **OneNote ページタイトル** の詳細（タイトル文字列、日付、時間）を設定します。用途に合わせて文字列を変更してください。

```java
// Set page title properties
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

### Step 6: Assign the Title to the Page  
`Title` オブジェクトを `Page` にリンクさせて **OneNote にタイトルを追加** します。

```java
page.setTitle(title);
```

### Step 7: Append Page to Document  
設定したページをドキュメント構造に追加します。

```java
doc.appendChildLast(page);
```

### Step 8: Save OneNote Document  
出力ファイル名を指定し、ノートブックを保存します。これで **java create onenote file** のプロセスが完了です。

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// Save OneNote document
doc.save(dataDir);
```

## Common Issues & Tips

| Issue | Solution |
|-------|----------|
| **Invalid file path** | `dataDir` が正しいセパレータ（`/` または `\\`）で終わっているか、フォルダーが存在するか確認してください。 |
| **Title not visible** | 各 `RichText` 要素に `ParagraphStyle` が適用されているか確認してください。 |
| **License exception** | テスト時はトライアルライセンスを使用し、本番前に正式ライセンスを適用してください。 |
| **Date shows wrong month** | Java の月は 0 基準です。`cal.set(2018, 04, 03)` は実際には 5 月を設定します。適宜調整してください。 |

## Frequently Asked Questions

**Q: Aspose.Note for Java はさまざまな Java バージョンに対応していますか？**  
A: はい、ライブラリは Java 8 以降で動作し、環境に応じた柔軟性を提供します。

**Q: ページタイトルのフォントスタイルやサイズをカスタマイズできますか？**  
A: もちろんです！ Step 4 に示したように `ParagraphStyle` を使用して任意のフォント名、サイズ、色を設定できます。

**Q: ページにさらにコンテンツ（段落、画像など）を追加するには？**  
A: 追加の `RichText` や `Image` オブジェクトを作成し、スタイルを設定した上で `page.appendChildLast(yourObject)` でページに追加します。

**Q: Aspose.Note for Java のトライアル版はありますか？**  
A: はい、Aspose のウェブサイトから無料トライアルをダウンロードして、すべての機能を評価できます。

**Q: 問題が発生した場合、どこでサポートを受けられますか？**  
A: [Aspose.Note フォーラム](https://forum.aspose.com/c/note/28) でコミュニティの助けを得るか、Aspose にサポートチケットを提出してください。

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.Note for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}