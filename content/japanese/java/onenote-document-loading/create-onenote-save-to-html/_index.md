---
title: OneNote ドキュメントを作成して HTML に保存する - Java
linktitle: OneNote ドキュメントを作成して HTML に保存する - Java
second_title: Aspose.Note Java API
description: Aspose.Note for Java を使用して OneNote ドキュメントを HTML として作成し、保存する方法を学びます。 Java アプリケーションに統合して、プログラムによる OneNote ファイル処理を実現します。

type: docs
weight: 18
url: /ja/java/onenote-document-loading/create-onenote-save-to-html/
---
## 導入

Aspose.Note for Java は、開発者が Microsoft OneNote ファイルをプログラムで操作できるようにする強力なライブラリです。このチュートリアルでは、Aspose.Note for Java を使用して OneNote ドキュメントを作成し、それを HTML 形式で保存する方法を説明します。

## 前提条件

始める前に、以下のものがあることを確認してください。

1. Java Development Kit (JDK) がシステムにインストールされています。
2.  Java ライブラリの Aspose.Note。からダウンロードできます[ここ](https://releases.aspose.com/note/java/).
3. Java プログラミングの基本的な知識。

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## ステップ 1: OneNote ドキュメント オブジェクトを作成する

```java
Document document = new Document("Path_to_your_sample_one_file");
```

このコードは`Document`サンプル OneNote ファイルをロードしてオブジェクトを作成します。

## ステップ 2: HTML として Memory Stream に保存する

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

ここでは、HTML 保存オプションを設定し、ドキュメントをメモリ ストリームに保存します。

## ステップ 3: リソースを別のファイルに含めて HTML として保存する

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

この手順では、CSS、フォント、画像などのリソースを含むドキュメントを HTML として別のファイルに保存します。

## ステップ 4: リソースを保存するためのコールバックを使用して、HTML として Memory Stream に保存する

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

ここでは、リソースの節約を処理するコールバックを使用して、ドキュメントを HTML としてメモリ ストリームに保存します。

## 結論

おめでとう！ Aspose.Note for Java を使用して OneNote ドキュメントを作成し、HTML 形式で保存する方法を学習しました。この機能を Java アプリケーションに統合して、プログラムで OneNote ファイルを操作できるようになりました。

## よくある質問

### Q1: 複数の OneNote ドキュメントを一度に HTML に変換できますか?

A1: はい、複数のドキュメントをループして、保存プロセスを繰り返し適用できます。

### Q2: Aspose.Note for Java は HTML 以外の出力形式をサポートしていますか?

A2: はい、Aspose.Note for Java は、PDF、DOCX、画像形式などのさまざまな出力形式をサポートしています。

### Q3: Aspose.Note for Java の試用版はありますか?

A3: はい、以下から無料試用版をダウンロードできます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.Note for Java のサポートはどこで入手できますか?

 A4: サポートを受けることができます。[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28).

### Q5: Aspose.Note for Java のライセンスはどのように購入できますか?

 A5: ライセンスは以下から購入できます。[Aspose ウェブサイト](https://purchase.aspose.com/buy).