---
title: Erstellen Sie ein OneNote-Dokument und speichern Sie es in Aspose.Note im HTML-Format
linktitle: Erstellen Sie ein OneNote-Dokument und speichern Sie es in Aspose.Note im HTML-Format
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie mithilfe der Aspose.Note-API Microsoft OneNote-Dokumente in .NET-Anwendungen erstellen und im HTML-Format speichern. Folgen Sie unserem umfassenden Tutorial mit Schritt-für-Schritt-Beispielen.
type: docs
weight: 14
url: /de/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## Einführung

Aspose.Note für .NET ist eine leistungsstarke API, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dokumenten in ihren .NET-Anwendungen zu arbeiten. Mit Aspose.Note können Sie OneNote-Dateien mühelos erstellen, bearbeiten und konvertieren. In diesem Tutorial erfahren Sie, wie Sie ein OneNote-Dokument erstellen und es mithilfe verschiedener Optionen der Aspose.Note für .NET-API im HTML-Format speichern.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

- Grundkenntnisse der Programmiersprache C#.
- Visual Studio ist auf Ihrem System installiert.
-  Aspose.Note für .NET API in Ihrem Projekt installiert. Sie können es herunterladen unter[Hier](https://releases.aspose.com/note/net/).
- Vertrautheit mit der Struktur von Microsoft OneNote-Dokumenten.

## Namespaces importieren

Bevor wir in den Codierungsteil eintauchen, importieren wir die erforderlichen Namespaces:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Lassen Sie uns nun jedes Beispiel in mehrere Schritte aufteilen und sehen, wie Sie mit Aspose.Note für .NET ein OneNote-Dokument erstellen und es im HTML-Format speichern.

## Schritt 1: Erstellen Sie ein OneNote-Dokument mit Standardoptionen

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // OneNote-Dokument initialisieren
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Standardstil für den gesamten Text im Dokument.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Im HTML-Format speichern
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

In diesem Schritt initialisieren wir ein neues OneNote-Dokument, fügen eine Seite mit einem Titel hinzu und speichern es mit Standardoptionen im HTML-Format.

## Schritt 2: Erstellen und speichern Sie einen bestimmten Seitenbereich im HTML-Format

```csharp
public static void CreateAndSavePageRange()
{
    // OneNote-Dokument initialisieren
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Standardstil für den gesamten Text im Dokument.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Im HTML-Format speichern
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Hier zeigen wir, wie Sie ein Dokument erstellen und einen bestimmten Seitenbereich im HTML-Format speichern.

## Schritt 3: Als HTML im Memory Stream mit eingebetteten Ressourcen speichern

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Laden Sie das OneNote-Dokument
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Geben Sie HTML-Speicheroptionen an
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Speichern Sie das Dokument in einem Speicherstream
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Dieser Schritt veranschaulicht, wie Sie ein OneNote-Dokument im HTML-Format mit eingebetteten Ressourcen (CSS, Schriftarten und Bilder) in einem Speicherstream speichern.

## Schritt 4: Als HTML in einer Datei mit Ressourcen in separaten Dateien speichern

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Laden Sie das OneNote-Dokument
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Geben Sie HTML-Speicheroptionen an
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //Speichern Sie das Dokument in einer HTML-Datei, wobei die Ressourcen in separaten Dateien gespeichert werden
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

In diesem Schritt speichern wir ein OneNote-Dokument im HTML-Format, wobei alle Ressourcen (CSS, Schriftarten und Bilder) in separaten Dateien gespeichert werden.

## Schritt 5: Als HTML im Memory Stream mit Rückrufen speichern, um Ressourcen zu sparen

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Geben Sie die Konfiguration zum Speichern von Rückrufen an
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Geben Sie HTML-Speicheroptionen an
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Laden Sie das OneNote-Dokument
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Speichern Sie das Dokument im HTML-Format mit Ressourcen, die durch benutzerdefinierte Rückrufe verwaltet werden
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Hängen Sie Daten manuell an den CSS-Stream an
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Hier zeigen wir, wie man ein OneNote-Dokument im HTML-Format speichert, wobei die Ressourcen durch benutzerdefinierte Rückrufe verwaltet werden.

## Abschluss

In diesem Artikel haben wir untersucht, wie Sie mit OneNote-Dokumenten arbeiten und diese mithilfe von Aspose.Note für .NET im HTML-Format speichern. Wenn Sie der Schritt-für-Schritt-Anleitung folgen, können Sie dies ganz einfach tun

 Integrieren Sie diese Funktionalität in Ihre .NET-Anwendungen, sodass Sie OneNote-Dateien effizient bearbeiten können.

## FAQs

### F1: Kann ich das Erscheinungsbild der gespeicherten HTML-Datei anpassen?

A1: Ja, Sie können das Erscheinungsbild anpassen, indem Sie die während des Konvertierungsprozesses generierten CSS-Stylesheets ändern.

### F2: Unterstützt Aspose.Note die Konvertierung in andere Formate außer HTML?

A2: Ja, Aspose.Note unterstützt die Konvertierung in verschiedene Formate wie PDF, Bilder und Microsoft Word-Dokumente.

### F3: Ist Aspose.Note mit .NET Core-Anwendungen kompatibel?

A3: Ja, Aspose.Note ist sowohl mit .NET Framework- als auch mit .NET Core-Anwendungen kompatibel.

### F4: Kann ich mit Aspose.Note Text und Bilder aus OneNote-Dokumenten extrahieren?

A4: Ja, Sie können mit der Aspose.Note-API Text und Bilder extrahieren sowie verschiedene andere Manipulationen durchführen.

### F5: Gibt es eine Testversion zum Testen der Aspose.Note-Funktionen?

 A5: Ja, Sie können eine kostenlose Testversion herunterladen von[Hier](https://releases.aspose.com/).