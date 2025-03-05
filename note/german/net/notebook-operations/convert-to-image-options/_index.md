---
title: Konvertieren Sie Notizbücher mit Optionen in Aspose Note .NET in ein Bild
linktitle: Konvertieren Sie Notizbücher mit Optionen in Aspose Note .NET in ein Bild
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie mit Aspose.Note für .NET Notizbücher mit anpassbaren Optionen in Bilder konvertieren.
type: docs
weight: 13
url: /de/net/notebook-operations/convert-to-image-options/
---
## Einführung

In diesem Tutorial befassen wir uns mit der Konvertierung von Notizbüchern in Bilder mit verschiedenen Optionen mithilfe der Aspose.Note für .NET-Bibliothek. Aspose.Note ist eine leistungsstarke .NET-API, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten. Indem Sie die in dieser Anleitung beschriebenen Schritte befolgen, erfahren Sie, wie Sie Notizbücher mühelos in Bilder umwandeln und gleichzeitig die Ausgabe entsprechend Ihren Anforderungen anpassen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Grundkenntnisse in C#: Um die bereitgestellten Codefragmente zu verstehen und umzusetzen, sind Kenntnisse der Programmiersprache C# unerlässlich.

2.  Aspose.Note für .NET: Laden Sie Aspose.Note für .NET von herunter und installieren Sie es[Webseite](https://releases.aspose.com/note/net/). Sie können je nach Bedarf eine kostenlose Testversion erhalten oder eine Lizenz erwerben.

3. Entwicklungsumgebung: Richten Sie Ihre bevorzugte Entwicklungsumgebung mit Visual Studio oder einer anderen IDE ein, die die .NET-Entwicklung unterstützt.

## Namespaces importieren

Importieren wir zunächst die erforderlichen Namespaces für die Arbeit mit Aspose.Note für .NET.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

Lassen Sie uns nun den Prozess der Konvertierung von Notizbüchern in Bilder mit Optionen in mehrere Schritte unterteilen.

## Schritt 1: Laden Sie das Notebook

Laden Sie zunächst die Notebook-Datei, die Sie in ein Bild konvertieren möchten.

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";

// Laden Sie ein OneNote-Notizbuch
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Schritt 2: Legen Sie die Optionen zum Speichern von Bildern fest

Geben Sie die Optionen zum Speichern des Notizbuchs als Bild an. Hier stellen wir das Bildformat auf PNG ein und passen die Auflösung an.

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
```

## Schritt 3: Speichern Sie das Notizbuch als Bild

Speichern Sie das Notizbuch mit den angegebenen Optionen als Bild.

```csharp
dataDir = dataDir + "ConvertToImageWithOptions_out.png";

// Speichern Sie das Notizbuch
notebook.Save(dataDir, notebookSaveOptions);
```

## Abschluss

Abschließend haben wir untersucht, wie Sie mit Aspose.Note für .NET Notizbücher mit verschiedenen Optionen in Bilder konvertieren können. Wenn Sie die in diesem Tutorial beschriebenen Schritte befolgen, können Sie diese Funktionalität nahtlos in Ihre .NET-Anwendungen integrieren und so eine effiziente Bearbeitung von Microsoft OneNote-Dateien ermöglichen.

## FAQs

### F1: Kann ich mit Aspose.Note für .NET mehrere Notizbücher gleichzeitig konvertieren?

A1: Ja, Sie können mehrere Notebook-Dateien durchlaufen und sie mit ähnlichen Methoden, die in diesem Tutorial gezeigt werden, in Bilder konvertieren.

### F2: Ist Aspose.Note für .NET mit .NET Core kompatibel?

A2: Ja, Aspose.Note für .NET ist sowohl mit .NET Framework- als auch mit .NET Core-Umgebungen kompatibel.

### F3: Gibt es Einschränkungen hinsichtlich der Größe von Notizbüchern, die in Bilder konvertiert werden können?

A3: Aspose.Note für .NET legt keine besonderen Beschränkungen für die Größe der konvertierbaren Notebooks fest, die Leistung kann jedoch je nach Größe und Komplexität des Notebooks variieren.

### F4: Kann ich die Bildausgabe über die Auflösungseinstellungen hinaus noch weiter anpassen?

A4: Ja, Aspose.Note für .NET bietet verschiedene Optionen zum Anpassen der Bildausgabe, wie zum Beispiel das Anpassen von Rändern, Farben und Komprimierungsstufen.

### F5: Unterstützt Aspose.Note für .NET neben PNG auch andere Bildformate?

A5: Ja, Aspose.Note für .NET unterstützt mehrere Bildformate, darunter JPEG, BMP, GIF und TIFF.