---
title: Konvertieren Sie Notizbücher mit Optionen in Aspose Note .NET in PDF
linktitle: Konvertieren Sie Notizbücher mit Optionen in Aspose Note .NET in PDF
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie Microsoft OneNote-Notizbücher mithilfe der Aspose.Note für .NET-Bibliothek mit anpassbaren Optionen in das PDF-Format konvertieren.
weight: 16
url: /de/net/notebook-operations/convert-to-pdf-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertieren Sie Notizbücher mit Optionen in Aspose Note .NET in PDF

## Einführung

In diesem Tutorial werden wir den Prozess der Konvertierung von Notizbüchern in das PDF-Format mithilfe der Aspose.Note für .NET-Bibliothek durchgehen. Aspose.Note für .NET bietet leistungsstarke Funktionen für die programmgesteuerte Arbeit mit Microsoft OneNote-Dateien.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

### 1. Aspose.Note für .NET-Bibliothek
 Stellen Sie sicher, dass Sie die Aspose.Note für .NET-Bibliothek heruntergeladen und installiert haben. Sie können es hier herunterladen[Webseite](https://releases.aspose.com/note/net/).

### 2. Entwicklungsumgebung
Sie sollten eine Entwicklungsumgebung wie Visual Studio eingerichtet haben, in der das erforderliche .NET-Framework installiert ist.

## Namespaces importieren

Bevor wir Aspose.Note für .NET in unserem Projekt verwenden, importieren wir die erforderlichen Namespaces:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

Lassen Sie uns nun den Prozess der Konvertierung von Notizbüchern in PDF mit Optionen in mehrere Schritte unterteilen:

## Schritt 1: Laden Sie das Notebook

Zuerst müssen wir das OneNote-Notizbuch laden, das wir in eine PDF-Datei konvertieren möchten.

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";

// Laden Sie ein OneNote-Notizbuch
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Schritt 2: Legen Sie die PDF-Speicheroptionen fest

Als Nächstes legen wir die Optionen zum Speichern des Notizbuchs als PDF-Datei fest. Wir können verschiedene Einstellungen wie Seitenaufteilungsalgorithmus, Ränder und Seitengröße anpassen.

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## Schritt 3: Speichern Sie das Notizbuch als PDF

Jetzt speichern wir das Notizbuch mit den angegebenen Optionen als PDF-Datei.

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

// Speichern Sie das Notizbuch
notebook.Save(dataDir, notebookSaveOptions);
```

## Schritt 4: Konvertierung überprüfen

Überprüfen Sie abschließend, ob die Konvertierung erfolgreich war, und drucken Sie den Speicherort der PDF-Datei aus.

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## Abschluss

In diesem Tutorial haben wir gelernt, wie man OneNote-Notizbücher mithilfe der Aspose.Note für .NET-Bibliothek in das PDF-Format konvertiert. Wenn Sie die oben beschriebenen Schritte befolgen, können Sie diese Funktionalität problemlos in Ihre .NET-Anwendungen integrieren.

## FAQs

### F1: Ist Aspose.Note für .NET mit allen Versionen von Microsoft OneNote kompatibel?

A1: Ja, Aspose.Note für .NET unterstützt verschiedene Versionen von Microsoft OneNote, einschließlich der Formate .one und .onetoc2.

### F2: Kann ich das Erscheinungsbild der PDF-Ausgabe anpassen?

A2: Ja, Sie können verschiedene Optionen wie Seitengröße, Ränder und Seitenaufteilungsalgorithmus angeben, um das Erscheinungsbild der PDF-Ausgabe anzupassen.

### F3: Bietet Aspose.Note für .NET Unterstützung für andere Dateiformate?

A3: Ja, Aspose.Note für .NET unterstützt die Konvertierung in verschiedene andere Formate wie Bilder, HTML und Microsoft Word-Dokumente.

### F4: Gibt es eine kostenlose Testversion für Aspose.Note für .NET?

A4: Ja, Sie können eine kostenlose Testversion von Aspose.Note für .NET von der Website herunterladen, um die Funktionen zu testen, bevor Sie einen Kauf tätigen.

### F5: Wie erhalte ich technischen Support für Aspose.Note für .NET?

 A5: Sie können technischen Support für Aspose.Note für .NET erhalten, indem Sie die besuchen[Aspose.Note-Forum](https://forum.aspose.com/c/note/28) oder wenden Sie sich direkt an das Aspose-Supportteam.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
