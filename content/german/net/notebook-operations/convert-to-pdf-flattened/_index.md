---
title: Konvertieren Sie Notizbücher in Aspose Note .NET in PDF (komprimiert).
linktitle: Konvertieren Sie Notizbücher in Aspose Note .NET in PDF (komprimiert).
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie OneNote-Notizbücher mit Aspose.Note für .NET mühelos in vereinfachte PDFs konvertieren. Bewahren Sie Ihre Inhalte nahtlos auf.
type: docs
weight: 15
url: /de/net/notebook-operations/convert-to-pdf-flattened/
---
## Einführung

Möchten Sie Ihre OneNote-Notizbücher mit Aspose Note .NET in reduzierte PDFs konvertieren? Hier sind Sie richtig! In diesem Tutorial gehen wir den Prozess Schritt für Schritt durch.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1.  Aspose.Note für .NET: Stellen Sie sicher, dass Sie Aspose.Note für .NET heruntergeladen und installiert haben. Wenn nicht, können Sie es hier erhalten[Hier](https://releases.aspose.com/note/net/).
2. Visual Studio: Zum Codieren und Kompilieren muss Visual Studio auf Ihrem System installiert sein.
3. OneNote-Notizbuch: Halten Sie ein OneNote-Notizbuch bereit, das Sie in ein PDF konvertieren möchten.

## Namespaces importieren

Beginnen wir mit dem Importieren der erforderlichen Namespaces in Ihren C#-Code:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## Schritt 1: Laden Sie das OneNote-Notizbuch

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";

// Laden Sie ein OneNote-Notizbuch
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

 In diesem Schritt laden wir das OneNote-Notizbuch mit`Notebook` Klasse, bereitgestellt von Aspose.Note.

## Schritt 2: Konvertieren in PDF mit Reduzierung

```csharp
// Speichern Sie das Notizbuch als PDF mit Reduzierung
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

 Hier speichern wir das geladene Notizbuch als PDF mit dem`Flatten` Eigenschaft festgelegt auf`true`. Diese Eigenschaft reduziert den gesamten Inhalt, einschließlich Anmerkungen und Bilder, in der PDF-Datei.

## Schritt 3: Erfolgsmeldung drucken

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

Abschließend drucken wir eine Erfolgsmeldung zusammen mit dem Pfad, in dem die PDF-Datei gespeichert ist.

## Abschluss

Glückwunsch! Sie haben Ihr OneNote-Notizbuch mit Aspose.Note für .NET erfolgreich in eine reduzierte PDF-Datei konvertiert. Dieser Prozess stellt sicher, dass alle Ihre Inhalte genau im PDF-Format gespeichert werden, was die Weitergabe und Verteilung erleichtert.

## FAQs

### F1: Kann ich interaktive Elemente im PDF beibehalten?

A1: Aspose.Note glättet den Inhalt, einschließlich interaktiver Elemente wie Kontrollkästchen oder Formularfelder, im PDF und macht ihn statisch.

### F2: Unterstützt Aspose.Note die Konvertierung von Notizbüchern in andere Formate?

A2: Ja, Aspose.Note unterstützt die Konvertierung von Notizbüchern in verschiedene Formate wie PDF, HTML, Bild und mehr.

### F3: Kann ich die Konvertierungsoptionen anpassen?

A3: Auf jeden Fall! Aspose.Note bietet umfangreiche Anpassungsmöglichkeiten während des Konvertierungsprozesses, sodass Sie die Ausgabe entsprechend Ihren Anforderungen anpassen können.

### F4: Gibt es eine Testversion?

 A4: Ja, Sie können eine kostenlose Testversion von Aspose.Note erhalten von[Hier](https://releases.aspose.com/).

### F5: Wo kann ich Unterstützung erhalten, wenn ich auf Probleme stoße?

 A5: Sie können Unterstützung von der Aspose-Community unter erhalten[Aspose.Note-Foren](https://forum.aspose.com/c/note/28).