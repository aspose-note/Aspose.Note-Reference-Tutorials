---
title: Skaffa sidrevisioner i OneNote - Aspose.Note
linktitle: Skaffa sidrevisioner i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du hämtar sidversioner i OneNote med Aspose.Note för Java. Följ vår steg-för-steg-guide för effektiv spårning av ändringar.
weight: 14
url: /sv/java/onenote-page-manipulation/get-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skaffa sidrevisioner i OneNote - Aspose.Note

## Introduktion

OneNote är ett kraftfullt verktyg för att organisera och hantera dina anteckningar, men ibland behöver du spåra ändringar och revideringar som görs på dina sidor. Med Aspose.Note för Java kan du enkelt hämta sidrevisioner programmatiskt. I den här handledningen guidar vi dig genom processen för att få sidrevisioner i OneNote med Aspose.Note för Java.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar på plats:

### 1. Java Development Kit (JDK)

Se till att du har Java Development Kit (JDK) installerat på ditt system. Du kan ladda ner och installera JDK från Oracles webbplats.

### 2. Aspose.Note för Java

Ladda ner och installera Aspose.Note för Java från[nedladdningslänk](https://releases.aspose.com/note/java/).

### 3. Exempel på OneNote-dokument

Förbered ett exempel på OneNote-dokument (`Sample1.one`) som innehåller de sidor du vill hämta versioner från.

## Importera paket

Först måste du importera de nödvändiga paketen från Aspose.Note för Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Låt oss nu dela upp exemplet i flera steg:

## Steg 1: Konfigurera dokumentkatalog

Definiera katalogsökvägen där ditt OneNote-dokument finns.

```java
String dataDir = "Your Document Directory";
```

## Steg 2: Ladda OneNote-dokument

 Ladda OneNote-dokumentet med`LoadOptions` för att aktivera laddningshistorik.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Steg 3: Skaffa första sidan

Hämta den första sidan från det laddade dokumentet.

```java
Page firstPage = document.getFirstChild();
```

## Steg 4: Iterera genom sidrevisioner

Gå igenom varje sidrevision och hämta relevant information som senast ändrade tidpunkt, skapelsetid, titel, nivå och författare.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Slutsats

I den här handledningen har vi lärt oss hur man hämtar sidversioner i OneNote med Aspose.Note för Java. Genom att följa dessa steg kan du effektivt spåra ändringar som görs på dina OneNote-sidor programmatiskt.

## FAQ's

### F1: Kan jag använda Aspose.Note för Java för att ändra sidversioner?

S1: Nej, Aspose.Note för Java stöder för närvarande hämtning av sidversioner men inte modifiering av dem.

### F2: Är Aspose.Note för Java kompatibelt med olika versioner av OneNote-dokument?

S2: Ja, Aspose.Note för Java stöder olika versioner av OneNote-dokument, vilket gör att du kan arbeta med olika filformat sömlöst.

### F3: Kräver Aspose.Note för Java en licens för att kunna användas?

S3: Ja, du måste köpa en licens för att använda Aspose.Note för Java i kommersiella projekt. Men du kan också få en tillfällig licens för utvärderingsändamål.

### F4: Kan jag söka support om jag stöter på några problem när jag använder Aspose.Note för Java?

 S4: Ja, du kan söka stöd från Aspose.Note-forumet[här](https://forum.aspose.com/c/note/28).

### F5: Finns det en gratis testversion tillgänglig för Aspose.Note för Java?

 S5: Ja, du kan få tillgång till en gratis testversion av Aspose.Note för Java från[hemsida](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
