---
date: 2025-12-17
description: JavaでTIFF JPEG圧縮、PackBits、またはCCITT Group 3 Faxを使用してOneNoteドキュメントをTIFFファイルとして保存する方法を学びましょう。Aspose.Noteで画像品質、ファイルサイズ、カラーモードを制御できます。
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

このチュートリアルでは、**TIFF JPEG圧縮** と他の 2 つの一般的な圧縮方法を使用して OneNote ドキュメントを TIFF ファイルに保存する方法を学びます。必要なセットアップの手順、必要な Java パッケージのインポート、各圧縮オプションのコードをステップバイステップで解説します。最後まで実施すれば、**TIFF 画像品質** を制御し、ファイルサイズを削減し、さらにはファックス向けの白黒 TIFF を生成できるようになります。

## クイック回答
- **TIFF JPEG 圧縮とは？** 画像品質を保ちつつ TIFF ファイルサイズを削減するロスィ圧縮方式です。  
- **変換を担当するライブラリは？** Aspose.Note for Java。  
- **ライセンスは必要ですか？** テスト用の無料トライアルは利用可能です。製品環境ではライセンスが必要です。  
- **画像品質は変更できますか？** はい、`ImageSaveOptions` の `quality` プロパティで設定できます。  
- **バッチ変換は可能ですか？** もちろんです。ドキュメントをループして同じオプションを適用できます。

## TIFF JPEG圧縮とは？

TIFF JPEG 圧縮は、画像データを TIFF コンテナに格納しつつ、JPEG のロスィアルゴリズムを適用してファイルを縮小します。**tiff image quality** と小さなファイルサイズのバランスが必要な Web やアーカイブ用途に最適です。

## なぜ異なるTIFF圧縮タイプを使用するのか？

- **JPEG** – 写真に適しており、品質を調整可能。  
- **PackBits** – シンプルなロスレスランレングスエンコーディング。均一領域が多いグラフィックに有用。  
- **CCITT Group 3 Fax** – 白黒専用。スキャン文書やファックス送信に最適。  

適切な圧縮方式を選択すれば、ストレージ制約を満たしつつ、アプリケーションに必要な視覚的忠実度を犠牲にしません。

## 前提条件

- Java Development Kit (JDK) がインストールされていること。  
- Aspose.Note for Java ライブラリがプロジェクトに追加されていること（Maven/Gradle または手動 JAR）。  
- Java の基本構文に慣れていること。

## パッケージのインポート

まず、必要な Aspose.Note クラスを Java ファイルにインポートします。

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 手順1: TIFF JPEG圧縮を使用してFFに保存する

以下は、OneNote ファイルを読み込み、JPEG 圧縮で TIFF として保存する完全なメソッドです。`quality` 値 (0‑100) を調整して **tiff image quality** を制御します。

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

**説明**

- `ImageSaveOptions` は Aspose.Note に TIFF ファイルの出力を指示します。  
- `setTiffCompression(TiffCompression.Jpeg)` が JPEG 圧縮を選択します。  
- `setQuality(93)`（任意）は画像品質を微調整します。値が低いほどファイルは小さくなります。

### JavaでJPEG圧縮でTIFFを保存する方法
1. `dataDir` を `.one` ファイルが格納されているフォルダーに設定します。  
2. メインメソッドまたはサービスから `SaveToTiffUsingJpegCompression()` を呼び出します。  
3. 生成された `.tiff` ファイルが同じディレクトリに出力されます。

## 手順2: PackBits圧縮を使用してTIFFに保存する

ロスレスが必要な場合、PackBits は単純なランレングスアルゴリズムで、均一色のグラフィックに適しています。

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

**説明**

- `setTiffCompression(TiffCompression.PackBits)` が圧縮方式を切り替えます。  
- PackBits はロスレスのため、品質設定は不要です。

## 手順3: CCITT Group 3 Fax圧縮（白黒TIFF）を使用してTIFFに保存する

ファックススタイルの文書では **白黒 TIFF** が求められます。CCITT Group 3 はモノクロ画像に高圧縮率を提供します。

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

**説明**

- `setColorMode(ColorMode.BlackAndWhite)` がモノクロ出力を強制します。  
- `setTiffCompression(TiffCompression.Ccitt3)` がファックス向け圧縮を適用します。

## よくある問題とヒント

| 問題 | 解決策 |
|------|--------|
| **出力ファイルが予想より大きい** | JPEG の `quality` 値を下げるか、ロスレスが許容できる場合は PackBits に切り替えてください。 |
| **色がくすんで見える** | カラーが必要な場合に `ColorMode.BlackAndWhite` を誤って設定していないか確認してください。 |
| **Unsupported image format エラー** | 使用している Aspose.Note のバージョンが古くないか確認してください。古いビルドでは一部圧縮列挙子が未実装の場合があります。 |
| **実行時に LicenseException が発生** | 有効な Aspose.Note ライセンスをインストールしてください（`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`）。 |

## よくある質問

**Q: 他のドキュメント形式（例: PDF、DOCX）も同様のオプションで TIFF に変換できますか？**  
A: はい。Aspose.Note は OneNote に特化していますが、Aspose の他のライブラリ（PDF、Words など）でも同様の `ImageSaveOptions` が提供されています。

**Q: TIFF JPEG 圧縮は標準の JPEG ファイルとどう違うのですか？**  
A: 画像データは TIFF コンテナ内に格納、メタデータ保持や複数ページが可能です。圧縮アルゴリズム自体は JPEG と同じです。

**Q: 多数の `.one` ファイルをバッチ処理できますか？**  
A: もちろんです。フォルダーを走査し、各ファイルに対して任意の 3 つのメソッドを呼び出し、TIFF を生成してください。

**Q: 出力 TIFF の DPI/解像度は制御できますか？**  
A: はい。保存前に `options.setResolution(int dpi)` を使用してください。

**Q: Aspose.Note は非同期処理をサポートしていますか？**  
A: API 自体は同期ですが、`CompletableFuture` やスレッドプールでラップすれば並列実行が可能です。

## 結論

これで **java tiff conversion** ツールキットが完成し、OneNote ドキュメントを JPEG、PackBits、または CCITT Group 3 Fax 圧縮で TIFF に保存できるようになりました。品質、カラーモード、解像度を調整して、特定の **tiff image quality** 要件を満たし、バッチワークフローに組み込んで生産性を最大化してください。

---

**最終更新日:** 2025-12-17  
**テスト環境:** Aspose.Note for Java 23.12（執筆時点での最新）  
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}