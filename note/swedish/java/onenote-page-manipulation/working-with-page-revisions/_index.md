---
title: Arbeta med sidrevisioner i OneNote - Aspose.Note
linktitle: Arbeta med sidrevisioner i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du hanterar sidrevisioner i OneNote-dokument med Aspose.Note för Java. Ger en steg-för-steg-guide för effektiv revisionsspårning och samarbete.
type: docs
weight: 21
url: /sv/java/onenote-page-manipulation/working-with-page-revisions/
---
## Introduktion

OneNote är ett kraftfullt verktyg för att organisera och hantera anteckningar, men ibland måste du arbeta med revisioner för att spåra ändringar och samarbeta effektivt. Med Aspose.Note för Java kan du enkelt hantera sidrevisioner i OneNote-dokument programmatiskt. Denna handledning guidar dig genom processen steg för steg.

## Förutsättningar

Innan du börjar, se till att du har följande:

### Java utvecklingsmiljö

Se till att du har Java Development Kit (JDK) installerat på ditt system.

### Aspose.Note för Java Library

Ladda ner och installera Aspose.Note för Java-biblioteket från[här](https://releases.aspose.com/note/java/).

### OneNote-dokument

Ha ett exempel på OneNote-dokument redo för teständamål.

## Importera paket

I ditt Java-projekt, importera de nödvändiga paketen för att fungera med Aspose.Note för Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Låt oss dela upp exemplet i flera steg för en tydlig förståelse.

## Steg 1: Ladda OneNote-dokument

Ladda först OneNote-dokumentet och hämta den första underordnade sidan.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Steg 2: Läs sammanfattningen av sidrevision

Läs sammanfattningen av innehållsrevisionen för sidan.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Steg 3: Uppdatera sammanfattning av sidrevision

Uppdatera sidans revisionssammanfattning med ny författare och ändrat datum.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Slutsats

Hantera sidrevisioner i OneNote-dokument programmatiskt kan förenklas med Aspose.Note för Java. Genom att följa stegen som beskrivs i den här handledningen kan du effektivt arbeta med sidrevisioner för att spåra ändringar och samarbeta sömlöst.

## FAQ's

### F1: Kan jag använda Aspose.Note för Java med andra Java-bibliotek?

S: Ja, Aspose.Note för Java kan integreras med andra Java-bibliotek för att förbättra funktionaliteten.

### F2: Stöder Aspose.Note för Java alla versioner av OneNote-dokument?

S: Aspose.Note för Java stöder olika versioner av OneNote-dokument, inklusive äldre versioner.

### F3: Är Aspose.Note för Java lämplig för applikationer på företagsnivå?

S: Absolut, Aspose.Note för Java är designad för att möta behoven hos applikationer på företagsnivå med robusta funktioner och skalbarhet.

### F4: Kan jag anpassa sidversioner med Aspose.Note för Java?

S: Ja, du kan anpassa sidversioner enligt dina krav med Aspose.Note för Java.

### F5: Var kan jag få support för Aspose.Note för Java?

 S: Du kan få support för Aspose.Note för Java från[Aspose.Note forum](https://forum.aspose.com/c/note/28).