---
title: Fügen Sie Hyperlinks in Aspose.Note-Dokumenten hinzu
linktitle: Fügen Sie Hyperlinks in Aspose.Note-Dokumenten hinzu
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie mit Aspose.Note für .NET Hyperlinks zu Aspose.Note-Dokumenten hinzufügen. Verbessern Sie die Interaktivität von Dokumenten mit dieser Schritt-für-Schritt-Anleitung.
type: docs
weight: 10
url: /de/net/hyperlinks/add-hyperlinks/
---
## Einführung

In diesem Tutorial erfahren Sie, wie Sie mithilfe des .NET-Frameworks Hyperlinks zu Text in Aspose.Note-Dokumenten hinzufügen. Aspose.Note bietet leistungsstarke Funktionen zum programmgesteuerten Bearbeiten von OneNote-Dokumenten. Das Hinzufügen von Hyperlinks kann die Interaktivität und Benutzerfreundlichkeit Ihrer Dokumente verbessern und sie für Benutzer ansprechender machen.

## Voraussetzungen:

Bevor Sie beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Grundlegendes Verständnis der Programmiersprache C#.
2. Visual Studio ist auf Ihrem System installiert.
3.  Aspose.Note für .NET-Bibliothek installiert. Sie können es herunterladen unter[Hier](https://releases.aspose.com/note/net/).
4. Vertrautheit mit der Struktur und den Komponenten von Aspose.Note-Dokumenten.

## Namespaces importieren:

Zunächst müssen Sie die erforderlichen Namespaces in Ihr C#-Projekt importieren. Diese Namespaces bieten Zugriff auf die Klassen und Methoden, die für die Arbeit mit Aspose.Note-Dokumenten erforderlich sind.

```csharp
using System;
using System.Drawing;
```

## Schritt 1: Erstellen Sie ein neues Dokumentobjekt:

Beginnen Sie mit der Erstellung einer neuen Instanz der Document-Klasse. Dieses Objekt stellt Ihr Aspose.Note-Dokument dar, zu dem Sie den Hyperlink hinzufügen.

```csharp
Document doc = new Document();
```

## Schritt 2: Textstile definieren:

Definieren Sie die Textstile für den regulären Text und den Hyperlink-Text. Sie können verschiedene Attribute wie Schriftfarbe, Schriftname und Schriftgröße nach Ihren Wünschen anpassen.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

## Schritt 3: RichText-Objekte erstellen:

Erstellen Sie RichText-Objekte für die Textsegmente, die Sie in Ihr Dokument aufnehmen möchten. Hängen Sie den entsprechenden Text an und wenden Sie die gewünschten Textstile auf jedes Segment an.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

## Schritt 4: Gliederung und Gliederungselement erstellen:

Erstellen Sie ein Outline-Objekt und ein OutlineElement-Objekt, um Ihren Dokumentinhalt zu strukturieren. Hängen Sie das RichText-Objekt, das den Hyperlink enthält, an das OutlineElement an.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

## Schritt 5: Elemente zur Seite hinzufügen:

Erstellen Sie ein Title-Objekt und ein Page-Objekt. Hängen Sie das Outline-Objekt an die Seite an. Hängen Sie abschließend die Seite an das Dokument an.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Schritt 6: Speichern Sie das Dokument:

Geben Sie den Dateipfad an, in dem Sie das Aspose.Note-Dokument speichern möchten, und rufen Sie die Save-Methode auf, um es zu speichern.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## Abschluss:

In diesem Tutorial haben Sie gelernt, wie Sie mit Aspose.Note für .NET Hyperlinks zu Aspose.Note-Dokumenten hinzufügen. Indem Sie diese Schritte befolgen, können Sie die Interaktivität Ihrer Dokumente verbessern und den Benutzern ein dynamischeres Erlebnis bieten.

## FAQs

### F1: Kann ich mit Aspose.Note mehrere Hyperlinks innerhalb desselben Dokuments hinzufügen?

A1: Ja, Sie können innerhalb eines einzelnen Aspose.Note-Dokuments mehrere Hyperlinks zu verschiedenen Textsegmenten hinzufügen.

### F2: Kann ich das Erscheinungsbild von Hyperlinks in Aspose.Note-Dokumenten anpassen?

A2: Ja, Sie können verschiedene Attribute wie Schriftfarbe, Schriftgröße und Schriftstil für Hyperlinks in Aspose.Note-Dokumenten anpassen.

### F3: Unterstützt Aspose.Note Hyperlinks zu externen Websites?

A3: Ja, mit Aspose.Note können Sie Hyperlinks erstellen, die Benutzer zu externen Websites oder Webseiten weiterleiten.

### F4: Ist Aspose.Note mit allen Versionen von Microsoft OneNote kompatibel?

A4: Aspose.Note ist für die Verwendung mit Microsoft OneNote 2010 und späteren Versionen konzipiert.

### F5: Kann ich Hyperlinks programmgesteuert mithilfe der Aspose.Note-APIs hinzufügen?

A5: Ja, Aspose.Note bietet APIs, mit denen Sie in Ihren .NET-Anwendungen programmgesteuert Hyperlinks zu Text hinzufügen können.