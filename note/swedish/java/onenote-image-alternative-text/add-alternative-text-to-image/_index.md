---
date: 2025-12-23
description: Lär dig hur du lägger till alt‑text till bilder i OneNote‑dokument med
  Java och Aspose.Note. Denna guide visar hur du lägger till alternativ bildtext för
  bättre tillgänglighet.
linktitle: How to Add Alt Text to Image in OneNote using Java
second_title: Aspose.Note Java API
title: Hur man lägger till alt‑text till en bild i OneNote med Java
url: /sv/java/onenote-image-alternative-text/add-alternative-text-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man lägger till alt‑text till bild i OneNote med Java

## Introduktion

I den här handledningen kommer du att upptäcka **hur man lägger till alt**‑text till bilder i OneNote‑dokument med Java och Aspose.Note‑API:t. Att lägga till alternativ text (alt‑text) förbättrar tillgängligheten för skärmläsaranvändare och ökar den övergripande inkluderingen av ditt innehåll. I slutet av guiden kommer du att kunna sätta bild‑alt‑text i Java, vilket gör dina OneNote‑filer mer förenliga med tillgänglighetsstandarder.

## Snabba svar
- **Vilket bibliotek krävs?** Aspose.Note for Java  
- **Vilket primärt nyckelord riktar sig den här handledningen mot?** how to add alt  
- **Behöver jag en licens för produktion?** Ja, en kommersiell licens krävs (en gratis provversion finns tillgänglig).  
- **Kan jag lägga till alt‑text till flera bilder?** Absolut – upprepa bara stegen för varje bild.  
- **Vilken Java‑version stöds?** Java 8 eller högre.

## Vad betyder “how to add alt” i OneNote‑sammanhang?

Att lägga till alt‑text innebär att tillhandahålla en textuell beskrivning av en bild som kan läsas av hjälpmedelstekniker. Denna beskrivning hjälper användare som inte kan se bilden att förstå dess syfte.

## Varför lägga till alt‑text till bilder i OneNote?

- **Tillgänglighet:** Uppfyller WCAG‑riktlinjer och förbättrar upplevelsen för användare med synnedsättningar.  
- **Sökbarhet:** Sökmotorer kan indexera beskrivningen, vilket gör ditt innehåll mer upptäckbart.  
- **Professionalism:** Visar ett engagemang för inkluderande design.

## Förutsättningar

Innan du dyker ner i handledningen, se till att du har följande förutsättningar:

1. Java Development Kit (JDK) – version 8 eller senare.  
2. Aspose.Note for Java Library – ladda ner den från [here](https://releases.aspose.com/note/java/).  
3. En IDE såsom IntelliJ IDEA eller Eclipse.  
4. Grundläggande kunskap i Java‑programmering.

## Importera paket

Importera först de nödvändiga paketen i ditt Java‑projekt för att använda Aspose.Note‑funktionaliteten.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;
```

Nu ska vi gå igenom processen för att lägga till **alternativ text bild** i ett OneNote‑dokument med Java och Aspose.Note i steg‑för‑steg‑instruktioner.

## Hur man lägger till alt‑text till bilder i OneNote med Java

### Steg 1: Ställ in dokumentkatalogen

```java
String dataDir = "Your Document Directory";
```

Ersätt `"Your Document Directory"` med sökvägen till den mapp som innehåller din källbild och där utdatafilen ska sparas.

### Steg 2: Skapa ett dokumentobjekt

```java
Document document = new Document();
```

Detta skapar ett nytt, tomt OneNote‑dokument.

### Steg 3: Skapa ett sidobjekt

```java
Page page = new Page();
```

En sida kommer att hysa bilden vi håller på att lägga till.

### Steg 4: Lägg till en bild på sidan

```java
Image image = new Image(null, dataDir + "image.jpg");
```

`Image`‑konstruktorn laddar bildfilen från den angivna sökvägen.

### Steg 5: Ställ in alternativ text‑titel

```java
image.setAlternativeTextTitle("ImageAlternativeText Title");
```

Här **lägger vi till alt‑text** som fungerar som en kort titel för bilden.

### Steg 6: Ställ in alternativ text‑beskrivning

```java
image.setAlternativeTextDescription("ImageAlternativeText Description");
```

Denna beskrivning ger en mer detaljerad förklaring – perfekt för skärmläsare.

### Steg 7: Lägg till bilden på sidan

```java
page.appendChildLast(image);
```

Bilden (nu berikad med alt‑text) läggs till på sidan.

### Steg 8: Lägg till sidan i dokumentet

```java
document.appendChildLast(page);
```

Fäst sidan i OneNote‑dokumentet.

### Steg 9: Spara dokumentet

```java
document.save(dataDir + "AlternativeText_out.one");
```

Dokumentet sparas med den alternativa texten inbäddad i bilden.

## Vanliga problem och lösningar

- **FileNotFoundException:** Verifiera att `dataDir` pekar på rätt mapp och att `image.jpg` finns.  
- **NullPointerException på bild:** Säkerställ att bildens sökväg är giltig och att filen inte är skadad.  
- **Licensfel:** Använd en giltig Aspose.Note‑licensfil eller kör i provläge för utvärdering.

## Vanliga frågor

**Q: Kan jag lägga till alt‑text till flera bilder i ett och samma dokument?**  
A: Ja, upprepa helt enkelt steg 4‑6 för varje bild du vill annotera.

**Q: Vilka bildformat stöds för att lägga till alt‑text?**  
A: Aspose.Note stöder JPEG, PNG, GIF, BMP och flera andra vanliga format.

**Q: Är det möjligt att ändra eller ta bort alt‑text efter att den har satts?**  
A: Absolut. Anropa `setAlternativeTextTitle("")` eller `setAlternativeTextDescription("")` för att rensa värdena, eller ange nya strängar för att uppdatera dem.

**Q: Tillhandahåller Aspose.Note API:er för andra språk än Java?**  
A: Ja, biblioteket finns också för .NET, C++ och Python.

**Q: Var kan jag ladda ner en provversion av Aspose.Note?**  
A: Du kan få en gratis provversion från [here](https://releases.aspose.com/).

## Slutsats

Genom att följa den här steg‑för‑steg‑guiden vet du nu **hur man lägger till alt**‑text till bilder i OneNote med Java. Att implementera `add alternative text image` gör inte bara dina dokument mer tillgängliga utan förbättrar också deras sökbarhet och övergripande kvalitet. Känn dig fri att experimentera med olika titlar och beskrivningar för att bäst förmedla innebörden av varje bild.

---

**Last Updated:** 2025-12-23  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}