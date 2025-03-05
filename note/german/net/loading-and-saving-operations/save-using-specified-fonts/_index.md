---
title: Speichern Sie mit angegebenen Schriftarten in Aspose.Note
linktitle: Speichern Sie mit angegebenen Schriftarten in Aspose.Note
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie Dokumente mit bestimmten Schriftarten in Aspose.Note für .NET speichern. Passen Sie die Schriftarteinstellungen einfach an, um eine konsistente Dokumentformatierung zu gewährleisten.
type: docs
weight: 28
url: /de/net/loading-and-saving-operations/save-using-specified-fonts/
---
## Einführung

In diesem Tutorial erfahren Sie, wie Sie Dokumente mit bestimmten Schriftarten in Aspose.Note für .NET speichern. Wir werden Schritt für Schritt verschiedene Methoden erkunden, um dies zu erreichen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1.  Aspose.Note für .NET: Stellen Sie sicher, dass Sie Aspose.Note für .NET installiert haben. Sie können es herunterladen unter[Hier](https://releases.aspose.com/note/net/).

2. Entwicklungsumgebung: Sie benötigen eine für die .NET-Entwicklung eingerichtete Entwicklungsumgebung.

## Namespaces importieren

Importieren wir zunächst die notwendigen Namespaces:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Schritt 1: Speichern mit dem Standardschriftnamen

In diesem Schritt speichern wir ein Dokument unter einem angegebenen Standardschriftnamen.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // Der Pfad zum Dokumentenverzeichnis.
    string dataDir = "Your Document Directory";

    // Laden Sie das Dokument in Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Speichern Sie das Dokument als PDF mit der angegebenen Standardschriftart.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Schritt 2: Speichern mit der Standardschriftart aus der Datei

Als Nächstes speichern wir ein Dokument mit einer aus einer Datei geladenen Standardschriftart.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // Der Pfad zum Dokumentenverzeichnis.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Laden Sie das Dokument in Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Speichern Sie das Dokument als PDF mit der aus der Datei geladenen Standardschriftart.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Schritt 3: Speichern mit der Standardschriftart aus Stream

Zum Schluss speichern wir ein Dokument mit einer aus einem Stream geladenen Standardschriftart.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // Der Pfad zum Dokumentenverzeichnis.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Laden Sie das Dokument in Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Speichern Sie das Dokument als PDF mit der aus dem Stream geladenen Standardschriftart.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Abschluss

In diesem Tutorial haben wir untersucht, wie Sie Dokumente mit bestimmten Schriftarten in Aspose.Note für .NET speichern. Wenn Sie diese Schritte befolgen, können Sie die Schriftarteinstellungen entsprechend Ihren Anforderungen anpassen und so sicherstellen, dass Ihre Dokumente wie gewünscht formatiert sind.

## FAQs

### F1: Kann ich jede Schriftart zum Speichern von Dokumenten in Aspose.Note verwenden?

A1: Ja, Sie können eine beliebige Schriftart zum Speichern von Dokumenten angeben. Stellen Sie einfach sicher, dass auf die Schriftartdatei zugegriffen werden kann und sie korrekt geladen wird.

### F2: Ist Aspose.Note mit verschiedenen Dokumentformaten kompatibel?

A2: Aspose.Note funktioniert hauptsächlich mit OneNote-Dokumenten, bietet jedoch Optionen zum Speichern in verschiedenen Formaten, einschließlich PDF.

### F3: Wie kann ich beim Speichern von Dokumenten mit fehlenden Schriftarten umgehen?

A3: Aspose.Note bietet Optionen zur Verwendung von Standardschriftarten für den Fall, dass die angegebene Schriftart fehlt, um eine konsistente Dokumentformatierung sicherzustellen.

### F4: Unterstützt Aspose.Note die Einbettung von Schriftarten in Ausgabedokumenten?

A4: Ja, Aspose.Note ermöglicht das Einbetten von Schriftarten, um die Portabilität von Dokumenten und eine konsistente Darstellung auf verschiedenen Plattformen sicherzustellen.

### F5: Wo kann ich weitere Unterstützung zu Aspose.Note erhalten?

 A5: Für weitere Hilfe oder technischen Support können Sie die besuchen[Aspose.Note-Forum](https://forum.aspose.com/c/note/28).