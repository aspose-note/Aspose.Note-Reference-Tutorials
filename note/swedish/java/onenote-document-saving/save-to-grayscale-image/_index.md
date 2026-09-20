---
date: 2026-06-30
description: Lär dig hur du exporterar OneNote genom att spara ett dokument som en
  gråskalebild i PNG-format med Aspose.Note för Java. Inkluderar steg för att läsa
  in OneNote-dokumentet och skapa en gråskalebild.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Exportera OneNote som gråskalebild – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: Exportera OneNote som gråskalebild – Aspose.Note
url: /sv/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara som gråskala bild i OneNote - Aspose.Note

## Introduktion

I den här handledningen kommer du att upptäcka **how to export onenote** genom att konvertera en OneNote `.one`-fil till en högkvalitativ gråskala PNG-bild med Aspose.Note för Java. Gråskalakonvertering är ofta behövd av Java‑utvecklare för utskrift, arkivering eller för att **reduce OneNote size** utan att förlora viktigt innehåll. Vi kommer att gå igenom att ladda ett OneNote‑dokument, konfigurera sparalternativen—inklusive **adjust image resolution**—och slutligen spara dokumentet som en PNG.

## Snabba svar
- **What does “how to export onenote” mean?** Det betyder att programatiskt konvertera en OneNote‑fil till ett annat format, såsom en bild, med kod.  
- **Which format is best for grayscale output?** PNG fungerar bra eftersom det bevarar förlustfri kvalitet och stödjer ett dedikerat gråskalefärgläge.  
- **Do I need a license?** En giltig Aspose.Note‑licens krävs för produktionsbruk; en tillfällig provlicens finns tillgänglig för testning.  
- **What Java version is required?** Java 8 eller högre rekommenderas.  
- **Can I change the image size?** Ja, du kan justera `ImageSaveOptions`‑egenskaper som `Resolution` eller `PageSize` innan du sparar.

## Vad är “how to export onenote”?

Att exportera OneNote betyder att programatiskt konvertera en OneNote `.one`‑fil till en annan representation—såsom PDF, HTML eller en bild. I den här guiden fokuserar vi på **creating grayscale PNG**‑bilder, ett vanligt krav för dokumentation eller utskriftsklara arbetsflöden. Med Aspose.Note sker konverteringen helt i minnet, så du behöver aldrig ha Microsoft OneNote installerat på servern.

## Varför exportera OneNote som en gråskalebild?

Gråskala‑PNG är vanligtvis **30‑40 % mindre** än sina färgade motsvarigheter, vilket snabbar upp webbleverans och minskar lagringskostnader. De ger också **clearer contrast** på laserskrivare, vilket gör rapporter lättare att läsa. Eftersom PNG är universellt stödjande fungerar de resulterande filerna i webbläsare, mobila enheter och skrivbordsredigerare utan extra codecs.

## Förutsättningar

1. Java Development Kit (JDK) 8 eller nyare installerat.  
2. Aspose.Note för Java‑bibliotek – ladda ner den senaste versionen från [here](https://releases.aspose.com/note/java/).  
3. Grundläggande förståelse för Java‑syntax och Maven/Gradle‑projektuppsättning.  

## Importera paket

`ImageSaveOptions`‑klassen styr hur dokumentet renderas till en bild.  
`ColorMode` är en uppräkning som låter dig växla mellan full‑color och gråskalautmatning.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Steg 1: Ladda OneNote‑dokumentet

`Document` representerar en OneNote‑anteckningsbok och tillhandahåller metoder för att ladda, redigera och spara dess innehåll. Först, **load the OneNote document** i Aspose.Note. Ersätt `"Your Document Directory"` med sökvägen till din lokala mapp och `"Aspose.one"` med namnet på din OneNote‑fil.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Steg 2: Ange utsökväg och alternativ

`ImageSaveOptions` konfigurerar hur ett OneNote‑dokument renderas till en bildfil. `ColorMode`‑uppräkning väljer färgrenderingsläget, såsom gråskala eller full‑color. Definera utsökvägen för gråskalebilden och specificera sparalternativen. Vi kommer att sätta `ColorMode` till `GrayScale` och använda **save document as PNG**‑formatet. Du kan också **adjust image resolution** till 300 DPI för högkvalitativa utskrifter.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Steg 3: Spara dokumentet

Slutligen, spara dokumentet som en gråskala PNG‑bild med de konfigurerade alternativen. `save`‑metoden skriver filen till disk utan att kräva några mellansteg eller temporära filer.

```java
oneFile.save(dataDir, options);
```

## Vanliga problem och lösningar
- **FileNotFoundException** – Verifiera att `dataDir` pekar på rätt mapp och att `.one`‑filen finns.  
- **LicenseException** – Säkerställ att du har applicerat en giltig Aspose.Note‑licens innan du anropar `save`.  
- **Low‑resolution output** – Justera `options.setResolution(300)` för att öka DPI; högre DPI ger skarpare utskrifter men större filstorlekar.  

## Vanliga frågor

**Q1: Kan jag spara gråskalebilden i ett annat format?**  
A1: Ja, ändra helt enkelt `SaveFormat`‑parametern i `ImageSaveOptions`‑konstruktorn till `Jpeg`, `Bmp` eller någon av de 20+ stödda bildformaten.

**Q2: Är Aspose.Note kompatibel med alla versioner av OneNote‑dokument?**  
A2: Aspose.Note stödjer Microsoft OneNote 2010 och senare, vilket täcker över 95 % av de anteckningsböcker som är i aktiv användning idag.

**Q3: Kräver Aspose.Note en licens för att använda?**  
A3: En giltig licens krävs för produktionsbruk, men en tillfällig provlicens kan erhållas för utvärdering utan kostnad.

**Q4: Kan jag manipulera andra aspekter av dokumentet innan jag sparar det som en bild?**  
A4: Absolut! Aspose.Note tillhandahåller API:er för att redigera sektioner, sidor och enskilda element såsom text, tabeller och bilder innan export.

**Q5: Var kan jag hitta support om jag stöter på problem?**  
A5: Du kan hitta support på Aspose.Note‑forumet [here](https://forum.aspose.com/c/note/28).

## Slutsats

Du har nu lärt dig **how to export onenote** genom att ladda en OneNote‑fil, konfigurera sparalternativen för att **create a grayscale image**, och **saving the document as PNG**. Detta tillvägagångssätt är idealiskt för att generera lätta, utskriftsklara visualiseringar från OneNote‑anteckningsböcker. Känn dig fri att experimentera med andra `ColorMode`‑inställningar, högre DPI‑värden eller alternativa bildformat för att matcha ditt projekts krav.

---

**Senast uppdaterad:** 2026-06-30  
**Testat med:** Aspose.Note 27.0 for Java  
**Författare:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Exportera OneNote‑sida till PNG‑bild i Java med Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote set jpeg resolution – Ställ in utskriftsbildens upplösning i OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Hur man sparar OneNote som PDF med Aspose.Note för Java](/note/java/onenote-document-loading/load-save-format/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}