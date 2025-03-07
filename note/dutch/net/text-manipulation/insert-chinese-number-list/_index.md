---
title: Voeg Chinese nummerlijst in Aspose.Note-tekst in
linktitle: Voeg Chinese nummerlijst in Aspose.Note-tekst in
second_title: Aspose.Note .NET API
description: Leer hoe u moeiteloos Chinese nummerlijsten kunt invoegen in Aspose.Note voor .NET-documenten. Verbeter uw vaardigheden op het gebied van documentopmaak met deze stapsgewijze handleiding.
weight: 20
url: /nl/net/text-manipulation/insert-chinese-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Voeg Chinese nummerlijst in Aspose.Note-tekst in

## Invoering
Wilt u uw Aspose.Note voor .NET-vaardigheden verbeteren door Chinese nummerlijsten in uw documenten op te nemen? Dan ben je hier aan het juiste adres! In deze zelfstudie begeleiden we u bij het invoegen van Chinese nummerlijsten met Aspose.Note voor .NET. Met deze krachtige bibliotheek kunt u OneNote-documenten naadloos manipuleren.
## Vereisten
Voordat we ingaan op de tutorial, zorg ervoor dat je aan de volgende vereisten voldoet:
- Basiskennis van programmeren in C#.
-  Aspose.Note voor .NET geïnstalleerd. Je kunt het downloaden[hier](https://releases.aspose.com/note/net/).
## Naamruimten importeren
Importeer om te beginnen de benodigde naamruimten in uw project:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Stap 1: Initialiseer het OneNote-document
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Stap 2: Initialiseer de OneNote-pagina
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## Stap 3: Pas tekststijlinstellingen toe
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Stap 4: Maak overzichtselementen
Laten we nu drie overzichtselementen maken met Chinese nummerlijsten:
### Stap 4.1: Eerste element
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Stap 4.2: Tweede element
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Stap 4.3: Derde element
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Stap 5: Voeg elementen toe aan de omtrek
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Stap 6: Voeg een overzicht toe aan de pagina
```csharp
page.AppendChildLast(outline);
```
## Stap 7: Pagina aan document toevoegen
```csharp
doc.AppendChildLast(page);
```
## Stap 8: Bewaar OneNote-document
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Gefeliciteerd! U hebt met succes Chinese nummerlijsten in uw Aspose.Note-document ingevoegd met behulp van de .NET-bibliotheek.
## Conclusie
In deze zelfstudie hebben we het stapsgewijze proces besproken van het opnemen van Chinese nummerlijsten in uw Aspose.Note voor .NET-documenten. Verbeter uw vaardigheden op het gebied van documentopmaak en maak uw inhoud aantrekkelijker met deze technieken.
## Veelgestelde vragen
### Vraag: Kan ik de opmaak van Chinese nummerlijsten aanpassen?
 A: Ja, u kunt de opmaak aanpassen door de parameters in het`NumberList` bouwer.
### Vraag: Is Aspose.Note compatibel met de nieuwste versie van .NET?
A: Ja, Aspose.Note wordt regelmatig bijgewerkt om de nieuwste versies van .NET te ondersteunen.
### Vraag: Waar kan ik aanvullende voorbeelden en documentatie vinden?
A: Ontdek het uitgebreide[Aspose.Note-documentatie](https://reference.aspose.com/note/net/).
### Vraag: Hoe kan ik een tijdelijke licentie krijgen voor Aspose.Note?
 A: Zorg voor een tijdelijke licentie[hier](https://purchase.aspose.com/temporary-license/).
### Vraag: Waar kan ik hulp zoeken of Aspose.Note-gerelateerde vragen bespreken?
 A: Bezoek de[Aspose.Note-ondersteuningsforum](https://forum.aspose.com/c/note/28) voor gemeenschapssteun.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
