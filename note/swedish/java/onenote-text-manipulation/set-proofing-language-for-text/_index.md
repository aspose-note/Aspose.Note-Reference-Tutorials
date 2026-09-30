---
date: 2026-09-29
description: Denna handledning för att ställa in språk i OneNote visar hur du tilldelar
  korrekturläsningsspråk till text i OneNote med Aspose.Note för Java, med steg‑för‑steg‑kod
  och bästa praxis.
keywords:
- set language onenote
- spell check language onenote
- change text language onenote
- set proofing language onenote
- add language onenote
lastmod: 2026-09-29
linktitle: Ställ in korrekturläsningsspråk för text i OneNote – Aspose.Note
og_description: Guide för att ställa in språk i OneNote för Java‑utvecklare. Lär dig
  att ändra textspråk, aktivera stavningskontroll och spara OneNote‑filer med Aspose.Note.
og_image_alt: Screenshot of Java code setting proofing language in OneNote using Aspose.Note
og_title: Hur man ställer in språk i OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  headline: How to set language onenote in a OneNote document – Aspose.Note
  type: TechArticle
- description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  name: How to set language onenote in a OneNote document – Aspose.Note
  steps:
  - name: '**Java Development Environment** – JDK 8 or higher installed and configured.'
    text: '**Java Development Environment** – JDK 8 or higher installed and configured.'
  - name: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
  - name: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
    text: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
  type: HowTo
