---
title: Anwenden der Nummerierung auf Text in Aspose.Note
linktitle: Anwenden der Nummerierung auf Text in Aspose.Note
second_title: Aspose.Note .NET-API
description: Erfahren Sie in diesem umfassenden Tutorial, wie Sie die Textnummerierung in Aspose.Note für .NET anwenden. Verbessern Sie mühelos die Formatierung Ihrer Dokumente.
type: docs
weight: 12
url: /de/net/text-manipulation/apply-numbering-on-text/
---
## Einführung
Aspose.Note für .NET bietet leistungsstarke Tools für die Dokumentbearbeitung in C#-Anwendungen. In diesem Tutorial untersuchen wir den Prozess der Nummerierung von Texten mithilfe von Aspose.Note. Befolgen Sie diese Schritt-für-Schritt-Anleitung, um die Formatierung Ihres Dokuments mühelos zu verbessern.
## Voraussetzungen
Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
- Grundlegendes Verständnis der Programmiersprache C#.
-  Aspose.Note für .NET installiert. Sie können es herunterladen[Hier](https://releases.aspose.com/note/net/).
- Eine integrierte Entwicklungsumgebung (IDE) wie Visual Studio.
## Namespaces importieren
Stellen Sie zunächst sicher, dass Sie die erforderlichen Namespaces in Ihr C#-Projekt importieren:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Schritt 1: Richten Sie Ihr Dokument ein
Beginnen Sie mit der Erstellung eines neuen Dokuments und der Initialisierung der erforderlichen Objekte:
```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";
//Erstellen Sie ein Objekt der Document-Klasse
Document doc = new Document();
// Initialisieren Sie das Page-Klassenobjekt
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Initialisieren Sie das Outline-Klassenobjekt
Outline outline = new Outline(doc);
```
## Schritt 2: Definieren Sie den Standardstil
Richten Sie den Standardstil für Ihren Text mithilfe der ParagraphStyle-Klasse ein:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Schritt 3: Nummerierung anwenden
Initialisieren Sie Objekte der OutlineElement-Klasse und wenden Sie eine Nummerierung auf jedes Element an:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Schritt 4: Gliederungselemente hinzufügen
Hängen Sie die Gliederungselemente an die Gliederung an:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Schritt 5: Speichern Sie das Dokument
Speichern Sie das OneNote-Dokument mit der angewendeten Nummerierung:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## Abschluss
Glückwunsch! Sie haben erfolgreich gelernt, wie Sie in Aspose.Note für .NET Nummerierung auf Text anwenden. Experimentieren Sie mit verschiedenen Formatierungsoptionen, um mühelos optisch ansprechende Dokumente zu erstellen.
## FAQs
### 1. Kann ich das Nummerierungsformat anpassen?
Ja, mit der NumberList-Klasse können Sie das Nummerierungsformat nach Ihren Wünschen anpassen.
### 2. Gibt es weitere Formatierungsoptionen?
Aspose.Note bietet eine breite Palette an Formatierungsoptionen, einschließlich Schriftart, Farbe und mehr.
### 3. Ist Aspose.Note mit Visual Studio kompatibel?
Absolut! Aspose.Note lässt sich nahtlos in Visual Studio integrieren und sorgt so für ein reibungsloses Entwicklungserlebnis.
### 4. Kann ich Aspose.Note vor dem Kauf testen?
 Sicherlich! Sie können eine kostenlose Testversion ausprobieren[Hier](https://releases.aspose.com/).
### 5. Wo bekomme ich Support für Aspose.Note?
 Wenn Sie Hilfe oder Fragen haben, besuchen Sie die[Aspose.Note-Forum](https://forum.aspose.com/c/note/28).