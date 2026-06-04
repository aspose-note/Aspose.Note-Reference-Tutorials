---
date: 2026-01-10
description: Java 用の Aspose.Note ページ改訂チュートリアルを学びましょう – Aspose.Note を使用してプログラムで OneNote
  ページの改訂を取得します。ステップバイステップのガイドに従ってください。
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: aspose.note ページ改訂チュートリアル – OneNote でページ改訂を取得する
url: /ja/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote でページのリビジョンを取得 - Aspose.Note

OneNote は強力なノート作成プラットフォームで、変更の監査が必要なときは、**aspose.note page revisions tutorial** が数行の Java コードだけでリビジョン履歴を取得する方法を正確に示します。このガイドでは、環境設定から各リビジョンの詳細を出力するまで、必要な手順をすべて解説するので、編集、作者の貢献、タイムスタンプを簡単に追跡できます。

## クイック回答
- **このチュートリアルの対象は何ですか？** Aspose.Note for Java を使用して OneNote ファイルからページのリビジョン履歴を取得します。  
- **どのライブラリバージョンが必要ですか？** `LoadOptions.setLoadHistory` をサポートする最近の Aspose.Note for Java リリースであればどれでも構いません。  
- **ライセンスは必要ですか？** テスト用の一時評価ライセンスで動作しますが、製品版では商用ライセンスが必要です。  
- **リビジョンを変更できますか？** API はリビジョンに対して読み取り専用で、取得のみ可能です。  
- **主な前提条件は何ですか？** Java JDK、Aspose.Note for Java、そしてリビジョンデータを含む OneNote ドキュメントです。

## “aspose.note page revisions tutorial” とは？
このチュートリアルは、プログラムから OneNote ページの履歴バージョンにアクセスする方法を示します。各リビジョンには作者、作成時刻、変更時刻といったメタデータが含まれ、アプリケーション内で監査トレイルや変更ログ機能を構築できるようになります。

## ページリビジョン追跡に Aspose.Note を使用する理由
- **UI 依存なし** – 完全にコード上で動作し、バックエンドサービスに最適です。  
- **クロスプラットフォーム** – Java は Windows、Linux、macOS 上で動作します。  
- **フルコントロール** – OneNote を手動で開かずに、すべてのリビジョンプロパティを取得できます。  
- **パフォーマンス** – 履歴のロードが最適化されているため、大規模なノートブックでも高速に処理できます。

## 前提条件

### 1. Java Development Kit (JDK)
最新の JDK（8 以上）がインストールされ、`JAVA_HOME` が設定されていることを確認してください。

### 2. Aspose.Note for Java
ライブラリは[download link](https://releases.aspose.com/note/java/)からダウンロードしてください。

### 3. Sample OneNote Document
リビジョン履歴を含む OneNote ファイル（例: `Sample1.one`）を作成または取得してください。

## パッケージのインポート
まず、必要な Aspose.Note クラスをインポートします。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## ステップバイステップ実装

### ステップ 1: ドキュメントディレクトリの設定
OneNote ファイルが格納されているフォルダーを定義します。

```java
String dataDir = "Your Document Directory";
```

### ステップ 2: 履歴を有効にして OneNote ドキュメントをロード
`LoadOptions` フラグを有効にしてリビジョンデータを取得します。

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### ステップ 3: 最初のページを取得
最初のページオブジェクトを取得します。これが履歴取得の基準点となります。

```java
Page firstPage = document.getFirstChild();
```

### ステップ 4: ページリビジョンを反復処理
各リビジョンをループし、タイムスタンプ、タイトル、レベル、作者などの有用なメタデータを出力します。

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

> **プロのコツ:** 特定の作者や日付範囲でリビジョンをフィルタリングしたい場合は、`for` ループ内に条件チェックを追加するだけです。

## よくある問題と解決策
- **リビジョンが返されない:** ドキュメントをロードする前に `loadOptions.setLoadHistory(true)` が呼び出されていることを確認してください。  
- **作者またはタイトルが null:** 古い OneNote バージョンではこれらのフィールドが保存されていないことがあります。`null` 値は適切に処理してください。  
- **大規模ノートブックでのパフォーマンス低下:** 必要なセクションだけをロードするか、JVM のヒープサイズを増やしてください。

## よくある質問

**Q1: Aspose.Note for Java を使用してページリビジョンを変更できますか？**  
A1: いいえ、API は現在ページリビジョンに対して読み取り専用で、変更はできません。

**Q2: Aspose.Note for Java はさまざまなバージョンの OneNote ドキュメントに対応していますか？**  
A2: はい、複数の OneNote ファイル形式に対応しており、バージョン間でシームレスに処理できます。

**Q3: Aspose.Note for Java の使用にはライセンスが必要ですか？**  
A3: 製品環境での使用には商用ライセンスが必要ですが、テスト用の一時評価ライセンスは利用可能です。

**Q4: Aspose.Note for Java 使用中に問題が発生した場合、サポートを受けられますか？**  
A4: はい、Aspose.Note フォーラム [here](https://forum.aspose.com/c/note/28) で質問できます。

**Q5: Aspose.Note for Java の無料トライアルはありますか？**  
A5: はい、[website](https://releases.aspose.com/) から無料トライアルをダウンロードできます。

**最終更新日:** 2026-01-10  
**テスト環境:** Aspose.Note for Java (latest release)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}