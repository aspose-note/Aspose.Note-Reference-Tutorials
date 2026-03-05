---
date: 2026-03-05
description: Lär dig hur du sparar OneNote som PDF samtidigt som du skapar en numrerad
  lista med Aspose.Note för Java. Inkluderar steg för att ställa in standardtextstil
  och anpassa numrering.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: Spara OneNote som PDF – Skapa numrerad lista med Aspose.Note
url: /sv/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara OneNote som PDF – Skapa numrerad lista med Aspose.Note

## Introduktion
Aspose.Note for Java ger Java‑utvecklare möjlighet att **spara OneNote som PDF** och berika dokumentet med avancerad formatering, såsom numrerade listor. I den här handledningen går vi igenom hela processen – från att ställa in en standardtextstil till att anpassa numreringsformatet – så att du kan exportera OneNote till PDF med ett professionellt utseende.

## Snabba svar
- **Vad täcker den här handledningen?** Skapa en numrerad lista i OneNote och spara filen som PDF med Aspose.Note for Java.  
- **Vilket primärt nyckelord är inriktat?** *save onenote as pdf*  
- **Behöver jag en licens?** En gratis provversion finns tillgänglig; en kommersiell licens krävs för produktion.  
- **Vilken Java‑version krävs?** JDK 8 eller senare.  
- **Hur lång tid tar implementeringen?** Ungefär 10–15 minuter för en grundläggande lista.

## Vad är “save OneNote as PDF”?
Att spara OneNote som PDF konverterar den rika OneNote‑sidan till ett portabelt, fast layout‑dokument som kan delas över plattformar utan att kräva OneNote. Detta är särskilt användbart för arkivering, rapportering eller distribution av innehåll till användare som inte har OneNote installerat.

## Varför skapa en numrerad lista innan export?
En numrerad lista ger struktur och läsbarhet, vilket får den exporterade PDF‑filen att se ut som en polerad rapport. Med Aspose.Note kan du **anpassa numreringsformat**, ange teckensnitt och kontrollera avstånd – allt medan du bevarar OneNotes ursprungliga layout.

## Förutsättningar
- Java Development Kit (JDK) installerat på din maskin.  
- Aspose.Note for Java‑biblioteket nedladdat från [here](https://releases.aspose.com/note/java/).  

## Importera paket
Först importerar du de nödvändiga klasserna så att du kan arbeta med OneNote‑objekt och PDF‑konvertering.

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

## Hur man sparar OneNote som PDF med en numrerad lista?
Nedan följer en steg‑för‑steg‑guide som visar **hur man skapar list**‑element, **ställer in standardtextstil**, och slutligen **exporterar OneNote till PDF**.

### Steg 1: Initiera dokument, sida och outline‑objekt
Vi börjar med att skapa de grundläggande OneNote‑strukturerna. Detta demonstrerar också användning av **add outline element java**.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Proffstips:** Håll `dataDir`‑sökvägen absolut eller använd `System.getProperty("user.dir")` för att undvika sökvägsproblem.

### Steg 2: Ställ in standardtextstil
En konsekvent stil säkerställer att listan ser enhetlig ut över alla objekt.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### Steg 3: Skapa outline‑element (Numrerad lista)
Här **anpassar vi numreringsformatet** med `NumberList`. Mönstret `"{0})"` ger “1)”, “2)”, osv.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **Varför detta är viktigt:** Genom att fästa en `NumberList` på varje `OutlineElement` får du full kontroll över numreringsstil, teckensnitt och storlek.

### Steg 4: Lägg till outline‑element i outline‑en
Nu samlar vi de enskilda listobjekten i ett enda outline.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Steg 5: Fäst outline på sidan
Outline blir en del av OneNote‑sidans hierarki.

```java
page.appendChildLast(outline);
```

### Steg 6: Spara dokumentet som PDF
Till sist **sparar vi OneNote som PDF**. Utdatafilen kommer att innehålla den numrerade listan exakt som definierad.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

När du kör koden ovan genereras en PDF med namnet `CreateNumberedList_out.pdf` i den angivna katalogen, vilket bevarar det numrerade listformatet.

## Vanliga problem och lösningar
| Problem | Lösning |
|-------|----------|
| **PDF är tom** | Se till att `doc.appendChildLast(page);` anropas innan `doc.save()`. |
| **Numrering visas inte** | Verifiera att `NumberList`‑mönster och `NumberFormat` är korrekt inställda. |
| **Fil‑ej‑hittad‑fel** | Använd en absolut sökväg för `dataDir` eller skapa katalogen i förväg. |
| **Fel teckensnitt** | Installera teckensnittet (t.ex. Arial) på maskinen som kör koden. |

## Vanliga frågor
### Q: Kan jag anpassa numreringsformatet i min OneNote‑lista?
A: Absolut! Du kan anpassa numreringsformatet med hjälp av `NumberList`‑klassen som tillhandahålls av Aspose.Note for Java.

### Q: Finns det en provversion av Aspose.Note for Java?
A: Ja, du kan ladda ner en gratis provversion [here](https://releases.aspose.com/).

### Q: Hur kan jag få support för Aspose.Note for Java?
A: Besök [Aspose.Note for Java forum](https://forum.aspose.com/c/note/28) för gemenskapsstöd.

### Q: Var kan jag hitta detaljerad dokumentation för Aspose.Note for Java?
A: Se [documentation](https://reference.aspose.com/note/java/) för omfattande information.

### Q: Hur köper jag en licens för Aspose.Note for Java?
A: Du kan köpa en licens [here](https://purchase.aspose.com/buy).

## Slutsats
I den här handledningen visade vi hur man **sparar OneNote som PDF** samtidigt som man skapar en ren, numrerad lista med Aspose.Note for Java. Genom att ställa in en standardtextstil, anpassa numreringsformatet och följa steg‑för‑steg‑guiden kan du snabbt och pålitligt generera professionella PDF‑filer från OneNote‑sidor.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2026-03-05  
**Testat med:** Aspose.Note for Java 24.11  
**Författare:** Aspose