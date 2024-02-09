---
title: Importieren Sie PDF-Dokumente in Aspose.Note
linktitle: Importieren Sie PDF-Dokumente in Aspose.Note
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie PDF-Dokumente mühelos in Aspose.Note für .NET importieren und dabei verschiedene Zusammenführungsoptionen für eine nahtlose Integration nutzen.
type: docs
weight: 10
url: /de/net/import/import-pdf-documents/
---
## Einführung

Angesichts der großen Menge an digitalen Inhalten, die heute verfügbar sind, ist die nahtlose Integration von PDF-Dokumenten in Ihre Projekte von entscheidender Bedeutung. Aspose.Note für .NET bietet leistungsstarke Funktionen zum effizienten Import von PDF-Dokumenten. In diesem Tutorial erfahren Sie Schritt für Schritt, wie Sie PDF-Dokumente mit Aspose.Note für .NET importieren.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1.  Aspose.Note für .NET: Laden Sie die Bibliothek herunter und installieren Sie sie[Hier](https://releases.aspose.com/note/net/).
2. Grundkenntnisse in C# und .NET Framework: Kenntnisse der Programmiersprache C# und .NET Framework sind von Vorteil.

## Namespaces importieren

Stellen Sie sicher, dass Sie die erforderlichen Namespaces importieren, um auf die für die PDF-Importfunktion erforderlichen Klassen und Methoden zuzugreifen:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;

using Aspose.Note.Importing;

```

## Schritt 1: PDF-Dokumente mit Simple Merge importieren

Der Simple Merge-Ansatz ermöglicht das seitenweise Importieren aller Seiten aus mehreren PDF-Dokumenten:

```csharp
public static void ImportSetOfFiles_SimpleMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    d.Import(Path.Combine(dataDir, "sampleText.pdf"))
     .Import(Path.Combine(dataDir, "sampleImage.pdf"))
     .Import(Path.Combine(dataDir, "sampleTable.pdf"));

    d.Save(Path.Combine(dataDir, "sample_SimpleMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## Schritt 2: Importieren Sie PDF-Dokumente mithilfe der strukturierten Zusammenführung

Structured Merge importiert alle Seiten aus PDF-Dokumenten und fügt gleichzeitig Seiten aus jedem Dokument als untergeordnete Elemente einer OneNote-Seite der obersten Ebene ein:

```csharp
public static void ImportSetOfFiles_StructuredMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    foreach (var file in new[] { "sampleText.pdf", "sampleImage.pdf", "sampleTable.pdf" })
    {
        d.AppendChildLast(new Page()).Title = new Title() { TitleText = new RichText() { ParagraphStyle = ParagraphStyle.Default }.Append(file) };
        d.Import(Path.Combine(dataDir, file), new PdfImportOptions(), new MergeOptions() { InsertAt = int.MaxValue, InsertAsChild = true });
    }

    d.Save(Path.Combine(dataDir, "sample_StructuredMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## Schritt 3: Importieren Sie PDF-Dokumente mithilfe der Einzelseitenzusammenführung

Single Page Merge führt Inhalte aus mehreren PDF-Dokumenten auf einer einzigen OneNote-Seite zusammen:

```csharp
public static void ImportSetOfFiles_SinglePageMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    var importOptions = new PdfImportOptions();
    var mergeOptions = new MergeOptions() { ImportAsSinglePage = true, PageSpacing = 100 };

    d.Import(Path.Combine(dataDir, "sampleText.pdf"), importOptions, mergeOptions)
     .Import(Path.Combine(dataDir, "sampleImage.pdf"), importOptions, mergeOptions)
     .Import(Path.Combine(dataDir, "sampleTable.pdf"), importOptions, mergeOptions);

    d.Save(Path.Combine(dataDir, "sample_SinglePageMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## Schritt 4: Importieren Sie PDF-Dokumente mit der benutzerdefinierten Zusammenführung

Mit der benutzerdefinierten Zusammenführung können Seiten aus PDF-Dokumenten anhand benutzerdefinierter Kriterien in einzelne OneNote-Seiten gruppiert werden:

```csharp
public static void ImportSetOfFiles_CustomMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    var mergeOptions = new MergeOptions() { ImportAsSinglePage = true, PageSpacing = 100 };

    IEnumerable<Page> pages = PdfImporter.Import(Path.Combine(dataDir, "SampleGrouping.pdf"));
    while (pages.Any())
    {
        d.Merge(pages.Take(5), mergeOptions);
        pages = pages.Skip(5);
    }

    d.Save(Path.Combine(dataDir, "sample_CustomMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## Abschluss

Die Integration von PDF-Dokumenten in Ihre .NET-Anwendungen mit Aspose.Note ist ein unkomplizierter Prozess und bietet verschiedene Zusammenführungsoptionen, die auf die Anforderungen Ihres Projekts zugeschnitten sind. Unabhängig davon, ob Sie mehrere Seiten importieren oder Inhalte hierarchisch organisieren müssen, bietet Aspose.Note die notwendigen Tools für eine nahtlose Integration.

## FAQs

### F1: Kann ich verschlüsselte PDF-Dokumente importieren?

A1: Ja, Aspose.Note unterstützt den Import verschlüsselter PDF-Dokumente. Stellen Sie sicher, dass Sie die erforderlichen Anmeldeinformationen für die Entschlüsselung angeben.

### F2: Gibt es Einschränkungen hinsichtlich der PDF-Dateigröße für den Import?

A2: Aspose.Note hat keine inhärenten Beschränkungen hinsichtlich der PDF-Dateigröße für den Import. Berücksichtigen Sie jedoch die Auswirkungen auf Systemressourcen und Leistung bei großen PDF-Dateien.

### F3: Kann ich das Erscheinungsbild importierter PDF-Inhalte anpassen?

A3: Ja, Sie können das Erscheinungsbild importierter PDF-Inhalte mithilfe verschiedener von Aspose.Note bereitgestellter Optionen anpassen, z. B. Schriftarten, Farben und Layoutanpassungen.

### F4: Ist Aspose.Note mit .NET Core kompatibel?

A4: Ja, Aspose.Note ist mit .NET Core kompatibel, sodass Sie PDF-Importfunktionen in plattformübergreifende Anwendungen integrieren können.

### F5: Wo finde ich zusätzliche Unterstützung oder Ressourcen?

 A5: Weitere Unterstützung, Dokumentation oder Community-Unterstützung finden Sie unter[Aspose.Note-Forum](https://forum.aspose.com/c/note/28).