---
date: 2026-08-08
description: Aspose.Note for Java を使用して page revisions をプログラムで取得し、OneNote の変更を追跡する方法を学びます。
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: OneNote の page revisions を取得 - Aspose.Note
og_description: Aspose.Note for Java を使用して page revisions をプログラムで取得し、OneNote の変更を追跡する方法を学びます。
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: OneNote の変更履歴を追跡 – Aspose.Note を使用した page revisions
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: OneNote の変更履歴を追跡 – Aspose.Note を使用した page revisions
url: /ja/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote の変更履歴の追跡 – Aspose.Note を使用したページリビジョン

このチュートリアルでは、Aspose.Note Java API を使用してページの完全なリビジョン履歴を抽出することで、**OneNote の変更履歴を追跡**する方法を学びます。開発環境の設定から各リビジョンの作成者、タイムスタンプ、タイトルの出力までをカバーし、任意の OneNote ベースのソリューション向けに信頼性の高い監査トレイル機能を構築できるようにします。

## クイック回答
- **このチュートリアルの内容は何ですか？** Aspose.Note for Java を使用して OneNote ファイルからページリビジョン履歴を取得します。  
- **必要なライブラリのバージョンは？** `LoadOptions.setLoadHistory` をサポートする最近の Aspose.Note for Java リリースであればどれでも構いません。  
- **ライセンスは必要ですか？** テスト用の一時評価ライセンスで動作しますが、製品環境では商用ライセンスが必要です。  
- **リビジョンを変更できますか？** API はリビジョンに対して読み取り専用で、取得のみ可能です。  
- **主な前提条件は何ですか？** Java JDK、Aspose.Note for Java、そしてリビジョンデータを含む OneNote ドキュメント。

## “aspose.note page revisions tutorial” とは何ですか？
このチュートリアルは、プログラムから OneNote ページの履歴バージョンにアクセスする方法を示します。各リビジョンには作成者、作成時刻、変更時刻などのメタデータが含まれ、アプリケーション内で監査トレイルや変更ログ機能を構築できるようになります。

## ページリビジョン追跡に Aspose.Note を使用する理由
標準的な 2 GHz CPU 上で 500 ページのファイルを 5 秒未満でノートブック全体のリビジョン履歴をロードし、OneNote UI を起動せずにメタデータを取得できます。ライブラリは 30 以上の入出力フォーマットをサポートし、Windows、Linux、macOS 上で動作（サーバー環境の 95 % 以上をカバー）し、すべてのリビジョンプロパティを完全に制御できます。

## 前提条件

### 1. Java Development Kit (JDK)
最近の JDK（8 以上）がインストールされ、`JAVA_HOME` が設定されていることを確認してください。

### 2. Aspose.Note for Java
ライブラリは[download link](https://releases.aspose.com/note/java/)からダウンロードしてください。

### 3. Sample OneNote Document
リビジョン履歴を含むページがある OneNote ファイル（例: `Sample1.one`）を作成するか取得してください。

## パッケージのインポート
まず、必要な Aspose.Note クラスをインポートします。  
`Document` は OneNote ノートブックを表し、`LoadOptions` は読み込み動作を構成し、`Page` は単一ページを表します。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## ステップバイステップ実装

### Step 1: ドキュメントディレクトリの設定
OneNote ファイルが存在するフォルダーを定義します。

```java
String dataDir = "Your Document Directory";
```

### Step 2: 履歴を有効にして OneNote ドキュメントをロード
`LoadOptions` は Aspose.Note にファイルを開く方法（リビジョンデータを読むかどうか）を指示する構成クラスです。ドキュメントをロードする前にフラグを有効にしてください。

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Step 3: 最初のページを取得
最初のページオブジェクトを取得します。これが履歴取得の基準点となります。

```java
Page firstPage = document.getFirstChild();
```

### Step 4: ページリビジョンを反復処理
各リビジョンをループし、タイムスタンプ、タイトル、レベル、作成者などの有用なメタデータを出力します。

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **プロのコツ:** 特定の作成者や日付範囲でリビジョンをフィルタリングする必要がある場合は、`for` ループ内に条件チェックを追加するだけです。

## 一般的な問題と解決策
- **リビジョンが返されない:** ドキュメントをロードする前に `loadOptions.setLoadHistory(true)` が呼び出されていることを確認してください。  
- **作成者またはタイトルが null:** 古い OneNote バージョンではこれらのフィールドが保存されていない場合があります。`null` 値は適切に処理してください。  
- **大規模ノートブックでのパフォーマンス低下:** 必要なセクションだけをロードするか、JVM ヒープサイズを増やしてください。

## よくある質問

**Q1: Aspose.Note for Java を使用してページリビジョンを変更できますか？**  
A1: いいえ、API は現在ページリビジョンへの読み取り専用アクセスのみをサポートしています。

**Q2: Aspose.Note for Java はさまざまなバージョンの OneNote ドキュメントと互換性がありますか？**  
A2: はい、さまざまな OneNote ファイル形式に対応しており、バージョン間でシームレスに処理できます。

**Q3: Aspose.Note for Java の使用にはライセンスが必要ですか？**  
A3: 本番環境での使用には商用ライセンスが必要ですが、テスト用の一時評価ライセンスが利用可能です。

**Q4: Aspose.Note for Java 使用中に問題が発生した場合、サポートを受けられますか？**  
A4: はい、[Aspose.Note forum](https://forum.aspose.com/c/note/28) で質問できます。

**Q5: Aspose.Note for Java の無料トライアルはありますか？**  
A5: はい、[website](https://releases.aspose.com/) から無料トライアルをダウンロードできます。

---

**最終更新日:** 2026-08-08  
**テスト環境:** Aspose.Note for Java (latest release)  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [OneNote の変更履歴の追跡 – Aspose.Note でページリビジョンを管理](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Aspose Java チュートリアル - OneNote のページ情報取得 - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [OneNote ページの背景を変更 – Aspose.Note for Java](/note/java/onenote-page-manipulation/set-page-background-color/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}