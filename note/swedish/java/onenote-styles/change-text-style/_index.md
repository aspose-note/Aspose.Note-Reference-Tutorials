---
date: 2026-01-18
description: Lär dig hur du ställer in teckenfärg i Java i OneNote med Aspose.Note,
  markerar text, ändrar teckenstorlek och sparar OneNote som PDF. Steg‑för‑steg‑guide
  med kod.
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Ställ in teckenfärg Java i OneNote – Aspose.Note
url: /sv/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ställ in teckensnittsfärg Java i OneNote – Aspose.Note

## Introduktion

I den här handledningen kommer du att upptäcka hur du **ställer in teckensnittsfärg Java** för text i ett OneNote-dokument med Aspose.Note för Java API. Vi går igenom att ladda en `.one`-fil, komma åt dess RichText‑noder, applicera färg, markering och teckenstorleksändringar, och slutligen **spara OneNote som PDF**. Oavsett om du behöver **markera text onenote**, **ändra teckenstorlek onenote**, eller helt enkelt ändra den övergripande textstilen, ger stegen nedan en komplett, produktionsklar lösning.

## Snabba svar
- **Kan jag ändra teckensnittsfärgen för specifika ord?** Ja – iterera genom `TextRun`-objekt och anropa `setFontColor`.
- **Tillåter Aspose.Note mig att spara OneNote som PDF?** Absolut; använd `document.save("output.pdf")`.
- **Vilken Java-version krävs?** Java 8 eller högre.
- **Stöds markering?** Använd `setHighlight(Color)` på `TextStyle`.
- **Kan jag konvertera OneNote till PDF på en rad?** Inte direkt, men `save`‑metoden hanterar konverteringen.

## Vad är “set font color java”?

Frasen avser att programatiskt tilldela en ny teckensnittsfärg till textelement i en OneNote‑fil med Java‑kod. Med Aspose.Note får du full kontroll över stilattribut som teckensnittsfärg, markering och storlek utan att öppna OneNote‑gränssnittet.

## Varför ändra textstil onenote?

- **Förbättrad läsbarhet** – färgad eller markerad text drar uppmärksamhet till viktiga punkter.
- **Varumärkeskonsekvens** – upprätthåll företagsfärger i mötesanteckningar.
- **Exportkvalitet** – stilade anteckningar ser professionella ut när du **konverterar onenote till pdf** för delning.

## Förutsättningar

1. Grundläggande kunskaper i Java‑programmering.  
2. JDK 8 eller nyare installerat.  
3. Aspose.Note för Java‑biblioteket tillagt i ditt projekt (Maven/Gradle eller manuell JAR).  
4. En exempel‑OneNote‑fil (`Sample1.one`) att experimentera med.  

## Importera paket

Först, importera de klasser vi behöver:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## Steg‑för‑steg‑guide

### Steg 1: Ladda dokumentet

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

Vi laddar OneNote‑filen (`Sample1.one`) så att Aspose.Note kan arbeta med dess interna struktur.

### Steg 2: Åtkomst till RichText‑noder

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

`RichText`‑objekt innehåller de faktiska styckena. Genom att hämta den första noden får vi ett grepp om den text vi vill formatera.

### Steg 3: Ändra textstil (set font color java)

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

Inuti loopen **ställer vi in teckensnittsfärg Java** till gult, applicerar en blå markering (som demonstrerar **highlight text onenote**), och ökar storleken till 20 punkter, vilket illustrerar **modify font size onenote**.

### Steg 4: Spara dokumentet (save onenote as pdf)

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

Genom att anropa `save` med en `.pdf`‑extension konverteras automatiskt **convert onenote to pdf**, vilket ger dig en färdig att dela‑fil.

## Vanliga problem & lösningar

| Problem | Orsak | Lösning |
|-------|--------|-----|
| Ingen färgändring synlig | Dokumentet var öppnat i OneNote innan det sparades | Stäng OneNote eller ladda om filen efter att Java‑processen är klar |
| Markering inte tillämpad | Använder en färg som matchar bakgrunden | Välj en kontrasterande `Color` (t.ex. `Color.yellow`) |
| `document.save` kastar `IOException` | Ogiltig utskrivningssökväg | Säkerställ att katalogen finns och att du har skrivrättigheter |

## Vanliga frågor

**Q: Kan jag applicera dessa stiländringar endast på vissa sektioner i min OneNote‑fil?**  
A: Ja – filtrera `RichText`‑noder efter deras föräldra‑`Section` eller `Page` innan du itererar över `TextRun`s.

**Q: Förutom färg, markering och storlek, vilken annan formatering kan Aspose.Note hantera?**  
A: Du kan ändra teckensnittsfamilj, fet/kursiv/understruken, justering och till och med styckeavstånd.

**Q: Är det möjligt att batch‑processa flera OneNote‑filer?**  
A: Absolut. Lägg in laddnings‑ och stil‑logiken i en loop som bearbetar varje `.one`‑fil i en mapp.

**Q: Stöder biblioteket att spara direkt till andra format som DOCX?**  
A: Ja – Aspose.Note kan exportera till PDF, DOCX, HTML och flera bildformat.

**Q: Var kan jag hitta fler exempel och API‑referens?**  
A: Besök den officiella Aspose.Note‑dokumentationssidan, utforska API‑referensen och ladda ner gratisprovversionen för praktisk testning.

## Slutsats

Du har nu ett komplett, end‑to‑end‑exempel på hur du **ställer in teckensnittsfärg Java**, markerar text, justerar teckenstorlek och **sparar OneNote som PDF** med Aspose.Note. Känn dig fri att anpassa koden för att rikta in dig på specifika sidor, tillämpa villkorlig formatering eller integrera den i större dokument‑bearbetningspipelines.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-18  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose