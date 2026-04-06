---
date: 2026-04-06
description: Lär dig hur du skapar OneNote‑dokument och infogar en bild programatiskt
  med Aspose.Note för .NET. Följ enkla steg för att lägga till bilder, ställa in justering
  och mer.
keywords:
- create onenote document
- how to insert image
- insert image onenote
- set image alignment
- multiple images onenote
linktitle: Skapa dokument och infoga bild i Aspose.Note
second_title: Aspose.Note .NET API
title: Skapa OneNote-dokument och infoga bild med Aspose.Note
url: /sv/net/images/build-doc-insert-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa OneNote-dokument och infoga bild med Aspose.Note

## Introduktion

I den här handledningen kommer du att **skapa OneNote-dokument** och lära dig **hur du infogar en bild** i det med hjälp av Aspose.Note för .NET. Aspose.Note ger dig full kontroll över OneNote-filer, vilket gör det enkelt att lägga till rikt innehåll som bilder, tabeller och anpassade layouter programatiskt.

## Snabba svar
- **Vad är huvudsyftet?** Att skapa ett OneNote-dokument och infoga en bild med anpassad justering.  
- **Vilket bibliotek krävs?** Aspose.Note för .NET (ladda ner [här](https://releases.aspose.com/note/net/)).  
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en betald licens krävs för produktion.  
- **Kan jag lägga till flera bilder?** Ja – upprepa infogningsstegen för varje bild (se tipset “multiple images onenote”).  
- **Stöds PDF-konvertering?** Absolut – du kan senare konvertera OneNote-dokumentet till PDF med Aspose.Note:s `Save`-metod i PDF-format.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar:

1. **Visual Studio** – en fullutrustad IDE för .NET‑utveckling.  
2. **Aspose.Note for .NET** – ladda ner och installera biblioteket från den officiella webbplatsen.  
3. **Basic Understanding of C#** – bekantskap med C#‑syntax hjälper dig att följa kodexemplen.

## Importera namnrymder

Låt oss börja med att importera de nödvändiga namnrymderna i ditt C#‑projekt. Dessa namnrymder innehåller klasser och metoder som vi kommer att använda för att utföra dokumentmanipuleringsuppgifter.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Nu ska vi gå igenom processen att bygga ett dokument och infoga en bild i flera steg:

## Steg 1: Skapa dokumentobjekt

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document();
```

Den här koden initierar en ny instans av `Document`‑klassen, som representerar ett OneNote-dokument.

## Steg 2: Initiera sidobjekt

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

Här initierar vi en ny instans av `Page`‑klassen, som representerar en sida i OneNote-dokumentet.

## Steg 3: Initiera outline‑objekt

```csharp
Outline outline = new Outline(doc);
```

`Outline`‑klassen representerar en outline‑nod i dokumenthierarkin. Vi skapar ett nytt outline‑objekt för att strukturera vårt dokument.

## Steg 4: Initiera OutlineElement‑objekt

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

Ett `OutlineElement` representerar ett element inom en outline. Här skapar vi ett nytt outline‑element för att lägga till innehåll i vårt dokument.

## Steg 5: Ladda bild

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg");
```

Vi laddar en bildfil från den angivna sökvägen med `Image`‑klassens konstruktor.

## Steg 6: Ställ in bildjustering

```csharp
image.Alignment = HorizontalAlignment.Right;
```

Den här raden sätter **bildjusteringen** till högra sidan av sidan. Du kan också välja `Left` eller `Center` beroende på dina layoutbehov.

## Steg 7: Lägg till bild i Outline‑element

```csharp
outlineElem.AppendChildLast(image);
```

Här lägger vi till bilden i outline‑elementet, vilket placerar den i dokumentstrukturen.

## Steg 8: Lägg till Outline‑element i Outline

```csharp
outline.AppendChildLast(outlineElem);
```

Vi lägger till outline‑elementet, tillsammans med den infogade bilden, i dokumentets outline‑struktur.

## Steg 9: Lägg till Outline i sida

```csharp
page.AppendChildLast(outline);
```

Outline‑elementet, som innehåller bilden, läggs till i sidans struktur i dokumentet.

## Steg 10: Lägg till sida i dokument

```csharp
doc.AppendChildLast(page);
```

Slutligen lägger vi till sidan, komplett med sitt innehåll, i dokumentet.

## Steg 11: Spara dokument

```csharp
dataDir = dataDir + "BuildDocAndInsertImage_out.one";
doc.Save(dataDir);
```

Den här raden sparar det modifierade OneNote-dokumentet till den angivna platsen. Du kan senare **konvertera OneNote till PDF** genom att anropa `doc.Save("output.pdf")`.

## Varför detta är viktigt

- **Automation** – Att programatiskt skapa OneNote-dokument sparar tid jämfört med manuell redigering.  
- **Consistency** – Att använda kod säkerställer att varje dokument följer samma layout- och stilregler.  
- **Scalability** – Samma metod kan utökas för att infoga **multiple images onenote**‑dokument eller generera rapporter i bulk.

## Vanliga fallgropar & tips

- **Path Issues** – Verifiera alltid att `dataDir` pekar på en giltig mapp; annars misslyckas bildladdningen.  
- **Image Size** – Stora bilder kan öka filstorleken kraftigt; överväg att ändra storlek innan infogning.  
- **Multiple Images** – För att lägga till mer än en bild, upprepa Steg 5‑7 för varje bild och lägg till varje i samma eller olika `OutlineElement`.

## Vanliga frågor

### Q1: Kan jag infoga flera bilder i ett enda dokument med Aspose.Note för .NET?

A1: Absolut! Du kan infoga så många bilder du behöver i ett dokument genom att följa samma infogningssteg för varje bild.

### Q2: Stöder Aspose.Note andra filformat förutom OneNote?

A2: Ja, Aspose.Note erbjuder omfattande stöd för olika filformat, inklusive PDF, DOCX, HTML och mer.

### Q3: Är Aspose.Note lämplig för företagsnivå dokumenthanteringslösningar?

A3: Självklart! Aspose.Note erbjuder robusta funktioner och utmärkt prestanda, vilket gör det till ett idealiskt val för företagsdokumenthantering.

### Q4: Kan jag anpassa utseendet på infogade bilder i dokumentet?

A4: Ja, Aspose.Note erbjuder omfattande alternativ för att anpassa bildens utseende, inklusive justering, storlek och rotation.

### Q5: Var kan jag hitta ytterligare resurser och support för Aspose.Note för .NET?

A5: Du kan utforska Aspose.Note-dokumentationen [här](https://reference.aspose.com/note/net/) och söka hjälp i Aspose‑communityforumet [här](https://forum.aspose.com/c/note/28/).

---

**Senast uppdaterad:** 2026-04-06  
**Testat med:** Aspose.Note 24.11 för .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}