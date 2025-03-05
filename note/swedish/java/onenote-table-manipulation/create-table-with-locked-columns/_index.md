---
title: Skapa tabell med låsta kolumner i OneNote - Aspose.Note
linktitle: Skapa tabell med låsta kolumner i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Förbättra din OneNote-upplevelse med Aspose.Note för Java. Lär dig hur du skapar tabeller med låsta kolumner med hjälp av en steg-för-steg-guide. Ladda ner din kostnadsfria testversion nu!
type: docs
weight: 12
url: /sv/java/onenote-table-manipulation/create-table-with-locked-columns/
---
## Introduktion
OneNote är ett kraftfullt verktyg för att organisera information, och Aspose.Note för Java förbättrar dess kapacitet genom att tillhandahålla ett sömlöst sätt att skapa tabeller med låsta kolumner. I den här handledningen kommer vi att guida dig genom processen att använda Aspose.Note för Java för att skapa en tabell med låsta kolumner i OneNote.
## Förutsättningar
Innan du börjar, se till att du har följande förutsättningar på plats:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)installerat på din maskin.
- [Aspose.Note för Java](https://downloads.aspose.com/note/java) biblioteket har laddats ner och lagts till i ditt projekt.
## Importera paket
I ditt Java-projekt, importera de nödvändiga paketen för att arbeta med Aspose.Note:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Steg 1: Konfigurera ditt projekt
Börja med att skapa ett nytt Java-projekt och lägga till Aspose.Note-biblioteket i din klassväg. Se till att ditt projekt är konfigurerat för att använda JDK.
## Steg 2: Initiera dokument- och sidobjekt
```java
// Sökvägen till dokumentkatalogen.
String dataDir = "Your Document Directory";
//Skapa ett objekt av klassen Document
Document doc = new Document();
// Initiera Sidklassobjekt
Page page = new Page();
```
## Steg 3: Skapa tabellrader och celler
```java
// Initiera TableRow-klassobjekt
TableRow row1 = new TableRow();
// Initiera TableCell-klassobjekt och ställ in textinnehåll
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initiera TableRow-klassobjekt
TableRow row2 = new TableRow();
// Initiera TableCell-klassobjekt och ställ in textinnehåll
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Steg 4: Skapa och anpassa tabellen
```java
// Initiera Table-klassobjekt
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Lägg till rader
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Steg 5: Lägg till tabell till disposition och sida
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Lägg till tabellnod
outlineElem.appendChildLast(table);
// Lägg till konturelementnod
outline.appendChildLast(outlineElem);
// Lägg till konturnod
page.appendChildLast(outline);
// Lägg till sidnod
doc.appendChildLast(page);
```
## Steg 6: Spara dokumentet
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Grattis! Du har framgångsrikt skapat en tabell med låsta kolumner i OneNote med Aspose.Note för Java.
## Slutsats
den här handledningen utforskade vi processen att använda Aspose.Note för Java för att förbättra din OneNote-upplevelse genom att skapa tabeller med låsta kolumner. Den här funktionen lägger till ett nytt lager av organisation och struktur till dina anteckningar.
## Vanliga frågor
### Är Aspose.Note for Java kompatibel med alla Java-versioner?
Ja, Aspose.Note för Java är kompatibel med Java 6 och senare versioner.
### Kan jag anpassa utseendet på bordet ytterligare?
Absolut! Aspose.Note för Java tillhandahåller omfattande alternativ för att anpassa tabeller, som att justera kanter, cellavstånd och mer.
### Finns det en testversion innan köp?
 Jo det kan du[ladda ner en gratis testversion](https://releases.aspose.com/) för att utforska funktionerna i Aspose.Note för Java.
### Var kan jag hitta ytterligare stöd eller diskussioner i samhället?
 Besök[Aspose.Note forum](https://forum.aspose.com/c/note/28) för stöd och samhällsdiskussioner.
### Hur kan jag få en tillfällig licens för Aspose.Note för Java?
 Besök[den här länken](https://purchase.aspose.com/temporary-license/) för att få en tillfällig licens för teständamål.