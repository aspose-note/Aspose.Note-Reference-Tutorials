---
title: Skapa dokument med rot- och undersidor i OneNote
linktitle: Skapa dokument med rot- och undersidor i OneNote
second_title: Aspose.Note Java API
description: Skapa ett dokument med rot- och undersidor i OneNote med Aspose.Note för Java. Följ steg-för-steg-guiden för att effektivt organisera dina anteckningar.
type: docs
weight: 11
url: /sv/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## Introduktion

I den här handledningen guidar vi dig genom processen att skapa ett dokument med rot- och undersidor i OneNote med Aspose.Note för Java. Genom att följa dessa steg kan du effektivt organisera dina OneNote-dokument med hierarkisk struktur.

## Förutsättningar

Innan du börjar, se till att du har följande förutsättningar:

1. Java Development Kit (JDK): Se till att du har JDK installerat på ditt system.
2. Aspose.Note for Java: Ladda ner och installera Aspose.Note for Java från[hemsida](https://purchase.aspose.com/buy).
3. Integrated Development Environment (IDE): Välj en Java IDE som IntelliJ IDEA, Eclipse eller NetBeans.

## Importera paket

Börja med att importera de nödvändiga paketen i ditt Java-projekt:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Steg 1: Konfigurera dokumentkatalog

Definiera katalogen där du vill spara ditt OneNote-dokument:

```java
String dataDir = "Your Document Directory";
```

## Steg 2: Skapa dokumentobjekt

 Instantiera en`Document` objekt:

```java
Document doc = new Document();
```

## Steg 3: Skapa sidor

Initiera sidobjekt och ställ in deras nivåer:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Steg 4: Lägg till noder på sidor

### Lägga till noder på första sidan

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Lägga till noder på andra sidan

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Lägga till noder på tredje sidan

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Steg 5: Lägg till sidor i dokumentet

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Steg 6: Spara dokumentet

Spara OneNote-dokumentet:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Hantera undantag
}
```

Grattis! Du har framgångsrikt skapat ett dokument med rot- och undersidor i OneNote med Aspose.Note för Java.

## Slutsats

Att organisera dina OneNote-dokument med hierarkisk struktur är avgörande för bättre hantering och navigering. Med Aspose.Note för Java kan du effektivt skapa dokument med rot- och undersidor, vilket ger en tydlig och organiserad layout för dina anteckningar.

## FAQ's

### F1: Kan jag skapa flera nivåer av undersidor med Aspose.Note för Java?

S1: Ja, du kan skapa flera nivåer av undersidor genom att ställa in lämplig nivå för varje sida.

### F2: Är Aspose.Note for Java kompatibelt med olika Java IDE:er?

S2: Ja, Aspose.Note för Java är kompatibel med populära Java IDEs som IntelliJ IDEA, Eclipse och NetBeans.

### F3: Kan jag anpassa formateringen av text i mitt OneNote-dokument?

S3: Ja, du kan anpassa teckensnitt, färg, storlek och andra formateringsalternativ med Aspose.Note för Javas rika textfunktioner.

### F4: Stöder Aspose.Note för Java att spara dokument i olika format?

S4: Ja, Aspose.Note för Java stöder att spara dokument i olika format inklusive BMP, PDF, PNG och mer.

### F5: Finns det en testversion tillgänglig för Aspose.Note för Java?

S5: Ja, du kan ladda ner en gratis testversion av Aspose.Note för Java från webbplatsen.