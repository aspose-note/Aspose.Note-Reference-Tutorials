---
date: 2026-01-10
description: Lär dig aspose.note‑handledning för sidrevideringar i Java – hämta OneNote‑sidrevideringar
  programatiskt med Aspose.Note. Följ vår steg‑för‑steg‑guide.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: aspose.note sidrevideringar handledning – Hämta sidrevideringar i OneNote
url: /sv/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hämta sidrevisioner i OneNote - Aspose.Note

OneNote är en kraftfull plattform för att ta anteckningar, och du behöver granska ändringar visar **aspose.note page revisions tutorial** exakt hur du hämtar revisionshistorik med bara några rader Java‑kod. I den här guiden går vi igenom allt du behöver—från att sätta upp miljön till att skriva ut varje revisions detaljer—så att du enkelt kan spåra redigeringar, författarbidrag och tidsstämplar.

## Snabba svar
- **What does the tutorial cover?** Hämtning av sidrevisionens historik från en OneNote‑fil med hjälp av Aspose.Note för Java.  
- **Which library version is required?** Vilken som helst ny Aspose.Note för Java‑utgåva som stödjer `LoadOptions.setLoadHistory`.  
- **Do I need a license?** En tillfällig utvärderingslicens fungerar för testning; en kommersiell licens krävs för produktion.  
- **Can I modify revisions?** API‑et är skrivskyddat förer; du kan bara hämta dem.  
- **What are the main prerequisites?** Java JDK, Aspose.Note för Java och ett OneNote‑dokument med revisionsdata.

## Vad är “aspose.note page revisions tutorial”?
Handledningen visar hur du programatiskt får åtkomst till de historiska versionerna av en OneNote‑sida. Varje revision innehåller metadata såsom författare, skapningstid och ändringstid, vilket gör det möjligt att bygga revisionsspår eller förändringslogg‑funktioner i dina applikationer.

## Varför använda Aspose.Note för spårning av sidrevisioner?
- **No UI dependency** – fungerar helt i kod, perfekt för backend‑tjänster.  
- **Cross‑platform** – Java körs på Windows, Linux och macOS.  
- **Full control** – hämta varje revisionsegenskap utan att öppna OneNote manuellt.  
- **Performance** – laddning av historik är optimerad, så även stora anteckningsböcker bearbetas snabbt.

## Förutsättningar

### 1. Java Development Kit (JDK)
Se till att en aktuell JDK (8 eller högre) är installerad och att `JAVA_HOME` är satt.

### 2. Aspose.Note för Java
Ladda ner biblioteket från [download link](https://releases.aspose.com/note/java/).

### 3. Exempel OneNote‑dokument
Skapa eller skaffa en OneNote‑fil (t.ex. `Sample1.one`) som innehåller sidor med revisionshistorik.

## Importera paket
Importera först de nödvändiga Aspose.Note‑klasserna.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Steg‑för‑steg‑implementering

### Steg 1: Ställ in dokumentkatalog
Definiera mappen där din OneNote‑fil finns.

```java
String dataDir = "Your Document Directory";
```

### Steg 2: Ladda OneNote‑dokument med historik aktiverad
Aktivera `LoadOptions`‑flaggan för att hämta revisionsdata.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Steg 3: Hämta den första sidan
Hämta det första sidobjektet; detta blir referenspunkten för att hämta dess historik.

```java
Page firstPage = document.getFirstChild();
```

### Steg 4: Iterera genom sidrevisioner
Loopa igenom varje revision och skriv ut användbar metadata såsom tidsstämplar, titel, nivå och författare.

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

> **Pro tip:** Om du behöver filtrera revisioner efter en specifik författare eller datumintervall, lägg bara till villkorskontroller i `for`‑loopen.

## Vanliga problem & lösningar
- **No revisions returned:** Verifiera att `loadOptions.setLoadHistory(true)` anropas innan dokumentet laddas.  
- **Null author or title:** Vissa äldre OneNote‑versioner kanske inte lagrar dessa fält; hantera `null`‑värden på ett smidigt sätt.  
- **Performance lag on large notebooks:** Ladda bara de sektioner du behöver eller öka JVM‑heap‑storleken.

## Vanliga frågor

**Q1: Kan jag använda Aspose.Note för Java för att ändra sidrevisioner?**  
A1: Nej, API‑et stöder för närvarande endast skrivskyddad åtkomst till sidrevisioner.

**Q2: Är Aspose.Note för Java kompatibel med olika versioner av OneNote‑dokument?**  
A2: Ja, den fungerar med olika OneNote‑filformat, vilket möjliggör sömlös bearbetning över versioner.

**Q3: Kräver Aspose.Note för Java en licens för att använda?**  
A3: En kommersiell licens krävs för produktionsanvändning, men en tillfällig utvärderingslicens finns tillgänglig för testning.

**Q4: Kan jag få support om jag stöter på problem när jag använder Aspose.Note för Java?**  
A4: Ja, du kan ställa frågor på Aspose.Note‑forumet [here](https://forum.aspose.com/c/note/28).

**Q5: Finns det en gratis provperiod för Aspose.Note för Java?**  
A5: Ja, du kan ladda ner en gratis provperiod från [website](https://releases.aspose.com/).

---

**Senast uppdaterad:** 2026-01-10  
**Testad med:** Aspose.Note for Java (senaste versionen)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}