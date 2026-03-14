---
date: 2026-03-14
description: JavaでTIFF JPEG圧縮、TIFF PackBits圧縮、またはCCITT Group 3 Faxを使用してOneNoteドキュメントをTIFFファイルとして保存する方法を学びましょう。Aspose.Noteを使って画像品質、ファイルサイズ、カラー
  モードを制御できます。
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: OneNoteでTIFF JPEG圧縮を使用してTIFF画像に保存
url: /ja/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNoteでTIFF JPEG圧縮を使用してTIFF画像を保存する

## はじめに

このチュートリアルでは、**TIFF JPEG 圧縮** と他の 2 つの一般的な圧縮方法を使用して OneNote ドキュメントを TIFF ファイルに保存する方法を学びます。必要なセットアップの手順、Java パッケージのインポート方法、各圧縮オプションごとのステップバイステップのコード例を示します。最後まで読むと、**TIFF 画像品質** を制御し、ファイルサイズを削減し、さらにはファックス向けの白黒 TIFF も作成できるようになります。

## クイック回答
- **TIFF JPEG 圧縮とは？** 画像品質を保ちつつ TIFF ファイルサイズを削減するロッシー圧縮方式です。  
- **変換を担当するライブラリは？** Aspose.Note for Java。  
- **ライセンスは必要ですか？** テスト用の無料トライアルは利用可能です。製品版ではライセンスが必要です。  
- **画像品質は変更できますか？** はい、`ImageSaveOptions` の `quality` プロパティで設定できます。  
- **バッチ変換は可能ですか？** もちろんです。ドキュメントをループして同じオプションを適用できます。

## TIFF JPEG 圧縮とは？
TIFF JPEG 圧縮は、画像データを TIFF コンテナに格納しつつ JPEG のロッシーアルゴリズムを適用してファイルを縮小します。**tiff image quality** とファイルサイズのバランスが必要な Web やアーカイブ用途に最適です。

## なぜ異なる TIFF 圧縮タイプを使い分けるのか？
- **JPEG** – 写真に適し、品質を調整可能。  
- **PackBits** – シンプルなロスレスランレングス符号化。均一な領域が多いグラフィックに有用。  
- **CCITT Group 3 Fax** – 白黒専用。スキャン文書やファックス送信に最適。  

適切な圧縮方式を選択することで、ストレージ制限を満たしつつアプリケーションに必要な視覚的忠実度を保てます。

## Aspose.Note で OneNote を TIFF に変換する
**OneNote を TIFF に変換** したい場合、以下の 3 つのメソッドが最も一般的なシナリオをカバーします。各メソッドは `.one` ファイルを読み込み、`ImageSaveOptions` を設定し、結果を `.tiff` ファイルとして保存します。

## 前提条件

- Java Development Kit (JDK) がインストールされていること。  
- Aspose.Note for Java ライブラリがプロジェクトに追加されていること（Maven/Gradle または手動 JAR）。  
- Java の基本的な構文に慣れていること。

## パッケージのインポート

まず、必要な Aspose.Note クラスを Java ファイルにインポートします。

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 手順 1: TIFF JPEG 圧縮で TIFF に保存する

以下は OneNote ファイルを読み込み、JPEG 圧縮で TIFF として保存する完全なメソッドです。`quality` の値 (0‑100) を調整して **tiff image quality** を制御します。

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**解説**

- `ImageSaveOptions` は Aspose.Note に TIFF ファイルの出力を指示します。  
- `setTiffCompression(TiffCompression.Jpeg)` が JPEG 圧縮を選択します。  
- `setQuality(93)`（任意）は画像品質を微調整します。値が低いほどファイルは小さくなります。

### Java で JPEG 圧縮付き TIFF を保存する手順
1. `dataDir` を `.one` ファイルが格納されているフォルダーに設定します。  
2. メインメソッドまたはサービスから `SaveToTiffUsingJpegCompression()` を呼び出します。  
3. 生成された `.tiff` ファイルが同じディレクトリに作成されます。

## TIFF PackBits 圧縮の概要

PackBits は、均一な色領域が大きい画像に最適なロスレス圧縮アルゴリズムです。ドキュメントではしばしば **tiff packbits compression** と呼ばれます。

## 手順 2: PackBits 圧縮で TIFF に保存する

ロスレスが必要な場合、PackBits は単純なランレングス方式で、単色や均一色のグラフィックに適しています。

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**解説**

- `setTiffCompression(TiffCompression.PackBits)` が圧縮方式を PackBits に切り替えます。  
- PackBits はロスレスのため、品質設定は不要です。

## 手順 3: CCITT Group 3 Fax 圧縮（白黒 TIFF）で保存する

ファックス形式の文書では **白黒 TIFF** が求められます。CCITT Group 3 はモノクロ画像に対して高い圧縮率を提供します。

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**解説**

- `setColorMode(ColorMode.BlackAndWhite)` がモノクロ出力を強制します。  
- `setTiffCompression(TiffCompression.Ccitt3)` がファックス向け圧縮を適用します。

## よくある問題と対策

| 問題 | 解決策 |
|------|--------|
| **出力ファイルが予想より大きい** | JPEG の `quality` 値を下げるか、ロスレスが許容できる場合は PackBits に切り替えてください。 |
| **色がくすんで見える** | カラーが必要な場合に `ColorMode.BlackAndWhite` を誤って設定していないか確認してください。 |
| **Unsupported image format エラー** | 使用している Aspose.Note のバージョンが古く、圧縮列挙型が未実装の場合があります。最新版に更新してください。 |
| **実行時に LicenseException が発生** | 有効な Aspose.Note ライセンスをインストールします（`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`）。 |

## FAQ

**Q: 他のドキュメント形式（PDF、DOCX など）も同様のオプションで TIFF に変換できますか？**  
A: はい。Aspose.Note は OneNote に特化していますが、Aspose.PDF、Aspose.Words などのライブラリでも同様の `ImageSaveOptions` が利用可能です。

**Q: TIFF JPEG 圧縮は標準的な JPEG ファイルと何が違うのですか？**  
A: アルゴリズムは同じですが、画像データが TIFF コンテナ内に格納されます。TIFF は複数ページやリッチメタデータを保持できます。

**Q: 多数の `.one` ファイルをバッチ処理できますか？**  
A: もちろんです。ディレクトリを走査し、各ファイルに対して 3 つのメソッドのいずれかを呼び出し、結果の TIFF を収集してください。

**Q: 出力 TIFF の DPI/解像度は制御できますか？**  
A: はい。保存前に `options.setResolution(int dpi)` を使用します。

**Q: Aspose.Note は非同期処理をサポートしていますか？**  
A: API 自体は同期ですが、Java の `CompletableFuture` やスレッドプールでラップすれば並列実行が可能です。

## 結論

これで **java tiff conversion** ツールキットが完成し、OneNote ドキュメントを JPEG、PackBits、または CCITT Group 3 Fax 圧縮で TIFF に保存できるようになりました。品質、カラーモード、解像度を調整して、求められる **tiff image quality** を満たし、バッチワークフローに組み込んで生産性を最大化してください。

---

**最終更新日:** 2026-03-14  
**テスト環境:** Aspose.Note for Java 23.12（執筆時点の最新）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}