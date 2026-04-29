---
date: 2026-01-18
description: Lär dig hur du skriver ut OneNote‑dokument med Aspose.Note för Java.
  Den här guiden visar hur du skriver ut till PDF, anpassar utskriftsinställningarna
  och använder virtuella skrivare i Java.
linktitle: Print Documents in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Hur man skriver ut OneNote – Aspose.Note
url: /sv/java/onenote-printing-documents/print-documents/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skriv ut dokument i OneNote - Aspose.Note

## Introduction

Att skriva ut OneNote‑sidor från en Java‑applikation är ett vanligt krav, oavsett om du behöver papperskopior, PDF‑arkiv eller integration med virtuella skrivare. I den här handledningen **kommer du att lära dig hur du skriver ut OneNote**‑dokument med Aspose.Note för Java, med täckning av enkel utskrift, anpassning av utskriftsinställningar, utskrift till PDF och utnyttjande av ett virtuellt skrivar‑Java‑arbetsflöde.

## Quick Answers
- **Kan jag skriva ut OneNote direkt till PDF från Java?** Ja – använd `DocumentPrintAttributeSet` med en PDF‑virtuell skrivare som “Microsoft XPS Document Writer” eller “doPDF 8”.  
- **Behöver jag en licens för utskrift?** En giltig Aspose.Note för Java‑licens krävs för produktionsanvändning.  
- **Hur begränsar jag de utskrivna sidorna?** Ställ in utskriftsintervallet via `asposeAttr.setPrintRange(startPage, endPage)`.  
- **Kan jag ändra antalet kopior?** Ja, använd `asposeAttr.setCopies(numberOfCopies)`.  
- **Stöds en virtuell skrivare?** Absolut – Aspose.Note fungerar med vilken installerad virtuell skrivare som helst som Java kan komma åt.

## What is “how to print onenote”?

Uttrycket avser processen att skicka OneNote‑sidans innehåll från din applikation till en skrivare eller ett filformat (som PDF) programatiskt. Aspose.Note för Java abstraherar de lågnivå‑utskrifts‑API:erna, så att du kan fokusera på affärslogik istället för enhetshantering.

## Why use Aspose.Note for Java to print OneNote?
- **Full kontroll** över utskriftsalternativ (intervall, kopior, skrivarselektion).  
- **Sömlös PDF‑generering** med stöd för “print to pdf java” via virtuella skrivare.  
- **Ingen COM‑interop** – ren Java, idealisk för plattformsoberoende servrar.  
- **Robust felhantering** med `PrintException` och detaljerade attributklasser.

## Prerequisites

Innan du börjar, se till att du har:

