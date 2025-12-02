---
date: 2025-12-02
description: Aspose.Note for Java を使用して OneNote を HTML として保存する際にフォントをエクスポートする方法を学びましょう。このガイドでは、プログラムで
  OneNote を作成し、フォント、CSS、画像を埋め込む方法を示します。
language: ja
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: OneNoteをHTMLとして保存するときにフォントをエクスポートする方法 – Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote を HTML として保存する際のフォントのエクスポート方法 – Java

## Introduction

このチュートリアルでは、Aspose.Note for Java を使用して **OneNote を HTML として保存** する際に **フォントをエクスポートする方法** を紹介します。プログラムで OneNote ドキュメントを作成し、HTML 保存オプションを設定し、必要なフォントファイルを埋め込む手順を解説します。これにより、生成された HTML が元の OneNote ページとまったく同じ外観になります。このアプローチは、OneNote コンテンツの視覚的忠実性をウェブフレンドリーな形式で保持したい場合に最適です。

## Quick Answers
- **エクスポートを処理するライブラリは？** Aspose.Note for Java  
- **HTML にフォントを埋め込むことはできますか？** はい – `ExportFonts` を `ExportEmbedded` に設定します  
- **本番環境でライセンスが必要ですか？** 商用利用には有効な Aspose.Note ライセンスが必要です  
- **サポートされている Java バージョンは？** Java 8 以上  
- **リソースを別ファイルとして保存できますか？** もちろんです – `ResourceExportType` を適切に設定します  

## What is “how to export fonts” in the context of OneNote HTML conversion?

OneNote ノートブックを HTML に変換する際、視覚的な外観は CSS、画像、そして特に元ページで使用されているフォントに依存します。**フォントのエクスポート** とは、フォントファイル（例: TTF）を HTML パッケージに直接埋め込むことで、ユーザーのローカルにそのフォントがインストールされていなくても、ブラウザが OneNote と同じようにテキストを表示できるようにすることです。

## Why create OneNote programmatically and save it as HTML?

- **自動化:** 手動でコピー＆ペーストすることなく、OneNote からレポート、ドキュメント、ナレッジベース記事を生成します。  
- **一貫性:** デバイス間でレイアウト、スタイル、カスタムフォントを保持します。  
- **ポータビリティ:** HTML はどこでも閲覧可能で、OneNote クライアントは不要です。  

## Prerequisites

1. Java Development Kit (JDK) 8 以上がインストールされていること。  
2. Aspose.Note for Java ライブラリ – [here](https://releases.aspose.com/note/java/) からダウンロードしてください。  
3. 読み込むサンプル OneNote ファイル（`.one`）またはプログラムで新規作成できるもの。  

## Import Packages

First, import the required classes into your Java project:

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

## How to Export Fonts While Saving OneNote as HTML?

以下は、**フォントをエクスポート** する方法とその他リソースの手順です。

### Step 1: Create a OneNote document programmatically  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

この行は既存の `.one` ファイルを読み込みます。**プログラムで OneNote を作成** する必要がある場合は、新しい `Document` オブジェクトをインスタンス化し、API を使用してセクションやページを追加できます（ここではフォントのエクスポートに焦点を当てるため省略しています）。

### Step 2: Save to a memory stream with embedded fonts  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` は Aspose.Note にフォントを HTML パッケージに直接 **エクスポート** するよう指示します。  
- `setFontFaceTypes(FontFaceType.Ttf)` は TrueType フォントを使用することを保証し、幅広いブラウザでサポートされます。  

### Step 3: Save as HTML with separate resource files (still exporting fonts)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

CSS と画像は埋め込まれていますが、キャッシュを容易にするために別ファイルが必要な場合は `ResourceExportType` を `ExportExternal` に変更できます。重要なポイントである **フォントのエクスポート** は変わりません。

### Step 4: Use callbacks to control where each resource is stored  

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

`UserSavingCallbacks` クラス（`ICssSavingCallback`、`IImageSavingCallback`、`IFontSavingCallback` を実装する必要があります）はフォルダー構造を完全に制御でき、フォントを専用の `fonts` ディレクトリに保存しつつ **フォントを正しくエクスポート** できます。

## Common Issues & Tips

- **出力にフォントが欠如している:** `setExportFonts(ResourceExportType.ExportEmbedded)` が設定されていること、そして元の OneNote ファイルが実際に埋め込みフォントを使用していることを確認してください。  
- **HTML ファイルが大きくなる:** フォントを埋め込むとサイズが増加します。帯域幅が問題になる場合は `ExportFonts` を `ExportExternal` に切り替え、フォントを CDN でホストしてください。  
- **コールバック実装エラー:** コールバッククラスがストリームを書き込み、リソースを正しくクローズしてファイル破損を防止していることを確認してください。  

## Frequently Asked Questions

**Q: 複数の OneNote ドキュメントを一括で HTML に変換できますか？**  
A: はい、各 `Document` インスタンスをループし、同じ `HtmlSaveOptions` を適用します。

**Q: Aspose.Note for Java は HTML 以外の出力形式をサポートしていますか？**  
A: もちろんです。適切な保存オプションを使用して、PDF、DOCX、PNG、JPEG などにエクスポートできます。

**Q: Aspose.Note for Java のトライアル版はありますか？**  
A: はい、[here](https://releases.aspose.com/) から無料トライアルをダウンロードしてください。

**Q: Aspose.Note for Java のサポートはどこで受けられますか？**  
A: コミュニティと公式サポートのために [Aspose.Note forum](https://forum.aspose.com/c/note/28) をご利用ください。

**Q: Aspose.Note for Java のライセンスはどのように購入できますか？**  
A: ライセンスは [Aspose website](https://purchase.aspose.com/buy) で入手可能です。

## Conclusion

これで、Aspose.Note for Java を使用して **OneNote を HTML として保存** する際に **フォントをエクスポート** する方法が分かりました。`HtmlSaveOptions` を設定し、必要に応じてコールバックを使用することで、カスタムフォントを含む OneNote ページの正確な外観をウェブ上で提供できます。プロジェクトのパフォーマンスやストレージ要件に合わせて、さまざまな `ResourceExportType` 設定を試してみてください。

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
