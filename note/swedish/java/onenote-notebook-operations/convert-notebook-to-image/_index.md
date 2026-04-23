---
date: 2026-03-24
description: Lär dig hur du sparar OneNote som bild och konverterar OneNote till bild
  med Aspose.Note för Java. Steg‑för‑steg‑guide för Java‑utvecklare.
linktitle: Save OneNote as Image – Convert Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: Spara OneNote som bild – Konvertera anteckningsbok till bild med Aspose.Note
url: /sv/java/onenote-notebook-operations/convert-notebook-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara OneNote som bild – Konvertera anteckningsbok till bild med Aspose.Note

## Introduktion

I den här handledningen lär du dig **hur du sparar OneNote som bild** genom att konvertera en OneNote‑anteckningsbok till en PNG (eller annat bildformat) med hjälp av Aspose.Note för Java‑biblioteket. Att göra om anteckningssidorna till bilder är praktiskt när du behöver dela anteckningar på plattformar som inte stödjer OneNote‑filer, bädda in dem i PDF‑filer eller inkludera dem i bildspel.

## Snabba svar
- **Vilket bibliotek behövs?** Aspose.Note för Java.  
- **Vilka bildformat stöds?** PNG, JPEG, BMP, GIF, TIFF osv.  
- **Behöver jag en licens?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.  
- **Hur lång tid tar konverteringen?** Vanligtvis några sekunder per anteckningsbok, beroende på storlek.  
- **Kan jag batch‑processa anteckningsböcker?** Ja – loopa bara igenom filerna och återanvänd samma kod.

## Vad är **spara OneNote som bild**?

Att spara OneNote som bild betyder att rendera varje sida i en `.one`‑anteckningsbok till en rasterbildfil (t.ex. PNG). Detta skapar en portabel, endast‑visningsrepresentation som kan visas var som helst utan att OneNote krävs.

## Varför konvertera OneNote till bild?

- **Plattformsoberoende delning** – Mottagare kan visa innehållet på vilken enhet som helst.  
- **Bädda in i dokument** – Infoga bilden i Word, PowerPoint eller PDF‑filer.  
- **Arkivering** – Spara en visuell ögonblicksbild som inte förändras om originalanteckningsboken redigeras.  
- **Presentationsklar** – Använd högupplösta PNG‑filer direkt i bildspel.

## Förutsättningar

Innan du börjar, se till att du har:

1. **Java Development Kit (JDK)** – Ladda ner den senaste JDK:n från [webbplatsen](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).  
2. **Aspose.Note för Java‑bibliotek** – Hämta JAR‑filen från [Aspose‑webbplatsen](https://releases.aspose.com/note/java/) och lägg till den i ditt projekts classpath.

## Importera paket

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Låt oss nu gå igenom konverteringsprocessen steg för steg.

## Steg 1: Läs in anteckningsboksdokumentet

```java
// Specify the directory where your notebook file is located
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

Vi pekar API‑et på mappen som innehåller `Sample1.one` och laddar den i ett `Document`‑objekt. Härifrån kan du komma åt sidor, sektioner och andra anteckningsbokselement.

## Steg 2: Initiera ImageSaveOptions

```java
// Initialize PdfSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` talar om för Aspose.Note hur du vill att utdata ska renderas. I detta exempel väljer vi PNG, men du kan ersätta `SaveFormat.Png` med `SaveFormat.Jpeg`, `SaveFormat.Bmp` osv. för att **konvertera OneNote till bild** i ett annat format.

## Steg 3: Spara dokumentet som bild

```java
// Save the document as PNG
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Anropet `save()` skriver de renderade anteckningssidorna till `ConvertToImage_out.png`. Om anteckningsboken innehåller flera sidor genererar Aspose.Note automatiskt separata bildfiler (t.ex. `ConvertToImage_out_1.png`, `ConvertToImage_out_2.png`).

## Steg 4: Skriv ut bekräftelse

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Ett enkelt konsolmeddelande bekräftar att **spara OneNote som bild**‑operationen lyckades och talar om var du hittar utdatafilen.

## Vanliga problem & tips

- **Stora anteckningsböcker** – Öka JVM‑heapen (`-Xmx`) om du får `OutOfMemoryError`.  
- **Upplösningskontroll** – Använd `options.setResolution(300);` för att öka DPI för utskriftskvalitet.  
- **Batch‑konvertering** – Lägg in stegen ovan i en `for`‑loop som itererar över en lista med `.one`‑filer.  

## FAQ

### Q1: Kan jag konvertera anteckningsböcker till andra bildformat än PNG?

A1: Ja, det går. Aspose.Note‑biblioteket stödjer olika bildformat som JPEG, BMP, GIF, TIFF osv. Du kan ange önskat format i `ImageSaveOptions`‑objektet.

### Q2: Är Aspose.Note kompatibelt med alla versioner av OneNote?

A2: Aspose.Note erbjuder omfattande stöd för olika versioner av OneNote, vilket säkerställer kompatibilitet över olika miljöer och filformat.

### Q3: Kan jag anpassa bildutdatainställningarna under konverteringen?

A3: Absolut. Aspose.Note har många alternativ för att anpassa den genererade bilden, inklusive upplösning, kvalitet, färgdjup och mer. Du kan skräddarsy dessa inställningar efter dina behov.

### Q4: Stöder Aspose.Note batch‑konvertering av flera anteckningsböcker?

A4: Ja, du kan batch‑konvertera flera anteckningsböcker till bilder effektivt med Aspose.Note. Iterera bara igenom din lista med anteckningsfiler och tillämpa konverteringsprocessen som beskrivs i denna handledning.

### Q5: Var kan jag hitta ytterligare resurser och support för Aspose.Note?

A5: För mer dokumentation, exempel och community‑support, besök [Aspose.Note‑forumet](https://forum.aspose.com/c/note/28) och utforska [dokumentationen](https://reference.aspose.com/note/java/).

---

**Senast uppdaterad:** 2026-03-24  
**Testad med:** Aspose.Note för Java 24.8  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}