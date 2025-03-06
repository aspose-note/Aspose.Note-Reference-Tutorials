---
title: Lägg till textnod med tagg i OneNote - Aspose.Note
linktitle: Lägg till textnod med tagg i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Utforska hur du lägger till textnoder med taggar i OneNote med Aspose.Note för Java. Enkelt, effektivt och utvecklarvänligt. Ladda ner biblioteket nu!
weight: 13
url: /sv/java/onenote-tag-operations/add-text-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till textnod med tagg i OneNote - Aspose.Note

## Introduktion
I den här handledningen kommer vi att utforska hur man lägger till en textnod med en tagg i OneNote med Aspose.Note för Java. Aspose.Note är ett kraftfullt Java-bibliotek som låter utvecklare arbeta med Microsoft OneNote-filer programmatiskt. Att lägga till textnoder med taggar är ett vanligt krav vid dokumentbehandling, och Aspose.Note förenklar denna uppgift.
## Förutsättningar
Innan vi dyker in i handledningen, se till att du har följande förutsättningar:
- Grundläggande kunskaper i Java-programmering.
-  Aspose.Note för Java-biblioteket installerat. Du kan ladda ner den[här](https://releases.aspose.com/note/java/).
- En integrerad utvecklingsmiljö (IDE) inrättad för Java-utveckling.
## Importera paket
Börja med att importera de nödvändiga paketen för ditt Java-projekt. Inkludera följande importer i din kod:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
## Steg 1: Skapa dokumentobjekt
Initiera ett dokumentklassobjekt för att representera OneNote-dokumentet:
```java
// Sökvägen till dokumentkatalogen.
String dataDir = "Your Document Directory";
//Skapa ett objekt av klassen Document
Document doc = new Document();
```
## Steg 2: Initiera sidklassobjekt
Initiera ett sidklassobjekt för att representera sidan i dokumentet:
```java
// Initiera Sidklassobjekt
Page page = new Page();
```
## Steg 3: Initiera Outline Class Object
Initiera ett Outline-klassobjekt för att strukturera innehållet på sidan:
```java
// Initiera Outline-klassobjekt
Outline outline = new Outline();
```
## Steg 4: Initiera OutlineElement Class Object
Initiera ett OutlineElement-klassobjekt för att representera ett element i konturen:
```java
// Initiera OutlineElement-klassobjekt
OutlineElement outlineElem = new OutlineElement();
```
## Steg 5: Anpassa textstil
Ställ in stilen för textnoden, som teckensnittsfärg, namn och storlek:
```java
// Anpassa textstil
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```
## Steg 6: Skapa RichText-objekt
Skapa ett RichText-objekt och lägg till önskad text till det:
```java
// Skapa RichText-objekt
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```
## Steg 7: Lägg till Note Tag
Lägg till en anteckningstagg, till exempel en gul stjärna, i texten:
```java
// Lägg till anteckningstagg
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
## Steg 8: Lägg till textnod
Lägg till textnoden i konturelementet:
```java
// Lägg till textnod
outlineElem.appendChildLast(text);
```
## Steg 9: Lägg till Outline Element till Outline
Lägg till dispositionselementet till dispositionen:
```java
// Lägg till konturelementnod
outline.appendChildLast(outlineElem);
```
## Steg 10: Lägg till Outline på sidan
Lägg till dispositionen på sidan:
```java
// Lägg till konturnod
page.appendChildLast(outline);
```
## Steg 11: Lägg till sida till dokument
Lägg till sidan i dokumentet:
```java
// Lägg till sidnod
doc.appendChildLast(page);
```
## Steg 12: Spara OneNote-dokument
Spara OneNote-dokumentet i den angivna katalogen:
```java
// Spara OneNote-dokument
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```
Grattis! Du har framgångsrikt lagt till en textnod med en tagg i OneNote med Aspose.Note för Java.
## Slutsats
I den här handledningen täckte vi steg-för-steg-processen att lägga till en textnod med en tagg i OneNote med Aspose.Note för Java-biblioteket. Detta kraftfulla bibliotek förenklar dokumentbearbetningsuppgifter, vilket gör det enkelt för utvecklare att manipulera OneNote-filer programmatiskt.
## Vanliga frågor
### F: Kan jag använda Aspose.Note för Java med andra Java-bibliotek?
S: Ja, Aspose.Note för Java kan sömlöst integreras med andra Java-bibliotek för att förbättra dokumentbehandlingskapaciteten.
### F: Finns det en gratis testversion tillgänglig för Aspose.Note för Java?
 S: Ja, du kan komma åt den kostnadsfria provperioden[här](https://releases.aspose.com/).
### F: Hur kan jag få support för Aspose.Note för Java?
S: Du kan söka stöd från Aspose.Note-communityt[forum](https://forum.aspose.com/c/note/28).
### F: Finns tillfälliga licenser tillgängliga för Aspose.Note för Java?
 S: Ja, du kan få tillfälliga licenser[här](https://purchase.aspose.com/temporary-license/).
### F: Var kan jag hitta dokumentationen för Aspose.Note för Java?
 S: Dokumentationen finns tillgänglig[här](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
