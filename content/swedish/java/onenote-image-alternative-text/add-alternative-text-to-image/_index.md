---
title: Lägg till alternativ text till bild i OneNote med Java
linktitle: Lägg till alternativ text till bild i OneNote med Java
second_title: Aspose.Note Java API
description: Lär dig hur du lägger till alternativ text till bilder i OneNote-dokument med Java med Aspose.Note, vilket förbättrar tillgängligheten och inkluderingen.
type: docs
weight: 10
url: /sv/java/onenote-image-alternative-text/add-alternative-text-to-image/
---
## Introduktion

I den här handledningen kommer vi att fördjupa oss i en omfattande guide om hur du använder Aspose.Note för Java för att lägga till alternativ text till bilder i OneNote-dokument. Alternativ text fungerar som en textbeskrivning av bilder, vilket underlättar tillgänglighet och förståelse för individer som kanske inte kan se bilder direkt, till exempel de som använder skärmläsare. Genom att följa den här handledningen lär du dig hur du sömlöst integrerar alternativ text i dina OneNote-dokument med hjälp av programmeringsspråket Java.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar:

1. Java Development Kit (JDK): Se till att du har JDK installerat på ditt system.
2.  Aspose.Note for Java Library: Ladda ner och installera Aspose.Note for Java-biblioteket från[här](https://releases.aspose.com/note/java/).
3. Integrated Development Environment (IDE): Ha en IDE som IntelliJ IDEA eller Eclipse inställd för Java-utveckling.
4. Grundläggande kunskaper om Java-programmering: Bekanta dig med grundläggande Java-programmeringskoncept.

## Importera paket

Först måste du importera de nödvändiga paketen till ditt Java-projekt för att använda Aspose.Note-funktionerna.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;
```

Låt oss nu dela upp processen att lägga till alternativ text till en bild i ett OneNote-dokument med hjälp av Java och Aspose.Note i steg-för-steg-instruktioner.

## Steg 1: Konfigurera dokumentkatalog

```java
String dataDir = "Your Document Directory";
```

 Se till att byta ut`"Your Document Directory"` med sökvägen till din dokumentkatalog.

## Steg 2: Skapa ett dokumentobjekt

```java
Document document = new Document();
```

Skapa en ny instans av klassen Document.

## Steg 3: Skapa ett sidobjekt

```java
Page page = new Page();
```

Skapa en ny instans av klassen Page.

## Steg 4: Lägg till en bild på sidan

```java
Image image = new Image(null, dataDir + "image.jpg");
```

Skapa en instans av klassen Image och skicka bildfilens sökväg som en parameter.

## Steg 5: Ställ in alternativ texttitel

```java
image.setAlternativeTextTitle("ImageAlternativeText Title");
```

Ställ in den alternativa texttiteln för bilden.

## Steg 6: Ställ in alternativ textbeskrivning

```java
image.setAlternativeTextDescription("ImageAlternativeText Description");
```

Ställ in den alternativa textbeskrivningen för bilden.

## Steg 7: Lägg till bild på sidan

```java
page.appendChildLast(image);
```

Lägg till bilden på sidan.

## Steg 8: Lägg till sida till dokumentet

```java
document.appendChildLast(page);
```

Lägg till sidan i dokumentet.

## Steg 9: Spara dokument

```java
document.save(dataDir + "AlternativeText_out.one");
```

Spara det ändrade dokumentet med alternativ text till bilden.

## Slutsats

I den här handledningen har vi utforskat hur man kan förbättra tillgängligheten för OneNote-dokument genom att lägga till alternativ text till bilder med Java med Aspose.Note. Genom att följa den steg-för-steg-guide som beskrivs ovan kan du säkerställa att dina dokument är mer inkluderande och tillgängliga för en bredare publik.

## FAQ's

### F1: Kan jag lägga till alternativ text till flera bilder i ett enda dokument?

S1: Ja, du kan lägga till alternativ text till flera bilder genom att iterera genom varje bild och ställa in alternativ text därefter.

### F2: Är Aspose.Note kompatibel med olika bildformat?

S2: Ja, Aspose.Note stöder olika bildformat som JPEG, PNG, GIF, etc.

### F3: Kan alternativ text redigeras eller tas bort när den väl har lagts till i en bild?

S3: Ja, du kan redigera eller ta bort alternativ text från en bild genom att ändra respektive egenskaper.

### F4: Ger Aspose.Note stöd för andra programmeringsspråk förutom Java?

S4: Ja, Aspose.Note är tillgängligt för flera programmeringsspråk inklusive .NET, C++, och Python.

### F5: Finns det en testversion tillgänglig för Aspose.Note?

 S5: Ja, du kan använda en gratis testversion av Aspose.Note från[här](https://releases.aspose.com/).