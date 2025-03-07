---
title: Fügen Sie eine chinesische Nummernliste in den Aspose.Note-Text ein
linktitle: Fügen Sie eine chinesische Nummernliste in den Aspose.Note-Text ein
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie mühelos chinesische Nummernlisten in Aspose.Note für .NET-Dokumente einfügen. Verbessern Sie Ihre Fähigkeiten im Bereich der Dokumentformatierung mit dieser Schritt-für-Schritt-Anleitung.
weight: 20
url: /de/net/text-manipulation/insert-chinese-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Fügen Sie eine chinesische Nummernliste in den Aspose.Note-Text ein

## Einführung
Möchten Sie Ihre Aspose.Note für .NET-Kenntnisse verbessern, indem Sie chinesische Nummernlisten in Ihre Dokumente integrieren? Dann sind Sie hier genau richtig! In diesem Tutorial führen wir Sie durch den Prozess des Einfügens chinesischer Nummernlisten mit Aspose.Note für .NET. Mit dieser leistungsstarken Bibliothek können Sie OneNote-Dokumente nahtlos bearbeiten.
## Voraussetzungen
Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
- Grundkenntnisse der C#-Programmierung.
-  Aspose.Note für .NET installiert. Sie können es herunterladen[Hier](https://releases.aspose.com/note/net/).
## Namespaces importieren
Importieren Sie zunächst die erforderlichen Namespaces in Ihr Projekt:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Schritt 1: OneNote-Dokument initialisieren
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Schritt 2: OneNote-Seite initialisieren
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## Schritt 3: Textstileinstellungen anwenden
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Schritt 4: Gliederungselemente erstellen
Lassen Sie uns nun drei Gliederungselemente mit chinesischen Nummernlisten erstellen:
### Schritt 4.1: Erstes Element
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Schritt 4.2: Zweites Element
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Schritt 4.3: Drittes Element
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Schritt 5: Elemente an die Gliederung anhängen
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Schritt 6: Gliederung an die Seite anhängen
```csharp
page.AppendChildLast(outline);
```
## Schritt 7: Seite an Dokument anhängen
```csharp
doc.AppendChildLast(page);
```
## Schritt 8: OneNote-Dokument speichern
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Glückwunsch! Sie haben mithilfe der .NET-Bibliothek erfolgreich chinesische Nummernlisten in Ihr Aspose.Note-Dokument eingefügt.
## Abschluss
In diesem Tutorial haben wir den schrittweisen Prozess der Integration chinesischer Nummernlisten in Ihre Aspose.Note für .NET-Dokumente behandelt. Verbessern Sie Ihre Fähigkeiten zur Dokumentformatierung und gestalten Sie Ihre Inhalte mit diesen Techniken ansprechender.
## FAQs
### F: Kann ich die Formatierung chinesischer Nummernlisten anpassen?
 A: Ja, Sie können die Formatierung anpassen, indem Sie die Parameter im anpassen`NumberList` Konstrukteur.
### F: Ist Aspose.Note mit der neuesten Version von .NET kompatibel?
A: Ja, Aspose.Note wird regelmäßig aktualisiert, um die neuesten Versionen von .NET zu unterstützen.
### F: Wo finde ich zusätzliche Beispiele und Dokumentation?
A: Entdecken Sie das umfassende[Aspose.Note-Dokumentation](https://reference.aspose.com/note/net/).
### F: Wie kann ich eine temporäre Lizenz für Aspose.Note erhalten?
 A: Besorgen Sie sich eine temporäre Lizenz[Hier](https://purchase.aspose.com/temporary-license/).
### F: Wo kann ich Hilfe suchen oder Aspose.Note-bezogene Fragen besprechen?
 A: Besuchen Sie die[Aspose.Note-Supportforum](https://forum.aspose.com/c/note/28) für die Unterstützung der Gemeinschaft.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
