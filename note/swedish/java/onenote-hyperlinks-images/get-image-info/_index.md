---
title: Få bildinformation från OneNote med Java
linktitle: Få bildinformation från OneNote med Java
second_title: Aspose.Note Java API
description: Extrahera bildinformation från OneNote-dokument i Java! Få bildmått, filnamn och mer. Enkla steg & kodexempel ingår. #OneNote #Java #Aspose
weight: 15
url: /sv/java/onenote-hyperlinks-images/get-image-info/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Få bildinformation från OneNote med Java

## Introduktion

Inom Java-utvecklingen är det en vanlig uppgift att extrahera information från olika dokumentformat. OneNote, en populär plattform för anteckningar, innehåller ofta bilder vid sidan av text. Att hämta bildinformation programmatiskt från OneNote-filer med Java kan effektivisera arbetsflöden för dokumentbearbetning. I den här handledningen kommer vi att fördjupa oss i hur man extraherar bilddetaljer från OneNote-dokument med Aspose.Note för Java.

## Förutsättningar

Innan vi går in i implementeringen, se till att du har följande förutsättningar på plats:

### 1. Java Development Kit (JDK)

Se till att du har Java Development Kit (JDK) installerat på ditt system. Du kan ladda ner och installera den senaste JDK från[Oracle hemsida](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Aspose.Note för Java Library

 Ladda ner och inkludera Aspose.Note for Java-biblioteket i ditt projekt. Du kan hämta biblioteket från[nedladdningssida](https://releases.aspose.com/note/java/).

### 3. OneNote-dokument

Förbered ett exempel på OneNote-dokument som innehåller bilder. Detta dokument kommer att användas för att extrahera bildinformation programmatiskt.

## Importera paket

För att börja, importera nödvändiga paket från Aspose.Note för Java:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

Låt oss dela upp koden ovan i steg-för-steg-instruktioner:

## Steg 1: Ställ in dokumentkatalog

```java
String dataDir = "Your Document Directory";
```

 Byta ut`"Your Document Directory"` med sökvägen till ditt OneNote-dokument.

## Steg 2: Ladda dokumentet

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Ladda OneNote-dokumentet med Aspose.Note för Java-biblioteket. Se till att du anger rätt sökväg till ditt dokument.

## Steg 3: Hämta alla bilder

```java
List<Image> list = doc.getChildNodes(Image.class);
```

Hämta alla bilder från det inlästa OneNote-dokumentet.

## Steg 4: Skriv ut totalt antal bilder

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

Skriv ut det totala antalet bilder som finns i dokumentet.

## Steg 5: Gå igenom och skriv ut bildinformation

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

Gå igenom listan med bilder och skriv ut detaljer som bredd, höjd, originalmått, filnamn och senast ändrad tid för varje bild.

## Slutsats

Genom att följa stegen som beskrivs i denna handledning kan du effektivt hämta bildinformation från OneNote-dokument med hjälp av Java med hjälp av Aspose.Note for Java-biblioteket. Genom att integrera denna funktion i dina applikationer kan uppgifter relaterade till dokumentbehandling automatiseras, vilket ökar effektiviteten och produktiviteten.

## FAQ's

### F1: Kan Aspose.Note för Java hantera andra dokumentformat förutom OneNote?

S1: Ja, Aspose.Note för Java stöder olika dokumentformat, inklusive OneNote, PDF och Microsoft Word.

### F2: Är Aspose.Note för Java lämplig för både personlig och kommersiell användning?

S2: Ja, du kan använda Aspose.Note för Java för både personliga och kommersiella ändamål.

### F3: Erbjuder Aspose.Note för Java teknisk support?

 S3: Ja, teknisk support är tillgänglig via Aspose-forumen på[här](https://forum.aspose.com/c/note/28).

### F4: Kan jag prova Aspose.Note för Java innan jag köper?

 S4: Ja, du kan utforska en gratis testversion av Aspose.Note för Java från[Aspose.Note för Java](https://releases.aspose.com/note/java/).

### F5: Hur kan jag få en tillfällig licens för Aspose.Note för Java?
 
 S5: Du kan skaffa en tillfällig licens från[Tillfällig licens/](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
