---
title: Skriv tabell i OneNote - Aspose.Note
linktitle: Skriv tabell i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du komponerar tabeller i OneNote programmatiskt med Aspose.Note för Java. Steg-för-steg-guide för effektivt dokumentskapande.
type: docs
weight: 11
url: /sv/java/onenote-table-manipulation/compose-table/
---
## Introduktion
dagens konkurrensutsatta affärsmiljö är effektiv kommunikation och samarbete nyckelfaktorer för att nå framgång. Aspose.Note för Java tillhandahåller en kraftfull lösning för att skapa och manipulera OneNote-dokument programmatiskt. I den här handledningen kommer vi att utforska hur man komponerar tabeller i OneNote med Aspose.Note för Java. Följ steg-för-steg-guiden nedan för att förbättra din process för att skapa dokument.
## Förutsättningar
Innan du dyker in i handledningen, se till att du har följande förutsättningar:
- Grundläggande kunskaper i Java-programmering.
-  Aspose.Note för Java-biblioteket installerat. Du kan ladda ner den från[här](https://releases.aspose.com/note/java/).
- En integrerad utvecklingsmiljö (IDE) inrättad för Java-utveckling.
## Importera paket
Se till att importera de nödvändiga paketen för att kickstarta ditt projekt. Lägg till följande importsatser till din Java-klass:
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.stream.StreamSupport;
```
## Steg 1: Ställ in dokumentkatalog
```java
String dataDir = "Your Document Directory";
```
Se till att ersätta "Din dokumentkatalog" med den faktiska sökvägen där du vill spara ditt OneNote-dokument.
## Steg 2: Skriv rubrik
```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```
Skapa en iögonfallande rubrik för ditt dokument. Justera teckenstorlek, djärvhet och justering efter behov.
## Steg 3: Skapa sida och disposition
```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```
Skapa en ny sida och disposition och lägg sedan till den tidigare skapade rubriken till dispositionen.
## Steg 4: Lägg till sammanfattningstext
```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```
Inkludera en kort sammanfattningstext för att skapa sammanhang för tabellen.
## Steg 5: Skriv tabell
```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
// Återstående steg är involverade i att ställa in tabellstrukturen, rubrikraden och lägga till tomma rader.
// Se den medföljande koden för detaljerad implementering.
```
Komponera tabellstrukturen och fyll i den med relevant information. Den medföljande koden inkluderar att lägga till kolumner, rubrikrad, tomma rader och mallinnehåll för kolumnen "Kontakter".
## Steg 6: Spara dokument
```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```
Spara ditt sammansatta dokument med ett angivet filnamn och katalogsökväg.
## Slutsats
Grattis! Du har framgångsrikt skapat en tabell i OneNote med Aspose.Note för Java. Denna handledning demonstrerade steg-för-steg-processen, vilket ger dig möjlighet att förbättra dina dokumentskapande möjligheter programmatiskt.
## Vanliga frågor
### F: Var kan jag hitta dokumentationen för Aspose.Note för Java?
 Du kan hänvisa till dokumentationen[här](https://reference.aspose.com/note/java/).
### F: Hur laddar jag ner Aspose.Note för Java?
 Du kan ladda ner den från[den här länken](https://releases.aspose.com/note/java/).
### F: Finns det en gratis provperiod?
 Ja, du kan komma åt den kostnadsfria provperioden[här](https://releases.aspose.com/).
### F: Var kan jag få support för Aspose.Note för Java?
 Besök supportforumet[här](https://forum.aspose.com/c/note/28).
### F: Kan jag få en tillfällig licens?
 Ja, du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).