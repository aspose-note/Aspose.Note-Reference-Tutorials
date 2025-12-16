---
date: 2025-12-16
description: Lär dig hur du sparar OneNote‑dokument som BMP‑bilder med hjälp av Aspose.Note
  för Javas bildsparalternativ. Se också hur du sparar OneNote till PDF eller PNG.
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: Hur man sparar OneNote till BMP-bild med bildsparalternativ
url: /sv/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man sparar onenote till BMP-bild med Bildsparalternativ

## Introduktion

Aspose.Note for Java är ett kraftfullt bibliotek som gör det möjligt för Java‑utvecklare att programatiskt arbeta med Microsoft OneNote‑filer. **I den här handledningen lär du dig hur du sparar onenote‑dokument till BMP‑bilder** med hjälp av Image Save Options‑funktionen i Aspose.Note for Java. Vi går igenom varje steg, förklarar varför du kan välja BMP framför andra format och visar hur du integrerar denna funktion i dina egna applikationer.

## Snabba svar
- **Vad gör klassen Image Save Options?** Den låter dig ange utdataformat för bilden (BMP, PNG, JPEG osv.) när du konverterar en OneNote‑sida.  
- **Behöver jag en licens för att köra exemplet?** En gratis provversion fungerar för utvärdering, men en kommersiell licens krävs för produktionsanvändning.  
- **Kan jag konvertera en OneNote‑sida till PDF eller PNG istället för BMP?** Ja – ändra helt enkelt `SaveFormat`‑enumet (t.ex. `SaveFormat.Pdf` eller `SaveFormat.Png`).  
- **Vilken Java‑version stöds?** Java 8 och senare stöds fullt ut.  
- **Finns det någon speciell hantering för stora dokument?** Du kan strömma utdata för att undvika hög minnesförbrukning.

## Vad är “Image Save Options” i Aspose.Note?
`ImageSaveOptions`‑klassen ger fin‑granulär kontroll över hur OneNote‑sidor renderas som rasterbilder. Du kan ange bildformat, upplösning, färgdjup och mer. Denna flexibilitet gör det enkelt att generera BMP‑filer för äldre system eller PNG/JPEG‑filer för webbbruk.

## Förutsättningar

1. Grundläggande kunskap om programmeringsspråket Java.  
2. JDK (Java Development Kit) installerat på din maskin.  
3. En IDE såsom Eclipse eller IntelliJ IDEA.  
4. Aspose.Note for Java‑biblioteket – ladda ner det från [här](https://releases.aspose.com/note/java/).

## Importera paket

Först, importera de nödvändiga Aspose.Note‑klasserna och standard Java I/O‑verktygen:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Steg 1: Ladda OneNote‑dokumentet

Här pekar vi på mappen som innehåller källfilen OneNote (`Aspose.one`) och laddar den i ett `Document`‑objekt. Detta objekt ger dig full åtkomst till sidor, sektioner och andra element i anteckningsboken.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Steg 2: Spara dokumentet som en BMP‑bild

Vi sammanfogar filnamnet för utdata och anropar sedan `save` med en `ImageSaveOptions`‑instans konfigurerad för **BMP** (`SaveFormat.Bmp`).  
Om du vill **spara onenote‑sida** som PNG, ersätt helt enkelt `SaveFormat.Bmp` med `SaveFormat.Png`. På samma sätt låter `SaveFormat.Pdf` dig utföra en **onenote‑till‑pdf**‑konvertering.

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

## Varför välja BMP?
- **Förlustfri kvalitet** – BMP lagrar rå pixeldata och bevarar exakt hur den ursprungliga sidan ser ut.  
- **Kompatibilitet** – Äldre Windows‑program kräver ofta BMP‑filer.  
- **Enkelhet** – Ingen komprimeringsartefakter, vilket gör den idealisk för vidare bildbehandling.

## Vanliga problem & tips

- **Fel i filsökväg** – Se till att `dataDir` slutar med rätt filseparator (`/` eller `\`).  
- **Stora anteckningsböcker** – För mycket stora OneNote‑filer, överväg att spara varje sida individuellt för att hålla minnesanvändningen låg.  
- **Licensundantag** – Att köra koden utan en giltig licens kommer att lägga till ett vattenmärke på den genererade bilden.

## Slutsats

I den här guiden demonstrerade vi **hur man sparar onenote**‑dokument till BMP‑bilder med hjälp av Aspose.Note for Java:s `ImageSaveOptions`. Genom att byta `SaveFormat`‑enum kan du även generera PNG, JPEG, PDF eller andra stödda format, vilket ger dig ett flexibelt sätt att exportera OneNote‑innehåll för alla efterföljande scenarier.

## Vanliga frågor

**Q1: Kan jag spara OneNote‑dokument till andra bildformat än BMP?**  
A: Ja, du kan använda `ImageSaveOptions` med `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` eller `SaveFormat.Tiff` för att exportera till dessa format.

**Q2: Stöder Aspose.Note for Java konvertering mellan olika dokumentformat?**  
A: Absolut. Förutom bildformat kan du konvertera OneNote‑filer till PDF, DOCX, HTML och mer med hjälp av lämplig `SaveFormat`.

**Q3: Är Aspose.Note for Java kompatibel med de senaste versionerna av OneNote?**  
A: Ja, biblioteket uppdateras regelbundet för att hålla sig i takt med de senaste OneNote‑utgåvorna.

**Q4: Kan jag manipulera innehållet i OneNote‑dokument programatiskt?**  
A: Ja, du kan lägga till, redigera eller ta bort sidor, sektioner och rikt innehåll (text, bilder, tabeller) via API‑t.

**Q5: Ger Aspose.Note for Java teknisk support?**  
A: Ja, Aspose erbjuder teknisk support och ett dedikerat forum. Besök [Aspose.Note‑forumet](https://forum.aspose.com/c/note/28) för hjälp.

---

**Senast uppdaterad:** 2025-12-16  
**Testat med:** Aspose.Note for Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
