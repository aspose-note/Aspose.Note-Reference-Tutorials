---
title: Spara till gråskalebild i OneNote - Aspose.Note
linktitle: Spara till gråskalebild i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du sparar ett dokument som en gråskalebild i OneNote med Aspose.Note för Java. Hantera enkelt Microsoft OneNote-dokument programmatiskt.
weight: 17
url: /sv/java/onenote-document-saving/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara till gråskalebild i OneNote - Aspose.Note

## Introduktion

I den här handledningen kommer vi att utforska hur man sparar ett dokument som en gråskalebild i OneNote med Aspose.Note för Java. Gråskalebilder är monokromatiska bilder där färginformationen endast representeras av gråtoner. Aspose.Note är ett kraftfullt Java API som tillåter manipulering av Microsoft OneNote-dokument programmatiskt.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. Java Development Kit (JDK) installerat på ditt system.
2.  Aspose.Note för Java-bibliotek. Du kan ladda ner den från[här](https://releases.aspose.com/note/java/).
3. Grundläggande förståelse för Java-programmering.

## Importera paket

För att komma igång, importera nödvändiga paket:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Steg 1: Ladda dokumentet

 Ladda först dokumentet i Aspose.Note. Byta ut`"Your Document Directory"` med sökvägen till din dokumentkatalog och`"Aspose.one"` med namnet på ditt OneNote-dokument.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Steg 2: Ställ in utmatningsväg och alternativ

Definiera utdatasökvägen för gråskalebilden och ange sparalternativen. Vi ställer in färgläget på gråskala.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Steg 3: Spara dokumentet

Slutligen sparar du dokumentet som en gråskalebild med de angivna alternativen.

```java
oneFile.save(dataDir, options);
```

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du sparar ett dokument som en gråskalebild i OneNote med Aspose.Note för Java. Detta kan vara otroligt användbart för olika applikationer där gråskalebilder krävs.

## FAQ's

### F1: Kan jag spara gråskalebilden i ett annat format?

 A1: Ja, det kan du. Ändra helt enkelt`SaveFormat` parametern i`ImageSaveOptions` konstruktor till önskat format.

### F2: Är Aspose.Note kompatibel med alla versioner av OneNote-dokument?

S2: Aspose.Note stöder Microsoft OneNote 2010 och senare.

### F3: Kräver Aspose.Note en licens för att kunna användas?

S3: Ja, du behöver en giltig licens för att använda Aspose.Note i produktionsmiljöer. Du kan dock få en tillfällig licens för teständamål.

### F4: Kan jag manipulera andra aspekter av dokumentet innan jag sparar det som en bild?

A4: Absolut! Aspose.Note tillhandahåller ett brett utbud av funktioner för att redigera OneNote-dokument programmatiskt.

### F5: Var kan jag hitta support om jag stöter på problem?

S5: Du kan hitta support på Aspose.Note-forumet[här](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
