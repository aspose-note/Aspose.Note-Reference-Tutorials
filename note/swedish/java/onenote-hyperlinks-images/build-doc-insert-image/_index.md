---
date: 2026-03-19
description: Lär dig hur du lägger till en bild i OneNote med Aspose.Note för Java.
  Denna steg‑för‑steg‑guide visar hur du skapar OneNote‑dokument, infogar en bild
  i OneNote och sparar OneNote som PDF.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Hur man lägger till en bild i OneNote med Java – Bygg dokument och infoga bild
url: /sv/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man lägger till bild i OneNote med Java – Skapa dokument och infoga bild

## Introduktion

I den här handledningen kommer du att lära dig **hur man lägger till bild i OneNote** med hjälp av Aspose.Note Java API. Vi går igenom hur du skapar ett OneNote‑dokument från grunden, infogar en bild och sparar resultatet som PDF. Oavsett om du bygger ett rapporteringsverktyg, automatiserar anteckningar eller helt enkelt behöver bädda in grafik programmässigt, ger den här guiden dig en tydlig, praktisk väg.

## Snabba svar
- **Vilket bibliotek behöver jag?** Aspose.Note for Java.  
- **Kan jag infoga valfritt bildformat?** JPEG, PNG, BMP, GIF och fler stöds.  
- **Vilka utdataformat är tillgängliga?** Du kan spara som OneNote, PDF, XPS, HTML, etc.  
- **Behöver jag en licens för produktion?** Ja, en kommersiell licens krävs för icke‑testanvändning.  
- **Är koden plattformsoberoende?** Absolut – Java körs på Windows, Linux och macOS.

## Hur man lägger till bild i OneNote med Java

Att lägga till en bild i OneNote innebär att programmässigt bädda in en bildfil i en OneNote‑sida så att den visas tillsammans med text, outlines eller andra element. Aspose.Note API abstraherar OneNote‑filformatet, så att du kan fokusera på innehållet istället för den underliggande XML‑strukturen.

### Varför infoga bild i OneNote?

- **Automation:** Generera mötesprotokoll med skärmdumpar automatiskt.  
- **Consistency:** Säkerställ att varje sida följer samma layout och varumärke.  
- **Integration:** Kombinera data från andra system (t.ex. diagram) direkt i OneNote‑anteckningsböcker.  
- **Cross‑platform:** Java låter dig köra samma kod på vilken server eller skrivbordsmiljö som helst.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. **Java Development Kit (JDK)** – någon aktuell version (8 eller senare).  
2. **Aspose.Note for Java‑bibliotek** – ladda ner det från den [webbplatsen](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse eller någon annan Java‑kompatibel editor du föredrar.  

## Importera paket

Börja med att importera de nödvändiga klasserna i din Java‑källfil:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Steg‑för‑steg‑guide

### Steg 1: Skapa dokumentet

Skapa ett nytt OneNote‑dokument och en sidbehållare där innehållet kommer att ligga.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Steg 2: Initiera outline

En *outline* fungerar som en behållare för element som text och bilder. Vi sätter dess offset till noll så att innehållet börjar i övre vänstra hörnet.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Steg 3: Ladda och justera bilden

Ladda bilden du vill infoga och justera den till högra sidan av sidan. Detta är där vi faktiskt **lägger till bild i OneNote**. `Image`‑konstruktorn visar hur man **laddar bildfil java** i kod.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Steg 4: Fäst bilden till ett Outline‑element

Omslut bilden i ett `OutlineElement`. Detta steg länkar det visuella objektet till dokumentets outline‑hierarki och **infogar bild i OneNote**.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Steg 5: Sätt ihop dokumentstrukturen

Lägg till outline‑elementet i outline, fäst sedan outline till sidan och lägg slutligen till sidan i dokumentet.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Steg 6: Spara OneNote‑dokumentet

Spara dokumentet på disk. I det här exemplet exporterar vi till PDF, vilket visar hur man **sparar OneNote som PDF** eller **konverterar OneNote till PDF**. Du kan också spara som en inbyggd OneNote‑fil (`.one`) genom att ändra `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Vanliga problem och lösningar

| Problem | Varför det händer | Lösning |
|---------|-------------------|--------|
| **Image not appearing** | Fel filväg eller format som inte stöds. | Verifiera att `dataDir` pekar på rätt mapp och använd en stödjande bildtyp (JPEG, PNG, etc.). |
| **Document saved as empty PDF** | Outline‑offset är felaktigt inställd. | Se till att `setVerticalOffset(0)` och `setHorizontalOffset(0)` anropas, eller justera offset för att placera innehållet inom sidans gränser. |
| **IOException on save** | Destinationsmappen finns inte eller saknar skrivbehörighet. | Skapa mappen i förväg eller kör programmet med lämpliga behörigheter. |

## Vanliga frågor

**Q1: Var kan jag hitta dokumentationen för Aspose.Note för Java?**  
A1: Du kan komma åt dokumentationen [här](https://reference.aspose.com/note/java/).

**Q2: Hur laddar jag ner Aspose.Note för Java?**  
A2: Du kan ladda ner Aspose.Note för Java från [nedladdningssidan](https://releases.aspose.com/note/java/).

**Q3: Finns det en gratis provversion av Aspose.Note för Java?**  
A3: Ja, du kan få en gratis provversion från [webbplatsen](https://releases.aspose.com/).

**Q4: Var kan jag få support för Aspose.Note för Java?**  
A4: För support, besök [Aspose.Note‑forumet](https://forum.aspose.com/c/note/28).

**Q5: Kan jag få en tillfällig licens för Aspose.Note för Java?**  
A5: Ja, du kan begära en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

**Q6: Kan jag använda den här koden för att **spara OneNote som PDF** på en Linux‑server?**  
A6: Absolut. Aspose.Note‑biblioteket är plattformsoberoende, så samma kod fungerar på Windows, Linux och macOS.

**Q7: Stöder API:t **embed image in OneNote** med transparenta PNG‑filer?**  
A7: Ja, PNG‑filer med alfakanaler stöds fullt ut och behåller transparens när de infogas.

---

**Senast uppdaterad:** 2026-03-19  
**Testat med:** Aspose.Note for Java 24.12 (latest)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}