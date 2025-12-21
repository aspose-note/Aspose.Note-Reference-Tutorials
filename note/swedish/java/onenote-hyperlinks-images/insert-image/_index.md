---
date: 2025-12-21
description: Lär dig hur du lägger till bild i OneNote‑dokument med Java och Aspose.Note
  för Java. Följ vår steg‑för‑steg‑guide för att infoga bilder och eventuellt spara
  OneNote som PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Hur man lägger till en bild i OneNote med Java
url: /sv/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Infoga en bild i OneNote-dokument med Java

## Introduktion

I den här handledningen kommer vi att utforska hur man infogar en bild i ett OneNote-dokument med Java med hjälp av Aspose.Note for Java. Aspose.Note for Java är ett kraftfullt bibliotek som låter utvecklare arbeta med Microsoft OneNote-filer programatiskt, vilket möjliggör olika operationer såsom att skapa, läsa och manipulera OneNote-dokument.

## Snabba svar
- **Vad är det enklaste sättet att lägga till en bild i OneNote med Java?**  
  Använd Aspose.Note for Java's `Image`-klass och lägg till den på en sida.
- **Behöver jag en licens för produktionsbruk?**  
  Ja, en kommersiell licens krävs för produktionsdistributioner.
- **Kan jag ange egna dimensioner för bilden?**  
  Absolut – anropa `setWidth()` och `setHeight()` på `Image`-objektet.
- **Är det möjligt att spara OneNote-filen som PDF efter att ha lagt till bilden?**  
  Ja, anropa `save(..., SaveFormat.Pdf)` för att **spara OneNote som PDF**.
- **Vilken Java-version stöds?**  
  Aspose.Note for Java fungerar med JDK 8 och senare.

## Hur lägger man till en bild i OneNote med Java?

Innan vi dyker ner i koden, låt oss kort diskutera varför du kan vilja programatiskt bädda in bilder i OneNote. Oavsett om du genererar mötesprotokoll, skapar automatiserade rapporter eller bygger en dokumentationspipeline, ger infogning av bilder dina anteckningar en visuell kontext som ren text inte kan erbjuda. Med Aspose.Note for Java kan du göra detta helt i kod, utan att öppna OneNote‑gränssnittet.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar på plats:

### 1. Java Development Kit (JDK)
Se till att du har Java Development Kit (JDK) installerat på ditt system. Du kan ladda ner och installera JDK från Oracles webbplats.

### 2. Aspose.Note for Java Library
Ladda ner och installera Aspose.Note for Java-biblioteket genom att följa [dokumentationen](https://reference.aspose.com/note/java/).

## Importera paket

Börja med att importera de nödvändiga paketen i ditt Java‑projekt. Dessa paket inkluderar Aspose.Note‑biblioteket och andra erforderliga beroenden.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Låt oss dela upp processen för att infoga en bild i ett OneNote‑dokument i flera steg:

## Steg 1: Ladda OneNote‑dokumentet

Först, ladda OneNote‑dokumentet där du vill infoga bilden.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Steg 2: Hämta sidan

Hämta sidan i dokumentet där du vill infoga bilden.

```java
Page page = oneFile.getFirstChild();
```

## Steg 3: Ladda bilden

Ladda bilden som du vill infoga i OneNote‑dokumentet.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Steg 4: Anpassa bildattribut (valfritt)

Valfritt kan du anpassa bildens storlek, placering och justering enligt dina krav. Det är här du **sätter bilddimensioner i Java**‑stil.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Steg 5: Lägg till bilden på sidan

Lägg till bilden på sidan i OneNote‑dokumentet.

```java
page.appendChildLast(image);
```

## Steg 6: Spara dokumentet

Spara det modifierade dokumentet, inklusive den infogade bilden. Du kan också **spara OneNote som PDF** i detta steg.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Slutsats

I den här handledningen har vi lärt oss hur man infogar en bild i ett OneNote‑dokument med Java med hjälp av Aspose.Note for Java‑biblioteket. Genom att följa den steg‑för‑steg‑guiden kan du enkelt integrera bilder i dina OneNote‑dokument programatiskt.

## Vanliga frågor

### Q1: Kan jag infoga flera bilder i ett enda OneNote‑dokument med den här metoden?
Ja, du kan infoga flera bilder i ett enda OneNote‑dokument genom att upprepa processen som beskrivs i den här handledningen för varje bild.

### Q2: Är Aspose.Note for Java kompatibel med alla versioner av OneNote?
Aspose.Note for Java stödjer arbete med OneNote‑filer som skapats i Microsoft OneNote 2010 och senare versioner.

### Q3: Kan jag infoga bilder i olika format, såsom PNG eller GIF, i ett OneNote‑dokument?
Ja, Aspose.Note for Java stödjer infogning av bilder i olika format, inklusive PNG, JPEG, GIF och fler.

### Q4: Finns det en provversion av Aspose.Note for Java tillgänglig för teständamål?
Ja, du kan ladda ner en gratis provversion av Aspose.Note for Java från webbplatsen för utvärderingsändamål.

### Q5: Hur kan jag få teknisk support för Aspose.Note for Java?
Du kan få teknisk support för Aspose.Note for Java genom att besöka [forumet](https://forum.aspose.com/c/note/28) som är dedikerat till Aspose.Note‑produkter.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}