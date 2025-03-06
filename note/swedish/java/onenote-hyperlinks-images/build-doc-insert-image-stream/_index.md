---
title: Bygg dokument och infoga bild med Stream i OneNote - Java
linktitle: Bygg dokument och infoga bild med Stream i OneNote - Java
second_title: Aspose.Note Java API
description: Lär dig hur du enkelt integrerar bilder i OneNote-dokument med Aspose.Note för Java. Steg-för-steg handledning för Java-utvecklare.
weight: 13
url: /sv/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bygg dokument och infoga bild med Stream i OneNote - Java

## Introduktion

Välkommen till vår omfattande handledning om hur du använder Aspose.Note för Java för att bygga dokument och infoga bilder med bildströmmar i OneNote! I den här handledningen guidar vi dig genom processen steg för steg, så att du har en tydlig förståelse för varje steg. I slutet kommer du att enkelt kunna integrera bilder i dina OneNote-dokument med hjälp av Java.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:

### Java Development Kit (JDK)

Se till att du har Java Development Kit (JDK) installerat på ditt system. Du kan ladda ner den från Oracles webbplats.

### Aspose.Note för Java Library

 Ladda ner och installera Aspose.Note for Java-biblioteket från det medföljande[länk](https://releases.aspose.com/note/java/).

### IDE-inställning

Konfigurera din Integrated Development Environment (IDE) med nödvändiga konfigurationer för att arbeta med Java-projekt.

## Importera paket

För att börja, importera de nödvändiga paketen till ditt Java-projekt. Dessa paket kommer att tillhandahålla den nödvändiga funktionaliteten för att arbeta med OneNote-dokument och bilder.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Steg 1: Konfigurera dokumentkatalog

 Definiera katalogen där ditt dokument och dina bilder finns. Byta ut`"Your Document Directory"` med sökvägen till din katalog.

```java
String dataDir = "Your Document Directory";
```

## Steg 2: Skapa dokumentobjekt

 Initiera en instans av`Document` klass för att börja arbeta med ditt OneNote-dokument.

```java
Document doc = new Document();
```

## Steg 3: Initiera sidobjekt

 Skapa en`Page` objekt för att representera sidan i dokumentet.

```java
Page page = new Page();
```

## Steg 4: Skapa disposition

 Initiera en`Outline` objekt för att strukturera innehållet på sidan.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Steg 5: Skapa dispositionselement

 Skapa en`OutlineElement` för att hålla bilden och ange dess position.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Steg 6: Ladda bildström

 Ladda bildströmmen med hjälp av`FileInputStream` för önskad bild.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Steg 7: Infoga bild

 Infoga bilden i dokumentet genom att skapa en`Image` objekt och ställer in dess inriktning.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Steg 8: Lägg till bild till Outline Element

Lägg till bilden i konturelementet.

```java
outlineElem1.appendChildLast(image);
```

## Steg 9: Lägg till Outline Element till Outline

Lägg till konturelementet till konturen.

```java
outline1.appendChildLast(outlineElem1);
```

## Steg 10: Lägg till disposition på sidan

Lägg till dispositionen på sidan.

```java
page.appendChildLast(outline1);
```

## Steg 11: Lägg till sida till dokument

Lägg till sist sidan till dokumentet.

```java
doc.appendChildLast(page);
```

## Steg 12: Spara dokument

Spara det ändrade dokumentet och ange önskat format (t.ex. PDF).

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Genom att följa dessa steg kan du enkelt bygga dokument och infoga bilder med bildströmmar i OneNote med Aspose.Note för Java.

## Slutsats

Sammanfattningsvis, att behärska integrationen av bilder i dina OneNote-dokument med Java kan avsevärt förbättra din process för att skapa dokument. Med Aspose.Note för Java har du ett kraftfullt verktyg till ditt förfogande för att utföra denna uppgift sömlöst.

## FAQ's

### F1: Är Aspose.Note för Java kompatibel med alla versioner av OneNote?

S1: Aspose.Note för Java stöder olika versioner av OneNote, vilket säkerställer kompatibilitet mellan olika miljöer.

### F2: Kan jag anpassa utseendet på infogade bilder i OneNote-dokument med Aspose.Note för Java?

S2: Ja, du kan anpassa olika aspekter av infogade bilder, såsom justering, storlek och orientering, för att passa dina specifika krav.

### F3: Ger Aspose.Note för Java stöd för andra dokumentformat än PDF?

S3: Ja, Aspose.Note för Java stöder ett brett utbud av dokumentformat, inklusive DOCX, HTML och mer, vilket ger dig flexibilitet i dina dokumenthanteringsuppgifter.

### F4: Var kan jag hitta ytterligare resurser och support för Aspose.Note för Java?

S4: Du kan komma åt dokumentation, nedladdningslänkar, supportforum och tillfälliga licenser för Aspose.Note för Java via de medföljande länkarna.

### F5: Finns det en testversion tillgänglig för Aspose.Note för Java?

S5: Ja, du kan få en gratis testversion av Aspose.Note för Java för att utforska dess funktioner och möjligheter innan du fattar ett köpbeslut.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
