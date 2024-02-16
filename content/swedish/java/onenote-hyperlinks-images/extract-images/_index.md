---
title: Extrahera bilder från OneNote-dokument med Java
linktitle: Extrahera bilder från OneNote-dokument med Java
second_title: Aspose.Note Java API
description: Lär dig hur du extraherar bilder från OneNote-dokument med Java med Aspose.Note-biblioteket. Följ vår steg-för-steg-guide för sömlös bildextraktion.
type: docs
weight: 14
url: /sv/java/onenote-hyperlinks-images/extract-images/
---
## Introduktion

I den här handledningen guidar vi dig genom processen att extrahera bilder från ett OneNote-dokument med hjälp av Java med hjälp av Aspose.Note-biblioteket.

## Förutsättningar

Innan du börjar, se till att du har följande:

1.  Java Development Kit (JDK): Se till att du har Java installerat på ditt system. Du kan ladda ner och installera den från[hemsida](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Aspose.Note-bibliotek: Ladda ner och inkludera Aspose.Note-biblioteket i ditt Java-projekt. Du kan få det från[nedladdningslänk](https://releases.aspose.com/note/java/).

## Importera paket

För att börja, importera nödvändiga paket:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Steg 1: Ladda dokumentet

Ladda först OneNote-dokumentet med Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Steg 2: Hämta alla bilder

Hämta sedan alla bilder från dokumentet:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Steg 3: Extrahera bilder

Gå igenom listan med bilder och spara varje bild i en fil:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Slutsats

Att extrahera bilder från ett OneNote-dokument med Java kan utföras sömlöst med Aspose.Note-biblioteket. Genom att följa stegen som beskrivs i denna handledning kan du enkelt hämta bilder från dina dokument för vidare bearbetning eller analys.

## FAQ's

### F1: Kan jag extrahera bilder från lösenordsskyddade OneNote-dokument?

S1: Ja, Aspose.Note stöder även extrahering av bilder från lösenordsskyddade dokument.

### F2: Är Aspose.Note kompatibel med olika versioner av Java?

S2: Aspose.Note är kompatibel med olika versioner av Java, vilket säkerställer flexibilitet för utvecklare.

### F3: Kan jag extrahera bilder från flera OneNote-dokument i en enda körning?

S3: Absolut, du kan iterera genom flera dokument och extrahera bilder från vart och ett av dem med Aspose.Note.

### F4: Finns det några storleksbegränsningar för OneNote-dokumenten?

A4: Aspose.Note hanterar dokument av olika storlekar effektivt och säkerställer inga begränsningar av dokumentstorleken för bildextraktion.

### F5: Stöder Aspose.Note extrahering av andra typer av innehåll förutom bilder?

S5: Ja, förutom bilder tillåter Aspose.Note extrahering av text, bilagor och andra innehållstyper från OneNote-dokument.