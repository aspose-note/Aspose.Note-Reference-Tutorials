---
date: 2026-01-15
description: Aspose.Note for Java を使用して、OneNote の変更を追跡し、OneNote ドキュメント内のページ改訂を管理する方法を学びます。改訂サマリーの例と改訂日付の変更方法が含まれています。
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNoteで変更履歴を追跡 – Aspose.Noteでページのリビジョンを管理
url: /ja/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote のページリビジョンの操作 - Aspose.Note

## はじめに

OneNote はノートを整理するための強力なツールであり、**track changes onenote** が必要な場合、ページリビジョンの管理は効果的なコラボレーションに不可欠です。Aspose.Note for Java を使用すると、リビジョンをプログラムで処理し、ページを編集した人物を確認したり、タイムスタンプを調整したりできます。このチュートリアルでは、ドキュメントの読み込みからリビジョンサマリーの更新まで、各ステップを順に解説します。

## クイック回答
- **“track changes onenote” とは何ですか？** OneNote のページを誰がいつ編集したかを監視することを指します。
- **必要なライブラリはどれですか？** Aspose.Note for Java。
- **リビジョンの作成者や日付を変更できますか？** はい、RevisionSummary API（`modify revision date`）を使用します。
- **事前に OneNote ファイルが必要ですか？** はい、サンプルの `.one` ファイルが必要です。
- **本番環境でライセンスは必要ですか？** 商用利用には有効な Aspose.Note ライセンスが必要です。

## リビジョンサマリーの例とは何ですか？

*revision summary* はページ上の最新変更に関するメタデータ（作成者名、最終更新時刻、その他の詳細）を提供します。このガイドでは、その情報を取得して表示し、**modify revision date** の方法を示します。

## Aspose.Note で track changes onenote を行う理由は？

- **コラボレーション:** 最新の編集者をすぐに確認できます。
- **監査:** コンプライアンスのために信頼できる変更履歴を保持します。
- **自動化:** リビジョン処理をバックエンドサービスや移行ツールに統合します。

## 前提条件

### Java 開発環境
システムに Java Development Kit (JDK) がインストールされていることを確認してください。

### Aspose.Note for Java ライブラリ
以下のリンクから Aspose.Note for Java ライブラリをダウンロードしてインストールしてください。[here](https://releases.aspose.com/note/java/)

### OneNote ドキュメント
テスト用にサンプルの OneNote ドキュメントを用意してください。

## パッケージのインポート

Java プロジェクトで、Aspose.Note for Java を使用するために必要なパッケージをインポートします。

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

提供された例を複数のステップに分解し、わかりやすく説明します。

## ステップ 1: OneNote ドキュメントの読み込み

まず、OneNote ドキュメントを読み込み、最初の子ページを取得します。

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## ステップ 2: ページリビジョンサマリーの読み取り

ページのコンテンツリビジョンサマリーを読み取ります。これは、ページを最後に編集した人物を示す **revision summary example** です。

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## ステップ 3: ページリビジョンサマリーの更新

新しい作成者と新しい更新日付でページリビジョンサマリーを更新します。これは、プログラムで **modify revision date** を行う方法のデモです。

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## 結論

OneNote ドキュメントのページリビジョンをプログラムで管理することは、Aspose.Note for Java を使用すると簡素化できます。このチュートリアルで示した手順に従うことで、効果的に **track changes onenote** を行い、リビジョンの詳細を確認し、さらに **modify revision date** をワークフローに合わせて変更できます。

## FAQ

### Q1: Aspose.Note for Java を他の Java ライブラリと併用できますか？

A: はい、Aspose.Note for Java は他の Java ライブラリと統合して機能を拡張できます。

### Q2: Aspose.Note for Java はすべてのバージョンの OneNote ドキュメントをサポートしていますか？

A: Aspose.Note for Java は、古いバージョンを含むさまざまなバージョンの OneNote ドキュメントをサポートしています。

### Q3: Aspose.Note for Java はエンタープライズレベルのアプリケーションに適していますか？

A: もちろんです。Aspose.Note for Java は、堅牢な機能とスケーラビリティでエンタープライズレベルのアプリケーションのニーズに応えるよう設計されています。

### Q4: Aspose.Note for Java でページリビジョンをカスタマイズできますか？

A: はい、Aspose.Note for Java を使用して、要件に合わせてページリビジョンをカスタマイズできます。

### Q5: Aspose.Note for Java のサポートはどこで受けられますか？

A: [Aspose.Note フォーラム](https://forum.aspose.com/c/note/28) からサポートを受けられます。

---

**最終更新日:** 2026-01-15  
**テスト環境:** Aspose.Note for Java 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}