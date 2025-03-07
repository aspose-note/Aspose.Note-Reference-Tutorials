---
title: Få information om sidor i OneNote - Aspose.Note
linktitle: Få information om sidor i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Upptäck sidhemligheter i dina OneNote-dokument! Extrahera revisioner, skapelsetider och mer med Aspose.Note. Steg-för-steg guide & kod ingår! #OneNote #Java #Aspose
weight: 12
url: /sv/java/onenote-page-manipulation/get-information-about-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Få information om sidor i OneNote - Aspose.Note

## Introduktion

den här handledningen kommer vi att guida dig genom processen att extrahera information om sidor i OneNote med Aspose.Note för Java. Aspose.Note är ett kraftfullt API som låter dig arbeta med Microsoft OneNote-dokument programmatiskt. Oavsett om du behöver komma åt sidrevisioner, skapelsetider, titlar eller författare, förenklar Aspose.Note uppgiften med sitt intuitiva gränssnitt.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. Java Development Kit (JDK): Se till att du har JDK installerat på ditt system.
2.  Aspose.Note for Java: Ladda ner och installera Aspose.Note for Java-biblioteket. Du kan få det från[hemsida](https://purchase.aspose.com/buy).
3. Exempel på OneNote-dokument: Förbered ett exempel på OneNote-dokument som du ska använda för att hämta information från.

## Importera paket

Först måste du importera de nödvändiga paketen för att arbeta med Aspose.Note i ditt Java-projekt.

```java
import java.io.IOException;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Steg 1: Ladda OneNote-dokumentet

Börja med att ladda OneNote-dokumentet med Aspose.Note.

```java
String dataDir = "Your Document Directory";
// Ladda dokumentet i Aspose.Note
LoadOptions options = new LoadOptions();
Document doc = new Document(dataDir + "Sample1.one", options);
```

 Byta ut`"Your Document Directory"` med sökvägen till ditt OneNote-dokument.

## Steg 2: Hämta sidinformation

Hämta sedan information om sidorna i OneNote-dokumentet.

```java
// Få sidarevisioner
List<Page> pages = doc.getChildNodes(Page.class);

// Gå igenom sidorna
for (Page pageRevision : pages) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
}
```

Detta kodavsnitt itererar genom varje sida i dokumentet och skriver ut information som senast ändrade tidpunkt, skapelsetid, titel, nivå och författare till varje sida.

## Slutsats

I den här handledningen lärde du dig hur du hämtar information om sidor i OneNote med Aspose.Note för Java. Genom att följa stegen som beskrivs ovan kan du sömlöst integrera Aspose.Note i dina Java-applikationer för att extrahera värdefull data från OneNote-dokument.

## FAQ's

### F1: Kan jag använda Aspose.Note för Java för att redigera OneNote-dokument?

S1: Ja, Aspose.Note tillhandahåller en omfattande uppsättning funktioner för att redigera och manipulera OneNote-dokument programmatiskt.

### F2: Är Aspose.Note kompatibel med alla versioner av OneNote?

S2: Aspose.Note stöder olika versioner av OneNote, vilket säkerställer kompatibilitet mellan olika miljöer.

### F3: Kan jag konvertera OneNote-dokument till andra format med Aspose.Note?

S3: Absolut, Aspose.Note låter dig konvertera OneNote-dokument till format som PDF, HTML och bilder utan ansträngning.

### F4: Erbjuder Aspose.Note teknisk support till utvecklare?

S4: Ja, Aspose tillhandahåller dedikerad teknisk support för att hjälpa utvecklare med alla problem de stöter på när de använder Aspose.Note.

### F5: Finns det en testversion tillgänglig för Aspose.Note för Java?

 S5: Ja, du kan ladda ner en gratis testversion av Aspose.Note för Java från[här](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
