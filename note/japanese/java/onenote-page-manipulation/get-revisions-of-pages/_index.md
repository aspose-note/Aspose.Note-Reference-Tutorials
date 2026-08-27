---
date: 2026-01-10
description: Aspose.Note for Java を使用して OneNote ページの最終更新時刻の取得方法とリビジョンの取得方法を学びましょう。これを
  Java アプリに統合して、効率的なドキュメント管理を実現してください。
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNoteページの最終更新日時を取得する方法 – Aspose.Note
url: /ja/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote のページのリビジョン取得 - Aspose.Note

## Introduction

このチュートリアルでは、OneNote ドキュメント内のページの **最終更新時刻** を取得し、Aspose.Note for Java を使用して完全なリビジョン履歴を取得する方法を解説します。ドキュメント管理システムの構築、変更の監査、または単にページが最後に編集された時刻を表示したい場合でも、本ガイドはプログラムで情報を抽出する手順を正確に示します。

## Quick Answers
- **「最終更新時刻を取得する」 は何を返しますか？** OneNote ページで最後に行われた編集のタイムスタンプを返します。  
- **どのクラスがリビジョン履歴を提供しますか？** `Document.getPageHistory(Page)` で取得できる `PageHistory` クラスです。  
- **この機能を使用するのにライセンスは必要ですか？** はい、商用利用には有効な Aspose.Note ライセンスが必要です。  
- **サポートされている Java バージョンは？** Java 8 以上 (JDK 8+) がサポートされています。  
- **作者でリビジョンをフィルタリングできますか？** 各 `Page` オブジェクトの `Author` プロパティを取得し、独自にフィルタを適用できます。

## What is “get last modified time” in OneNote?

**最終更新時刻** は、各ページに保存されるメタデータフィールドで、ページが最後に変更された日時を記録します。Aspose.Note はこの値を `Page.getLastModifiedTime()` メソッドで公開しており、変更日付の表示やログ記録が簡単に行えます。

## Why retrieve page revisions?

- **監査トレイル:** 誰が何をいつ変更したかの記録を保持します。  
- **バージョン比較:** 2 つのリビジョンを並べて比較する機能を構築できます。  
- **ユーザーコラボレーションの洞察:** 共有ノートブックでの編集パターンを把握できます。  

## Prerequisites

開始する前に、以下が揃っていることを確認してください。

### Java Development Kit (JDK) Installed
Oracle のウェブサイトまたはお好みのパッケージマネージャーから JDK 8 以降をインストールします。

### Aspose.Note for Java Library
公式サイトからライブラリをダウンロードします。ダウンロードリンクは **[here](https://releases.aspose.com/note/java/)** にあります。インストール手順はドキュメントの **[here](https://reference.aspose.com/note/java/)** を参照してください。

## Import Packages

まず、Java プロジェクトに必要なパッケージをインポートします。これらのパッケージにより、Aspose.Note for Java が提供する機能を利用できます。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

次に、提供されたサンプルコードを複数のステップに分解し、各コンポーネントとその機能を理解しましょう。

## How to Get Last Modified Time of a OneNote Page

### Step 1: Set Document Directory
OneNote ドキュメントが格納されているディレクトリを定義します。

```java
String dataDir = "Your Document Directory";
```

### Step 2: Load the Document
OneNote ドキュメントを Aspose.Note にロードします。

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Step 3: Get First Page
ドキュメントから最初のページを取得します。

```java
Page firstPage = doc.getFirstChild();
```

### Step 4: Get Page Revisions
ページのリビジョン履歴を取得します。

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Step 5: Traverse Page Revisions
ページリビジョンのリストを走査し、**最終更新時刻** を含む関連情報を取得します。

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

## Common Issues and Solutions
- **`PageHistory` が null:** ドキュメントにリビジョンが実際に含まれているか確認してください。含まれていない場合、`getPageHistory` は `null` を返すことがあります。  
- **タイムゾーンの違い:** `getLastModifiedTime()` はシステムのデフォルトタイムゾーンで `java.util.Date` を返します。必要に応じて UTC に変換してください。  
- **ライセンスがロードされていない:** 有効なライセンスがない場合、Aspose.Note は評価モードで動作し、処理できるページ数が制限されます。

## Frequently Asked Questions

### Q1: Can I use Aspose.Note for Java to create new OneNote documents?
A1: はい、Aspose.Note for Java はプログラムから OneNote ドキュメントの作成、読み取り、操作を包括的にサポートします。

### Q2: Is Aspose.Note for Java compatible with different versions of OneNote files?
A2: はい、Aspose.Note for Java はさまざまなバージョンの Microsoft OneNote ファイルに対応しており、異なる環境間での互換性を確保します。

### Q3: Can I customize the output format when exporting OneNote documents?
A3: もちろんです。Aspose.Note for Java は PDF、HTML、画像など複数の形式へのエクスポートを柔軟にカスタマイズできるオプションを提供します。

### Q4: Does Aspose.Note for Java require a license for commercial use?
A4: はい、商用利用には有効なライセンスが必要です。ライセンスは Aspose のウェブサイトから取得できます。

### Q5: Where can I seek assistance if I encounter issues or have questions about Aspose.Note for Java?
A5: サポートや質問は Aspose.Note フォーラム **[here](https://forum.aspose.com/c/note/28)** で受け付けています。質問の投稿や経験の共有、他のユーザーやエキスパートとの交流が可能です。

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}