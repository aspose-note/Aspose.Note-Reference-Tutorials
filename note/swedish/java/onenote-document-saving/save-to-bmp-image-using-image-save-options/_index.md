---
title: Spara till BMP-bild med hjälp av bildsparalternativ i OneNote
linktitle: Spara till BMP-bild med hjälp av bildsparalternativ i OneNote
second_title: Aspose.Note Java API
description: Lär dig hur du sparar OneNote-dokument till BMP-bilder programmatiskt med Aspose.Note för Java. Steg-för-steg guide med kodexempel.
weight: 16
url: /sv/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara till BMP-bild med hjälp av bildsparalternativ i OneNote

## Introduktion

Aspose.Note för Java är ett kraftfullt bibliotek som gör det möjligt för Java-utvecklare att arbeta med Microsoft OneNote-filer programmatiskt. Med Aspose.Note för Java kan du skapa, manipulera och konvertera OneNote-dokument sömlöst. I den här handledningen kommer vi att fördjupa oss i hur man sparar ett OneNote-dokument till en BMP-bild med hjälp av Image Save Options från Aspose.Note för Java.

## Förutsättningar

Innan du fortsätter med den här handledningen, se till att du har följande:

1. Grundläggande kunskaper i programmeringsspråket Java.
2. Installerade JDK (Java Development Kit) på ditt system.
3. Integrated Development Environment (IDE) som Eclipse eller IntelliJ IDEA.
4.  Aspose.Note för Java-bibliotek. Du kan ladda ner den från[här](https://releases.aspose.com/note/java/).

## Importera paket

Först måste du importera de nödvändiga paketen från Aspose.Note för Java för att kunna använda dess funktioner. Lägg till följande importsats i din Java-fil:

```java
import com.aspose.note.*;
import java.io.IOException;
```

Låt oss nu dela upp exemplet i flera steg:

## Steg 1: Ladda dokumentet

```java
// Sökvägen till dokumentkatalogen.
String dataDir = "Your Document Directory";

// Ladda dokumentet i Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

 det här steget anger vi sökvägen till katalogen där vårt OneNote-dokument finns. Sedan laddar vi dokumentet med hjälp av`Document` klass tillhandahållen av Aspose.Note för Java.

## Steg 2: Spara till BMP-bild

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Spara dokumentet.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

 I det här steget anger vi utdatasökvägen för BMP-bilden som kommer att genereras från OneNote-dokumentet. Vi använder`save` metod för`Document` klass för att spara dokumentet som en BMP-bild, vilket ger utdatasökvägen och en instans av`ImageSaveOptions` med det önskade`SaveFormat` (I detta fall,`SaveFormat.Bmp`).

## Slutsats

I den här handledningen lärde vi oss hur man sparar ett OneNote-dokument till en BMP-bild med Aspose.Note för Java. Genom att följa steg-för-steg-guiden kan du sömlöst integrera den här funktionen i dina Java-applikationer, vilket gör att du enkelt kan manipulera OneNote-dokument.

## FAQ's

### F1: Kan jag spara OneNote-dokument till andra bildformat än BMP?

S1: Ja, du kan spara OneNote-dokument i olika bildformat som JPEG, PNG, GIF och TIFF med Aspose.Note för Java.

### F2: Stöder Aspose.Note för Java konvertering mellan olika dokumentformat?

S2: Ja, Aspose.Note för Java stöder konvertering mellan OneNote-dokument och andra format som PDF, DOCX, HTML och mer.

### F3: Är Aspose.Note för Java kompatibel med de senaste versionerna av OneNote?

S3: Ja, Aspose.Note för Java uppdateras regelbundet för att säkerställa kompatibilitet med de senaste versionerna av OneNote.

### F4: Kan jag manipulera innehållet i OneNote-dokument programmatiskt med Aspose.Note för Java?

S4: Ja, du kan manipulera innehållet, strukturen och formateringen av OneNote-dokument programmatiskt med Aspose.Note för Java.

### F5: Ger Aspose.Note för Java teknisk support?

 S5: Ja, Aspose tillhandahåller teknisk support för sina produkter. Du kan besöka[Aspose.Note forum](https://forum.aspose.com/c/note/28) för assistens.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
