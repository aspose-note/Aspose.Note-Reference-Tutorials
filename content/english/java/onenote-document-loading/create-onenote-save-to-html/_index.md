---
title: Create OneNote Document and Save to HTML - Java
linktitle: Create OneNote Document and Save to HTML - Java
second_title: Aspose.Note Java API
description: Learn how to use Aspose.Note for Java to create OneNote documents and save them as HTML with embedded resources.
type: docs
weight: 18
url: /java/onenote-document-loading/create-onenote-save-to-html/
---
## Introduction

Aspose.Note for Java is a powerful library that allows developers to work with Microsoft OneNote files programmatically. In this tutorial, we will explore how to create a OneNote document and save it to HTML format using Aspose.Note for Java.

## Prerequisites

Before we begin, ensure that you have the following:

1. Java Development Kit (JDK) installed on your system.
2. Aspose.Note for Java library. You can download it from [here](https://releases.aspose.com/note/java/).
3. Basic knowledge of Java programming.

## Import Packages

First, import the necessary packages to your Java project:

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
<<<<<<< Updated upstream


public class CreateOneNoteDocandSavetoHtml {

	public static void main(String[] args) throws IOException {
		// TODO Auto-generated method stub

		SaveAsHtmlToMemoryStream();

		SaveAsHtmlWithResourcesInSeparateFiles();

		SaveAsHtmlWithResourcesInSeparateFiles();
	}

	public static void SaveAsHtmlToMemoryStream() throws IOException {
		String dataDir = "Your Document Directory";

		// ExStart: SaveAsHtmlToMemoryStream
		Document document = new Document(dataDir + "Sample1.one");

		HtmlSaveOptions options = new HtmlSaveOptions();
		options.setExportCss(ResourceExportType.ExportEmbedded);
		options.setExportImages(ResourceExportType.ExportEmbedded);
		options.setExportFonts(ResourceExportType.ExportEmbedded);
		options.setFontFaceTypes(FontFaceType.Ttf);

		ByteArrayOutputStream r = new ByteArrayOutputStream();
		document.save(r, options);
		// ExEnd: SaveAsHtmlToMemoryStream
	}

	public static void SaveAsHtmlWithResourcesInSeparateFiles() throws IOException {
		String dataDir = "Your Document Directory";

		// ExStart: SaveAsHtmlWithResourcesInSeparateFiles
		Document document = new Document(dataDir + "Sample1.one");

		HtmlSaveOptions options = new HtmlSaveOptions();
		options.setExportCss(ResourceExportType.ExportEmbedded);
		options.setExportFonts(ResourceExportType.ExportEmbedded);
		options.setExportImages(ResourceExportType.ExportEmbedded);

		document.save(dataDir + "document.html", options);
		// ExEnd: SaveAsHtmlWithResourcesInSeparateFiles
	}

	public static void SaveAsHtmlToMemoryStreamWithCallbacksToSaveResources() throws IOException {
		String dataDir = "Your Document Directory";

		// ExStart: SaveAsHtmlToMemoryStreamWithCallbacksToSaveResources
		Document document = new Document(dataDir + "Sample1.one");

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

		try (OutputStreamWriter writer = new OutputStreamWriter(savingCallbacks.getCssStream(), "utf-8")) {
			writer.write(System.lineSeparator());
			writer.write("/* This line is appended to stream manually by user */");
			writer.close();
		}
		// ExEnd: SaveAsHtmlToMemoryStreamWithCallbacksToSaveResources
	}
}

class UserSavingCallbacks implements ICssSavingCallback, IFontSavingCallback, IImageSavingCallback {
	// ExStart: UserSavingCallbacks
	public final int getCssSaved() {
		return auto_CssSaved;
	}

	private void setCssSaved(int value) {
		auto_CssSaved = value;
	}

	private int auto_CssSaved;

	public final int getFontsSaved() {
		return auto_FontsSaved;
	}

	private void setFontsSaved(int value) {
		auto_FontsSaved = value;
	}

	private int auto_FontsSaved;

	public final int getImagessSaved() {
		return auto_ImagessSaved;
	}

	private void setImagessSaved(int value) {
		auto_ImagessSaved = value;
	}

	private int auto_ImagessSaved;

	public final String getRootFolder() {
		return auto_RootFolder;
	}

	public final void setRootFolder(String value) {
		auto_RootFolder = value;
	}

	private String auto_RootFolder;

	public final boolean getKeepCssStreamOpened() {
		return auto_KeepCssStreamOpened;
	}

	public final void setKeepCssStreamOpened(boolean value) {
		auto_KeepCssStreamOpened = value;
	}

	private boolean auto_KeepCssStreamOpened;

	public final String getCssFolder() {
		return auto_CssFolder;
	}

	public final void setCssFolder(String value) {
		auto_CssFolder = value;
	}

	private String auto_CssFolder;

	public final OutputStream getCssStream() {
		return auto_CssStream;
	}

	private void setCssStream(OutputStream value) {
		auto_CssStream = value;
	}

	private OutputStream auto_CssStream;

	public final String getFontsFolder() {
		return auto_FontsFolder;
	}

	public final void setFontsFolder(String value) {
		auto_FontsFolder = value;
	}

	private String auto_FontsFolder;

	public final String getImagesFolder() {
		return auto_ImagesFolder;
	}

	public final void setImagesFolder(String value) {
		auto_ImagesFolder = value;
	}

	private String auto_ImagesFolder;

	public final void fontSaving(FontSavingArgs args) {
		String uri = null;
		OutputStream stream = null;
		String[] referenceToUri = { uri };
		OutputStream[] referenceToStream = { stream };
		this.createResourceInFolder(this.getFontsFolder(), args.getFileName(), /* out */ referenceToUri,
				/* out */ referenceToStream);
		uri = referenceToUri[0];
		stream = referenceToStream[0];
		args.setStream(stream);
		args.setUri(Paths.get("..", uri).toString().replace("\\", "\\\\"));

		this.setFontsSaved(this.getFontsSaved() + 1);
	}

	public final void cssSaving(CssSavingArgs args) {
		String uri = null;
		OutputStream stream = null;
		String[] referenceToUri = { uri };
		OutputStream[] referenceToStream = { stream };
		this.createResourceInFolder(this.getCssFolder(), args.getFileName(), /* out */ referenceToUri,
				/* out */ referenceToStream);
		uri = referenceToUri[0];
		stream = referenceToStream[0];
		this.setCssStream(stream);
		args.setStream(stream);
		args.setKeepStreamOpen(this.getKeepCssStreamOpened());
		args.setUri(uri);

		this.setCssSaved(this.getCssSaved() + 1);
	}

	public final void imageSaving(ImageSavingArgs args) {
		String uri = null;
		OutputStream stream = null;
		String[] referenceToUri = { uri };
		OutputStream[] referenceToStream = { stream };
		this.createResourceInFolder(this.getImagesFolder(), args.getFileName(), /* out */ referenceToUri,
				/* out */ referenceToStream);
		uri = referenceToUri[0];
		stream = referenceToStream[0];
		args.setStream(stream);
		args.setUri(uri);

		this.setImagessSaved(this.getImagessSaved() + 1);
	}

	private void createResourceInFolder(String folder, String filename, /* out */ String[] uri,
			/* out */ OutputStream[] stream) {
		String relativePath = folder;

		String fullPath = Paths.get(this.getRootFolder(), relativePath).toString();
		File dir = new File(fullPath);
		try {
			if (!dir.exists()) {
				dir.mkdir();
			}

			stream[0] = new FileOutputStream(Paths.get(fullPath, filename).toFile());
		} catch (IOException e) {
			throw new RuntimeException(e);
		}
		uri[0] = Paths.get(relativePath, filename).toString();
	}
	// ExEnd: UserSavingCallbacks
}

=======
import com.aspose.note.examples.Utils;
>>>>>>> Stashed changes
```

## Step 1: Create a OneNote Document Object

```java
Document document = new Document("Path_to_your_sample_one_file");
```

This code initializes a `Document` object by loading a sample OneNote file.

## Step 2: Save as HTML to Memory Stream

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Here, we set up the HTML save options and save the document to a memory stream.

## Step 3: Save as HTML with Resources in Separate Files

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

This step saves the document as HTML with resources like CSS, fonts, and images in separate files.

## Step 4: Save as HTML to Memory Stream with Callbacks to Save Resources

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

Here, we save the document as HTML to a memory stream using callbacks to handle resource saving.

## Conclusion

Congratulations! You have learned how to create a OneNote document and save it to HTML format using Aspose.Note for Java. You can now integrate this functionality into your Java applications to work with OneNote files programmatically.

## FAQ's

### Q1: Can I convert multiple OneNote documents to HTML in one go?

A1: Yes, you can loop through multiple documents and apply the saving process iteratively.

### Q2: Does Aspose.Note for Java support other output formats besides HTML?

A2: Yes, Aspose.Note for Java supports various output formats including PDF, DOCX, and image formats.

### Q3: Is there a trial version available for Aspose.Note for Java?

A3: Yes, you can download a free trial version from [here](https://releases.aspose.com/).

### Q4: Where can I get support for Aspose.Note for Java?

A4: You can get support from the [Aspose.Note forum](https://forum.aspose.com/c/note/28).

### Q5: How can I purchase a license for Aspose.Note for Java?

A5: You can purchase a license from the [Aspose website](https://purchase.aspose.com/buy).
