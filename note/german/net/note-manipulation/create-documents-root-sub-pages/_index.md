---
title: Erstellen Sie Dokumente mit Stamm- und Unterseiten mit Aspose.Note
linktitle: Erstellen Sie Dokumente mit Stamm- und Unterseiten mit Aspose.Note
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie mit Aspose.Note für .NET dynamische OneNote-Dokumente mit hierarchischen Strukturen erstellen.
weight: 11
url: /de/net/note-manipulation/create-documents-root-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Erstellen Sie Dokumente mit Stamm- und Unterseiten mit Aspose.Note

## Einführung

Willkommen zu unserem Tutorial zum Erstellen von Dokumenten mit Stamm- und Unterseiten mit Aspose.Note für .NET! Aspose.Note ist eine leistungsstarke Bibliothek, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten und so OneNote-Dokumente zu erstellen, zu bearbeiten und zu konvertieren.

In diesem Tutorial führen wir Sie Schritt für Schritt durch den Prozess der Erstellung eines OneNote-Dokuments mit Stamm- und Unterseiten. Wir stellen detaillierte Erklärungen und Codeausschnitte mit Aspose.Note für .NET bereit, damit Sie die Anleitung leicht nachvollziehen und in Ihre eigenen Projekte implementieren können.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Visual Studio: Sie müssen Visual Studio auf Ihrem System installiert haben, um .NET-Code schreiben und kompilieren zu können.
2.  Aspose.Note für .NET: Laden Sie Aspose.Note für .NET von herunter und installieren Sie es[Download-Seite](https://releases.aspose.com/note/net/).
3. Grundlegende C#-Kenntnisse: Um die Codebeispiele zu verstehen und umzusetzen, sind Kenntnisse der Programmiersprache C# erforderlich.

Nachdem Sie nun alles eingerichtet haben, beginnen wir mit dem Tutorial!

## Namespaces importieren

Importieren wir zunächst die notwendigen Namespaces in unser Projekt:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## Schritt 1: Dokumentobjekt initialisieren

```csharp
//Erstellen Sie ein Objekt der Document-Klasse
Document doc = new Document();
```

## Schritt 2: Stammseite und Unterseiten erstellen

```csharp
// Initialisieren Sie Page-Klassenobjekte und legen Sie ihre Ebenen fest
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### Für Seite 1:

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### Für Seite 2:

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### Für Seite 3:

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## Schritt 4: Seiten zum Dokument hinzufügen

```csharp
// Fügen Sie dem OneNote-Dokument Seiten hinzu
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## Schritt 5: Dokument speichern

```csharp
// OneNote-Dokument speichern
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.Note für .NET Dokumente mit Stamm- und Unterseiten erstellen. Jetzt können Sie dieses Wissen nutzen, um komplexe OneNote-Dokumente in Ihren Anwendungen dynamisch zu generieren.

## FAQs

### F1: Kann Aspose.Note große OneNote-Dokumente verarbeiten?

A1: Ja, Aspose.Note ist darauf ausgelegt, große OneNote-Dokumente effizient zu verarbeiten, ohne die Leistung zu beeinträchtigen.

### F2: Ist Aspose.Note mit .NET Core kompatibel?

A2: Ja, Aspose.Note unterstützt .NET Core zusammen mit dem traditionellen .NET Framework.

### F3: Kann ich OneNote-Dokumente mit Aspose.Note in andere Formate konvertieren?

A3: Absolut, Aspose.Note bietet Konvertierungsfunktionen in verschiedene Formate, darunter PDF, DOCX, HTML und mehr.

### F4: Bietet Aspose.Note eine Cloud-Integration?

A4: Aspose.Note konzentriert sich hauptsächlich auf die lokale Entwicklung, Sie können es jedoch mit der richtigen Einrichtung auch in Cloud-Umgebungen verwenden.

### F5: Ist technischer Support für Aspose.Note verfügbar?

A5: Ja, Aspose bietet über sein Forum speziellen technischen Support, in dem Sie Fragen stellen und Hilfe erhalten können.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
