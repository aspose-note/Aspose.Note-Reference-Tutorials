---
date: 2026-03-19
description: Lär dig hur du lägger till en bild i OneNote med Java och Aspose.Note
  för Java, inklusive hur du ställer in bildens dimensioner i Java och sparar OneNote
  som PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Lägg till bild i OneNote med Java
url: /sv/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Infoga en bild i OneNote-dokument med Java

## Introduktion

I den här handledningen kommer du att lära dig **hur man lägger till en bild i OneNote** programatiskt med Java och Aspose.Note for Java‑biblioteket. Att bädda in bilder i OneNote‑sidor är praktiskt när du behöver skapa mötesprotokoll, automatiserade rapporter eller dokumentation som kombinerar text med visuella data. I slutet av guiden kan du läsa in en befintlig OneNote‑fil, infoga en bild, eventuellt justera dess storlek och position, och till och med **spara OneNote som PDF** – allt utan att öppna OneNote‑gränssnittet.

## Snabba svar
- **Vad är det enklaste sättet att lägga till en bild i OneNote med Java?**  
  Använd Aspose.Note for Javas `Image`‑klass och lägg till den på en sida.
- **Behöver jag en licens för produktionsanvändning?**  
  Ja, en kommersiell licens krävs för produktionsdistributioner.
- **Kan jag ange anpassade dimensioner för bilden?**  
  Absolut – anropa `setWidth()` och `setHeight()` på `Image`‑objektet.
- **Är det möjligt att spara OneNote-filen som PDF efter att ha lagt till bilden?**  
  Ja, anropa `save(..., SaveFormat.Pdf)` för att **spara OneNote som PDF**.
- **Vilken Java-version stöds?**  
  Aspose.Note for Java fungerar med JDK 8 och senare.

## Varför lägga till bild i OneNote?

Att lägga till visuella element gör anteckningarna lättare att förstå och mer engagerande. Bilder kan illustrera diagram, skärmdumpar eller datadiagram som annars skulle kräva långa textbeskrivningar. Att automatisera detta steg sparar tid, särskilt när man genererar stora mängder anteckningar från datakällor.

## Förutsättningar

Innan vi börjar, se till att du har följande redo:

### 1. Java Development Kit (JDK)
Installera JDK 8 eller nyare. Du kan ladda ner den från Oracles webbplats eller använda en OpenJDK‑distribution.

### 2. Aspose.Note for Java Library
Ladda ner det senaste Aspose.Note for Java‑biblioteket och lägg till det i ditt projekts classpath. Detaljerade installationsinstruktioner finns i den officiella [documentation](https://reference.aspose.com/note/java/).

## Importera paket

Börja med att importera de nödvändiga klasserna. Dessa importeringar ger dig tillgång till kärnfunktionaliteten i Aspose.Note samt grundläggande Java‑verktyg.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Steg‑för‑steg guide

Nedan följer en kortfattad, numrerad genomgång. Varje steg innehåller en kort förklaring följt av exakt kod som du kan kopiera.

### Steg 1: Ladda OneNote-dokumentet

Vi skapar en `LoadOptions`‑instans (användbar för framtida anpassningar) och öppnar den befintliga `.one`‑filen.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

### Steg 2: Hämta mål sidan

För enkelhetens skull arbetar vi med den första sidan i dokumentet, men du kan navigera till vilken sida du än behöver.

```java
Page page = oneFile.getFirstChild();
```

### Steg 3: Ladda bilden du vill bädda in

Instansiera ett `Image`‑objekt genom att skicka dokumentreferensen och sökvägen till bildfilen.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

### Steg 4: Ställ in bilddimensioner Java (valfritt)

Om du behöver att bilden ska passa ett specifikt område, justera dess bredd, höjd och förskjutningar. Här kommer det sekundära nyckelordet **set image dimensions java** till nytta.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

### Steg 5: Lägg till bilden på sidan

Metoden `appendChildLast` lägger till bilden som det sista elementet på den valda sidan.

```java
page.appendChildLast(image);
```

### Steg 6: Spara dokumentet – du kan också spara OneNote som PDF

Till sist sparas ändringarna. Exemplet visar hur du sparar filen som PDF, vilket uppfyller det sekundära nyckelordet **save onenote as pdf**.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Vanliga problem och lösningar

| Symptom | Trolig orsak | Lösning |
|---------|--------------|---------|
| `FileNotFoundException` när bilden laddas | Felaktig bildsökväg | Verifiera att `dataDir` och bildfilnamnet är korrekta. |
| Bilden visas förvrängd | Bredd/höjd är felaktigt inställda | Använd bildens originaldimensioner eller beräkna ett korrekt bildförhållande innan du anropar `setWidth`/`setHeight`. |
| PDF-utdata är tom | Saknad licens för Aspose.Note | Applicera en giltig licens innan du anropar `save`. |

## Vanliga frågor

### Q1: Kan jag infoga flera bilder i ett enda OneNote‑dokument med den här metoden?

**A:** Ja. Upprepa helt enkelt Steg 3‑5 för varje bild du vill lägga till, antingen på samma eller på olika sidor.

### Q2: Är Aspose.Note for Java kompatibel med alla versioner av OneNote?

**A:** Aspose.Note for Java stödjer OneNote‑filer som skapats med Microsoft OneNote 2010 och senare versioner.

### Q3: Kan jag infoga bilder i olika format, såsom PNG eller GIF, i ett OneNote‑dokument?

**A:** Absolut. Biblioteket accepterar PNG, JPEG, GIF, BMP och flera andra vanliga format.

### Q4: Finns det en provversion av Aspose.Note for Java för teständamål?

**A:** Ja, du kan ladda ner en gratis provversion från Aspose‑webbplatsen för att utvärdera API‑et innan du köper.

### Q5: Hur kan jag få teknisk support för Aspose.Note for Java?

**A:** Du kan få hjälp genom att besöka [forum](https://forum.aspose.com/c/note/28) som är dedikerat till Aspose.Note‑produkter.

## Slutsats

Du har nu ett komplett, produktionsklart exempel som visar **hur man lägger till en bild i OneNote** med Java, anpassar dess utseende och eventuellt **sparar OneNote som PDF**. Anpassa gärna koden efter dina egna arbetsflöden – oavsett om du bygger en rapporteringsmotor, ett automatiserat dokumentationssystem eller en skräddarsydd anteckningsapplikation.

---

**Last Updated:** 2026-03-19  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}