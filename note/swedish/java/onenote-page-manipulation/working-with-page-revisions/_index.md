---
date: 2026-01-15
description: Lär dig hur du spårar ändringar i OneNote och hanterar sidrevisioner
  i OneNote‑dokument med Aspose.Note för Java. Inkluderar ett exempel på revisionssammanfattning
  och hur du ändrar revisionsdatum.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Spåra ändringar i OneNote – Hantera sidrevisioner med Aspose.Note
url: /sv/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Arbeta med sidrevisioner i OneNote - Aspose.Note

## Introduktion

OneNote är ett kraftfullt verktyg för att organisera anteckningar, och när du behöver **track changes onenote** blir hantering av sidrevisioner avgörande för effektivt samarbete. Med Aspose.Note för Java kan du programatiskt hantera revisioner, visa vem som redigerade en sida och till och med justera tidsstämplar. Denna handledning guidar dig genom varje steg, från att ladda ett dokument till att uppdatera revisionssammanfattningen.

## Snabba svar
- **Vad betyder “track changes onenote”?** Det hänvisar till att övervaka vem som redigerade en OneNote-sida och när.
- **Vilket bibliotek krävs?** Aspose.Note för Java.
- **Kan jag ändra författare eller datum för en revision?** Ja, med RevisionSummary API (`modify revision date`).
- **Behöver jag en OneNote-fil i förväg?** Ja, en exempel `.one`-fil krävs.
- **Behövs en licens för produktion?** En giltig Aspose.Note-licens krävs för kommersiell användning.

## Vad är ett exempel på revisionssammanfattning?
*revision summary* ger metadata om de senaste ändringarna på en sida — författarnamn, senast ändrad tid och andra detaljer. I den här guiden kommer vi att hämta och visa den informationen, och sedan visa hur man **modify revision date**.

## Varför spåra ändringar onenote med Aspose.Note?
- **Samarbete:** Se snabbt vem som gjort de senaste redigeringarna.
- **Revision:** Behåll en pålitlig historik över ändringar för efterlevnad.
- **Automation:** Integrera revisionshantering i back‑end‑tjänster eller migrationsverktyg.

## Förutsättningar

### Java Development Environment
Se till att du har Java Development Kit (JDK) installerat på ditt system.

### Aspose.Note for Java Library
Ladda ner och installera Aspose.Note för Java-biblioteket från [here](https://releases.aspose.com/note/java/).

### OneNote Document
Ha ett exempel på OneNote-dokument redo för teständamål.

## Importera paket

I ditt Java-projekt, importera de nödvändiga paketen för att arbeta med Aspose.Note för Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Låt oss bryta ner det medföljande exemplet i flera steg för en tydlig förståelse.

## Steg 1: Ladda OneNote-dokument

Först, ladda OneNote-dokumentet och hämta den första underordnade sidan.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Steg 2: Läs sidans revisionssammanfattning

Läs innehållsrevisionssammanfattningen för sidan. Detta är **revision summary example** som visar vem som senast redigerade sidan.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Steg 3: Uppdatera sidans revisionssammanfattning

Uppdatera sidans revisionssammanfattning med en ny författare och ett nytt ändringsdatum. Detta demonstrerar hur man **modify revision date** programatiskt.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Slutsats

Att hantera sidrevisioner i OneNote-dokument programatiskt kan förenklas med Aspose.Note för Java. Genom att följa stegen som beskrivs i den här handledningen kan du effektivt **track changes onenote**, visa revisionsdetaljer och till och med **modify revision date** för att passa ditt arbetsflöde.

## Vanliga frågor

### Q1: Kan jag använda Aspose.Note för Java med andra Java-bibliotek?

A: Ja, Aspose.Note för Java kan integreras med andra Java-bibliotek för att förbättra funktionaliteten.

### Q2: Stöder Aspose.Note för Java alla versioner av OneNote-dokument?

A: Aspose.Note för Java stöder olika versioner av OneNote-dokument, inklusive äldre versioner.

### Q3: Är Aspose.Note för Java lämplig för företagsapplikationer?

A: Absolut, Aspose.Note för Java är utformat för att möta behoven hos företagsapplikationer med robusta funktioner och skalbarhet.

### Q4: Kan jag anpassa sidrevisioner med Aspose.Note för Java?

A: Ja, du kan anpassa sidrevisioner enligt dina krav med Aspose.Note för Java.

### Q5: Var kan jag få support för Aspose.Note för Java?

A: Du kan få support för Aspose.Note för Java från [Aspose.Note forum](https://forum.aspose.com/c/note/28).

---

**Last Updated:** 2026-01-15  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}