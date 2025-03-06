---
title: Spara till binär bild med hjälp av fast tröskel i OneNote
linktitle: Spara till binär bild med hjälp av fast tröskel i OneNote
second_title: Aspose.Note Java API
description: Spara enkelt Microsoft OneNote-dokument som binära bilder med hjälp av fast tröskelvärde med Aspose.Note Java. Öka dina OneNote-filmanipuleringsmöjligheter.
weight: 14
url: /sv/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara till binär bild med hjälp av fast tröskel i OneNote

## Introduktion

Aspose.Note för Java är ett kraftfullt API som låter utvecklare arbeta med Microsoft OneNote-filer programmatiskt. I den här handledningen kommer vi att utforska hur man sparar ett dokument som en binär bild med hjälp av en fast tröskel. Följ stegen nedan för att uppnå detta.

## Förutsättningar

Innan du börjar, se till att du har följande:

1. Java Development Kit (JDK) installerat på ditt system.
2.  Aspose.Note för Java-bibliotek nedladdat. Du kan ladda ner den från[här](https://releases.aspose.com/note/java/).
3. Grundläggande kunskaper i Java-programmering.

## Importera paket

Importera först de nödvändiga paketen till din Java-fil.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Steg 1: Ladda dokumentet

Ladda OneNote-dokumentet med Aspose.Note API.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Steg 2: Ställ in binariseringsalternativ

Definiera binäriseringsalternativen för att spara dokumentet som en binär bild.

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

## Steg 3: Ställ in alternativ för bildspar

Ställ in alternativ för bildspar, inklusive färgläge och binariseringsalternativ.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## Steg 4: Spara dokumentet

Spara dokumentet som en binär bild med de angivna alternativen.

```java
oneFile.save(dataDir, options);
```

## Slutsats

den här handledningen lärde vi oss hur man sparar ett dokument som en binär bild med hjälp av en fast tröskel i Aspose.Note för Java. Genom att följa dessa steg kan du enkelt manipulera OneNote-filer programmatiskt.

## FAQ's

### F1: Kan jag justera tröskelvärdet för binarisering?

 S1: Ja, du kan justera tröskelvärdet enligt dina krav genom att ändra`setBinarizationThreshold()` metodparameter.

### F2: Är Aspose.Note för Java kompatibel med alla versioner av Microsoft OneNote?

S2: Aspose.Note för Java stöder olika versioner av Microsoft OneNote inklusive 2010, 2013 och 2016.

### F3: Finns det några begränsningar för storleken på dokument som kan behandlas?

S3: Aspose.Note för Java har inga begränsningar för storleken på dokument som kan bearbetas, vilket gör att du kan hantera stora filer effektivt.

### F4: Kan jag konvertera flera OneNote-dokument samtidigt?

S4: Ja, du kan batchbearbeta flera OneNote-dokument genom att iterera över varje fil och använda de nödvändiga åtgärderna.

### F5: Finns teknisk support tillgänglig för Aspose.Note för Java?

 S5: Ja, teknisk support är tillgänglig via[Aspose.Note forum](https://forum.aspose.com/c/note/28), där du kan ställa frågor och söka hjälp från experter.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