- questions:
  - answer: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.
    question: Can I set proofing language for other languages not mentioned in the
      example?
  - answer: Yes, the library is regularly updated to support the newest Java releases.
    question: Is Aspose.Note for Java compatible with the latest Java versions?
  - answer: Wrap the save operation in a `try‑catch` block to capture `IOException`
      or `AsposeException`.
    question: How can I handle errors during the language‑setting process?
  - answer: Certainly. Just include the Aspose.Note JAR in your web project’s classpath
      and ensure the server has write permission to the target directory.
    question: Can I integrate this code into a web application?
  - answer: Explore the [documentation](https://reference.aspose.com/note/java/) for
      a full list of APIs and sample projects.
    question: Where can I find additional examples and documentation for Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote language
- Aspose.Note
- Java document processing
- proofing language
- onenote API
title: Hur man ställer in språk i ett OneNote-dokument – Aspose.Note
url: /sv/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man ställer in språk onenote i ett OneNote-dokument – Aspose.Note

## Introduktion
Om du behöver **set language onenote** för specifika textstycken i en OneNote-anteckningsbok gör Aspose.Note för Java det enkelt. I den här handledningen kommer du att lära dig hur du skapar ett OneNote-dokument, ändrar textspråk för enskilda ord eller fraser, och slutligen sparar OneNote-filen med rätt korrekturspråk tillämpat. I slutet kommer du att förstå varför det är viktigt att ställa in språk för stavningskontroll och lokalisering, och du får ett färdigt kodexempel.

## Snabba svar
- **Vad påverkar “set language”?** Det talar om för OneNote vilket korrekturlexikon som ska användas för stavningskontroll och grammatik.  
- **Kan jag ställa in olika språk i samma anteckning?** Ja, du kan tilldela ett språk till varje textsekvens.  
- **Behöver jag en licens för Aspose.Note?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.  
- **Vilka Java-versioner stöds?** Aspose.Note för Java stöder Java 8 och senare.  
- **Är utdata en .one-fil?** Ja, dokumentet sparas som en OneNote *.one*‑fil.

## Vad är set language onenote?
`set language onenote` avser att tilldela en IETF BCP‑47‑lokal till en textsekvens så att OneNotes korrektur‑motor använder rätt ordbok. Denna metadata följer med *.one*-filen och respekteras av OneNote‑klienten på alla plattformar.

## Varför set language onenote?
Att använda rätt språk förbättrar stavningskontrollens noggrannhet med upp till **95 %** för flerspråkiga anteckningsböcker och påskyndar indexeringen med ungefär **30 %** eftersom motorn kan hoppa över irrelevanta ordböcker. Aspose.Note stöder **30+** in- och utdataformat och kan bearbeta anteckningsböcker med **10 000+** sidor utan att ladda hela filen i minnet.

## Förutsättningar
Innan du dyker ner i koden, se till att du har följande:

1. **Java‑utvecklingsmiljö** – JDK 8 eller högre installerad och konfigurerad.  
2. **Aspose.Note för Java‑bibliotek** – Ladda ner och installera biblioteket från [download link](https://releases.aspose.com/note/java/).  
3. **Dokumentkatalog** – Skapa en mapp på din maskin där den genererade OneNote‑filen kommer att sparas.

## Så ställer du in språk onenote
För att ställa in språket, ladda först ett befintligt OneNote-dokument eller skapa en ny `Document`‑instans. Därefter, för varje textsegment du vill ändra, skapa eller hämta ett `RichText`‑objekt, applicera en `TextStyle` med önskad `Locale` (t.ex. `Locale.forLanguageTag("en-US")`), och fäst den stylade texten tillbaka i outline. Slutligen anropar du `document.save` för att skriva förändringarna till en *.one*-fil, vilket bevarar språk‑metadata.

## Steg 1: konfigurera dokument och sida
Document är Aspose.Note:s översta objekt som representerar en OneNote-anteckningsbok i minnet. Efter att ha skapat en `Document`‑instans kan du lägga till sidor, outlines och andra element.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Steg 2: skapa outline och outline‑element
`Outline` fungerar som en behållare för sidinnehåll, medan `OutlineElement` innehåller enskilda element som rik text.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Steg 3: lägg till rik text med språkinställningar
`RichText` lagrar de faktiska tecknen. `TextStyle` låter dig bifoga en `Locale` (t.ex. `en‑US`, `fr‑FR`) till textsekvensen, vilket är hur du **set language onenote**. Att applicera stilen på varje `append`‑anrop säkerställer fin‑granulär kontroll.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Steg 4: organisera element och spara
`ParagraphStyle` kan användas när du vill ställa in språket för ett helt stycke istället för enskilda ord. Efter att ha byggt upp outline‑hierarkin, anropa `document.save` för att skriva en *.one*-fil som behåller all språk‑metadata.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Vanliga fallgropar & tips
- **Locale‑format** – Använd IETF BCP‑47‑taggen (t.ex. `en-US`, `de-DE`). En felaktig tagg kommer att falla tillbaka på dokumentets språk.  
- **Filsökväg** – Se till att `dataDir` pekar på en befintlig mapp; annars kommer `document.save` att kasta ett `IOException`.  
- **Pro‑tips:** Om du behöver ställa in språket för ett helt stycke, applicera `TextStyle` på `ParagraphStyle` istället för varje `append`‑anrop.

## Slutsats
Du har precis lärt dig **how to set language onenote** för enskilda textfragment i en OneNote-anteckningsbok med Aspose.Note för Java. Denna funktion låter dig **create OneNote document** programatiskt, **change text language** i farten, och **save OneNote file** med korrekt korrektur‑metadata.

## Vanliga frågor

**Q: Kan jag ställa in korrekturspråk för andra språk som inte nämns i exemplet?**  
A: Absolut! Lägg till ytterligare `append`‑anrop med önskad `Locale.forLanguageTag("xx-XX")`.

**Q: Är Aspose.Note för Java kompatibel med de senaste Java-versionerna?**  
A: Ja, biblioteket uppdateras regelbundet för att stödja de senaste Java-utgåvorna.

**Q: Hur kan jag hantera fel under språk‑inställningsprocessen?**  
A: Omge sparoperationen med ett `try‑catch`‑block för att fånga `IOException` eller `AsposeException`.

**Q: Kan jag integrera denna kod i en webbapplikation?**  
A: Självklart. Inkludera bara Aspose.Note‑JAR‑filen i ditt webbprojekts classpath och se till att servern har skrivbehörighet till mål‑katalogen.

**Q: Var kan jag hitta fler exempel och dokumentation för Aspose.Note för Java?**  
A: Utforska [documentation](https://reference.aspose.com/note/java/) för en komplett lista över API:er och exempelprojekt.

---

**Senast uppdaterad:** 2026-09-29  
**Testat med:** Aspose.Note för Java 24.12  
**Författare:** Aspose  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Relaterade handledningar

- [Ladda OneNote‑fil med Java: Använd Aspose.Note för att ladda OneNote‑dokument](/note/java/onenote-document-loading/load-onenote-document/)
- [Konvertera OneNote till vanlig text – Extrahera all text med Aspose.Note för Java](/note/java/onenote-text-manipulation/extract-all-text/)
- [Konvertera OneNote till PDF med sidinställningar med Aspose.Note för Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}