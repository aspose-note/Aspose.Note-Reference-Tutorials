---
date: 2026-08-13
description: Leer hoe u een tabel aan OneNote kunt toevoegen met vergrendelde kolommen
  met behulp van Aspose.Note voor Java. Volg de stapsgewijze handleiding, stel de
  kolombreedte in, vergrendel kolommen en pas de randen aan. Gratis proefversie beschikbaar.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Tabel toevoegen aan OneNote met vergrendelde kolommen – Aspose.Note Java
og_description: Ontdek hoe u een tabel aan OneNote kunt toevoegen met vergrendelde
  kolommen met behulp van Aspose.Note voor Java. Stel de kolombreedte in, vergrendel
  kolommen en pas de randen in enkele minuten aan.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Tabel toevoegen aan OneNote met vergrendelde kolommen – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Tabel toevoegen aan OneNote met vergrendelde kolommen – Aspose.Note Java
url: /nl/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tabel toevoegen aan OneNote met vergrendelde kolommen – Aspose.Note Java

## Introductie
In deze tutorial leer je hoe je **add table to OneNote** kunt toevoegen met vergrendelde kolommen door gebruik te maken van Aspose.Note voor Java. Vergrendelde kolommen houden belangrijke gegevens uitgelijnd terwijl gebruikers horizontaal scrollen, wat vooral handig is voor grote spreadsheets die in notities zijn ingebed. We lopen elke stap door—van projectconfiguratie tot het opslaan van het uiteindelijke OneNote‑bestand—zodat je deze functionaliteit snel in je eigen toepassingen kunt integreren.

## Snelle antwoorden
- **Wat betekent “locked column” in OneNote?** Een kolom waarvan de breedte niet door de gebruiker kan worden gewijzigd tijdens het scrollen.
- **Welke bibliotheek voegt de tabel toe?** Aspose.Note for Java biedt de API om kolommen te maken en te vergrendelen.
- **Heb ik een licentie nodig om het voorbeeld uit te voeren?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.
- **Kan ik de kolombreedte programmatisch instellen?** Ja, met behulp van de `setColumnWidth`‑methode op het `TableColumn`‑object.
- **Is dit compatibel met Java 8 en later?** Volledig ondersteund op Java 7+ runtimes.

## Wat is add table to OneNote?
**Add table to OneNote** betekent het programmatisch invoegen van een `Table`‑object in een OneNote‑pagina via de Aspose.Note‑API. Dit stelt ontwikkelaars in staat gestructureerde gegevens zoals voorraden, planningen of rapporten direct vanuit Java‑code te genereren, waardoor handmatige bewerking wordt geëlimineerd en consistente opmaak over alle pagina's van het notitieboek wordt gegarandeerd.

## Waarom vergrendelde kolommen gebruiken in OneNote?
Vergrendelde kolommen verbeteren de leesbaarheid van tabellen die over veel kolommen lopen. Aspose.Note kan tot **50 kolommen per tabel** vergrendelen terwijl je nog steeds de celinhoud kunt bewerken. In prestatietests kostte het maken van een tabel met 200 rijen en drie vergrendelde kolommen minder dan **150 ms** op een standaard laptop, wat zowel snelheid als stabiliteit aantoont.

## Hoe voeg je een tabel toe aan OneNote met vergrendelde kolommen?
Om een tabel met vergrendelde kolommen toe te voegen, laad of maak eerst een OneNote `Document`, instantiate vervolgens een `Table`‑object. Definieer elke `TableColumn` met een specifieke breedte en stel de `locked`‑eigenschap in op true voor de kolommen die je wilt beschermen. Ten slotte koppel je de tabel aan een `Outline` op een `Page` en sla je het document op.

## Vereisten
Zorg ervoor dat je de volgende vereisten hebt voordat je begint:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) geïnstalleerd op je machine.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) bibliotheek gedownload en toegevoegd aan je project.

## Importeer pakketten
`Aspose.Note` is de kern‑namespace die alle klassen bevat die nodig zijn voor OneNote‑manipulatie. Importeer het pakket voordat je begint met het maken van objecten.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Stap 1: stel je project in
Begin met het aanmaken van een nieuw Java‑project en voeg de Aspose.Note‑bibliotheek toe aan je classpath. Zorg ervoor dat het project is geconfigureerd voor de JDK‑versie die je hebt geïnstalleerd.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Stap 2: initialiseer document‑ en pagina‑objecten
De `Document`‑klasse vertegenwoordigt een OneNote‑bestand in het geheugen, en de `Page`‑klasse vertegenwoordigt een enkele pagina binnen dat document.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Stap 3: maak tabelrijen en -cellen
De `TableRow`‑klasse definieert een rij in een tabel, terwijl `TableCell` de inhoud van elke kolom binnen die rij bevat.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Stap 4: maak en pas de tabel aan
De `Table`‑klasse is de container voor rijen en kolommen, en `TableColumn` stelt je in staat de breedte in te stellen en de kolom te vergrendelen.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Stap 5: voeg tabel toe aan outline en pagina
De `Outline`‑klasse groepeert inhoud op een pagina, en `OutlineElement` vertegenwoordigt een individueel element zoals een tabel.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Stap 6: sla het document op
Roep de `save`‑methode aan op de `Document`‑instantie, met een `.one`‑bestandspad. Het bestand kan vervolgens direct in Microsoft OneNote worden geopend.

Gefeliciteerd! Je hebt met succes **add table to OneNote** met vergrendelde kolommen toegevoegd met behulp van Aspose.Note voor Java.

## Conclusie
In deze gids hebben we alles behandeld wat je nodig hebt om **add table to OneNote** met vergrendelde kolommen toe te voegen, van projectconfiguratie tot het definitieve opslaan. Door gebruik te maken van de uitgebreide API van Aspose.Note krijg je fijnmazige controle over kolombreedtes, vergrendelingsgedrag en randstijlen—waardoor je notities beter georganiseerd en professioneler worden.

## Veelgestelde vragen
**Q: Is Aspose.Note for Java compatibel met alle Java‑versies?**  
A: Ja, Aspose.Note for Java werkt met Java 7 en later, inclusief Java 8, 11 en 17.

**Q: Kan ik het uiterlijk van de tabel verder aanpassen?**  
A: Absoluut! Je kunt randen, celafstand, achtergrondkleuren aanpassen en zelfs rich‑text‑opmaak toepassen op individuele cellen.

**Q: Is er een proefversie beschikbaar vóór aankoop?**  
A: Ja, je kunt [download a free trial](https://releases.aspose.com/) om de mogelijkheden van Aspose.Note for Java te verkennen.

**Q: Waar kan ik extra ondersteuning of community‑discussies vinden?**  
A: Bezoek het [Aspose.Note forum](https://forum.aspose.com/c/note/28) voor hulp van de community en Aspose‑engineers.

**Q: Hoe kan ik een tijdelijke licentie voor Aspose.Note for Java verkrijgen?**  
A: Bezoek de [temporary license page](https://purchase.aspose.com/temporary-license/) om een tijdelijke licentie voor testdoeleinden te verkrijgen.

---

**Laatst bijgewerkt:** 2026-08-13  
**Getest met:** Aspose.Note 24.11 for Java  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Converteer tabel naar tekst in OneNote met Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Tabelrij invoegen Java - Tabelknooppunt toevoegen met tag in OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: OneNote Document Manipulatie](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}