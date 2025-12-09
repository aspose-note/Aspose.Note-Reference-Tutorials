---
date: 2025-12-02
description: Lär dig hur du skapar en OneNote‑sida med en titel i Java med hjälp av
  Aspose.Note för Java. Den här guiden visar hur du ställer in OneNote‑sidans titel
  och anpassar titelns teckensnitt.
linktitle: How to Create OneNote Page with Title - Java
second_title: Aspose.Note Java API
title: Hur du skapar OneNote-sida med titel – Java
url: /sv/java/onenote-document-loading/create-onenote-doc-page-title/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man skapar en OneNote‑sida med titel – Java

## Introduktion

Om du behöver **hur man skapar OneNote‑sida** programatiskt, gör Aspose.Note för Java det enkelt. I den här handledningen lär du dig hur du genererar en OneNote‑fil, sätter sidtiteln och till och med anpassar titelfonten – allt från Java‑kod. När du är klar har du ett färdigt OneNote‑dokument som du kan integrera i vilken Java‑applikation som helst.

## Snabba svar
- **Vilket bibliotek krävs?** Aspose.Note för Java.  
- **Kan jag ange ett eget teckensnitt för titeln?** Ja – använd `ParagraphStyle` för att definiera teckensnittsnamn, storlek och färg.  
- **Vilken Java‑version stöds?** Alla JDK 8+ (API‑et är bakåtkompatibelt).  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en licens krävs för produktion.  
- **Var sparas utdata?** Du anger sökvägen i variabeln `dataDir`.

## Vad är en OneNote‑sidtitel?
En OneNote‑sidtitel är rubriken som visas högst upp på varje sida. Den innehåller vanligtvis sidnamnet, skapelsedatum och tid. Att sätta denna titel programatiskt hjälper dig att skapa konsekventa, välstrukturerade anteckningsböcker.

## Varför sätta OneNote‑sidtitel programatiskt?
- **Automatisering:** Generera rapporter eller mötesanteckningar utan manuell redigering.  
- **Konsistens:** Upprätthålla en namngivningskonvention för alla sidor.  
- **Integration:** Kombinera OneNote med andra system (t.ex. CRM, projektstyrningsverktyg).  

## Förutsättningar

- **Java Development Kit (JDK)** – version 8 eller högre.  
- **Aspose.Note för Java** – ladda ner från den officiella webbplatsen **[här](https://releases.aspose.com/note/java/)**.  
- **IDE** – IntelliJ IDEA, Eclipse eller NetBeans (valfritt).

## Importera paket

Först importerar du de klasser vi behöver från Aspose.Note‑biblioteket.

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

### Steg 1: Ställ in dokumentkatalog  
Definiera var den genererade OneNote‑filen ska sparas.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

### Steg 2: Skapa dokumentobjekt  
Instansiera ett nytt `Document` – detta representerar OneNote‑filen du ska bygga.

```java
// Create an object of the Document class
Document doc = new Document();
```

### Steg 3: Initiera sidobjekt  
Skapa ett `Page`‑objekt som kommer att hålla titeln och eventuellt innehåll.

```java
// Initialize Page class object
Page page = new Page();
```

### Steg 4: Ange standardtextstil  
Definiera en standard `ParagraphStyle` som kommer att tillämpas på titeltexten. Detta är där vi **anpassar OneNote‑titelfonten**.

```java
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

### Steg 5: Ange sidtitels‑egenskaper  
Här **sätter vi OneNote‑sidtitel**‑detaljer – titeltext, datum och tid. Ändra gärna strängarna så att de passar ditt användningsfall.

```java
// Set page title properties
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

### Steg 6: Tilldela titeln till sidan  
Nu **lägger vi till titeln i OneNote** genom att länka `Title`‑objektet med `Page`.

```java
page.setTitle(title);
```

### Steg 7: Lägg till sidan i dokumentet  
Lägg till den konfigurerade sidan i dokumentstrukturen.

```java
doc.appendChildLast(page);
```

### Steg 8: Spara OneNote‑dokument  
Ange filnamnet för utdata och spara anteckningsboken. Detta slutför processen för **java create onenote file**.

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// Save OneNote document
doc.save(dataDir);
```

## Vanliga problem och tips

| Problem | Lösning |
|-------|----------|
| **Ogiltig filsökväg** | Se till att `dataDir` slutar med en korrekt separator (`/` eller `\\`) och att mappen finns. |
| **Titel syns inte** | Verifiera att `ParagraphStyle` tillämpas på varje `RichText`‑element. |
| **Licensundantag** | Använd en provlicens för testning; tillämpa en full licens innan distribution. |
| **Datum visar fel månad** | Java‑månader är nollbaserade; `cal.set(2018, 04, 03)` sätter faktiskt maj. Justera därefter. |

## Vanliga frågor

**Q: Är Aspose.Note för Java kompatibel med olika Java‑versioner?**  
A: Ja, biblioteket fungerar med Java 8 och nyare, vilket ger dig flexibilitet i olika miljöer.

**Q: Kan jag anpassa teckensnittsstil och storlek för sidtiteln?**  
A: Absolut! Använd `ParagraphStyle` (som visas i Steg 4) för att ange vilket teckensnitt, storlek och färg som helst.

**Q: Hur lägger jag till mer innehåll (t.ex. stycken, bilder) på sidan?**  
A: Skapa ytterligare `RichText`‑ eller `Image`‑objekt, ange deras stilar och lägg till dem i `Page` med `page.appendChildLast(yourObject)`.

**Q: Finns det en provversion av Aspose.Note för Java?**  
A: Ja, du kan ladda ner en gratis provversion från Aspose‑webbplatsen för att utvärdera alla funktioner.

**Q: Var kan jag få support om jag stöter på problem?**  
A: Besök [Aspose.Note‑forumet](https://forum.aspose.com/c/note/28) för hjälp från communityn eller öppna ett supportärende hos Aspose.

---

**Senast uppdaterad:** 2025-12-02  
**Testat med:** Aspose.Note för Java 24.12 (senaste vid skrivtillfället)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}