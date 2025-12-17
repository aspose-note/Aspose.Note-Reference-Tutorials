---
date: 2025-12-17
description: Aspose.Note for Java を使用して、OneNote ドキュメントをグレースケール PNG 画像として保存し、エクスポートする方法を学びます。OneNote
  ドキュメントの読み込み手順とグレースケール画像の作成が含まれています。
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: OneNote をグレースケール画像としてエクスポートする方法 – Aspose.Note
url: /ja/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote をグレースケール画像として保存 - Aspose.Note

## はじめに

このチュートリアルでは、Aspose.Note for Java を使用して **OneNote をエクスポート** し、ドキュメントをグレースケール画像として保存する方法を示します。グレースケール画像は、灰色の濃淡だけで構成された単色画像で、印刷やアーカイブ、ファイルサイズの削減に役立ちます。OneNote ドキュメントの読み込み、保存オプションを **グレースケール画像を作成** するように設定し、最終的に **PNG として保存** する手順を解説します。

## クイック回答
- **「OneNote をエクスポートする」とは何ですか？** プログラムから OneNote ファイルを別の形式（画像など）に変換することを指します。  
- **グレースケール出力に最適な形式はどれですか？** PNG はロスレス品質を保ち、グレースケールカラー モードをサポートするため適しています。  
- **ライセンスは必要ですか？** 本番環境で使用する場合は有効な Aspose.Note ライセンスが必要です。テスト用の一時トライアル ライセンスも利用可能です。  
- **必要な Java バージョンは？** Java 8 以上を推奨します。  
- **画像サイズは変更できますか？** はい、保存前に `ImageSaveOptions` の `Resolution` や `PageSize` などのプロパティを調整できます。

## 「OneNote をエクスポートする」とは？
OneNote のエクスポートとは、OneNote の `.one` ファイルをプログラムから PDF、HTML、画像など別の表現形式に変換することです。本ガイドでは、**グレースケール PNG 画像**へのエクスポートに焦点を当てます。これは、ドキュメント化や印刷ワークフローでよく求められる要件です。

## なぜ OneNote をグレースケール画像としてエクスポートするのか？
- **ファイルサイズの削減** – グレースケール PNG はフルカラー画像よりも一般的にサイズが小さくなります。  
- **可読性の向上** – 印刷レポートでは、グレースケールの方がコントラストがはっきりしやすいです。  
- **互換性** – PNG はブラウザ、エディタ、モバイルデバイスで広くサポートされています。  

## 前提条件

開始する前に、以下を用意してください。

1. システムにインストールされた Java Development Kit (JDK)。  
2. Aspose.Note for Java ライブラリ。ダウンロードは [こちら](https://releases.aspose.com/note/java/) から。  
3. Java プログラミングの基本的な知識。  

## パッケージのインポート

作業を始めるには、必要なパッケージをインポートします。

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 手順 1: OneNote ドキュメントの読み込み

まず、**OneNote ドキュメントを読み込み**ます。`"Your Document Directory"` をローカルフォルダのパスに、`"Aspose.one"` を OneNote ファイル名に置き換えてください。

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 手順 2: 出力パスとオプションの設定

グレースケール画像の出力パスを定義し、保存オプションを指定します。`ColorMode` を `GrayScale` に設定し、**PNG 形式で保存**します。

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## 手順 3: ドキュメントの保存

設定したオプションを使用して、ドキュメントをグレースケール PNG 画像として保存します。

```java
oneFile.save(dataDir, options);
```

## よくある問題と対策
- **FileNotFoundException** – `dataDir` が正しいフォルダを指しているか、`.one` ファイルが存在するか確認してください。  
- **LicenseException** – `save` を呼び出す前に有効な Aspose.Note ライセンスを適用してください。  
- **低解像度の出力** – 必要に応じて `options.setResolution(300)` などで DPI を上げてください。

## FAQ

**Q1: グレースケール画像を別の形式で保存できますか？**  
A1: はい、`ImageSaveOptions` コンストラクタの `SaveFormat` パラメータを `Jpeg`、`Bmp` などに変更すれば可能です。

**Q2: Aspose.Note はすべてのバージョンの OneNote ドキュメントに対応していますか？**  
A2: Aspose.Note は Microsoft OneNote 2010 以降のバージョンをサポートしています。

**Q3: Aspose.Note の使用にはライセンスが必要ですか？**  
A3: 本番環境での使用には有効なライセンスが必要ですが、評価用に一時的なトライアル ライセンスを取得できます。

**Q4: 画像として保存する前に、ドキュメントの他の要素を操作できますか？**  
A4: もちろんです！Aspose.Note はセクション、ページ、コンテンツの編集用 API を豊富に提供しています。

**Q5: 問題が発生した場合、どこでサポートを受けられますか？**  
A5: Aspose.Note フォーラムは [こちら](https://forum.aspose.com/c/note/28) で利用できます。

## 結論

これで **OneNote をエクスポート** し、ドキュメントを **グレースケール画像を作成** して **PNG として保存** する方法が理解できました。この手法は、OneNote ノートブックから軽量で印刷向きのビジュアルを生成する際に便利です。プロジェクトの要件に合わせて `ColorMode` の設定や画像形式を変更してみてください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2025-12-17  
**テスト環境:** Aspose.Note 24.12 for Java  
**作者:** Aspose  

---