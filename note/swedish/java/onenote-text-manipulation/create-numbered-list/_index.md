---
title: Skapa numrerad lista i OneNote - Aspose.Note
linktitle: Skapa numrerad lista i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du enkelt skapar en numrerad lista i OneNote med Aspose.Note för Java. Ladda ner en gratis testversion och dyk in i Java-utvecklingens värld!
weight: 14
url: /sv/java/onenote-text-manipulation/create-numbered-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa numrerad lista i OneNote - Aspose.Note

## Introduktion
Aspose.Note för Java ger Java-utvecklare möjlighet att sömlöst arbeta med Microsoft OneNote-filer. I den här handledningen går vi igenom processen att skapa en numrerad lista i OneNote med det kraftfulla Aspose.Note for Java-biblioteket.
## Förutsättningar
Innan du dyker in i handledningen, se till att följande förutsättningar är på plats:
- Installerat Java Development Kit (JDK) på din maskin.
-  Aspose.Note för Java-biblioteket hämtat från[här](https://releases.aspose.com/note/java/).
## Importera paket
Låt oss först importera de nödvändiga paketen i ditt Java-projekt för att få ut det mesta av Aspose.Note-funktionerna. Inkludera följande kod i ditt projekt:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
## Steg 1: Initiera dokument-, sida- och dispositionsobjekt
```java
// Din dokumentkatalog
String dataDir = "Your Document Directory";
// Skapa dokument, sida och dispositionsobjekt
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Ställ in standardtextstil
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## Steg 2: Ställ in standardtextstil
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## Steg 3: Skapa konturelement
Låt oss nu skapa elementen för din numrerade lista.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Upprepa för andra element (outlineElem2 och outlineElem3)
```
## Steg 4: Lägga till Outline-element till Outline
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Steg 5: Lägga till Outline på sidan
```java
page.appendChildLast(outline);
```
## Steg 6: Spara dokumentet
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
Följ dessa steg noggrant så skapar du enkelt en numrerad lista i OneNote med Aspose.Note för Java.
## Slutsats
den här handledningen utforskade vi den sömlösa processen att skapa en numrerad lista i OneNote med Aspose.Note för Java. Bibliotekets robusta funktioner gör det till ett ovärderligt verktyg för Java-utvecklare som arbetar med Microsoft OneNote-filer.
## Vanliga frågor
### F: Kan jag anpassa numreringsformatet i min OneNote-lista?
A: Absolut! Du kan anpassa numreringsformatet med klassen NumberList som tillhandahålls av Aspose.Note för Java.
### F: Finns det en testversion tillgänglig för Aspose.Note för Java?
 S: Ja, du kan ladda ner en gratis testversion[här](https://releases.aspose.com/).
### F: Hur kan jag få support för Aspose.Note för Java?
 A: Besök[Aspose.Note för Java-forum](https://forum.aspose.com/c/note/28) för samhällsstöd.
### F: Var kan jag hitta detaljerad dokumentation för Aspose.Note för Java?
 S: Se[dokumentation](https://reference.aspose.com/note/java/) för omfattande information.
### F: Hur köper jag en licens för Aspose.Note för Java?
 A: Du kan köpa en licens[här](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
