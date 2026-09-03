---
date: 2026-01-10
description: Lär dig hur du får fram den senaste ändringstiden och hämtar revisioner
  av OneNote‑sidor med Aspose.Note för Java. Integrera detta i dina Java‑appar för
  effektiv dokumenthantering.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Hur man får den senaste ändringstiden för OneNote‑sidor – Aspose.Note
url: /sv/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hämta revisioner av sidor i OneNote - Aspose.Note

## Introduktion

I den här handledningen kommer du **hämta senaste ändringstid** för sidor i ett OneNote-dokument och utforska hur du hämtar hela revisionshistoriken med Aspose.Note för Java. Oavsett om du bygger ett dokumenthanteringssystem, granskar ändringar eller helt enkelt behöver visa när en sida senast redigerades, visar den här guiden exakt hur du extraherar den informationen programmässigt.

## Snabba svar
- **Vad returnerar “get last modified time”?** Tidsstämpeln för den senaste redigeringen på en OneNote-sida.  
- **Vilken klass tillhandahåller revisionshistorik?** `PageHistory` via `Document.getPageHistory(Page)`.  
- **Behöver jag en licens för den här funktionen?** Ja, en giltig Aspose.Note-licens krävs för produktionsanvändning.  
- **Vilken Java-version stöds?** Java 8 eller högre (JDK 8+).  
- **Kan jag filtrera revisioner efter författare?** Du kan läsa `Author`-egenskapen för varje `Page`-objekt och tillämpa ditt eget filter.

## Vad är “get last modified time” i OneNote?

**Senaste ändringstid** är ett metadatafält som lagras med varje sida och registrerar när sidan senast ändrades. Aspose.Note exponerar detta värde via metoden `Page.getLastModifiedTime()`, vilket gör det enkelt att visa eller logga ändringsdatum.

## Varför hämta sidrevisioner?

- **Revisionsspår:** Behåll en register över vem som ändrade vad och när.  
- **Version jämförelse:** Bygg funktioner som jämför två revisioner sida‑vid‑sida.  
- **Insikter om användarsamarbete:** Förstå redigeringsmönster i delade anteckningsböcker.  

## Förutsättningar

Innan du börjar, se till att du har följande:

### Java Development Kit (JDK) installerat
Installera JDK 8 eller senare från Oracles webbplats eller din föredragna paketmanager.

### Aspose.Note för Java-biblioteket
Ladda ner biblioteket från den officiella webbplatsen. Du kan hitta nedladdningslänken **[here](https://releases.aspose.com/note/java/)**. Följ installationsinstruktionerna i dokumentationen **[here](https://reference.aspose.com/note/java/)**.

## Importera paket

För att börja, importera de nödvändiga paketen till ditt Java-projekt. Dessa paket gör att du kan utnyttja funktionaliteten som tillhandahålls av Aspose.Note för Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Låt oss nu bryta ner det medföljande exempelprogrammet i flera steg för att förstå varje komponent och dess funktionalitet.

## Hur man hämtar senaste ändringstid för en OneNote-sida

### Steg 1: Ange dokumentkatalog
Definiera katalogen där ditt OneNote-dokument finns.

```java
String dataDir = "Your Document Directory";
```

### Steg 2: Ladda dokumentet
Ladda OneNote-dokumentet i Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Steg 3: Hämta första sidan
Hämta den första sidan från dokumentet.

```java
Page firstPage = doc.getFirstChild();
```

### Steg 4: Hämta sidrevisioner
Hämta revisionshistoriken för sidan.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Steg 5: Gå igenom sidrevisioner
Iterera genom listan med sidrevisioner och hämta relevant information, inklusive **senaste ändringstid**.

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

## Vanliga problem och lösningar
- **Null `PageHistory`:** Se till att dokumentet faktiskt innehåller revisioner; annars kan `getPageHistory` returnera `null`.  
- **Tidszonskillnader:** `getLastModifiedTime()` returnerar ett `java.util.Date` i systemets standardtidszon. Konvertera till UTC om det behövs.  
- **Licens ej laddad:** Utan en giltig licens kan Aspose.Note köras i utvärderingsläge, vilket begränsar antalet sidor som behandlas.

## Vanliga frågor

### Q1: Kan jag använda Aspose.Note för Java för att skapa nya OneNote-dokument?
A1: Ja, Aspose.Note för Java erbjuder omfattande stöd för att programmässigt skapa, läsa och manipulera OneNote-dokument.

### Q2: Är Aspose.Note för Java kompatibel med olika versioner av OneNote-filer?
A2: Ja, Aspose.Note för Java stöder olika versioner av Microsoft OneNote-filer, vilket säkerställer kompatibilitet i olika miljöer.

### Q3: Kan jag anpassa utdataformatet när jag exporterar OneNote-dokument?
A3: Absolut, Aspose.Note för Java erbjuder flexibilitet att exportera OneNote-dokument till olika format som PDF, HTML och bilder, med anpassningsalternativ.

### Q4: Kräver Aspose.Note för Java en licens för kommersiell användning?
A4: Ja, en giltig licens krävs för kommersiell användning av Aspose.Note för Java. Du kan skaffa en licens från Aspose-webbplatsen.

### Q5: Var kan jag få hjälp om jag stöter på problem eller har frågor om Aspose.Note för Java?
A5: För support och hjälp kan du besöka Aspose.Note-forumet **[here](https://forum.aspose.com/c/note/28)**, där du kan ställa frågor, dela erfarenheter och interagera med andra användare och experter.

---

**Senast uppdaterad:** 2026-01-10  
**Testat med:** Aspose.Note för Java 23.12 (senaste vid skrivande tidpunkt)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}