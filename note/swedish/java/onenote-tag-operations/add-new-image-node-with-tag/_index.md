---
title: Lägg till ny bildnod med tagg i OneNote - Aspose.Note
linktitle: Lägg till ny bildnod med tagg i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du lägger till en ny bildnod med en tagg i OneNote med Aspose.Note för Java. Lyft dina Java-programmeringskunskaper utan ansträngning.
weight: 10
url: /sv/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till ny bildnod med tagg i OneNote - Aspose.Note

## Introduktion
Inom Java-programmering framstår Aspose.Note som ett kraftfullt verktyg för att enkelt hantera OneNote-dokument. Om du vill förbättra dina färdigheter och lära dig hur du lägger till en ny bildnod med en tagg i OneNote med Aspose.Note, har du kommit till rätt ställe. Den här steg-för-steg-guiden leder dig genom processen och säkerställer att du förstår varje koncept grundligt.
## Förutsättningar
Innan vi dyker in i handledningen, låt oss se till att du har allt du behöver:
1.  Aspose.Note för Java: Se till att du har Aspose.Note-biblioteket installerat. Om inte kan du ladda ner den[här](https://releases.aspose.com/note/java/).
2. Java-utvecklingsmiljö: Se till att du har en fungerande Java-utvecklingsmiljö inställd på din maskin.
Nu när vi har förutsättningarna på plats, låt oss gå vidare till nästa steg.
## Importera paket
Börja med att importera de nödvändiga paketen i ditt Java-projekt:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Steg 1: Skapa dokumentobjekt
```java
// Sökvägen till dokumentkatalogen.
String dataDir = "Your Document Directory";
// skapa ett objekt av klassen Document
Document doc = new Document();
```
## Steg 2: Initiera sidklassobjekt
```java
// initiera Page klassobjekt
Page page = new Page();
```
## Steg 3: Initiera Outline Class Object
```java
// initiera Outline-klassobjektet
Outline outline = new Outline();
```
## Steg 4: Initiera OutlineElement Class Object
```java
// initiera OutlineElement-klassobjektet
OutlineElement outlineElem = new OutlineElement();
```
## Steg 5: Ladda och infoga bild
```java
// ladda en bild
Image image = new Image(null, dataDir + "Input.jpg");
// infoga bild i dokumentnoden
outlineElem.appendChildLast(image);
```
## Steg 6: Lägg till anteckningstagg till bild
```java
// lägg till en gul stjärna-tagg till bilden
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Steg 7: Lägg till Outline Element Node
```java
// add outline element nod
outline.appendChildLast(outlineElem);
```
## Steg 8: Lägg till Outline Node
```java
// lägg till konturnod
page.appendChildLast(outline);
```
## Steg 9: Lägg till sidnod
```java
// lägg till sidnod
doc.appendChildLast(page);
```
## Steg 10: Spara OneNote-dokument
```java
// spara OneNote-dokument som PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Grattis! Du har framgångsrikt lagt till en ny bildnod med en tagg i OneNote med Aspose.Note för Java.
## Slutsats
 Att behärska Aspose.Note för Java öppnar upp spännande möjligheter i OneNote-dokumentmanipulation. Genom att följa denna handledning har du fått en praktisk färdighet som kan tillämpas på olika projekt. Fortsätt utforska Aspose.Note-dokumentationen[här](https://reference.aspose.com/note/java/)för mer avancerade funktioner och möjligheter.
## Vanliga frågor
### Var kan jag hitta Aspose.Note-dokumentationen?
 Du hittar dokumentationen[här](https://reference.aspose.com/note/java/).
### Hur laddar jag ner Aspose.Note för Java?
 Du kan ladda ner den från releasesidan[här](https://releases.aspose.com/note/java/).
### Finns det en gratis provperiod?
 Ja, du kan komma åt den kostnadsfria provperioden[här](https://releases.aspose.com/).
### Var kan jag få support för Aspose.Note?
 Besök gemenskapsforumet[här](https://forum.aspose.com/c/note/28) för support.
### Behöver jag en tillfällig licens?
 Vid behov kan du få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
