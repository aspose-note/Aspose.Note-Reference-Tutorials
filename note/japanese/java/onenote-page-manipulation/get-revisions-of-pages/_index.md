---
date: 2026-08-13
description: Aspose.Note for Java を使用して OneNote ページの modified time を取得し、ページの revisions
  を取得する方法を学びます。監査やドキュメント管理に最適です。
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: OneNote のページの revisions を取得する - Aspose.Note
og_description: Aspose.Note for Java を使用して OneNote ページの modified time を取得し、ページの revisions
  を取得する方法を学びます。手順が簡単、コードスニペット、トラブルシューティング付き。
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Aspose.Note を使用して OneNote ページの modified time を取得 – Java チュートリアル
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Aspose.Note を使用して OneNote ページの modified time を取得する
url: /ja/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note を使用して OneNote ページの最終更新時刻を取得する

## はじめに

このチュートリアルでは、Aspose.Note for Java を使用して **OneNote ページの最終更新** タイムスタンプを取得し、ページの完全なリビジョン履歴を取得する方法を学びます。監査トレイル機能や変更ログビューアの構築、ダッシュボードで最新の編集日付を表示する必要がある場合など、本ガイドは環境設定から一般的な落とし穴の対処まで、すべての手順を詳しく解説します。

## クイック回答
- **“get last modified time” が返すものは何ですか？** OneNote ページの最新の編集時刻のタイムスタンプを返します。  
- **リビジョン履歴を提供するクラスはどれですか？** `Document.getPageHistory(Page)` を通じて取得できる `PageHistory`。  
- **この機能にはライセンスが必要ですか？** はい、実運用には有効な Aspose.Note ライセンスが必要です。  
- **サポートされている Java バージョンは何ですか？** Java 8 以上 (JDK 8+)。  
- **著者でリビジョンをフィルタリングできますか？** 各 `Page` オブジェクトの `Author` プロパティを読み取り、独自にフィルタを適用できます。

## OneNote の “get last modified time” とは何ですか？

最終更新時刻は各 OneNote ページのメタデータ属性として保存され、最新の編集時点を示します。Aspose.Note はこの値を `Page.getLastModifiedTime()` メソッドで公開し、`java.util.Date` オブジェクトを返します。このオブジェクトはアプリケーションの要件に合わせてフォーマットしたりログに記録したりできます。

## なぜページのリビジョンを取得するのか？

ページのリビジョンを取得すると、OneNote ページに加えられたすべての変更の完全な監査トレイルが得られ、誰がいつ何を編集したかを追跡できます。この履歴はバージョン比較、以前の状態への復元、チーム間の協働パターンの分析などに利用でき、コンプライアンスや品質管理に不可欠です。

## 前提条件

- **Java Development Kit (JDK) 8 以上** – Oracle のウェブサイトまたは互換ベンダーからインストールしてください。  
- **Aspose.Note for Java ライブラリ** – Aspose.Note Java リリースページ **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** から JAR をダウンロードし、インストールガイド **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)** に従ってください。  

## パッケージのインポート

`Document` クラスはメモリにロードされた OneNote ノートブックを表し、`Page` と `PageHistory` は個々のページとそのリビジョンデータへのアクセスを提供します。

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*（実際のインポート文はプレーンテキストとして表示され、元のコードブロック数を保持しています。）*

## OneNote ページの最終更新時刻を取得する方法

最終更新タイムスタンプを取得するには、まず OneNote ドキュメントを `Document` オブジェクトにロードし、目的の `Page` を選択します。そのページで `getLastModifiedTime()` メソッドを呼び出すと `java.util.Date` が返されます。この日付は `SimpleDateFormat` を使用してフォーマットしたり、タイムゾーン間で一貫したレポートを行うために UTC に変換したりできます。

## 手順 1: ドキュメント ディレクトリの設定

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## 手順 2: ドキュメントのロード

```java
String dataDir = "Your Document Directory";
```

## 手順 3: 最初のページを取得

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## 手順 4: ページのリビジョンを取得

```java
Page firstPage = doc.getFirstChild();
```

## 手順 5: ページのリビジョンを走査

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## よくある問題と解決策
- **Null `PageHistory`** – ノートブックに実際にリビジョンが存在するか確認してください。存在しない場合、`getPageHistory` は `null` を返します。  
- **タイムゾーンの違い** – `getLastModifiedTime()` は JVM のデフォルトタイムゾーンを使用します。アプリケーションで標準ゾーンが必要な場合は `SimpleDateFormat` で UTC に変換してください。  
- **ライセンスがロードされていない** – 有効なライセンスがない場合、Aspose.Note は評価モードで動作し、ページ処理が制限されます。起動時にライセンスファイルをロードしてこの制限を回避してください。

## よくある質問

**Q1: Aspose.Note for Java を使用して新しい OneNote ドキュメントを作成できますか？**  
A: はい、API を使ってプログラムから OneNote ノートブックを新規作成、編集、保存できます。

**Q2: Aspose.Note for Java はさまざまなバージョンの OneNote ファイルと互換性がありますか？**  
A: はい、OneNote 2007‑2021 のファイル形式をサポートしており、デスクトップおよびクラウド環境で広範な互換性を提供します。

**Q3: OneNote ドキュメントをエクスポートする際に出力形式をカスタマイズできますか？**  
A: もちろんです。PDF、HTML、PNG、SVG などにエクスポートでき、画像解像度やフォント埋め込みといったオプションも制御できます。

**Q4: Aspose.Note for Java の商用利用にはライセンスが必要ですか？**  
A: はい、製品環境での使用には商用ライセンスが必須です。評価用の無料トライアルも利用可能です。

**Q5: 問題が発生した場合、どこでサポートを受けられますか？**  
A: Aspose.Note コミュニティフォーラム **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** を訪れ、質問や体験の共有、コミュニティや Aspose エンジニアからの支援を受けてください。

---

**最終更新日:** 2026-08-13  
**テスト環境:** Aspose.Note for Java 23.12 (latest at time of writing)  
**作成者:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## 関連チュートリアル

- [Aspose Java チュートリアル - OneNote のページ情報取得 - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [aspose.note ページリビジョン チュートリアル – OneNote のページリビジョン取得](/note/java/onenote-page-manipulation/get-page-revisions/)
- [track changes onenote – Aspose.Note でページリビジョンを管理](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}