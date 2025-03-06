---
title: Seitenaufteilung in Aspose.Note
linktitle: Seitenaufteilung in Aspose.Note
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie Seiten in Aspose.Note für .NET mithilfe verschiedener Algorithmen effektiv aufteilen. Sorgen Sie für eine übersichtliche Organisation von OneNote-Dokumenten im PDF-Format.
weight: 17
url: /de/net/loading-and-saving-operations/page-splitting/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Seitenaufteilung in Aspose.Note

## Einführung

In diesem Tutorial erfahren Sie, wie Sie Seiten mit Aspose.Note für .NET effektiv aufteilen. Die Seitenaufteilung ist eine entscheidende Funktion, insbesondere wenn es um lange OneNote-Seiten geht, die in das PDF-Format konvertiert werden müssen. Aspose.Note bietet verschiedene Algorithmen zur Steuerung der Aufteilungslogik und stellt so sicher, dass die resultierenden PDFs gut organisiert und lesbar sind.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Visual Studio: Installieren Sie Visual Studio auf Ihrem System.
2.  Aspose.Note für .NET: Laden Sie die Aspose.Note für .NET-Bibliothek von herunter und installieren Sie sie[Hier](https://releases.aspose.com/note/net/).
3. Grundkenntnisse in C#: Vertrautheit mit der Programmiersprache C# ist hilfreich.

## Namespaces importieren

Importieren wir zunächst die erforderlichen Namespaces in unser C#-Projekt:

```csharp
using System.IO;
using Aspose.Note;
using System;
using Aspose.Note.Saving;
```

## Schritt 1: Laden Sie das Dokument

Laden Sie das OneNote-Dokument mit dem folgenden Codeausschnitt in Aspose.Note:

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";

// Laden Sie das Dokument in Aspose.Note.
Document doc = new Document(dataDir + "Aspose.one");
```

## Schritt 2: Konfigurieren Sie die PDF-Speicheroptionen

 Konfigurieren Sie nun die PDF-Speicheroptionen einschließlich des Seitenaufteilungsalgorithmus. Aspose.Note bietet verschiedene Algorithmen zur Seitenaufteilung. Hier verwenden wir die`KeepPartAndCloneSolidObjectToNextPageAlgorithm` Algorithmus.

```csharp
var pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.PageSplittingAlgorithm = new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100);
// oder
pdfSaveOptions.PageSplittingAlgorithm = new KeepPartAndCloneSolidObjectToNextPageAlgorithm(400);
```

## Schritt 3: Speichern Sie das Dokument

Speichern Sie das geänderte Dokument mit dem angegebenen Seitenaufteilungsalgorithmus:

```csharp
string outputFilePath = dataDir + "PageSplittUsingKeepPartAndCloneSolidObjectToNextPageAlgorithm_out.pdf";
doc.Save(outputFilePath, pdfSaveOptions);
```

## Abschluss

In diesem Tutorial haben wir gelernt, wie man Seiten in Aspose.Note für .NET mithilfe verschiedener Algorithmen effektiv aufteilt. Wenn Sie diese Schritte befolgen, können Sie sicherstellen, dass Ihre langen OneNote-Seiten bei der Konvertierung in das PDF-Format ordentlich organisiert sind.

## FAQs

### F1: Kann ich den Seitenaufteilungsalgorithmus weiter anpassen?

A1: Ja, Aspose.Note bietet die Flexibilität, den Seitenaufteilungsalgorithmus entsprechend Ihren Anforderungen anzupassen.

### F2: Ist Aspose.Note für die Verarbeitung großer OneNote-Dokumente geeignet?

A2: Auf jeden Fall! Aspose.Note wurde entwickelt, um große Dokumente effizient zu verarbeiten und eine optimale Leistung zu gewährleisten.

### F3: Werden andere Ausgabeformate für die Seitenaufteilung unterstützt?

A3: Neben PDF unterstützt Aspose.Note verschiedene Ausgabeformate, darunter Bilder und Microsoft Word-Dokumente.

### F4: Bietet Aspose.Note Unterstützung für die plattformübergreifende Entwicklung?

A4: Aspose.Note zielt in erster Linie auf das .NET-Framework ab, kann jedoch in plattformübergreifenden Szenarien mit Frameworks wie .NET Core verwendet werden.

### F5: Wo kann ich Hilfe bekommen, wenn ich auf Probleme stoße?

 A5: Sie können Hilfe im Aspose.Note-Community-Forum suchen[Hier](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
