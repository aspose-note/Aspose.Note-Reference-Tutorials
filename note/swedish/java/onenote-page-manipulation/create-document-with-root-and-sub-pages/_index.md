---
description: Lär dig hur du sparar OneNote PDF och lägger till undersidor i OneNote
  med Aspose.Note för Java. Följ den här steg‑för‑steg‑guiden för att organisera dina
  anteckningar effektivt.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Hur man sparar OneNote PDF och lägger till undersidor
url: /sv/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man sparar OneNote PDF och lägger till undersidor

## Introduktion

I den här handledningen kommer du att upptäcka **hur man sparar OneNote PDF** medan du skapar ett dokument som innehåller både huvud‑ och undersidor med Aspose.Note för Java. Att organisera dina OneNote‑anteckningsböcker med en tydlig hierarki gör navigeringen enkel, och möjligheten att exportera till PDF säkerställer att du kan dela dina anteckningar i ett universellt läsbart format. Vi kommer också att visa dig hur du **lägger till undersidor onenote**‑stil, så att du enkelt kan bygga flernivåstrukturer.

## Snabba svar
- **Vad betyder huvudnyckelordet?** Det avser export av en OneNote‑anteckningsbok till PDF med Aspose.Note.  
- **Vilket API används?** Aspose.Note för Java.  
- **Kan jag skapa hierarkiska sidor?** Ja – ange sidnivån för att bygga huvud‑ och undersidor.  
- **Behöver jag en licens?** En gratis provversion finns tillgänglig; en kommersiell licens krävs för produktion.  
- **Vilka utdataformat stöds?** BMP, PDF, PNG och mer.

## Vad är “how to save OneNote PDF”?
Att spara OneNote som PDF konverterar anteckningsbokens sidor till ett fast layout‑dokument som behåller formatering, bilder och hierarki. Detta är idealiskt för att dela, arkivera eller skriva ut anteckningar.

## Varför lägga till undersidor onenote?
Att lägga till undersidor låter dig gruppera relaterat innehåll under en föräldrasida, vilket efterliknar en mapp‑liknande struktur. Det förbättrar organiseringen av anteckningar, gör sökningar snabbare och förbättrar läsupplevelsen när anteckningsboken exporteras till PDF.

## Förutsättningar

Innan du börjar, se till att du har följande förutsättningar:

1. Java Development Kit (JDK): Se till att du har JDK installerat på ditt system.  
2. Aspose.Note för Java: Ladda ner och installera Aspose.Note för Java från [webbplatsen](https://purchase.aspose.com/buy).  
3. Integrated Development Environment (IDE): Välj en Java‑IDE såsom IntelliJ IDEA, Eclipse eller NetBeans.

## Importera paket

Börja med att importera de nödvändiga paketen i ditt Java‑projekt:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Steg 1: Ställ in dokumentkatalog

Definiera katalogen där du vill spara ditt OneNote‑dokument:

```java
String dataDir = "Your Document Directory";
```

## Steg 2: Skapa dokumentobjekt

Instansiera ett `Document`‑objekt:

```java
Document doc = new Document();
```

## Steg 3: Skapa sidor

Initiera sidobjekt och ange deras nivåer. Att ange nivå bestämmer om en sida är en huvud‑ eller en undersida:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Steg 4: Lägg till noder på sidor

### Lägga till noder på första sidan

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Lägga till noder på andra sidan

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Lägga till noder på tredje sidan

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Steg 5: Lägg till sidor i dokumentet

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Steg 6: Spara dokumentet

Spara OneNote‑dokumentet som en PDF (eller BMP i detta exempel). Genom att ändra `SaveFormat` kan du exportera till PDF, vilket uppfyller kravet “how to save OneNote PDF”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Pro tip:** För att exportera direkt till PDF, ersätt `SaveFormat.Bmp` med `SaveFormat.Pdf`.

Grattis! Du har framgångsrikt skapat ett OneNote‑dokument med huvud‑ och undersidor och lärt dig **hur man sparar OneNote PDF** med Aspose.Note för Java.

## Varför detta är viktigt

- **Hierarkisk organisering:** Huvud‑ och undersidor låter dig efterlikna mappstrukturer i OneNote.  
- **Sömlös PDF‑export:** När strukturen är klar bevarar export till PDF hierarkin, vilket gör det slutgiltiga dokumentet lättläst och delbart.  
- **Automation:** Koden kan integreras i större Java‑applikationer, vilket möjliggör batch‑skapande av strukturerade anteckningsböcker.

## Vanliga fallgropar & hur man undviker dem

| Problem | Orsak | Lösning |
|-------|-------|----------|
| Sidor visas på samma nivå | Felaktigt `setLevel`‑värde | Använd `setLevel((byte) 1)` för huvud‑sidor och `setLevel((byte) 2)` (eller högre) för undersidor. |
| PDF‑utdata ser tom ut | Saknar `SaveFormat.Pdf` eller felaktig filsökväg | Verifiera att katalogen finns och använd `SaveFormat.Pdf`. |
| Typsnittet tillämpas inte | Fel typsnittsnamn eller saknat typsnitt på systemet | Se till att typsnittet (t.ex. “David Transparent”) är installerat på maskinen som kör koden. |

## Vanliga frågor

**Q: Kan jag skapa flera nivåer av undersidor med Aspose.Note för Java?**  
A: Ja, du kan skapa djupare hierarkier genom att ange högre nivånummer (t.ex. `setLevel((byte) 3)` för en tredje‑nivå‑undersida).

**Q: Är Aspose.Note för Java kompatibelt med olika Java‑IDE:er?**  
A: Absolut. Det fungerar med IntelliJ IDEA, Eclipse, NetBeans och alla IDE:er som stödjer Java‑utveckling.

**Q: Kan jag anpassa formateringen av text i mitt OneNote‑dokument?**  
A: Ja. Använd `ParagraphStyle` för att sätta typsnitt, storlek, färg och andra attribut för varje `RichText`‑element.

**Q: Stöder Aspose.Note för Java att spara dokument i andra format än BMP?**  
A: Ja. Stödda format inkluderar PDF, PNG, JPEG, DOCX och fler. Ändra `SaveFormat`‑enumen därefter.

**Q: Finns det en provversion av Aspose.Note för Java?**  
A: Ja, du kan ladda ner en gratis provversion från Aspose‑webbplatsen.

## Slutsats

Att organisera dina OneNote‑anteckningsböcker med en tydlig hierarkisk struktur och exportera dem som PDF gör dina anteckningar mer tillgängliga och delbara. Genom att följa stegen ovan vet du nu **hur man sparar OneNote PDF** och **lägger till undersidor onenote**‑stil programatiskt med Aspose.Note för Java.

---

**Senast uppdaterad:** 2026-01-07  
**Testad med:** Aspose.Note för Java 24.11 (senaste)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}