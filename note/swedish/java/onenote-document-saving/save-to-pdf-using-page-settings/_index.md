---
title: Spara till PDF med sidinställningar i OneNote - Aspose.Note
linktitle: Spara till PDF med sidinställningar i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du sparar OneNote-dokument till PDF i Java med Aspose.Note-biblioteket. Steg-för-steg guide med kodexempel för olika sidinställningar.
type: docs
weight: 19
url: /sv/java/onenote-document-saving/save-to-pdf-using-page-settings/
---
## Introduktion

I den här handledningen kommer vi att lära oss hur du sparar OneNote-dokument i PDF-format med hjälp av olika sidinställningar med Aspose.Note för Java. Vi kommer att täcka två metoder: spara med Letter-sidinställningar och spara med A4-sidinställningar utan höjdbegränsning.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar på plats:

1. Java Development Kit (JDK) installerat på ditt system.
2. Aspose.Note för Java-bibliotek nedladdat och inkluderat i ditt Java-projekt.
3. Grundläggande förståelse för programmeringsspråket Java.

## Importera paket

Se till att du har importerat de nödvändiga paketen för att använda Aspose.Note för Java i ditt projekt. Här är importförklaringen:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Spara till PDF med hjälp av Letter Page Settings

### Steg 1: Ladda dokumentet

Först laddar du OneNote-dokumentet i Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Steg 2: Definiera destinationssökväg

Ange destinationssökvägen för PDF-filen:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Steg 3: Spara dokumentet

Spara dokumentet med Letter-sidans inställningar:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Spara till PDF med A4-sidinställningar utan höjdbegränsning

### Steg 1: Ladda dokumentet

På samma sätt laddar du OneNote-dokumentet i Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Steg 2: Definiera destinationssökväg

Ange destinationssökvägen för PDF-filen:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Steg 3: Spara dokumentet

Spara dokumentet med A4-sidor utan höjdbegränsning:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Efter att ha följt dessa steg har du lyckats spara ditt OneNote-dokument till PDF med hjälp av olika sidinställningar.

## Slutsats

I den här handledningen har vi utforskat hur man sparar OneNote-dokument i PDF-format med Aspose.Note för Java-biblioteket. Genom att följa steg-för-steg-guiden kan du enkelt integrera denna funktion i dina Java-applikationer.

## FAQ's

### F1: Kan jag anpassa sidinställningarna ytterligare?

S1: Ja, du kan anpassa sidinställningarna enligt dina krav med Aspose.Note för Java.

### F2: Stöder Aspose.Note andra utdataformat förutom PDF?

S2: Ja, Aspose.Note stöder olika utdataformat inklusive bilder och HTML.

### F3: Är Aspose.Note kompatibel med olika versioner av OneNote-filer?

S3: Ja, Aspose.Note stöder OneNote-filer från olika versioner inklusive .one och .onetoc2.

### F4: Kan jag konvertera flera OneNote-filer till PDF i en enda körning?

S4: Ja, du kan batchbearbeta flera OneNote-filer med Aspose.Note för Java.

### F5: Finns det någon testversion tillgänglig för teständamål?

S5: Ja, du kan få en gratis provversion av Aspose.Note för Java från webbplatsen.