---
date: 2025-12-09
description: Lär dig hur du sparar OneNote som PDF med formaterad rik text i Java
  med Aspose.Note för Java. Följ vår steg‑för‑steg‑guide för sömlös dokumentautomatisering.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: Spara OneNote som PDF med formaterad rik text i Java
url: /sv/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara OneNote som PDF med formaterad Rich Text i Java

## Introduktion

Om du behöver **spara OneNote som PDF** samtidigt som du bevarar rich‑text‑formatering, har du kommit till rätt ställe. I den här handledningen går vi igenom hur du skapar ett OneNote‑dokument, tillämpar anpassade stilar och exporterar det direkt till PDF med Aspose.Note för Java. När du är klar har du ett återanvändbart kodexempel som du kan klistra in i vilket Java‑projekt som helst för att automatisera snygga OneNote‑till‑PDF‑konverteringar.

## Snabba svar
- **Vad lär den här handledningen ut?** Hur du skapar ett OneNote‑dokument med formaterad text och sparar det som en PDF.  
- **Vilket bibliotek krävs?** Aspose.Note för Java (nedladdningsbart från den officiella webbplatsen).  
- **Behöver jag en licens?** En tillfällig licens fungerar för testning; en full licens krävs för produktion.  
- **Vilken IDE kan jag använda?** Vilken Java‑IDE som helst – IntelliJ IDEA, Eclipse eller NetBeans.  
- **Kan jag ändra utdataformatet?** Ja, Aspose.Note stödjer PDF, HTML, PNG och mer.

## Vad betyder “save onenote as pdf”?
Att spara OneNote som PDF innebär att konvertera OneNote‑sidans struktur – inklusive text, bilder och formatering – till en statisk PDF‑fil som kan visas på vilken plattform som helst utan att behöva OneNote.

## Varför formatera rich text i Java?
Att applicera rich‑text‑formatering (typsnitt, färger, stilar) direkt i Java låter dig generera dokument som ser professionella ut och följer dina varumärkesriktlinjer utan manuellt redigeringsarbete.

## Förutsättningar

1. **Java Development Kit (JDK)** – någon aktuell version (8 eller högre).  
2. **Aspose.Note för Java JAR** – ladda ner den från [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse eller någon annan editor du föredrar.  

## Importera paket

Först måste du importera de nödvändiga paketen till ditt Java‑projekt. Lägg till följande import‑satser i början av din Java‑fil:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Steg 1: Skapa dokument och sida

Låt oss börja med att initiera `Document`‑ och `Page`‑objekten:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Steg 2: Skapa titel med formatering

Nu skapar vi en titel med formaterad text:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## Steg 3: Skapa rich text med formatering

Därefter skapar vi rich text olika formateringsstilar:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## Steg 4: Lägg till element på sidan och i dokumentet

Nu lägger vi till titeln och rich text på sidan samt i dokumentets struktur:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Steg 5: Spara dokumentet

Slutligen sparar vi det skapade OneNote‑dokumentet som en PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Vanliga problem och lösningar

| Problem | Lösning |
|-------|----------|
| **File not found** | Verifiera att `dataDir` pekar på en befintlig mapp och att du har skrivrättigheter. |
| **Missing fonts** | Säkerställ att de typsnitt du refererar till (t.ex. *Calibri*) är installerade på värddatorn. |
| **License not applied** | Ladda din Aspose‑licens innan du skapar `Document` för att undvika evaluerings‑vattenstämplar. |

## Vanliga frågor

**Q: Kan jag anpassa teckensnittsstilarna ytterligare?**  
A: Ja, du kan justera ytterligare egenskaper såsom understrykning, genomstrykning och textjustering via klasserna `TextStyle` och `ParagraphStyle`.

**Q: Är Aspose.Note för Java kompatibel med alla Java‑IDE:er?**  
A: Absolut. Så länge IDE:n stödjer standard Java‑utveckling kan du lägga till Aspose.Note‑JAR‑filen i projektets classpath.

**Q: Kan jag integrera denna funktionalitet i webbapplikationer?**  
A: Ja, samma kod fungerar i servlet‑baserade eller Spring Boot‑applikationer, vilket möjliggör dynamisk OneNote‑till‑PDF‑generering på serversidan.

**Q: Finns det licenskrav för att använda Aspose.Note för Java?**  
A: En kommersiell licens krävs för produktionsbruk. En tillfällig licens finns tillgänglig för utvärdering och testning.

**Q: Stöder Aspose.Note för Java andra dokumentformat än OneNote?**  
A: Ja, den stödjer PDF, HTML, PNG, JPEG och flera andra exportformat, vilket ger dig flexibilitet att konvertera OneNote‑sidor till det format du behöver.

## Slutsats

I den här guiden har vi demonstrerat hur du **sparar OneNote som PDF** samtidigt som du applicerar rich‑text‑formatering med Aspose.Note för Java. Genom att följa steg‑för‑steg‑instruktionerna kan du automatisera skapandet av välformade OneNote‑dokument och konvertera dem till PDF i vilken Java‑baserad lösning som helst.

---

**Senast uppdaterad:** 2025-12-09  
**Testad med:** Aspose.Note för Java 24.11 (senaste vid skrivtillfället)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}