1. **Java Development Kit (JDK)** – version 8 eller högre installerad.  
2. **Aspose.Note for Java JAR** – ladda ner den från den officiella sidan **[here](https://releases.aspose.com/note/java/)**.  
3. **OneNote‑dokument** – en `.one`‑fil som du vill skriva ut.  
4. (Valfritt) En **virtuell PDF‑skrivare** installerad (t.ex. Microsoft XPS Document Writer, doPDF).

## Import Packages

Först, importera de nödvändiga klasserna i din Java‑källfil:

```java
import javax.print.PrintException;

import com.aspose.note.Document;
import com.aspose.note.DocumentPrintAttributeSet;
import com.aspose.note.PrintOptions;
```

## Step‑by‑Step Guide

### Steg 1: Skriv ut ett dokument (Grundläggande)

Detta exempel skriver ut hela OneNote‑filen med standardskrivaren.

```java
public static void PrintDocument() throws PrintException {
    // Specify the directory where your document is located
    String dataDir = "Your Document Directory";
    
    // Load the OneNote document
    Document document = new Document(dataDir + "YourDocument.one");
    
    // Print the document
    document.print();
}
```

**Varför detta är viktigt:** Det visar det enklaste sättet att starta utskrift utan någon extra konfiguration.

### Steg 2: Skriv ut ett dokument med anpassade utskriftsinställningar

Om du behöver **anpassa utskriftsinställningarna**—till exempel skriva ut endast sidor 1‑2—kan du använda `DocumentPrintAttributeSet`.

```java
public static void PrintDocumentWithPrintOptions() throws PrintException {
    // Specify the directory where your document is located
    String dataDir = "Your Document Directory";

    // Load the OneNote document
    Document document = new Document(dataDir + "YourDocument.one");

    // Define print options
    final DocumentPrintAttributeSet asposeAttr = new DocumentPrintAttributeSet("Microsoft XPS Document Writer");
    asposeAttr.setPrintRange(1, 2);

    // Print the document with specified options
    document.print(asposeAttr);
}
```

**Tips:** Ersätt `"Microsoft XPS Document Writer"` med vilket installerat skrivarnamn som helst för att rikta utdata någon annanstans.

### Steg 3: Skriv ut dokument med en virtuell skrivare (Print to PDF Java)

Virtuella skrivare låter dig generera PDF‑filer utan att lämna Java. Nedan använder vi **doPDF 8** som exempel.

```java
public static void PrintDocumentsWithVirtualPrinter() throws PrintException {
    // Specify the directory where your document is located
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "YourDocument.one");
     
    // Define print options for virtual printer
    final DocumentPrintAttributeSet asposeAttr = new DocumentPrintAttributeSet("doPDF 8");
    asposeAttr.setPrintRange(1, 2);
    asposeAttr.setCopies(3);
     
    PrintOptions printOptions = new PrintOptions();
    printOptions.setDocumentName("YourDocument.one");
    printOptions.setPrinterSettings(asposeAttr);
      
    // Print the document using virtual printer
    doc.print(printOptions);
}
```

**Proffstips:** Justera `asposeAttr.setCopies()` för att styra hur många PDF‑kopior som genereras i ett enda körning.

## Common Issues & Solutions

| Issue | Solution |
|-------|----------|
| **Skrivare hittades inte** | Verifiera att skrivarnamnet exakt matchar det som visas i Windows > Enheter och skrivare. |
| **`PrintException` kastad** | Säkerställ att OneNote‑filen inte är låst och att JRE har behörighet att komma åt skrivaren. |
| **PDF‑utdata är tom** | Kontrollera att den virtuella skrivardrivrutinen är korrekt installerad och inställd som standard för utskriftsjobbet. |
| **Felaktigt sidintervall** | Kom ihåg att sidnumren börjar på 1; `setPrintRange(1, 2)` skriver ut de två första sidorna. |

## Frequently Asked Questions

### Q1: Kan jag skriva ut specifika sidor i ett OneNote‑dokument?
**A:** Ja, använd `asposeAttr.setPrintRange(startPage, endPage)` för att begränsa utdata till de sidor du behöver.

### Q2: Är Aspose.Note för Java kompatibel med virtuella skrivare?
**A:** Absolut. Biblioteket fungerar med vilken skrivare som helst som Windows exponerar, inklusive virtuella PDF‑skrivare.

### Q3: Kan jag anpassa utskriftsinställningar såsom antal kopior?
**A:** Ja, anropa `asposeAttr.setCopies(numberOfCopies)` innan du anropar `print()`.

### Q4: Kräver Aspose.Note för Java en licens för att skriva ut dokument?
**A:** En giltig licens krävs för produktionsdistributioner; en tillfällig provlicens finns tillgänglig för utvärdering.

### Q5: Var kan jag hitta mer support och resurser för Aspose.Note för Java?
**A:** Besök den officiella supportsidan på **[Aspose.Note for Java support page](https://forum.aspose.com/c/note/28)** för forum, dokumentation och exempel.

---

**Senast uppdaterad:** 2026-01-18  
**Testat med:** Aspose.Note för Java 24.12 (senaste vid skrivande stund)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}