---
title: Skapa OneNote-dokument och spara till HTML - Java
linktitle: Skapa OneNote-dokument och spara till HTML - Java
second_title: Aspose.Note Java API
description: Lär dig att skapa och spara OneNote-dokument som HTML med Aspose.Note för Java. Integrera i Java-applikationer för programmatisk OneNote-filhantering.

weight: 18
url: /sv/java/onenote-document-loading/create-onenote-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa OneNote-dokument och spara till HTML - Java

## Introduktion

Aspose.Note för Java är ett kraftfullt bibliotek som låter utvecklare arbeta med Microsoft OneNote-filer programmatiskt. I den här handledningen kommer vi att utforska hur man skapar ett OneNote-dokument och sparar det i HTML-format med Aspose.Note för Java.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. Java Development Kit (JDK) installerat på ditt system.
2.  Aspose.Note för Java-bibliotek. Du kan ladda ner den från[här](https://releases.aspose.com/note/java/).
3. Grundläggande kunskaper i Java-programmering.

## Importera paket

Importera först de nödvändiga paketen till ditt Java-projekt:

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

## Steg 1: Skapa ett OneNote-dokumentobjekt

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Denna kod initierar en`Document` objekt genom att ladda ett exempel på OneNote-fil.

## Steg 2: Spara som HTML till Memory Stream

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Här ställer vi in HTML-sparalternativen och sparar dokumentet i en minnesström.

## Steg 3: Spara som HTML med resurser i separata filer

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Detta steg sparar dokumentet som HTML med resurser som CSS, teckensnitt och bilder i separata filer.

## Steg 4: Spara som HTML till minnesström med återuppringningar för att spara resurser

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

Här sparar vi dokumentet som HTML till en minnesström med hjälp av callbacks för att hantera resursbesparing.

## Slutsats

Grattis! Du har lärt dig hur du skapar ett OneNote-dokument och sparar det i HTML-format med Aspose.Note för Java. Du kan nu integrera den här funktionen i dina Java-applikationer för att arbeta med OneNote-filer programmatiskt.

## FAQ's

### F1: Kan jag konvertera flera OneNote-dokument till HTML på en gång?

S1: Ja, du kan gå igenom flera dokument och tillämpa sparprocessen iterativt.

### F2: Stöder Aspose.Note för Java andra utdataformat förutom HTML?

S2: Ja, Aspose.Note för Java stöder olika utdataformat inklusive PDF, DOCX och bildformat.

### F3: Finns det en testversion tillgänglig för Aspose.Note för Java?

A3: Ja, du kan ladda ner en gratis testversion från[här](https://releases.aspose.com/).

### F4: Var kan jag få support för Aspose.Note för Java?

 A4: Du kan få stöd från[Aspose.Note forum](https://forum.aspose.com/c/note/28).

### F5: Hur kan jag köpa en licens för Aspose.Note för Java?

 S5: Du kan köpa en licens från[Aspose hemsida](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
