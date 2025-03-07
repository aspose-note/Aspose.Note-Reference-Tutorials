---
title: Bygg dokument och infoga bild i OneNote med Java
linktitle: Bygg dokument och infoga bild i OneNote med Java
second_title: Aspose.Note Java API
description: Lär dig hur du bygger OneNote-dokument och infogar bilder med Aspose.Note för Java. Steg-för-steg handledning för sömlös integration.
weight: 12
url: /sv/java/onenote-hyperlinks-images/build-doc-insert-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bygg dokument och infoga bild i OneNote med Java

## Introduktion

I den här handledningen kommer vi att utforska hur du använder Aspose.Note för Java för att bygga OneNote-dokument och infoga bilder i dem. Aspose.Note är ett kraftfullt Java API som gör det möjligt för utvecklare att arbeta med Microsoft OneNote-filer programmatiskt. Vi kommer att dela upp varje steg i detalj för att guida dig genom processen.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar:

1. Java Development Kit (JDK): Se till att du har JDK installerat på ditt system.
2.  Aspose.Note for Java-bibliotek: Ladda ner och installera Aspose.Note for Java-biblioteket från[hemsida](https://releases.aspose.com/note/java/).
3. IDE (Integrated Development Environment): Använd valfri Java-stödd IDE som IntelliJ IDEA eller Eclipse för kodning.

## Importera paket

Börja med att importera de nödvändiga paketen i din Java-kod:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Steg 1: Konfigurera dokumentet

Skapa först ett nytt OneNote-dokument och initiera nödvändiga objekt:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Steg 2: Initiera Outline

Ställ in dispositionen för dokumentet och ange offsetegenskaper:

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## Steg 3: Lägg till bild

Ladda en bild och ange dess justering:

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Steg 4: Lägg till bild till Outline Element

Bifoga bilden till ett konturelement:

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## Steg 5: Lägg till disposition och sidnoder

Lägg till kontur- och sidnoderna i dokumentet:

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Steg 6: Spara dokument

Slutligen, spara OneNote-dokumentet:

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du bygger OneNote-dokument och infogar bilder i dem med Aspose.Note för Java. Genom att följa dessa steg kan du effektivt hantera och manipulera OneNote-filer i dina Java-program.

## FAQ's

### F1: Var kan jag hitta dokumentationen för Aspose.Note för Java?

 S1: Du kan komma åt dokumentationen[här](https://reference.aspose.com/note/java/).

### F2: Hur laddar jag ner Aspose.Note för Java?

 S2: Du kan ladda ner Aspose.Note för Java från[nedladdningssida](https://releases.aspose.com/note/java/).

### F3: Finns det en gratis testversion tillgänglig för Aspose.Note för Java?

 A3: Ja, du kan få en gratis provperiod från[hemsida](https://releases.aspose.com/).

### F4: Var kan jag få support för Aspose.Note för Java?

 S4: För support, besök[Aspose.Note forum](https://forum.aspose.com/c/note/28).

### F5: Kan jag få en tillfällig licens för Aspose.Note för Java?

 A5: Ja, du kan begära en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
