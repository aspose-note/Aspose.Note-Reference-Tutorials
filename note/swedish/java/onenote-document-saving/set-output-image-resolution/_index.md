---
title: Ställ in bildupplösning i OneNote - Aspose.Note
linktitle: Ställ in bildupplösning i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du justerar bildupplösningen i OneNote-dokument med Aspose.Note för Java. Följ vår steg-för-steg-guide för enkel implementering
weight: 23
url: /sv/java/onenote-document-saving/set-output-image-resolution/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ställ in bildupplösning i OneNote - Aspose.Note

## Introduktion

Vill du manipulera upplösningen av bilder i dina OneNote-dokument med Java? Aspose.Note för Java erbjuder en robust lösning för sådana uppgifter. I den här handledningen går vi igenom stegen för att ställa in bildupplösningen med Aspose.Note.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar:

1. Java Development Kit (JDK): Installera JDK på ditt system.
2. Aspose.Note for Java: Ladda ner och installera Aspose.Note for Java från[hemsida](https://releases.aspose.com/note/java/).
3. Integrated Development Environment (IDE): Välj din föredragna IDE som Eclipse eller IntelliJ IDEA.

## Importera paket

Importera de nödvändiga Aspose.Note-paketen i ditt Java-projekt:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Steg 1: Ladda OneNote-dokumentet

Börja med att ladda OneNote-dokumentet i din Java-applikation:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

 Byta ut`"Your Document Directory"` med den faktiska katalogen där ditt OneNote-dokument finns.

## Steg 2: Ställ in alternativ för bildspar

Definiera bildsparalternativen och ange önskad upplösning:

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

 Här ställer vi in upplösningen till`120 dpi`. Du kan justera detta värde enligt dina krav.

## Steg 3: Spara dokumentet med ändrad upplösning

Spara dokumentet med den uppdaterade bildupplösningen:

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

Detta kommer att spara det ändrade dokumentet med den angivna upplösningen.

## Slutsats

I den här handledningen har vi utforskat hur man ställer in bildupplösningen i OneNote-dokument med Aspose.Note för Java. Genom att följa dessa enkla steg kan du effektivt manipulera bildernas upplösning för att möta din applikations krav.


## FAQ's

### F1: Kan jag justera bildupplösningen till ett värde högre än 120 dpi?

S1: Ja, du kan ställa in upplösningen till valfritt värde enligt dina behov.

### F2: Stöder Aspose.Note andra bildformat än JPEG?

S2: Ja, Aspose.Note stöder olika bildformat som PNG, BMP, GIF, etc.

### F3: Är Aspose.Note kompatibel med alla versioner av Java?

S3: Aspose.Note är kompatibel med Java 1.6 eller senare versioner.

### F4: Kan jag manipulera andra aspekter av bilder i OneNote-dokument med Aspose.Note?

S4: Ja, Aspose.Note tillhandahåller omfattande funktioner för bildmanipulering, inklusive storleksändring, beskärning och rotation.

### F5: Var kan jag få support för Aspose.Note-relaterade frågor?

 S5: Du kan söka hjälp från Aspose.Notes communityforum[här](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
