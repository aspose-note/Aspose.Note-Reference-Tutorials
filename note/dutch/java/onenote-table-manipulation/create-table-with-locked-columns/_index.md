---
title: Maak een tabel met vergrendelde kolommen in OneNote - Aspose.Note
linktitle: Maak een tabel met vergrendelde kolommen in OneNote - Aspose.Note
second_title: Aspose.Note Java-API
description: Verbeter uw OneNote-ervaring met Aspose.Note voor Java. Leer hoe u tabellen met vergrendelde kolommen maakt met behulp van een stapsgewijze handleiding. Download nu uw gratis proefversie!
weight: 12
url: /nl/java/onenote-table-manipulation/create-table-with-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak een tabel met vergrendelde kolommen in OneNote - Aspose.Note

## Invoering
OneNote is een krachtig hulpmiddel voor het organiseren van informatie, en Aspose.Note voor Java verbetert de mogelijkheden ervan door een naadloze manier te bieden om tabellen met vergrendelde kolommen te maken. In deze zelfstudie begeleiden we u bij het gebruik van Aspose.Note voor Java om een tabel met vergrendelde kolommen in OneNote te maken.
## Vereisten
Voordat u begint, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:
- [Java-ontwikkelkit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)op uw machine geïnstalleerd.
- [Aspose.Opmerking voor Java](https://downloads.aspose.com/note/java) bibliotheek gedownload en toegevoegd aan uw project.
## Pakketten importeren
Importeer in uw Java-project de benodigde pakketten om met Aspose te werken.Opmerking:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Stap 1: Stel uw project in
Begin met het maken van een nieuw Java-project en het toevoegen van de Aspose.Note-bibliotheek aan uw klassenpad. Zorg ervoor dat uw project is geconfigureerd om de JDK te gebruiken.
## Stap 2: Initialiseer document- en pagina-objecten
```java
// Het pad naar de documentenmap.
String dataDir = "Your Document Directory";
//Maak een object van de klasse Document
Document doc = new Document();
// Initialiseer het Page-klasseobject
Page page = new Page();
```
## Stap 3: Maak tabelrijen en cellen
```java
// Initialiseer het TableRow-klasseobject
TableRow row1 = new TableRow();
// Initialiseer het TableCell-klasseobject en stel de tekstinhoud in
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialiseer het TableRow-klasseobject
TableRow row2 = new TableRow();
// Initialiseer het TableCell-klasseobject en stel de tekstinhoud in
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Stap 4: Maak de tabel en pas deze aan
```java
// Initialiseer het Table-klasseobject
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Rijen toevoegen
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Stap 5: Tabel toevoegen aan overzicht en pagina
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Tabelknooppunt toevoegen
outlineElem.appendChildLast(table);
// Voeg een overzichtselementknooppunt toe
outline.appendChildLast(outlineElem);
// Voeg een overzichtsknooppunt toe
page.appendChildLast(outline);
// Paginaknooppunt toevoegen
doc.appendChildLast(page);
```
## Stap 6: Sla het document op
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Gefeliciteerd! U hebt met succes een tabel met vergrendelde kolommen in OneNote gemaakt met behulp van Aspose.Note voor Java.
## Conclusie
In deze zelfstudie hebben we het proces van het gebruik van Aspose.Note voor Java onderzocht om uw OneNote-ervaring te verbeteren door tabellen met vergrendelde kolommen te maken. Deze functionaliteit voegt een nieuwe laag organisatie en structuur toe aan uw notities.
## Veelgestelde vragen
### Is Aspose.Note voor Java compatibel met alle Java-versies?
Ja, Aspose.Note voor Java is compatibel met Java 6 en latere versies.
### Kan ik het uiterlijk van de tafel verder aanpassen?
Absoluut! Aspose.Note voor Java biedt uitgebreide opties voor het aanpassen van tabellen, zoals het aanpassen van randen, celafstanden en meer.
### Is er een proefversie beschikbaar voordat u deze aanschaft?
 Ja, dat kan[download een gratis proefversie](https://releases.aspose.com/) om de mogelijkheden van Aspose.Note voor Java te verkennen.
### Waar kan ik aanvullende ondersteuning of communitydiscussies vinden?
 Bezoek de[Aspose.Note-forum](https://forum.aspose.com/c/note/28) voor ondersteuning en gemeenschapsdiscussies.
### Hoe kan ik een tijdelijke licentie verkrijgen voor Aspose.Note voor Java?
 Bezoek[deze link](https://purchase.aspose.com/temporary-license/) om een tijdelijke licentie voor testdoeleinden te verkrijgen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
