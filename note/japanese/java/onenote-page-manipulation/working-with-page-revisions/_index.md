---
title: OneNote でのページ リビジョンの操作 - Aspose.Note
linktitle: OneNote でのページ リビジョンの操作 - Aspose.Note
second_title: Aspose.Note Java API
description: Aspose.Note for Java を使用して OneNote ドキュメントのページ リビジョンを管理する方法を学習します。効果的なリビジョン追跡とコラボレーションのためのステップバイステップのガイドを提供します。
weight: 21
url: /ja/java/onenote-page-manipulation/working-with-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote でのページ リビジョンの操作 - Aspose.Note

## 導入

OneNote はメモを整理および管理するための強力なツールですが、場合によっては変更を追跡し、効率的に共同作業するためにリビジョンを操作する必要があります。 Aspose.Note for Java を使用すると、OneNote ドキュメントのページ リビジョンをプログラムで簡単に管理できます。このチュートリアルでは、プロセスを段階的に説明します。

## 前提条件

始める前に、以下のものがあることを確認してください。

### Java開発環境

システムに Java Development Kit (JDK) がインストールされていることを確認してください。

### Java ライブラリの Aspose.Note

Java ライブラリ用の Aspose.Note を次からダウンロードしてインストールします。[ここ](https://releases.aspose.com/note/java/).

### OneNote ドキュメント

テスト目的でサンプルの OneNote ドキュメントを用意します。

## パッケージのインポート

Java プロジェクトで、Aspose.Note for Java で動作するために必要なパッケージをインポートします。

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

明確に理解できるように、提供された例を複数のステップに分けてみましょう。

## ステップ 1: OneNote ドキュメントをロードする

まず、OneNote ドキュメントを読み込み、最初の子ページを取得します。

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## ステップ 2: ページ改訂概要を読む

ページのコンテンツ改訂概要を読んでください。

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## ステップ 3: ページの改訂概要を更新する

新しい作成者と変更日を使用してページ改訂概要を更新します。

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## 結論

Aspose.Note for Java を使用すると、OneNote ドキュメントのページ リビジョンをプログラムで管理することが簡単になります。このチュートリアルで概説されている手順に従うことで、ページ リビジョンを効果的に操作して変更を追跡し、シームレスに共同作業することができます。

## よくある質問

### Q1: Aspose.Note for Java を他の Java ライブラリと一緒に使用できますか?

A: はい、Aspose.Note for Java は他の Java ライブラリと統合して機能を強化できます。

### Q2: Aspose.Note for Java は、OneNote ドキュメントのすべてのバージョンをサポートしていますか?

A: Aspose.Note for Java は、古いバージョンを含むさまざまなバージョンの OneNote ドキュメントをサポートしています。

### Q3: Aspose.Note for Java はエンタープライズ レベルのアプリケーションに適していますか?

A: もちろん、Aspose.Note for Java は、堅牢な機能と拡張性を備えたエンタープライズ レベルのアプリケーションのニーズを満たすように設計されています。

### Q4: Aspose.Note for Java を使用してページ リビジョンをカスタマイズできますか?

A: はい、Aspose.Note for Java を使用して、要件に応じてページ リビジョンをカスタマイズできます。

### Q5: Aspose.Note for Java のサポートはどこで入手できますか?

 A: Aspose.Note for Java のサポートは、[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
