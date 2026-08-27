---
date: 2026-01-28
description: Lär dig hur du skapar en disposition i OneNote, lägger till en tagg i
  OneNote och genererar PDF från OneNote med Aspose.Note för Java.
linktitle: Create Outline in OneNote and Add Tag – Aspose.Note
second_title: Aspose.Note Java API
title: Skapa disposition i OneNote och lägg till tagg – Aspose.Note
url: /sv/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa disposition i OneNote och lägg till tagg – Aspose.Note

## Introduktion
Letar du efter att **create outline in OneNote** och förbättra samarbetet med taggar med Java? Aspose.Note for Java gör det enkelt att lägga till taggar, strukturera dina anteckningar och till och med **generate PDF from OneNote**-filer. I den här handledningen går vi igenom varje steg, förklarar *varför* varje del är viktig och visar hur du producerar en polerad PDF i slutet.

## Snabba svar
- **Vad betyder “create outline in OneNote”?** Det bygger en hierarkisk struktur (outlines) som organiserar innehåll som rubriker och undersektioner.  
- **Vilket bibliotek lägger till taggar i OneNote?** Aspose.Note for Java tillhandahåller `NoteTag`-klassen för visuella markörer.  
- **Kan jag exportera resultatet till PDF?** Ja – använd `SaveFormat.Pdf` för att **generate PDF from OneNote**.  
- **Behöver jag en licens för produktion?** En tillfällig licens finns tillgänglig för testning; en full licens krävs för kommersiell användning.  
- **Vad är de viktigaste förutsättningarna?** JDK installerat, Aspose.Note for Java-biblioteket och grundläggande Java-kunskaper.

## Vad är “create outline in OneNote”?
Att skapa en outline i OneNote innebär att lägga till `Outline`- och `OutlineElement`-objekt som definierar en trädliknande struktur för dina anteckningar. Denna hierarki låter dig fälla ihop, expandera och organisera information precis som rubriker i ett dokument.

## Varför lägga till tagg i OneNote?
Taggar som stjärnor, kryssrutor eller anpassade ikoner ger läsarna visuella ledtrådar, förbättrar sökbarheten och hjälper team att prioritera objekt. Med Aspose.Note kan du programatiskt bifoga en `NoteTag` till vilken text som helst.

## Förutsättningar
- Java Development Kit (JDK) installerat.  
- Aspose.Note for Java-biblioteket nedladdat. Du kan hämta det [här](https://releases.aspose.com/note/java/).  
- Grundläggande förståelse för Java-programmering.

## Importera paket
Se till att du importerar de nödvändiga paketen för att starta ditt projekt:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
Låt oss gå igenom koden ovan steg för steg.

## Steg 1: Ställ in dokument och sida
Börja med att skapa ett nytt `Document`-objekt och initiera ett `Page`-objekt:
```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```
Här sätter vi sökvägen till dokumentkatalogen, skapar ett nytt `Document` och initierar en `Page`.

## Steg 2: Skapa en outline
Skapa sedan ett `Outline`-objekt för att strukturera ditt innehåll:
```java
Outline outline = new Outline();
```
Outlines ger en hierarkisk struktur till ditt dokument, vilket gör det enkelt att **create outline in OneNote** och hålla information organiserad.

## Steg 3: Initiera OutlineElement och ParagraphStyle
Initiera nu ett `OutlineElement` och sätt `ParagraphStyle` för textformatering:
```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```
`OutlineElement` representerar ett element inom outline, och `ParagraphStyle` definierar egenskaper för textformatering.

## Steg 4: Lägg till RichText med NoteTag
Skapa ett `RichText`-objekt, lägg till din OneNote-text och lägg till en `NoteTag`:
```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
`RichText` låter dig infoga formaterad text, och `NoteTag` **adds tag to OneNote** som en visuell ledtråd.

## Steg 5: Bygg outline-struktur
Lägg till textnoden, outline-elementnoden och outline-noden för att konstruera dokumentets struktur:
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```
Detta steg säkerställer att ditt innehåll är organiserat i dokumentet, vilket slutför processen **create outline in OneNote**.

## Steg 6: Spara dokumentet
Spara dokumentet i PDF-format, vilket **generates PDF from OneNote**:
```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```
Nu är ditt OneNote-dokument med tillagda taggar sparat som en PDF.

Genom att följa dessa steg kan du enkelt förbättra dina OneNote-dokument med Aspose.Note för Java.

## Slutsats
I den här handledningen utforskade vi hur man **create outline in OneNote**, lägger till en tagg i OneNote och sedan **generate PDF from OneNote** med Aspose.Note för Java. Att använda Java ger dig full kontroll över notstruktur, visuell taggning och exportalternativ, vilket gör dina anteckningar mer organiserade och delbara.

## Vanliga frågor
### 1. Kan jag använda Aspose.Note för Java med andra programmeringsspråk?
Aspose.Note stöder främst Java, men det finns också versioner tillgängliga för .NET.

### 2. Är Aspose.Note för Java lämplig för nybörjare?
Ja, Aspose.Note för Java tillhandahåller omfattande dokumentation och support, vilket gör den tillgänglig för både nybörjare och erfarna utvecklare.

### 3. Hur kan jag få en tillfällig licens för Aspose.Note för Java?
Du kan få en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

### 4. Var kan jag hitta ytterligare support?
För eventuella frågor eller hjälp, besök [Aspose.Note-forumet](https://forum.aspose.com/c/note/28).

### 5. Finns det en gratis provperiod?
Ja, du kan utforska en gratis provperiod [här](https://releases.aspose.com/).

**Additional Q&A**

**Q: Kan jag anpassa taggikonen?**  
A: Ja – Aspose.Note tillhandahåller många fördefinierade ikoner via `TagIcon` och tillåter även anpassade bilder.

**Q: Hur ändrar jag PDF-utdatainställningarna?**  
A: Använd `PdfSaveOptions` för att kontrollera bildkvalitet, komprimering och säkerhet innan du anropar `doc.save`.

**Q: Är det möjligt att lägga till flera taggar på samma text?**  
A: Absolut. Anropa `text.getTags().add()` flera gånger med olika `NoteTag`-instanser.

---

**Last Updated:** 2026-01-28  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}