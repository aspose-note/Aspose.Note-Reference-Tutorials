---
title: Få versioner av sidor i OneNote - Aspose.Note
linktitle: Få versioner av sidor i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du hämtar versioner av sidor i OneNote-dokument med Aspose.Note Java. Integrera detta i dina Java-appar för effektiv dokumenthantering.
weight: 15
url: /sv/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Få versioner av sidor i OneNote - Aspose.Note

## Introduktion

den här handledningen kommer vi att fördjupa oss i funktionerna i Aspose.Note för Java, ett kraftfullt bibliotek som gör att du kan arbeta med Microsoft OneNote-filer sömlöst i dina Java-applikationer. Specifikt kommer vi att fokusera på hur man hämtar revisioner av sidor i ett OneNote-dokument. I slutet av den här guiden kommer du att vara utrustad med kunskapen för att effektivt extrahera sidrevisioner, inklusive detaljer som senast ändrade tid, skapande, titel, nivå och författare.

## Förutsättningar

Innan du dyker in i den här handledningen, se till att du har följande förutsättningar inställda:

### Java Development Kit (JDK) installerat

Se till att du har Java Development Kit installerat på ditt system. Du kan ladda ner och installera det från Oracles webbplats eller använda en pakethanterare om du använder ett Unix-baserat system.

### Aspose.Note för Java Library

 Ladda ner och installera Aspose.Note för Java-biblioteket från webbplatsen. Du hittar nedladdningslänken[här](https://releases.aspose.com/note/java/) . Följ installationsinstruktionerna i dokumentationen[här](https://reference.aspose.com/note/java/).

## Importera paket

För att börja, importera de nödvändiga paketen till ditt Java-projekt. Dessa paket låter dig utnyttja funktionaliteten som tillhandahålls av Aspose.Note för Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Låt oss nu dela upp exempelkoden som tillhandahålls i flera steg för att förstå varje komponent och dess funktionalitet.

## Steg 1: Ställ in dokumentkatalog

Definiera katalogen där ditt OneNote-dokument finns.

```java
String dataDir = "Your Document Directory";
```

## Steg 2: Ladda dokumentet

Ladda OneNote-dokumentet i Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Steg 3: Skaffa första sidan

Hämta den första sidan från dokumentet.

```java
Page firstPage = doc.getFirstChild();
```

## Steg 4: Skaffa sidrevisioner

Skaffa sidans versionshistorik.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Steg 5: Gå igenom sidrevisioner

Gå igenom listan med sidrevisioner och hämta relevant information.

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Slutsats

I den här handledningen har vi utforskat hur man hämtar versioner av sidor i ett OneNote-dokument med Aspose.Note för Java. Genom att följa den steg-för-steg-guide och använda den medföljande exempelkoden kan du enkelt integrera denna funktion i dina Java-applikationer, vilket möjliggör effektiv hantering av OneNote-filer.

## FAQ's

### F1: Kan jag använda Aspose.Note för Java för att skapa nya OneNote-dokument?

S1: Ja, Aspose.Note för Java ger omfattande stöd för att skapa, läsa och manipulera OneNote-dokument programmatiskt.

### F2: Är Aspose.Note för Java kompatibel med olika versioner av OneNote-filer?

S2: Ja, Aspose.Note för Java stöder olika versioner av Microsoft OneNote-filer, vilket säkerställer kompatibilitet mellan olika miljöer.

### F3: Kan jag anpassa utdataformatet när jag exporterar OneNote-dokument?

S3: Absolut, Aspose.Note för Java erbjuder flexibilitet vid export av OneNote-dokument till olika format som PDF, HTML och bilder, med alternativ för anpassning.

### F4: Kräver Aspose.Note för Java en licens för kommersiellt bruk?

S4: Ja, en giltig licens krävs för kommersiell användning av Aspose.Note för Java. Du kan få en licens från Asposes webbplats.

### F5: Var kan jag söka hjälp om jag stöter på problem eller har frågor om Aspose.Note för Java?

 S5: För support och hjälp kan du besöka Aspose.Note-forumet[här](https://forum.aspose.com/c/note/28)där du kan ställa frågor, dela erfarenheter och interagera med andra användare och experter.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
