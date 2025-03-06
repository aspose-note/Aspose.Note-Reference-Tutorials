---
title: Erstellen Sie ein OneNote-Dokument und speichern Sie es in HTML – Java
linktitle: Erstellen Sie ein OneNote-Dokument und speichern Sie es in HTML – Java
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Aspose.Note für Java OneNote-Dokumente als HTML erstellen und speichern. Integrieren Sie in Java-Anwendungen für die programmatische OneNote-Dateiverarbeitung.

weight: 18
url: /de/java/onenote-document-loading/create-onenote-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Erstellen Sie ein OneNote-Dokument und speichern Sie es in HTML – Java

## Einführung

Aspose.Note für Java ist eine leistungsstarke Bibliothek, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten. In diesem Tutorial erfahren Sie, wie Sie mit Aspose.Note für Java ein OneNote-Dokument erstellen und es im HTML-Format speichern.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1. Java Development Kit (JDK) auf Ihrem System installiert.
2.  Aspose.Note für Java-Bibliothek. Sie können es herunterladen unter[Hier](https://releases.aspose.com/note/java/).
3. Grundkenntnisse der Java-Programmierung.

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt:

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

## Schritt 1: Erstellen Sie ein OneNote-Dokumentobjekt

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Dieser Code initialisiert a`Document` Objekt durch Laden einer OneNote-Beispieldatei.

## Schritt 2: Als HTML im Memory Stream speichern

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Hier richten wir die HTML-Speicheroptionen ein und speichern das Dokument in einem Speicherstream.

## Schritt 3: Als HTML mit Ressourcen in separaten Dateien speichern

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Dieser Schritt speichert das Dokument als HTML mit Ressourcen wie CSS, Schriftarten und Bildern in separaten Dateien.

## Schritt 4: Speichern Sie als HTML im Memory Stream mit Rückrufen, um Ressourcen zu sparen

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

Hier speichern wir das Dokument als HTML in einem Speicherstream und verwenden Rückrufe, um Ressourcen zu sparen.

## Abschluss

Glückwunsch! Sie haben gelernt, wie Sie mit Aspose.Note für Java ein OneNote-Dokument erstellen und es im HTML-Format speichern. Sie können diese Funktionalität jetzt in Ihre Java-Anwendungen integrieren, um programmgesteuert mit OneNote-Dateien zu arbeiten.

## FAQs

### F1: Kann ich mehrere OneNote-Dokumente auf einmal in HTML konvertieren?

A1: Ja, Sie können mehrere Dokumente durchlaufen und den Speichervorgang iterativ anwenden.

### F2: Unterstützt Aspose.Note für Java neben HTML auch andere Ausgabeformate?

A2: Ja, Aspose.Note für Java unterstützt verschiedene Ausgabeformate, darunter PDF, DOCX und Bildformate.

### F3: Gibt es eine Testversion für Aspose.Note für Java?

A3: Ja, Sie können eine kostenlose Testversion herunterladen von[Hier](https://releases.aspose.com/).

### F4: Wo erhalte ich Unterstützung für Aspose.Note für Java?

 A4: Sie können Unterstützung von erhalten[Aspose.Note-Forum](https://forum.aspose.com/c/note/28).

### F5: Wie kann ich eine Lizenz für Aspose.Note für Java erwerben?

 A5: Sie können eine Lizenz bei erwerben[Aspose-Website](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
