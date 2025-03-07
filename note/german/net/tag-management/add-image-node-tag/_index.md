---
title: Bildknoten mit Tag in Aspose.Note hinzufügen
linktitle: Bildknoten mit Tag in Aspose.Note hinzufügen
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie Ihre OneNote-Dokumente verbessern, indem Sie mit Aspose.Note für .NET Bilder mit benutzerdefinierten Tags hinzufügen.
weight: 10
url: /de/net/tag-management/add-image-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bildknoten mit Tag in Aspose.Note hinzufügen

## Einführung

In diesem Tutorial erfahren Sie, wie Sie mithilfe von Aspose.Note für .NET einen Bildknoten mit einem Tag hinzufügen. Mit dieser Funktion können Sie Ihre OneNote-Dokumente verbessern, indem Sie Bilder mit benutzerdefinierten Tags hinzufügen.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1. Visual Studio: Installieren Sie die Visual Studio-IDE auf Ihrem System.
2.  Aspose.Note für .NET: Laden Sie die Aspose.Note für .NET-Bibliothek von herunter und installieren Sie sie[Download-Link](https://releases.aspose.com/note/net/).
3. Grundkenntnisse: Machen Sie sich mit der Programmiersprache C# und dem .NET Framework vertraut.

## Namespaces importieren

Stellen Sie zunächst sicher, dass Sie die erforderlichen Namespaces in Ihren C#-Code aufnehmen:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Schritt 1: Dokument- und Seitenobjekte initialisieren

 Beginnen Sie mit der Erstellung einer Instanz von`Document` Klasse und a`Page` Objekt:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Schritt 2: Outline- und OutlineElement-Objekte initialisieren

 Als nächstes initialisieren`Outline` Und`OutlineElement` Objekte:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## Schritt 3: Bild laden und einfügen

Laden Sie das gewünschte Bild und fügen Sie es in den Dokumentknoten ein:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## Schritt 4: Tag zum Bild hinzufügen

Fügen Sie dem Bild ein benutzerdefiniertes Tag hinzu:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## Schritt 5: Gliederungselement und Seitenknoten anhängen

Hängen Sie das Gliederungselement und die Gliederungsknoten an die Seite an:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## Schritt 6: Speichern Sie das Dokument

Speichern Sie das geänderte OneNote-Dokument:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## Abschluss

Wenn Sie diese Schritte befolgen, können Sie mit Aspose.Note für .NET nahtlos einen Bildknoten mit einem benutzerdefinierten Tag hinzufügen und so Ihre OneNote-Dokumente mit personalisierten visuellen Elementen bereichern.

## FAQs

### F1: Kann ich mit Aspose.Note mehrere Bilder mit unterschiedlichen Tags in einem einzigen Dokument hinzufügen?

A1: Ja, Sie können mehrere Bilder mit unterschiedlichen Tags hinzufügen, indem Sie für jedes Bild ähnliche Schritte ausführen.

### F2: Ist Aspose.Note mit allen Versionen von OneNote kompatibel?

A2: Aspose.Note unterstützt verschiedene Versionen von OneNote und gewährleistet so die Kompatibilität in verschiedenen Umgebungen.

### F3: Kann ich das Erscheinungsbild des dem Bild hinzugefügten Tags anpassen?

A3: Ja, Aspose.Note bietet Flexibilität bei der Anpassung des Tag-Erscheinungsbilds an Ihre Vorlieben.

### F4: Bietet Aspose.Note Unterstützung für das Hinzufügen von Bildern aus URLs?

A4: Aspose.Note unterstützt in erster Linie das Hinzufügen von Bildern aus lokalen Verzeichnissen, Sie können jedoch auch externe Bilder einbinden, indem Sie diese zunächst lokal herunterladen.

### F5: Gibt es Einschränkungen hinsichtlich der Größe oder des Formats der Bilder, die hinzugefügt werden können?

A5: Aspose.Note unterstützt eine Vielzahl von Bildformaten und legt keine strengen Beschränkungen für die Bildgröße fest, sodass Sie vielfältige visuelle Elemente in Ihre Dokumente integrieren können.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
