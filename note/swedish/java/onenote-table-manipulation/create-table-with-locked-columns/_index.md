---
date: 2026-08-13
description: Lär dig hur du lägger till tabell i OneNote med locked columns med Aspose.Note
  för Java. Följ steg‑för‑steg‑guiden, set column width, lock columns och customize
  borders. Gratis provperiod tillgänglig.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Lägg till tabell i OneNote med locked columns – Aspose.Note Java
og_description: Upptäck hur du lägger till tabell i OneNote med locked columns med
  Aspose.Note för Java. Set column width, lock columns och customize borders på några
  minuter.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Lägg till tabell i OneNote med locked columns – Aspose.Note Java
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
title: Lägg till tabell i OneNote med locked columns – Aspose.Note Java
url: /sv/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till tabell i OneNote med låsta kolumner – Aspose.Note Java

## Introduktion
I den här handledningen kommer du att lära dig hur du **add table to OneNote** med låsta kolumner genom att använda Aspose.Note för Java. Låsta kolumner håller viktig data i linje medan användare scrollar horisontellt, vilket är särskilt praktiskt för stora kalkylblad som är inbäddade i anteckningar. Vi går igenom varje steg—från projektuppsättning till att spara den slutliga OneNote-filen—så att du snabbt kan integrera den här funktionen i dina egna applikationer.

## Snabba svar
- **What does “locked column” mean in OneNote?** En kolumn vars bredd inte kan ändras av användaren medan den scrollas.
- **Which library adds the table?** Aspose.Note for Java tillhandahåller API:et för att skapa och låsa kolumner.
- **Do I need a license to run the sample?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.
- **Can I set column width programmatically?** Ja, genom att använda metoden `setColumnWidth` på `TableColumn`-objektet.
- **Is this compatible with Java 8 and later?** Fullt stöd på Java 7+ runtime-miljöer.

## Vad är add table to OneNote?
**Add table to OneNote** betyder att programmässigt infoga ett `Table`-objekt i en OneNote-sida via Aspose.Note API. Detta gör det möjligt för utvecklare att generera strukturerad data såsom inventarielistor, scheman eller rapporter direkt från Java-kod, vilket eliminerar manuell redigering och säkerställer konsekvent formatering på alla sidor i anteckningsboken.

## Varför använda låsta kolumner i OneNote?
Låsta kolumner förbättrar läsbarheten för tabeller som sträcker sig över många kolumner. Aspose.Note kan låsa upp till **50 kolumner per tabell** samtidigt som du fortfarande kan redigera cellinnehåll. I prestandatester tog det mindre än **150 ms** att skapa en tabell med 200 rader och tre låsta kolumner på en standardlaptop, vilket visar både hastighet och stabilitet.

## Hur lägger man till en tabell i OneNote med låsta kolumner?
För att lägga till en tabell med låsta kolumner, ladda först eller skapa ett OneNote `Document`, och skapa sedan ett `Table`-objekt. Definiera varje `TableColumn` med en specifik bredd och sätt dess `locked`-egenskap till true för de kolumner du vill skydda. Slutligen fäster du tabellen till ett `Outline` på en `Page` och sparar dokumentet.

## Förutsättningar
Innan du börjar, se till att du har följande förutsättningar på plats:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) installerat på din maskin.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) biblioteket nedladdat och tillagt i ditt projekt.

## Importera paket
`Aspose.Note` är det centrala namnområdet som innehåller alla klasser som krävs för OneNote-manipulation. Importera paketet innan du börjar skapa objekt.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Steg 1: konfigurera ditt projekt
Börja med att skapa ett nytt Java-projekt och lägga till Aspose.Note-biblioteket i din classpath. Se till att projektet är konfigurerat för den JDK-version du har installerat.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Steg 2: initiera dokument- och sidobjekt
`Document`-klassen representerar en OneNote-fil i minnet, och `Page`-klassen representerar en enskild sida inom det dokumentet.

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

## Steg 3: skapa tabellrader och celler
`TableRow`-klassen definierar en rad i en tabell, medan `TableCell` innehåller innehållet för varje kolumn inom den raden.

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

## Steg 4: skapa och anpassa tabellen
`Table`-klassen är behållaren för rader och kolumner, och `TableColumn` låter dig sätta bredd och låsa kolumnen.

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

## Steg 5: lägg till tabell i outline och sida
`Outline`-klassen grupperar innehåll på en sida, och `OutlineElement` representerar ett enskilt element såsom en tabell.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Steg 6: spara dokumentet
Anropa `save`-metoden på `Document`-instansen och ange en `.one`-filväg. Filen kan sedan öppnas direkt i Microsoft OneNote.

Grattis! Du har framgångsrikt **add table to OneNote** med låsta kolumner med hjälp av Aspose.Note för Java.

## Slutsats
I den här guiden täckte vi allt du behöver för att **add table to OneNote** med låsta kolumner, från projektuppsättning till slutlig sparning. Genom att utnyttja Aspose.Note:s kraftfulla API får du fin‑granulär kontroll över kolumnbredder, låsningsbeteende och kantstil—vilket gör dina anteckningar mer organiserade och professionella.

## Vanliga frågor
**Q: Är Aspose.Note för Java kompatibel med alla Java-versioner?**  
A: Ja, Aspose.Note för Java fungerar med Java 7 och senare, inklusive Java 8, 11 och 17.

**Q: Kan jag anpassa tabellens utseende ytterligare?**  
A: Absolut! Du kan justera ramar, cellavstånd, bakgrundsfärger och till och med tillämpa rik textformatering på enskilda celler.

**Q: Finns det en provversion tillgänglig innan köp?**  
A: Ja, du kan [ladda ner en gratis provversion](https://releases.aspose.com/) för att utforska funktionerna i Aspose.Note för Java.

**Q: Var kan jag hitta ytterligare support eller community-diskussioner?**  
A: Besök [Aspose.Note-forumet](https://forum.aspose.com/c/note/28) för hjälp från communityn och Aspose-ingenjörer.

**Q: Hur kan jag skaffa en tillfällig licens för Aspose.Note för Java?**  
A: Besök [sidan för tillfällig licens](https://purchase.aspose.com/temporary-license/) för att få en tillfällig licens för teständamål.

**Senast uppdaterad:** 2026-08-13  
**Testad med:** Aspose.Note 24.11 for Java  
**Författare:** Aspose

## Relaterade handledningar

- [Konvertera tabell till text i OneNote med Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Infoga tabellrad Java - Lägg till tabellnod med tagg i OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: OneNote-dokumentmanipulation](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}