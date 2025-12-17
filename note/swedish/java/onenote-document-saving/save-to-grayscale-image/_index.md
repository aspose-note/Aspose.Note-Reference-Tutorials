---
date: 2025-12-17
description: Lär dig hur du exporterar OneNote genom att spara ett dokument som en
  gråskalebild i PNG-format med Aspose.Note för Java. Inkluderar steg för att läsa
  in OneNote‑dokumentet och skapa en gråskalebild.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: Hur man exporterar OneNote som gråskalebild – Aspose.Note
url: /sv/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara som gråskalebild i OneNote - Aspose.Note

## Introduktion

I den här handledningen visar vi dig **hur man exporterar onenote** genom att spara ett dokument som en gråskalebild med Aspose.Note för Java. Gråskalebilder är monokroma bilder som bara innehåller nyanser av grått, vilket kan vara användbart för utskrift, arkivering eller för att minska filstorleken. Vi går igenom hur man laddar ett OneNote‑dokument, konfigurerar sparalternativen för att **skapa en gråskalebild**, och slutligen **spara dokumentet som PNG**.

## Snabba svar
- **Vad betyder “how to export onenote”?** Det avser att konvertera en OneNote‑fil till ett annat format, t.ex. en bild, programmässigt.  
- **Vilket format är bäst för gråskalautmatning?** PNG fungerar bra eftersom det bevarar förlustfri kvalitet och stödjer gråskalefärgläge.  
- **Behöver jag en licens?** En giltig Aspose.Note‑licens krävs för produktionsanvändning; en tillfällig provlicens finns tillgänglig för testning.  
- **Vilken Java‑version krävs?** Java 8 eller högre rekommenderas.  
- **Kan jag ändra bildstorleken? Ja, du kan justera `ImageSaveOptions`‑egenskaper som `Resolution` eller `PageSize` innan du sparar.

## Vad är “how to export onenote”?
Att exportera OneNote innebär att programmässigt konvertera en OneNote‑`.one`‑fil till en annan representation—t.ex. PDF, HTML eller en bild. I den här guiden fokuserar vi på att exportera till en **gråskala‑PNG**‑bild, vilket är ett vanligt krav för dokumentation eller utskriftsarbetsflöden.

## Varför exportera OneNote som en gråskalebild?
- **Minskad filstorlek** – GråskalepNG är vanligtvis mindre än färgbilder.  
- **Bättre läsbarhet** – För utskrivna rapporter ger gråskala ofta tydligare kontrast.  
- **Kompatibilitet** – PNG stöds brett i webbläsare, redigeringsprogram och mobila enheter.  

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. Java Development Kit (JDK) installerat på ditt system.  
2. Aspose.Note för Java‑biblioteket. Du kan ladda ner det från [here](https://releases.aspose.com/note/java/).  
3. Grundläggande förståelse för Java‑programmering.  

## Importera paket

För att komma igång, importera de nödvändiga paketen:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Steg 1: Ladda OneNote‑dokumentet

Först, **load onenote document** into Aspose.Note. Replace `"Your Document Directory"` with the path to your local folder and `"Aspose.one"` with the name of your OneNote file.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Steg 2: Ange utsökväg och alternativ

Define the output path for the grayscale image and specify the saving options. We'll set the `ColorMode` to `GrayScale` and use the **save document as png** format.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Steg 3: Spara dokumentet

Finally, save the document as a grayscale PNG image using the configured options.

```java
oneFile.save(dataDir, options);
```

## Vanliga problem och lösningar
- **FileNotFoundException** – Verifiera att `dataDir` pekar på rätt mapp och att `.one`‑filen finns.  
- **LicenseException** – Se till att du har applicerat en giltig Aspose.Note‑licens innan du anropar `save`.  
- **Lågupplöst utdata** – Justera `options.setResolution(300)` för att öka DPI om det behövs.

## Vanliga frågor

**Q1: Kan jag spara gråskalebilden i ett annat format?**  
A1: Ja, ändra helt enkelt `SaveFormat`‑parametern i `ImageSaveOptions`‑konstruktorn till `Jpeg`, `Bmp` osv.

**Q2: Är Aspose.Note kompatibel med alla versioner av OneNote‑dokument?**  
A2: Aspose.Note stödjer Microsoft OneNote 2010 och senare versioner.

**Q3: Kräver Aspose.Note en licens för att använda?**  
A3: En giltig licens krävs för produktionsanvändning, men en tillfällig provlicens kan erhållas för utvärdering.

**Q4: Kan jag manipulera andra aspekter av dokumentet innan jag sparar det som en bild?**  
A4: Absolut! Aspose.Note erbjuder ett omfattande API för att redigera sektioner, sidor och innehåll innan export.

**Q5: Var kan jag hitta support om jag stöter på problem?**  
A5: Du kan hitta support på Aspose.Note‑forumet [here](https://forum.aspose.com/c/note/28).

## Slutsats

Du har nu lärt dig **hur man exporterar onenote** genom att ladda en OneNote‑fil, konfigurera sparalternativen för att **skapa en gråskalebild**, och **spara dokumentet som PNG**. Denna teknik är praktisk för att skapa lätta, utskriftsklara visualiseringar från OneNote‑anteckningsböcker. Känn dig fri att experimentera med andra `ColorMode`‑inställningar eller bildformat för att passa ditt projekts behov.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose  

---