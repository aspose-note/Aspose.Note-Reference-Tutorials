---
title: Konvertieren Sie Notizbücher in ein Bild (abgeflacht) in Aspose Note .NET
linktitle: Konvertieren Sie Notizbücher in ein Bild (abgeflacht) in Aspose Note .NET
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie OneNote-Notizbücher mit Aspose.Note für .NET in reduzierte Bilder konvertieren. Schritt-für-Schritt-Anleitung für eine nahtlose Integration.
type: docs
weight: 12
url: /de/net/notebook-operations/convert-to-image-flattened/
---
## Einführung

In diesem Tutorial erfahren Sie, wie Sie mit Aspose.Note für .NET Notizbücher in reduzierte Bilder konvertieren. Wir unterteilen den Prozess in einfache Schritte, damit Sie ihn verstehen und effektiv umsetzen können.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1.  Aspose.Note für .NET: Wenn Sie es noch nicht getan haben, laden Sie Aspose.Note für .NET herunter und installieren Sie es von[Hier](https://releases.aspose.com/note/net/).
2. Entwicklungsumgebung: Stellen Sie sicher, dass Sie eine geeignete Entwicklungsumgebung für die .NET-Entwicklung eingerichtet haben.
3. OneNote-Notizbuch: Bereiten Sie das OneNote-Notizbuch vor, das Sie in ein Bild konvertieren möchten.

## Namespaces importieren

Bevor Sie mit dem Konvertierungsprozess beginnen, müssen Sie die erforderlichen Namespaces in Ihren Code importieren:

```csharp
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Lassen Sie uns nun in die Schritt-für-Schritt-Anleitung zum Konvertieren von Notizbüchern in reduzierte Bilder mit Aspose.Note für .NET eintauchen.

## Schritt 1: Laden Sie das Notebook

Laden Sie zunächst das OneNote-Notizbuch, das Sie in Ihre Anwendung konvertieren möchten.

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";

// Laden Sie ein OneNote-Notizbuch
var notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## Schritt 2: Speicheroptionen festlegen

Definieren Sie die Speicheroptionen für das Notizbuch, einschließlich Bildformat und Auflösung.

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
notebookSaveOptions.Flatten = true;
```

## Schritt 3: Speichern Sie das Notizbuch als Bild

Speichern Sie nun das Notizbuch mit den definierten Speicheroptionen als reduziertes Bild.

```csharp
dataDir = dataDir + "ConvertToImageAsFlattenedNotebook_out.png";

// Speichern Sie das Notizbuch
notebook.Save(dataDir, notebookSaveOptions);
```

## Abschluss

In diesem Tutorial haben wir gelernt, wie man Notizbücher mit Aspose.Note für .NET in reduzierte Bilder konvertiert. Wenn Sie der Schritt-für-Schritt-Anleitung folgen, können Sie diese Funktionalität nahtlos in Ihre .NET-Anwendungen integrieren.

## FAQs

### F1: Kann Aspose.Note für .NET komplexe Notizbücher verarbeiten?

A1: Ja, Aspose.Note für .NET ist in der Lage, komplexe Notizbücher effizient zu verarbeiten.

### F2: Gibt es eine kostenlose Testversion für Aspose.Note für .NET?

 A2: Ja, Sie können eine kostenlose Testversion herunterladen[Hier](https://releases.aspose.com/).

### F3: Bietet Aspose Support für seine Produkte?

 A3: Ja, Sie können Unterstützung von der Aspose-Community erhalten[Hier](https://forum.aspose.com/c/note/28).

### F4: Kann ich eine temporäre Lizenz für Aspose.Note für .NET erwerben?

 A4: Ja, Sie können eine temporäre Lizenz erwerben[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Wo finde ich Dokumentation für Aspose.Note für .NET?

 A5: Sie finden die Dokumentation[Hier](https://reference.aspose.com/note/net/).