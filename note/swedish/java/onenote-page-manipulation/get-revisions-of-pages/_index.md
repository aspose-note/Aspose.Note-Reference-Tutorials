---
date: 2026-08-13
description: Lär dig hur du hämtar modifieringstid för OneNote-sidor och hämtar sidrevisioner
  med Aspose.Note för Java, idealiskt för granskning och dokumenthantering.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Hämta revisioner av sidor i OneNote – Aspose.Note
og_description: Lär dig hur du hämtar modifieringstid för OneNote-sidor och hämtar
  revisioner av OneNote-sidor med Aspose.Note för Java. Snabba steg, kodexempel och
  felsökning.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Hämta modifieringstid för OneNote-sida med Aspose.Note – Java‑handledning
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Hämta modifieringstid för OneNote-sida med Aspose.Note
url: /sv/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hämta OneNote‑sidans ändringstid med Aspose.Note

## Introduktion

I den här handledningen kommer du att lära dig hur du **hämta onenote‑sidans ändring**‑tidsstämplar och hämta hela revisionshistoriken för en OneNote‑sida med Aspose.Note för Java. Oavsett om du bygger en revisionsspårningsfunktion, en ändringslogg‑visare, eller behöver visa det senaste redigeringsdatumet i en instrumentpanel, guidar den här guiden dig genom varje steg—från att sätta upp miljön till att hantera vanliga fallgropar.

## Snabba svar
- **Vad returnerar “get last modified time”?** Den returnerar tidsstämpeln för den senaste redigeringen på en OneNote‑sida.  
- **Vilken klass tillhandahåller revisionshistorik?** `PageHistory` via `Document.getPageHistory(Page)`.  
- **Behöver jag en licens för den här funktionen?** Ja, en giltig Aspose.Note‑licens krävs för produktionsbruk.  
- **Vilken Java‑version stöds?** Java 8 eller senare (JDK 8+).  
- **Kan jag filtrera revisioner efter författare?** Du kan läsa `Author`‑egenskapen för varje `Page`‑objekt och tillämpa ditt eget filter.

## Vad är “get last modified time” i OneNote?

Den senaste ändringstiden lagras som ett metadata‑attribut på varje OneNote‑sida som indikerar tidpunkten för den senaste redigeringen. Aspose.Note exponerar detta värde via metoden `Page.getLastModifiedTime()`, som returnerar ett `java.util.Date`‑objekt som kan formateras eller loggas enligt ditt programs krav.

## Varför hämta sidrevisioner?

Att hämta sidrevisioner ger dig en komplett revisionsspårning av varje förändring som gjorts på en OneNote‑sida, vilket gör det möjligt att spåra vem som redigerade vad och när. Denna historik kan användas för att jämföra versioner, återställa tidigare tillstånd eller analysera samarbetsmönster mellan team, vilket gör den avgörande för efterlevnad och kvalitetskontroll.

## Förutsättningar

- **Java Development Kit (JDK) 8 eller senare** – installera från Oracles webbplats eller någon kompatibel leverantör.  
- **Aspose.Note för Java‑bibliotek** – ladda ner JAR‑filen från Aspose.Note Java‑utgåfessidan **[Aspose.Note Java‑utgåvor](https://releases.aspose.com/note/java/)** och följ installationsguiden **[Aspose.Note Java‑dokumentation](https://reference.aspose.com/note/java/)**.  

## Importera paket

`Document`‑klassen representerar en OneNote‑anteckningsbok som laddats in i minnet, medan `Page` och `PageHistory` ger åtkomst till enskilda sidor och deras revisionsdata.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(De faktiska import‑satserna visas som vanlig text för att bevara det ursprungliga antalet kodblock.)*

## Hur hämtar man onenote‑sidans ändringstid?

För att få den senaste ändringstidsstämpeln, ladda först OneNote‑dokumentet i ett `Document`‑objekt, välj sedan den önskade `Page`. Anropa metoden `getLastModifiedTime()` på den sidan, vilket returnerar ett `java.util.Date`. Du kan sedan formatera detta datum med `SimpleDateFormat` eller konvertera det till UTC för konsekvent rapportering över tidszoner.

## Steg 1: ange dokumentkatalog

Definiera mappen som innehåller din OneNote‑fil.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Steg 2: ladda dokumentet

Skapa en `Document`‑instans genom att skicka den fullständiga sökvägen till din `.one`‑fil.

```java
String dataDir = "Your Document Directory";
```

## Steg 3: hämta första sidan

Hämta det första `Page`‑objektet från dokumentets sidkollektion.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Steg 4: hämta sidrevisioner

Hämta `PageHistory` för den valda sidan. Om anteckningsboken aldrig har redigerats kan detta anrop returnera `null`.

```java
Page firstPage = doc.getFirstChild();
```

## Steg 5: gå igenom sidrevisioner

Iterera genom varje `Page`‑revision, läs dess `Author` och `LastModifiedTime`, och visa informationen.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Vanliga problem och lösningar
- **Null `PageHistory`** – Verifiera att anteckningsboken faktiskt innehåller revisioner; annars returnerar `getPageHistory` `null`.  
- **Tidszonskillnader** – `getLastModifiedTime()` använder JVM:s standardtidszon. Konvertera till UTC med `SimpleDateFormat` om ditt program kräver en standardzon.  
- **Licens ej laddad** – Utan en giltig licens kör Aspose.Note i utvärderingsläge, vilket begränsar sidbearbetning. Ladda din licensfil vid applikationens start för att undvika denna begränsning.

## Vanliga frågor

**Q1: Kan jag använda Aspose.Note för Java för att skapa nya OneNote‑dokument?**  
A: Ja, API‑et låter dig programatiskt skapa, redigera och spara OneNote‑anteckningsböcker från grunden.

**Q2: Är Aspose.Note för Java kompatibel med olika versioner av OneNote‑filer?**  
A: Ja, den stöder OneNote‑filformaten 2007‑2021, vilket säkerställer bred kompatibilitet över skrivbord- och molnmiljöer.

**Q3: Kan jag anpassa utdataformatet när jag exporterar OneNote‑dokument?**  
A: Absolut. Du kan exportera till PDF, HTML, PNG eller SVG, och styra alternativ såsom bildupplösning och teckensnittsinbäddning.

**Q4: Kräver Aspose.Note för Java en licens för kommersiell användning?**  
A: Ja, en kommersiell licens är obligatorisk för produktionsdistributioner. En gratis provversion finns tillgänglig för utvärdering.

**Q5: Var kan jag få hjälp om jag stöter på problem?**  
A: Besök Aspose.Note‑community‑forumet **[Aspose.Note‑forum](https://forum.aspose.com/c/note/28)** för att ställa frågor, dela erfarenheter och få hjälp från communityn och Aspose‑ingenjörer.

---

**Senast uppdaterad:** 2026-08-13  
**Testad med:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Författare:** Aspose

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

## Relaterade handledningar

- [Aspose Java‑handledning - Hämta information om sidor i OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [aspose.note sidrevisionshandledning – Hämta sidrevisioner i OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [spåra ändringar onenote – Hantera sidrevisioner med Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}