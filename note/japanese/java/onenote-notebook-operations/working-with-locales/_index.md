---
date: 2026-01-05
description: デフォルトロケールの設定、OneNoteドキュメントの読み込み、Aspose ライセンスの設定、OneNote を PNG に変換し、Aspose.Note
  for Java を使用して OneNote を画像として保存する方法を学びます。
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote のデフォルトロケールを設定 – Aspose.Note Java
url: /ja/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote のデフォルトロケール設定 – Aspose.Note Java

## Introduction

OneNote ファイルを処理する際に **デフォルトロケールを設定** したい場合、Aspose.Note for Java を使えば簡単です。このチュートリアルでは、製品のライセンス設定から OneNote ドキュメントの読み込み、ロケールの変更、最終的に PNG 画像への変換まで、必要な手順をすべて解説します。最後まで実行すれば、数行のコードで言語設定をカスタマイズし、ロケール固有の出力を生成できるようになります。

## Quick Answers
- **「デフォルトロケールを設定する」とは何ですか？** Aspose.Note が OneNote ファイルを読み書きする際に使用する言語と地域の書式設定を定義します。  
- **ライセンスは必要ですか？** はい。Aspose のライセンスを設定して、すべての機能を有効にしてください。  
- **必要な Java バージョンは？** JDK 8 以上であればすべてサポートされています。  
- **OneNote を PNG に変換できますか？** もちろんです。API を使ってページを画像として保存できます。  
- **この処理はスレッドセーフですか？** デフォルトロケールはグローバル設定なので、アプリケーション起動時に一度だけ設定すれば問題ありません。

## What is “set default locale” in Aspose.Note?
デフォルトロケールを設定すると、Aspose.Note が日付、数値、テキストを解析する際に適用する言語と文化的慣習が決まります。これは、異なるユーザーのロケール間で一貫した書式を保つ必要があるマルチリージョン アプリケーションにとって重要です。

## Why set the default locale when working with OneNote?
- **正確なデータ表現:** 日付や数値が対象ユーザーに合わせて正しく表示されます。  
- **一貫した UI 文字列:** OneNote から抽出したテキストが言語設定を尊重します。  
- **変換の簡素化:** 後で OneNote ファイルを PNG などに変換する際、レイアウトが期待通りのロケールに合わせて表示されます。

## Prerequisites

- **Java 開発環境:** JDK がインストールされ、`JAVA_HOME` が設定されていること。  
- **Aspose.Note ライブラリ:** 最新の JAR を [download link](https://releases.aspose.com/note/java/) からダウンロードしてください。  
- **有効な Aspose ライセンス ファイル**（テスト用の無料トライアルでも可）。

## Import Packages

コードを書く前に、必要な機能を提供するクラスをインポートします。

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Step 1: Set Aspose License

```java
License license = new License();
license.setLicense("licenseFile");
```

Aspose のライセンスを設定すると、ロケール処理や画像変換を含むすべての機能が有効になります。

## Step 2: Set Default Locale

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

ここではデフォルトロケールを英語 (`en`)、国コード `rs` に設定しています。対象地域に合わせて言語コードと国コードを変更してください。

## Step 3: Load OneNote Document

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

このステップで OneNote ドキュメントを `Document` オブジェクトに **ロード** し、内容にアクセスできるようにします。

## Step 4: Convert OneNote to PNG (OneNote file conversion)

```java
oneFile.save("sample.png");
```

`save` メソッドは **OneNote ファイル変換** を実行し、ノートブック（または特定のページ）を PNG 画像としてエクスポートします。実質的に **OneNote を PNG に変換** し、**OneNote を画像として保存** する操作です。

## Common Issues & Tips

- **ライセンスが見つからない:** `licenseFile` のパスが正しいか、ファイルに読み取り権限があるか確認してください。  
- **ロケールが適用されない:** ドキュメントをロードする **前に** `Locale.setDefault` を呼び出してください。  
- **画像出力がない:** OneNote ファイルにレンダリング可能なページが含まれているか確認してください。空のノートブックは空白の PNG になります。

## Frequently Asked Questions

**Q: Aspose.Note はさまざまな Java バージョンに対応していますか？**  
A: はい、Aspose.Note は Java 8 以降をサポートしており、幅広い開発環境で利用できます。

**Q: Aspose.Note を他の Java ライブラリと統合できますか？**  
A: もちろんです。API は Apache POI、Jackson、Spring などの一般的なライブラリとシームレスに連携します。

**Q: Aspose.Note は異なるファイル形式のサポートも提供していますか？**  
A: コアは OneNote ファイルですが、PNG、JPEG、PDF などの画像形式へエクスポートすることも可能です。

**Q: Aspose.Note ユーザー向けのコミュニティフォーラムはありますか？**  
A: はい、Aspose のコミュニティフォーラムではユーザーが専門家と交流し、質問や解決策を共有できます。サポートが必要な場合は [support forum](https://forum.aspose.com/c/note/28) をご利用ください。

**Q: 購入前に Aspose.Note を試用できますか？**  
A: もちろんです。ウェブサイトで提供されている無料トライアルで機能を確認できます。

## Conclusion

この手順に従うことで、**デフォルトロケールの設定**、**OneNote ドキュメントのロード**、**Aspose ライセンスの設定**、そして **OneNote を PNG に変換** する方法を習得できました。これにより、グローバルなオーディエンス向けにロケール対応のレポートや画像を簡単に生成できるようになります。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2026-01-05  
**テスト環境:** Aspose.Note 24.11 for Java  
**作者:** Aspose  

---