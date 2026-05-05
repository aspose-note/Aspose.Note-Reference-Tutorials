---
date: 2026-05-05
description: Lär dig hur du infogar bild i Aspose.Note‑dokument med .NET. Denna steg‑för‑steg‑guide
  visar dig hur du justerar bild, lägger till bild på sidan och förbättrar visuellt
  innehåll.
keywords:
- how to insert image
- how to align image
- append image to page
linktitle: Infoga bilder i Aspose.Note‑dokument
second_title: Aspose.Note .NET API
title: Hur man infogar bild i Aspose.Note-dokument med .NET
url: /sv/net/images/insert-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man infogar bild i Aspose.Note-dokument med .NET

## Introduktion

Om du vill göra dina Aspose.Note-filer mer engagerande, **how to insert image** är den första färdigheten du vill behärska. I den här handledningen går vi igenom de exakta stegen du behöver för att lägga till bilder, kontrollera deras storlek, placera dem exakt och även justera dem på det sätt du vill. I slutet kommer du att känna dig bekväm med att infoga bilder, justera dem och lägga till bild på sidan — allt med ren, läsbar C#-kod.

## Snabba svar
- **Vilket bibliotek krävs?** Aspose.Note for .NET  
- **Kan jag ställa in bildstorlek programatiskt?** Yes – use the Width and Height properties.  
- **Hur placerar jag en bild?** Adjust HorizontalOffset, VerticalOffset or use alignment options.  
- **Finns det någon gräns för bildformat?** JPG, PNG, BMP, GIF and others are supported.  
- **Behöver jag en licens för produktion?** A valid Aspose.Note license is required for commercial use.

## Vad är bildinfogning i Aspose.Note?

Att infoga en bild innebär att skapa ett Aspose.Note.Image‑objekt, konfigurera dess visuella egenskaper och fästa det på en sida i en OneNote‑kompatibel .one‑fil. Detta låter dig berika anteckningar med skärmdumpar, diagram eller någon visuell hjälp.

## Varför infoga bilder med Aspose.Note?

- **Bättre kommunikation:** Visuals clarify complex ideas faster than text alone.  
- **Enhetlig layout:** Programmatic control ensures every document follows the same design standards.  
- **Automatiseringsvänligt:** Ideal for generating reports, tutorials, or batch‑processed notebooks.

## Förutsättningar

1. Aspose.Note for .NET: Download and install Aspose.Note for .NET from [here](https://releases.aspose.com/note/net/).  
2. Image Files: Ha bildfilerna (JPG, PNG, etc.) du planerar att bädda in redo på disken.

## Importera namnrymder

Vi börjar med att importera namnrymderna som ger oss åtkomst till fil‑I/O och Aspose.Note‑API:n.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## Steg 1: Ladda dokument och hämta sida

Först, öppna det befintliga .one‑dokumentet och hämta sidan där bilden kommer att placeras.

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## Hur man justerar bild

Innan vi lägger till bilden, bestäm hur den ska placeras i förhållande till annat innehåll. Aspose.Note erbjuder horisontella justeringsalternativ (Left, Center, Right). Du kan också finjustera placeringen med offset‑värden.

## Steg 2: Ladda bild och ställ in egenskaper

Skapa Image‑objektet, peka det på din fil och definiera dess dimensioner, offset‑värden och justering.

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // Set image width
    Height = 100,               // Set image height
    HorizontalOffset = 100,     // Set horizontal offset
    VerticalOffset = 400,       // Set vertical offset
    Alignment = HorizontalAlignment.Right  // Set image alignment
};
```

## Lägg till bild på sidan

Nu när bilden är fullt konfigurerad, fäst den i sidans elementträd.

```csharp
page.AppendChildLast(image);
```

## Vanliga fallgropar och tips

- **Felaktiga offset:** Remember that offsets are measured from the top‑left corner of the page. A large vertical offset may push the image off‑screen.  
- **Ej stödd format:** If you try a format that isn’t recognized, Aspose.Note will throw an exception—convert the file to JPG or PNG first.  
- **Licensvarningar:** Running without a license adds a watermark to the generated document; always apply your license in production.

## Slutsats

Du har nu lärt dig **how to insert image** i ett Aspose.Note‑dokument, hur man **how to align image**, och hur man **append image to page** med några enkla rader C#. Dessa tekniker låter dig automatiskt bygga rikare, mer professionella anteckningsböcker.

## Vanliga frågor

### Q1: Kan jag infoga bilder av vilket format som helst i Aspose.Note-dokument?

A1: Ja, Aspose.Note stöder olika bildformat inklusive JPG, PNG, BMP, GIF, etc.

### Q2: Är det möjligt att ändra storlek på de infogade bilderna programatiskt?

A2: Absolut! Du kan justera bredd och höjd på bilderna enligt dina preferenser vid infogning.

### Q3: Ger Aspose.Note alternativ för att ändra bildjustering?

A3: Ja, du kan justera bilder till vänster, höger eller centrerat inom dina dokumentsidor.

### Q4: Kan jag infoga flera bilder på en enda sida i mitt dokument?

A4: Självklart! Du kan infoga så många bilder du behöver på en enda sida med Aspose.Note.

### Q5: Finns det någon gräns för filstorleken på bilder som kan infogas?

A5: Aspose.Note har inga strikta begränsningar för bildfilers storlek, men det rekommenderas att optimera bilder för bättre prestanda.

## Vanligt förekommande frågor

**Q: Hur laddar jag en bild från en ström istället för en filsökväg?**  
A: Använd Image(Stream, Document)‑konstruktorn och skicka en MemoryStream som innehåller bildens byte.

**Q: Kan jag ändra bilden efter att den har lagts till på sidan?**  
A: Ja, du kan ändra Width, Height, HorizontalOffset, VerticalOffset och Alignment‑egenskaperna för det befintliga Image‑objektet och sedan anropa page.Update().

**Q: Är det möjligt att lägga till en bildtext under bilden?**  
A: Infoga ett RichText‑element efter bilden och sätt dess text för att fungera som en bildtext.

**Q: Stöder Aspose.Note animerade GIF-filer?**  
A: Animerade GIF-filer behandlas som statiska bilder; endast den första ramen visas.

**Q: Vad ska jag göra om bilden blir suddig?**  
A: Säkerställ att källbilden har tillräcklig upplösning och undvik att skala upp den bortom dess ursprungliga storlek.

---

**Senast uppdaterad:** 2026-05-05  
**Testad med:** Aspose.Note 23.12 for .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}