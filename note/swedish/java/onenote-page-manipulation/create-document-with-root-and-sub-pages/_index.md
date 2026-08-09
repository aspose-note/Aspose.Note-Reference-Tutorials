---
date: 2026-04-30
description: Lär dig hur du **sparar onenote som pdf** och lägger till undersidor
  i OneNote med Aspose.Note för Java. Följ den här steg‑för‑steg‑guiden för att organisera
  dina anteckningar effektivt.
keywords:
- save onenote as pdf
- add sub pages onenote
- Aspose.Note Java
linktitle: Hur man sparar OneNote som PDF och lägger till undersidor
second_title: Aspose.Note Java API
title: Så sparar du OneNote som PDF och lägger till undersidor
url: /sv/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man sparar OneNote som PDF och lägger till undersidor

## Introduktion

I den här handledningen kommer du att upptäcka **how to save onenote as pdf** medan du skapar ett dokument som innehåller både rot- och undersidor med Aspose.Note för Java. Att organisera dina OneNote‑anteckningsböcker med en tydlig hierarki gör navigeringen enkel, och export till PDF säkerställer att du kan dela dina anteckningar i ett universellt läsbart format. Vi visar också hur du **add sub pages onenote**‑stil, så att du kan bygga flernivåstrukturer med lätthet.

## Snabba svar
- **Vad betyder “save onenote as pdf”?** Det hänvisar till att exportera en OneNote‑anteckningsbok till en PDF‑fil med hjälp av Aspose.Note för Java.  
- **Vilket API krävs?** Aspose.Note för Java tillhandahåller de nödvändiga klasserna och metoderna.  
- **Kan jag skapa hierarkiska sidor?** Ja – ange sidnivån för att bygga rot‑sidor och undersidor.  
- **Behöver jag en licens för produktion?** En gratis provversion finns tillgänglig, men en kommersiell licens krävs för produktionsbruk.  
- **Vilka format kan jag exportera till?** Förutom PDF kan du exportera till BMP, PNG, JPEG, DOCX och mer.

## Så sparar du OneNote som PDF

Att spara OneNote som PDF konverterar varje anteckningsboksida till ett fast layout‑dokument som bevarar formatering, bilder och sidhierarkin. Detta är idealiskt för att dela, arkivera eller skriva ut anteckningar samtidigt som den ursprungliga strukturen förblir intakt.

## Varför lägga till undersidor onenote?

Att lägga till undersidor låter dig gruppera relaterat innehåll under en föräldrasida, vilket speglar en mapp‑liknande struktur. Det förbättrar anteckningsorganisationen, påskyndar sökningar och förbättrar läsupplevelsen när anteckningsboken exporteras till PDF.

## Förutsättningar

Innan du börjar, se till att du har följande förutsättningar:

1. **Java Development Kit (JDK)** – Se till att du har JDK installerat på ditt system.  
2. **Aspose.Note for Java** – Ladda ner och installera Aspose.Note för Java från [website](https://purchase.aspose.com/buy).  
3. **Integrated Development Environment (IDE)** – Välj en Java‑IDE såsom IntelliJ IDEA, Eclipse eller NetBeans.

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

## Steg 1: Ställ in dokumentkatalogen

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

Initiera sidobjekt och ange deras nivåer. Att ange nivån bestämmer om en sida är en rotsida eller en undersida:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Steg 4: Lägg till noder på sidor

### Lägg till noder på första sidan

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

### Lägg till noder på andra sidan

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

### Lägg till noder på tredje sidan

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

Spara OneNote‑dokumentet som en PDF (eller BMP i detta exempel). Genom att ändra `SaveFormat` kan du exportera till PDF, vilket uppfyller kravet “save onenote as pdf”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Pro tip:** För att exportera direkt till PDF, ersätt `SaveFormat.Bmp` med `SaveFormat.Pdf`.

Grattis! Du har framgångsrikt skapat ett OneNote‑dokument med rot‑ och undersidor och lärt dig **how to save onenote as pdf** med Aspose.Note för Java.

## Varför detta är viktigt

- **Hierarkisk organisation:** Rot‑ och undersidor låter dig efterlikna mappstrukturer i OneNote.  
- **Sömlös PDF‑export:** När de är organiserade bevarar export till PDF hierarkin, vilket gör det slutliga dokumentet lätt att läsa och dela.  
- **Automation:** Koden kan integreras i större Java‑applikationer, vilket möjliggör batch‑skapande av strukturerade anteckningsböcker.

## Vanliga fallgropar & hur man undviker dem

| Problem | Orsak | Lösning |
|-------|-------|----------|
| Sidor visas på samma nivå | Fel `setLevel`‑värde | Använd `setLevel((byte) 1)` för rotsidor och `setLevel((byte) 2)` (eller högre) för undersidor. |
| PDF‑utdata ser tom ut | Saknad `SaveFormat.Pdf` eller felaktig filsökväg | Verifiera att katalogen finns och använd `SaveFormat.Pdf`. |
| Typsnitt tillämpas inte | Fel typsnittsnamn eller saknat typsnitt på systemet | Se till att typsnittet (t.ex. “David Transparent”) är installerat på maskinen som kör koden. |

## Vanliga frågor

**Q: Kan jag skapa flera nivåer av undersidor med Aspose.Note för Java?**  
A: Ja, du kan skapa djupare hierarkier genom att ange högre nivånummer (t.ex. `setLevel((byte) 3)` för en tredje‑nivå undersida).

**Q: Är Aspose.Note för Java kompatibel med olika Java‑IDE:er?**  
A: Absolut. Det fungerar med IntelliJ IDEA, Eclipse, NetBeans och alla IDE:er som stödjer Java‑utveckling.

**Q: Kan jag anpassa formateringen av text i mitt OneNote‑dokument?**  
A: Ja. Använd `ParagraphStyle` för att ange typsnittsnamn, storlek, färg och andra attribut för varje `RichText`‑element.

**Q: Stöder Aspose.Note för Java att spara dokument i andra format än BMP?**  
A: Ja. Stödda format inkluderar PDF, PNG, JPEG, DOCX och mer. Ändra `SaveFormat`‑enumen därefter.

**Q: Finns det en provversion tillgänglig för Aspose.Note för Java?**  
A: Ja, du kan ladda ner en gratis provversion från Aspose‑webbplatsen.

## Slutsats

Att organisera dina OneNote‑anteckningsböcker med en tydlig hierarkisk struktur och exportera dem som PDF‑filer gör dina anteckningar mer tillgängliga och delbara. Genom att följa stegen ovan vet du nu **how to save onenote as pdf** och **add sub pages onenote**‑stil programatiskt med Aspose.Note för Java.

---

**Senast uppdaterad:** 2026-04-30  
**Testad med:** Aspose.Note for Java 24.11 (latest)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}