---
date: 2025-12-13
description: Lär dig hur du justerar tröskelvärdet för att konvertera OneNote till
  PNG med Aspose.Note Java, och skapar svartvita OneNote‑bilder med bildbinarisering
  i Java.
linktitle: Save to Binary Image Using Fixed Threshold in OneNote
second_title: Aspose.Note Java API
title: Hur du justerar tröskeln när du sparar OneNote till en binär bild
url: /sv/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man justerar tröskelvärdet när man sparar OneNote till binär bild

## Introduktion

I den här handledningen kommer du att upptäcka **hur man justerar tröskelvärdet** för att exportera en Microsoft OneNote‑sida som en högkontrast, svart‑vit PNG‑bild. Genom att justera det fasta tröskelvärdet får du exakt kontroll över konverteringen, vilket gör det perfekt för scenarier som OCR‑förbehandling eller dokumentarkivering. Vi går igenom varje steg med hjälp av Aspose.Note Java API, så att du snabbt kan **konvertera OneNote till PNG** med pålitliga **image binarization Java**‑tekniker.

## Snabba svar
- **Vad betyder “adjust threshold”?** Det anger pixelintensitetens avklippningsvärde som används när en färgbild konverteras till svart‑vit.
- **Vilket format produceras?** En PNG‑fil som kan öppnas av vilken bildvisare som helst.
- **Kan jag ändra tröskelvärdet?** Ja – ändra anropet `setBinarizationThreshold()`.
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.
- **Är detta kompatibelt med alla OneNote‑versioner?** Aspose.Note stödjer OneNote 2010, 2013, 2016 och senare.

## Förutsättningar

Innan du börjar, se till att du har:

1. Java Development Kit (JDK) installerat.
2. Aspose.Note for Java‑biblioteket nedladdat från [here](https://releases.aspose.com/note/java/).
3. Grundläggande kunskap om Java‑syntax.

## Importera paket

Först, importera de nödvändiga klasserna i din Java‑källfil.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Steg 1: Ladda dokumentet

Ladda OneNote‑filen du vill bearbeta.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Steg 2: Ställ in binariseringalternativ

Definiera **image binarization Java**‑inställningarna och ange det fasta tröskelvärde du vill använda.

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

> **Proffstips:** Experimentera med tröskelvärden mellan 0‑255 för att hitta den optimala inställningen för ditt specifika dokument. Lägre värden ger ljusare bilder, högre värden ger mörkare resultat.

## Steg 3: Ställ in bildens sparalternativ

Konfigurera bildformatet, färgläget och bifoga binariseringalternativen.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

`ColorMode.BlackAndWhite`‑inställningen säkerställer att den slutliga filen är en **black and white OneNote**‑bild.

## Steg 4: Spara dokumentet

Utför sparoperationen med de tidigare definierade alternativen.

```java
oneFile.save(dataDir, options);
```

Efter att koden har körts hittar du en PNG‑fil med namnet `SaveToBinaryImageUsingFixedThreshold_out.png` i din utdata‑mapp, redo för vidare bearbetning eller arkivering.

## Slutsats

Vi har visat **hur man justerar tröskelvärdet** för att skapa en ren, högkontrast PNG från en OneNote‑fil med hjälp av Aspose.Note för Java. Genom att behärska **image binarization Java**‑alternativen kan du på ett pålitligt sätt **konvertera OneNote till PNG** och skapa **black and white OneNote**‑tillgångar för OCR, utskrift eller digital bevarande.

## Vanliga frågor

### Q1: Kan jag justera tröskelvärdet för binarisering?

A1: Ja, du kan justera tröskelvärdet enligt dina krav genom att ändra parametern i metoden `setBinarizationThreshold()`.

### Q2: Är Aspose.Note för Java kompatibel med alla versioner av Microsoft OneNote?

A2: Aspose.Note för Java stödjer olika versioner av Microsoft OneNote inklusive 2010, 2013 och 2016.

### Q3: Finns det några begränsningar för storleken på dokument som kan bearbetas?

A3: Aspose.Note för Java har inga begränsningar för storleken på dokument som kan bearbetas, vilket gör att du kan hantera stora filer effektivt.

### Q4: Kan jag konvertera flera OneNote‑dokument samtidigt?

A4: Ja, du kan batch‑bearbeta flera OneNote‑dokument genom att iterera över varje fil och tillämpa de nödvändiga operationerna.

### Q5: Finns teknisk support för Aspose.Note för Java?

A5: Ja, teknisk support finns tillgänglig via [Aspose.Note forum](https://forum.aspose.com/c/note/28), där du kan ställa frågor och få hjälp av experter.

## Vanliga frågor

**Q: Vad händer om jag sätter tröskelvärdet för lågt?**  
A: Den resulterande bilden kan bli urtvättad, med många gråtoner kvar istället för skarp svart‑vit kontrast.

**Q: Kan jag använda en annan binariseringmetod?**  
A: Ja, Aspose.Note stödjer även adaptiv tröskelvärdesättning; ersätt helt enkelt `BinarizationMethod.FixedThreshold` med `BinarizationMethod.Adaptive`.

**Q: Är det möjligt att exportera direkt till andra format som JPEG?**  
A: Absolut—byt `SaveFormat.Png` till `SaveFormat.Jpeg` i `ImageSaveOptions`‑konstruktorn hanterar jag lösenordsskyddade OneNote‑filer?**  
A: Ladda dokumentet med den lämpliga overload‑metoden som accepterar en lösenordsträng innan du tillämpar binariseringstegen.

**Q: Fungerar detta tillvägagångssätt på Linux/macOS?**  
A: Aspose.Note Java‑biblioteket är plattformsoberoende, så samma kod körs på alla operativsystem med en kompatibel JDK.

---

**Senast uppdaterad:** 2025-12-13  
**Testad med:** Aspose.Note for Java 24.12 (senaste)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}