---
title: Wenden Sie Aufzählungszeichen auf Text in Aspose.Note an
linktitle: Wenden Sie Aufzählungszeichen auf Text in Aspose.Note an
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie in Aspose.Note für .NET Aufzählungszeichen auf Text anwenden, um Ihre OneNote-Dokumente zu verbessern. Befolgen Sie diese Schritt-für-Schritt-Anleitung für eine effektive Formatierung.
type: docs
weight: 10
url: /de/net/text-manipulation/apply-bullets-on-text/
---
## Einführung
Willkommen bei dieser Schritt-für-Schritt-Anleitung zum Anwenden von Aufzählungszeichen auf Text mit Aspose.Note für .NET. Aspose.Note ist eine leistungsstarke Bibliothek, die es Entwicklern ermöglicht, nahtlos mit Microsoft OneNote-Dateien in ihren .NET-Anwendungen zu arbeiten. In diesem Tutorial führen wir Sie durch den Prozess des Anwendens von Aufzählungszeichen auf Text, um die visuelle Attraktivität Ihrer OneNote-Dokumente zu verbessern.
## Voraussetzungen
Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:
- Grundkenntnisse in C#- und .NET-Programmierung.
-  Aspose.Note für .NET-Bibliothek installiert. Sie können es herunterladen[Hier](https://releases.aspose.com/note/net/).
## Namespaces importieren
Stellen Sie sicher, dass Sie in Ihrem C#-Code die erforderlichen Namespaces einschließen:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Schritt 1: Richten Sie Ihr Dokument ein
```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";
//Erstellen Sie ein Objekt der Document-Klasse
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Schritt 2: Seite und Gliederung initialisieren
```csharp
// Initialisieren Sie das Page-Klassenobjekt
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Initialisieren Sie das Outline-Klassenobjekt
Outline outline = new Outline(doc);
```
## Schritt 3: Standardtextstil festlegen
```csharp
// Initialisieren Sie das TextStyle-Klassenobjekt und legen Sie Formatierungseigenschaften fest
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Schritt 4: Erstellen Sie Gliederungselemente mit Aufzählungszeichen
```csharp
// Initialisieren Sie OutlineElement-Klassenobjekte und wenden Sie Aufzählungszeichen an
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Wiederholen Sie den Vorgang für andere Gliederungselemente
```
## Schritt 5: Gliederungselemente zur Gliederung hinzufügen
```csharp
// Gliederungselemente hinzufügen
outline.AppendChildLast(outlineElem1);
// Wiederholen Sie den Vorgang für andere Gliederungselemente
```
## Schritt 6: Gliederung zur Seite hinzufügen
```csharp
// Gliederungsknoten hinzufügen
page.AppendChildLast(outline);
```
## Schritt 7: Seite zum Dokument hinzufügen
```csharp
//Seitenknoten hinzufügen
doc.AppendChildLast(page);
```
## Schritt 8: Speichern Sie das OneNote-Dokument
```csharp
// OneNote-Dokument speichern
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## Abschluss
Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.Note für .NET Aufzählungszeichen auf Text anwenden. Diese Funktion kann die Formatierung Ihrer OneNote-Dokumente erheblich verbessern und sie optisch ansprechender machen.
## FAQs
### Kann ich auf jedes Element in der Liste unterschiedliche Aufzählungszeichenstile anwenden?
 Ja, Sie können die Aufzählungszeichenstile anpassen, indem Sie die ändern`NumberList` Eigenschaften für jeden`OutlineElement`.
### Ist Aspose.Note mit der neuesten Version von Microsoft OneNote kompatibel?
Aspose.Note unterstützt verschiedene Versionen von Microsoft OneNote und gewährleistet so die Kompatibilität mit älteren und neueren Versionen.
### Kann ich Aspose.Note für kommerzielle Zwecke nutzen?
 Ja, Sie können Aspose.Note für .NET in kommerziellen Projekten verwenden. Um eine Lizenz zu erhalten, besuchen Sie[Hier](https://purchase.aspose.com/buy).
### Gibt es eine Testversion für Aspose.Note für .NET?
 Ja, Sie können eine kostenlose Testversion herunterladen[Hier](https://releases.aspose.com/).
### Wo finde ich zusätzliche Unterstützung und Ressourcen?
 Sie können das Aspose.Note-Community-Forum besuchen[Hier](https://forum.aspose.com/c/note/28) für Unterstützung und Diskussionen.