---
title: Fügen Sie einen Textknoten mit Tag in Aspose.Note hinzu
linktitle: Fügen Sie einen Textknoten mit Tag in Aspose.Note hinzu
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie mit Aspose.Note für .NET Textknoten mit Tags zu OneNote-Dokumenten hinzufügen.
weight: 12
url: /de/net/tag-management/add-text-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Fügen Sie einen Textknoten mit Tag in Aspose.Note hinzu

## Einführung

Aspose.Note für .NET ist eine leistungsstarke Bibliothek, die es Entwicklern ermöglicht, Microsoft OneNote-Dateien mithilfe des .NET-Frameworks programmgesteuert zu erstellen, zu bearbeiten und zu konvertieren. In diesem Tutorial erfahren Sie, wie Sie mithilfe von Aspose.Note für .NET einen Textknoten mit einem Tag zu einem OneNote-Dokument hinzufügen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Visual Studio: Stellen Sie sicher, dass Visual Studio auf Ihrem System installiert ist.
2.  Aspose.Note für .NET: Laden Sie Aspose.Note für .NET von herunter und installieren Sie es[Webseite](https://releases.aspose.com/note/net/).
3. Grundkenntnisse von C#: Machen Sie sich mit den Grundlagen der Programmiersprache C# vertraut.

## Namespaces importieren

Zunächst müssen Sie die erforderlichen Namespaces importieren, um auf die Klassen und Methoden zuzugreifen, die für die Arbeit mit Aspose.Note für .NET erforderlich sind.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Schritt 1: Erstellen Sie ein Dokumentobjekt

Initialisieren Sie ein Document-Objekt, um mit der Arbeit mit einem OneNote-Dokument zu beginnen.

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## Schritt 2: Seiten- und Gliederungsobjekte initialisieren

Erstellen Sie Seiten- und Gliederungsobjekte, um den Inhalt des OneNote-Dokuments zu strukturieren.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## Schritt 3: Textknoten mit Tag hinzufügen

Erstellen Sie ein RichText-Objekt mit dem gewünschten Text und Stil und fügen Sie es dann dem OutlineElement hinzu.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## Schritt 4: Gliederungselement und Seitenknoten anhängen

Hängen Sie das OutlineElement an die Gliederung und dann die Gliederung an die Seite an. Hängen Sie abschließend die Seite an das Dokument an.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Schritt 5: Speichern Sie das Dokument

Speichern Sie das geänderte OneNote-Dokument an einem angegebenen Speicherort.

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.Note für .NET einen Textknoten mit einem Tag zu einem OneNote-Dokument hinzufügen. Mit diesem Wissen können Sie Ihre OneNote-Dateien jetzt programmgesteuert anpassen und erweitern.

## FAQs

### F1: Kann ich im selben Dokument mehrere Textknoten mit unterschiedlichen Tags hinzufügen?

A1: Ja, Sie können mehrere Textknoten mit unterschiedlichen Tags hinzufügen, indem Sie für jeden Knoten den gleichen Vorgang ausführen.

### F2: Ist Aspose.Note für .NET mit allen Versionen von OneNote kompatibel?

A2: Aspose.Note für .NET unterstützt verschiedene Versionen von OneNote, einschließlich 2010, 2013, 2016 und höher.

### F3: Kann ich die Tag-Farben und -Stile anpassen?

A3: Ja, Sie können die Tag-Farben und -Stile entsprechend Ihren Anforderungen anpassen.

### F4: Unterstützt Aspose.Note für .NET die Dokumentverschlüsselung?

A4: Ja, Aspose.Note für .NET unterstützt die Dokumentenverschlüsselung, um die Datensicherheit zu gewährleisten.

### F5: Wo finde ich weitere Ressourcen und Unterstützung für Aspose.Note für .NET?

 A5: Sie können das erkunden[Aspose.Note für .NET-Dokumentation](https://reference.aspose.com/note/net/)und suchen Sie Hilfe bei der[Aspose.Note-Forum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
