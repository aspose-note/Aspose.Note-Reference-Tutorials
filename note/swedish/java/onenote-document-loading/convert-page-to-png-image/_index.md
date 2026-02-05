---
date: 2026-02-05
description: Lär dig hur du exporterar OneNote‑sidor och sparar OneNote som bild.
  Den här guiden visar hur du konverterar .one‑filer till png, anger sidindex och
  exporterar en OneNote‑sidbild med Aspose.Note för Java.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Hur man exporterar en OneNote-sida till PNG-bild i Java med Aspose.Note
url: /sv/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera OneNote-sida till PNG-bild i Java med Aspose.Note

## Introduktion

I den här handledningen kommer du att upptäcka **hur man exporterar OneNote-sida** till en PNG-bild med hjälp av Aspose.Note för Java-biblioteket. **Hur man exporterar onenote**-sidor är ett vanligt behov när du vill dela anteckningar utanför OneNote-ekosystemet, bädda in dem i rapporter eller bearbeta dem med bildbehandlingsverktyg. Vi går igenom allt du behöver—från att förbereda din miljö till att ange sidindex, konvertera sidan och spara resultatet som en högkvalitativ PNG-fil. I slutet kommer du att kunna **spara onenote som bild** i vilken Java-applikation som helst.

## Snabba svar
- **Vilket bibliotek behövs?** Aspose.Note for Java.  
- **Kan jag exportera en enda sida?** Ja—använd `setPageIndex` för att rikta in den exakta sidan.  
- **Vilka bildformat stöds?** PNG, JPEG, GIF, BMP, TIFF (PNG visas här).  
- **Behöver jag en licens?** En gratis provversion finns tillgänglig; en licens krävs för produktion.  
- **Hur lång tid tar implementeringen?** Vanligtvis under 10 minuter för en grundläggande konvertering.  
- **Hur konverterar man .one till png?** Ladda `.one`-filen med `Document`, ange sidindex och spara med `ImageSaveOptions`.  

## Vad är “exportera OneNote-sida”?
Att exportera en OneNote-sida innebär att konvertera en specifik sida i ett `.one`-dokument till en fristående bildfil (PNG i detta fall). Detta är användbart när du behöver **exportera onenote page image** för delning, inbäddning eller vidare bildbaserad analys.

## Varför använda Aspose.Note för Java för att konvertera OneNote till PNG?
- **Ingen Microsoft Office‑beroende** – fungerar på alla plattformar som kör Java.  
- **Finjusterad kontroll** – du kan välja vilken sida som helst via `setPageIndex`.  
- **Högkvalitativ output** – PNG bevarar vektorgrafik och textklarhet.  
- **Batch‑klar** – enkelt att loopa igenom sidor för masskonvertering, vilket gör det enkelt att **convert onenote to png** för många sidor på en gång.  

## Förutsättningar

Innan du börjar, se till att du har:

1. **Java Development Kit (JDK)** – version 8 eller högre.  
2. **Aspose.Note for Java** – ladda ner den senaste JAR-filen från [Aspose webbplats](https://releases.aspose.com/note/java/).  
3. **Ett OneNote-dokument** (`.one`) som innehåller sidan du vill exportera.

## Importera paket

Först, importera de nödvändiga Java-klasserna:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

Dessa importeringar ger dig åtkomst till kärn-API:et i Aspose.Note, inklusive inläsning av dokument och konfiguration av bild‑sparalternativ.

## Steg‑för‑steg‑guide

### Steg 1: Ladda OneNote-dokumentet

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Vi använder `Document`-klassen för att läsa OneNote-filen från disk. `LoadOptions`-objektet låter dig anpassa inläsningsbeteendet om så behövs. Detta steg är grunden för **convert .one to png**.

### Steg 2: Initiera ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` talar om för Aspose.Note att vi vill ha output i **PNG**-format. Du kan byta till JPEG, BMP osv. genom att ändra `SaveFormat`. Detta objekt låter dig också styra DPI, färgdjup och andra bildspecifika inställningar.

### Steg 3: Ange sidindex (Hur man konverterar OneNote-sida)

```java
// set page index
opts.setPageIndex(0);
```

`setPageIndex`-metoden väljer vilken sida som ska exporteras. Sidnumrering börjar på **0**, så `0` avser den första sidan. Justera detta värde för att **exportera en annan sida** eller för att loopa igenom sidor när du behöver **save onenote as image** för var och en.

### Steg 4: Spara dokumentet som PNG (Spara OneNote som PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Att anropa `save` skriver den valda sidan till en PNG-fil på disk. Filnamnet `ConvertSpecificPageToPngImage_out.png` är bara ett exempel—du kan namnge det hur du vill. Detta sista steg **exports onenote page image** redo för användning i rapporter, webbsidor eller vidare bearbetning.

## Vanliga problem & tips

- **Fel sidindex** – Kom ihåg att indexering börjar på 0. Om du får en tom bild, kontrollera indexvärdet.  
- **Saknad Aspose.Note JAR** – Se till att JAR-filen finns på din classpath; annars får du `ClassNotFoundException`.  
- **Stora sidor** – För mycket stora sidor, överväg att öka JVM:s heap‑storlek (`-Xmx`) för att undvika `OutOfMemoryError`.  
- **Upplösningskontroll** – Använd `opts.setResolution(300)` (eller någon DPI du behöver) innan du anropar `save` för att förbättra bildens klarhet.  

## Vanliga frågor

### Q1: Kan jag konvertera flera sidor till PNG‑bilder på en gång med Aspose.Note för Java?
A1: Ja, du kan loopa igenom dokumentets sidor, uppdatera `opts.setPageIndex(i)`, och anropa `save` för varje iteration.

### Q2: Stöder Aspose.Note för Java andra bildformat förutom PNG?
A2: Absolut. Du kan sätta `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` eller `SaveFormat.Tiff` i `ImageSaveOptions`.

### Q3: Finns det en gratis provversion av Aspose.Note för Java?
A3: Ja, du kan ladda ner en gratis provversion från [webbplatsen](https://releases.aspose.com/).

### Q4: Kan jag få teknisk support om jag stöter på problem med Aspose.Note för Java?
A4: Absolut, du kan söka support i Aspose community‑forum [här](https://forum.aspose.com/c/note/28).

### Q5: Var kan jag köpa en licens för Aspose.Note för Java?
A5: Du kan köpa en licens från [köpsidan](https://purchase.aspose.com/buy).

### Q6: Hur exporterar jag en sida som innehåller inbäddade bilder?
A6: Inbäddade bilder renderas automatiskt i PNG‑utdata; ingen extra kod krävs.

### Q7: Kan jag ställa in DPI eller bildupplösning?
A7: Ja, använd `opts.setResolution(int dpi)` innan du anropar `save` för att kontrollera output‑kvaliteten.

---

**Senast uppdaterad:** 2026-02-05  
**Testad med:** Aspose.Note for Java 24.11 (latest)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}