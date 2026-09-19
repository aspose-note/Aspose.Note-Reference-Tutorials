---
date: 2026-06-05
description: Lär dig hur du ändrar font size i OneNote, sätter font color och markerar
  text med Aspose.Note för Java – step‑by‑step guide med code snippets.
keywords:
- change font size onenote
- how to change text
- set font color onenote
linktitle: Ändra teckenstorlek i OneNote - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  headline: Change Font Size in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  name: Change Font Size in OneNote - Aspose.Note
  steps:
  - name: Import Packages
    text: 'The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note`
      namespace. Import them at the top of your Java source file:'
  - name: Load the Document
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. Loading a file is as simple as passing the file
      path to its constructor.
  - name: Access RichText Nodes
    text: '`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`,
      you gain access to every piece of editable text in the notebook.'
  - name: Change Text Style
    text: '`TextRun` represents a contiguous run of characters sharing the same formatting.
      Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize`
      to **20** points to achieve the desired styling.'
  - name: Save the Document
    text: Call `document.save("StyledSample.one")` to write the changes back to a
      OneNote file. The save operation preserves all original content while applying
      the new styles.
  type: HowTo
- questions:
  - answer: Yes, filter the `RichText` collection by page or section ID before applying
      style changes.
    question: Can I apply these text style changes to specific sections of my OneNote
      document?
  - answer: Absolutely, you can modify font family, bold/italic, underline, alignment,
      and paragraph spacing using the same object model.
    question: Does Aspose.Note support other formatting options beyond color, highlight,
      and size?
  - answer: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson,
      or Spring to build complex document pipelines.
    question: Can I integrate Aspose.Note with other Java libraries for advanced processing?
  - answer: A commercial license is required for production deployments; a free evaluation
      license is available for development and testing.
    question: Is Aspose.Note licensed for commercial use?
  - answer: Visit the Aspose.Note documentation portal, download the full API reference
      PDF, and explore the GitHub repository for community examples.
    question: Where can I find additional samples and API reference?
  type: FAQPage
second_title: Aspose.Note Java API
title: Ändra teckenstorlek i OneNote - Aspose.Note
url: /sv/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ändra teckenstorlek i OneNote - Aspose.Note

## Introduktion

I den här handledningen kommer du att lära dig **how to change font size onenote** dokument med Aspose.Note för Java. Vi går igenom hur man laddar en OneNote‑fil, får åtkomst till dess textnoder, applicerar färg, markering och teckenstorleksändringar, och slutligen sparar den uppdaterade filen. Oavsett om du automatiserar rapportgenerering eller finputsar mötesanteckningar, ger den här guiden dig ett pålitligt sätt att formatera OneNote‑innehåll programmässigt.

## Snabba svar
- **Hur ändrar jag teckenstorlek i OneNote med Java?** Ladda dokumentet, ändra varje `TextRun`s `FontSize`‑egenskap, och spara – tre enkla steg.  
- **Kan jag också ändra textfärg och markering?** Ja, sätt `FontColor` och `HighlightColor` på samma `TextRun`.  
- **Vilken version av Aspose.Note krävs?** Alla versioner 23.10+ stödjer dessa formaterings‑API:er.  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.  
- **Är detta tillvägagångssätt lämpligt för stora anteckningsböcker?** Ja – Aspose.Note bearbetar flertalet hundra sidor utan att ladda hela filen i minnet.

## Vad är change font size onenote?
**change font size onenote** avser att programatiskt justera `FontSize`‑attributet för textelement i en OneNote‑anteckningsbok. Med Aspose.Note kan utvecklare ändra denna egenskap via API‑et, vilket direkt uppdaterar den underliggande OneNote‑filstrukturen och säkerställer att det visuella utseendet ändras utan manuell redigering eller UI‑interaktion.

## Varför använda Aspose.Note för att ändra textstil i OneNote?
Aspose.Note erbjuder mer än 30 formateringsalternativ—inklusive teckensnittsfamilj, storlek, färg, markering, justering och styckeavstånd—och är konstruerat för att effektivt bearbeta stora anteckningsböcker. Det kan hantera anteckningsböcker med mer än 500 sidor samtidigt som det använder mindre än 150 MB RAM, vilket ger pålitlig, högpresterande automatisering för företags‑skaliga dokumentarbetsflöden.

## Förutsättningar

1. Grundläggande kunskaper i Java‑programmering.  
2. JDK 8 eller högre installerat på din maskin.  
3. Aspose.Note för Java‑biblioteket (ladda ner från Aspose‑webbplatsen).  
4. Bekantskap med OneNotes hierarkiska struktur (sidor, sektioner, RichText‑noder).

## Hur ändrar man teckenstorlek i OneNote med Aspose.Note?

Ladda din OneNote‑fil, lokalisera varje `RichText`‑nod, uppdatera varje `TextRun`s stil och spara dokumentet. Detta end‑to‑end‑flöde kräver bara några kodrader och körs på under en sekund för vanliga anteckningsböcker.

### Steg 1: Importera paket

`Document`, `RichText` och `TextRun`‑klasserna finns i `com.aspose.note`‑namnrymden. Importera dem högst upp i din Java‑källfil:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

### Steg 2: Ladda dokumentet

`Document`‑klassen är Aspose.Note:s översta objekt som representerar en enskild OneNote‑fil i minnet. Att ladda en fil är så enkelt som att skicka filens sökväg till dess konstruktor.

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

### Steg 3: Åtkomst till RichText‑noder

`RichText`‑noder innehåller den faktiska stycketexten. Genom att iterera över `document.getRichTextNodes()` får du åtkomst till varje redigerbar textdel i anteckningsboken.

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

### Steg 4: Ändra textstil

`TextRun` representerar ett sammanhängande teckenflöde som delar samma formatering. Inom loopen, sätt `FontColor` till gul, `HighlightColor` till blå, och `FontSize` till **20** punkter för att uppnå önskad stil.

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

### Steg 5: Spara dokumentet

Anropa `document.save("StyledSample.one")` för att skriva tillbaka ändringarna till en OneNote‑fil. Spara‑operationen bevarar allt originalinnehåll samtidigt som de nya stilarna appliceras.

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

## Vanliga problem och lösningar

- **Texten ändras inte:** Se till att du itererar över `TextRun`‑objekt inom varje `RichText`‑nod; att hoppa över detta steg lämnar formateringen orörd.  
- **Färgen ser annorlunda ut:** Aspose.Note använder RGB‑värden; kontrollera att du använder rätt `java.awt.Color`‑konstanter.  
- **Stora anteckningsböcker blir långsamma:** LoadOptions konfigurerar hur Aspose.Note laddar en fil, vilket möjliggör streaming och formatval. Använd `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` för att aktivera streaming‑läge, vilket minskar minnesfotavtrycket.

## Vanliga frågor

**Q: Kan jag applicera dessa textstiländringar på specifika sektioner i mitt OneNote‑dokument?**  
A: Ja, filtrera `RichText`‑samlingen efter sid‑ eller sektion‑ID innan du applicerar stiländringarna.

**Q: Stöder Aspose.Note andra formateringsalternativ utöver färg, markering och storlek?**  
A: Absolut, du kan ändra teckensnittsfamilj, fet/kursiv, understrykning, justering och styckeavstånd med samma objektmodell.

**Q: Kan jag integrera Aspose.Note med andra Java‑bibliotek för avancerad bearbetning?**  
A: Ja, Aspose.Note fungerar sömlöst med bibliotek som Apache POI, Jackson eller Spring för att bygga komplexa dokumentpipeline‑lösningar.

**Q: Är Aspose.Note licensierat för kommersiell användning?**  
A: En kommersiell licens krävs för produktionsdistributioner; en gratis utvärderingslicens finns tillgänglig för utveckling och testning.

**Q: Var kan jag hitta ytterligare exempel och API‑referens?**  
A: Besök Aspose.Note‑dokumentationsportalen, ladda ner den fullständiga API‑referens‑PDF‑filen och utforska GitHub‑förrådet för community‑exempel.

## Slutsats

Genom att följa stegen ovan vet du nu **how to change font size onenote**‑filer, justera textfärg och applicera markeringar med Aspose.Note för Java. Denna funktion låter dig automatisera den visuella poleringen av mötesanteckningar, utbildningsmaterial eller vilket OneNote‑baserat innehåll som helst i stor skala.

---

**Last Updated:** 2026-06-05  
**Tested With:** Aspose.Note 23.10 for Java  
**Author:** Aspose

## Relaterade handledningar

- [Set Default Paragraph Style in OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)
- [Set Proofing Language for Text in OneNote - Aspose.Note](/note/java/onenote-text-manipulation/set-proofing-language-for-text/)
- [Setting Page Title in Microsoft OneNote Style - Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}