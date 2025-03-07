---
title: Spara till TIFF-bild med hjälp av bildsparalternativ i OneNote
linktitle: Spara till TIFF-bild med hjälp av bildsparalternativ i OneNote
second_title: Aspose.Note Java API
description: Konvertera OneNote-dokument till TIFF och kontrollera filstorlek och kvalitet! Välj Jpeg-, PackBits- eller Faxkomprimering i Java. Få kodexempel och lär dig hur! #OneNote #Java #Aspose
weight: 21
url: /sv/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara till TIFF-bild med hjälp av bildsparalternativ i OneNote

## Introduktion

I den här handledningen kommer du att lära dig hur du sparar ett dokument i ett TIFF-bildformat med hjälp av olika komprimeringsmetoder i Aspose.Note för Java. Vi kommer att täcka förutsättningarna, importera paket och tillhandahålla en steg-för-steg-guide för varje komprimeringsmetod.

## Förutsättningar

Innan du börjar, se till att du har följande:

- Java Development Kit (JDK) installerat på ditt system.
- Aspose.Note för Java-bibliotek nedladdat och konfigurerat.
- Grundläggande förståelse för programmeringsspråket Java.

## Importera paket

Först måste du importera de nödvändiga paketen till din Java-fil:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Steg 1: Spara till TIFF med JPEG-komprimering

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // Sökvägen till dokumentkatalogen.
    String dataDir = "Your Document Directory";

    // Ladda dokumentet i Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  Ladda dokumentet med`Document` klass.
-  Skapa en instans av`ImageSaveOptions` och ange TIFF-komprimeringstypen som JPEG.
- Ställ in önskad kvalitet (valfritt).
- Spara dokumentet i TIFF-format med de angivna alternativen.

## Steg 2: Spara till TIFF med PackBits-komprimering

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // Sökvägen till dokumentkatalogen.
    String dataDir = "Your Document Directory";

    // Ladda dokumentet i Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  Ladda dokumentet med`Document` klass.
-  Skapa en instans av`ImageSaveOptions` och ange TIFF-komprimeringstypen som PackBits.
- Spara dokumentet i TIFF-format med de angivna alternativen.

## Steg 3: Spara till TIFF med CCITT Group 3 Fax Compression

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // Sökvägen till dokumentkatalogen.
    String dataDir = "Your Document Directory";

    // Ladda dokumentet i Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  Ladda dokumentet med`Document` klass.
-  Skapa en instans av`ImageSaveOptions` och ange TIFF-komprimeringstypen som CCITT Group 3 Fax.
- Ställ in färgläget på svartvitt.
- Spara dokumentet i TIFF-format med de angivna alternativen.

## Slutsats

I den här handledningen lärde du dig hur du sparar ett dokument i TIFF-bildformat med olika komprimeringsmetoder i Aspose.Note för Java. Genom att följa steg-för-steg-guiden kan du effektivt utnyttja funktionerna i Aspose.Note för att uppfylla dina krav.

## FAQ's

### F1: Kan jag använda Aspose.Note för Java för att konvertera andra dokumentformat till TIFF?

S1: Ja, Aspose.Note för Java stöder konvertering från olika dokumentformat till TIFF, inklusive OneNote-dokument.

### F2: Vad är betydelsen av att specificera komprimeringstypen när du sparar till TIFF?

S2: Genom att ange komprimeringstypen kan du kontrollera bildkvaliteten och filstorleken. Olika komprimeringsmetoder erbjuder kompromisser mellan kvalitet och kompressionsförhållande.

### F3: Är Aspose.Note för Java lämplig för batchbearbetning av dokument?

S3: Ja, Aspose.Note för Java tillhandahåller API:er för batchbearbetning, vilket gör att du kan automatisera dokumentkonverteringsuppgifter effektivt.

### F4: Kan jag anpassa komprimeringsinställningarna ytterligare?

A4: Ja, du kan justera parametrar som kvalitet, upplösning och komprimeringsmetod för att skräddarsy utdata enligt dina krav.

### F5: Erbjuder Aspose.Note för Java teknisk support?

S5: Ja, Aspose tillhandahåller omfattande teknisk support genom forum och biljettbaserade system.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
