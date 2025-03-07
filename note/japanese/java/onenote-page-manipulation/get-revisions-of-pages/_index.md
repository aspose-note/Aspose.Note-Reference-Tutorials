---
title: OneNote でページのリビジョンを取得する - Aspose.Note
linktitle: OneNote でページのリビジョンを取得する - Aspose.Note
second_title: Aspose.Note Java API
description: Aspose.Note Java を使用して OneNote ドキュメント内のページのリビジョンを取得する方法を学習します。これを Java アプリに統合して、効率的なドキュメント管理を実現します。
weight: 15
url: /ja/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote でページのリビジョンを取得する - Aspose.Note

## 導入

このチュートリアルでは、Java アプリケーションで Microsoft OneNote ファイルをシームレスに操作できるようにする強力なライブラリである Aspose.Note for Java の機能を詳しく説明します。具体的には、OneNote ドキュメント内のページのリビジョンを取得する方法に焦点を当てます。このガイドを終えると、最終変更時刻、作成時刻、タイトル、レベル、作成者などの詳細を含む、ページ リビジョンを効率的に抽出するための知識が身につくでしょう。

## 前提条件

このチュートリアルに進む前に、次の前提条件が設定されていることを確認してください。

### Java 開発キット (JDK) がインストールされている

システムに Java Development Kit がインストールされていることを確認してください。 Oracle Web サイトからダウンロードしてインストールするか、Unix ベースのシステムを使用している場合はパッケージ マネージャーを使用できます。

### Java ライブラリの Aspose.Note

 Web サイトから Aspose.Note for Java ライブラリをダウンロードしてインストールします。ダウンロードリンクが見つかります[ここ](https://releases.aspose.com/note/java/)。ドキュメントに記載されているインストール手順に従ってください[ここ](https://reference.aspose.com/note/java/).

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。これらのパッケージを使用すると、Aspose.Note for Java が提供する機能を利用できるようになります。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

ここで、提供されているサンプル コードを複数のステップに分けて、各コンポーネントとその機能を理解しましょう。

## ステップ 1: ドキュメント ディレクトリを設定する

OneNote ドキュメントが配置されるディレクトリを定義します。

```java
String dataDir = "Your Document Directory";
```

## ステップ 2: ドキュメントをロードする

OneNote ドキュメントを Aspose.Note に読み込みます。

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## ステップ 3: 最初のページを取得する

ドキュメントから最初のページを取得します。

```java
Page firstPage = doc.getFirstChild();
```

## ステップ 4: ページのリビジョンを取得する

ページの更新履歴を取得します。

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## ステップ 5: ページの改訂を確認する

ページ リビジョンのリストを繰り返し処理し、関連情報を取得します。

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

## 結論

このチュートリアルでは、Aspose.Note for Java を使用して OneNote ドキュメント内のページのリビジョンを取得する方法を説明しました。ステップバイステップのガイドに従い、提供されているサンプル コードを活用すると、この機能を Java アプリケーションに簡単に統合でき、OneNote ファイルを効率的に管理できるようになります。

## よくある質問

### Q1: Aspose.Note for Java を使用して新しい OneNote ドキュメントを作成できますか?

A1: はい、Aspose.Note for Java は、OneNote ドキュメントをプログラムで作成、読み取り、操作するための包括的なサポートを提供します。

### Q2: Aspose.Note for Java は、さまざまなバージョンの OneNote ファイルと互換性がありますか?

A2: はい、Aspose.Note for Java はさまざまなバージョンの Microsoft OneNote ファイルをサポートしており、さまざまな環境間での互換性が確保されています。

### Q3: OneNote ドキュメントをエクスポートするときに出力形式をカスタマイズできますか?

A3: もちろん、Aspose.Note for Java は、OneNote ドキュメントを PDF、HTML、画像などのさまざまな形式に柔軟にエクスポートでき、カスタマイズのオプションも提供します。

### Q4: Aspose.Note for Java を商用利用するにはライセンスが必要ですか?

A4: はい、Aspose.Note for Java を商用利用するには有効なライセンスが必要です。ライセンスは、Aspose Web サイトから取得できます。

### Q5: Aspose.Note for Java に関して問題が発生したり質問がある場合は、どこに問い合わせればよいですか?

 A5: サポートと支援が必要な場合は、Aspose.Note フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/note/28)、質問したり、経験を共有したり、他のユーザーや専門家と交流したりできます。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
