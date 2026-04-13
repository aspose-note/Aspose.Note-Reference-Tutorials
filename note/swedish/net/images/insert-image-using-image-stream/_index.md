---
date: 2026-04-13
description: Lär dig hur du lägger till bilder i OneNote‑dokument med bildströmmar
  i .NET med Aspose.Note. Denna steg‑för‑steg‑guide täcker hur du laddar bilder från
  en ström, lägger till dem i konturer och sparar filen.
keywords:
- add image to onenote
- how to insert image
- load image from stream
- append image to outline
- image stream .net
linktitle: Lägg till bild i OneNote via bildström med Aspose.Note
second_title: Aspose.Note .NET API
title: Lägg till bild i OneNote via bildström med Aspose.Note
url: /sv/net/images/insert-image-using-image-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till bild i OneNote via bildström med Aspose.Note

## Introduktion

I den här handledningen kommer du att upptäcka **hur man lägger till bild i OneNote**-dokument genom att läsa in en bild från en ström och lägga till den i en kontur med Aspose.Note för .NET. Oavsett om du bygger ett rapporteringsverktyg, en anteckningsapp eller automatiserar dokumentation, gör programmatisk infogning av bilder dina OneNote‑filer mycket mer engagerande och användbara.

## Snabba svar
- **Vilket bibliotek behöver jag?** Aspose.Note for .NET (free trial available).  
- **Vilka .NET‑versioner stöds?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Kan jag läsa in bilder från en ström?** Yes – use `FileStream` or any `Stream` implementation.  
- **Hur styr jag bildens justering?** Set the `Alignment` property (e.g., `HorizontalAlignment.Right`).  
- **Vilket filformat produceras?** A OneNote (`.one`) file that can be opened in Microsoft OneNote.

## Vad är “lägga till bild i OneNote”?

Att lägga till en bild i en OneNote‑fil innebär att bädda in ett visuellt element direkt i sidans innehållshierarki. Med Aspose.Note arbetar du med objekt som `Document`, `Page`, `Outline` och `OutlineElement`. Genom att infoga ett `Image`‑objekt i ett `OutlineElement` blir bilden en del av OneNote‑sidans layout.

## Varför använda Aspose.Note för bildinfogning?

- **Ingen Office‑installation krävs** – generera eller modifiera OneNote‑filer på en server.  
- **Full kontroll över layout** – justera, ändra storlek och placera bilder exakt där du behöver dem.  
- **Ström‑vänlig** – fungerar med vilken `Stream` som helst, perfekt för molnlagring eller minnes‑endast scenarier.  
- **Plattformsoberoende** – kompatibel med Windows, Linux och macOS .NET‑körmiljöer.

## Förutsättningar

1. **Utvecklingsmiljö** – Visual Studio 2022 eller någon .NET‑kompatibel IDE.  
2. **Aspose.Note‑bibliotek** – download it from the official site [here](https://releases.aspose.com/note/net/).  
3. **Bildfiler** – minst en bild (JPG, PNG, BMP, GIF eller TIFF) som du vill bädda in.  
4. **Grundläggande C#‑kunskaper** – bekantskap med filhantering och objekt‑orienterad kod.

## Importera namnrymder
Först importerar du namnrymderna som ger åtkomst till Aspose.Note‑klasser och standard .NET‑I/O‑verktyg.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Nu går vi igenom processen steg för steg.

### Steg 1: Initiera Document‑objekt
Vi börjar med att skapa en ny `Document`‑instans som kommer att innehålla OneNote‑filen.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

### Steg 2: Skapa Page‑objekt
En OneNote‑fil består av en eller flera sidor. Här skapar vi en ny sida för att hålla vårt innehåll.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### Steg 3: Initiera Outline‑ och OutlineElement‑objekt
Outlines är behållare för rikt innehåll (text, bilder, tabeller). Ett `OutlineElement` är ett barn som faktiskt innehåller objekten.

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```

### Steg 4: Läs in bild från ström
Genom att använda en `FileStream` (eller någon `Stream`) läser vi bildfilen och skapar ett `Image`‑objekt. Här kommer nyckelordet **load image from stream** till sin rätt.

```csharp
using (FileStream fs = File.OpenRead(dataDir + "image.jpg"))
{
    Aspose.Note.Image image1 = new Aspose.Note.Image(doc, "Penguins.jpg", fs)
    {
        Alignment = HorizontalAlignment.Right
    };
    outlineElem1.AppendChildLast(image1);
}
```

### Steg 5: Lägg till bild i OutlineElement
Bilden är nu en del av `OutlineElement`. Detta steg demonstrerar funktionen **append image to outline**.

```csharp
outlineElem1.AppendChildLast(image1);
```

### Steg 6: Lägg till OutlineElement i Outline
Vi bifogar nu elementet (med bilden) till outline‑behållaren.

```csharp
outline1.AppendChildLast(outlineElem1);
```

### Steg 7: Lägg till Outline i Page
Outlinen, som innehåller bilden, läggs till på sidan.

```csharp
page.AppendChildLast(outline1);
```

### Steg 8: Lägg till Page i Document
När sidan är klar, infogar vi den i dokumenthierarkin.

```csharp
doc.AppendChildLast(page);
```

### Steg 9: Spara Document
Slutligen sparar vi OneNote‑filen till disk. Den resulterande filen kan öppnas i Microsoft OneNote.

```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```

## Vanliga problem och lösningar

| Problem | Varför det händer | Lösning |
|-------|----------------|-----|
| **Bilden visas inte** | Strömmen stängdes innan bilden lades till. | Behåll `using`‑blocket runt anropet till `AppendChildLast` (som visat). |
| **Felaktig justering** | `Alignment`‑egenskapen är inte satt eller överskrivs senare. | Sätt `Alignment` när du skapar `Image` eller ändra `image1.Alignment` innan du lägger till. |
| **Bildformat stöds inte** | Försöker läsa in ett format som inte känns igen av Aspose.Note. | Konvertera bilden till JPG, PNG, BMP, GIF eller TIFF först. |
| **Fel i filsökväg** | `dataDir` pekar på en icke‑existerande mapp. | Använd `Path.Combine` och verifiera att mappen finns innan du kör. |

## Vanliga frågor

**Q: Kan jag infoga flera bilder i ett enda dokument med den här metoden?**  
A: Ja. Upprepa helt enkelt stegen *Load Image from Stream* och *Append Image to OutlineElement* för varje bild.

**Q: Stöder Aspose.Note andra bildformat förutom JPG?**  
A: Absolut. PNG, BMP, GIF och TIFF stöds alla.

**Q: Kan jag anpassa justering och storlek på infogade bilder?**  
A: Ja. Förutom `Alignment` kan du sätta `Width`, `Height` och `Scale`‑egenskaper på `Image`‑objektet.

**Q: Är Aspose.Note kompatibel med alla .NET‑versioner?**  
A: Den fungerar med .NET Framework 4.5+, .NET Core 3.1+, .NET 5 och .NET 6+.

**Q: Var kan jag hitta ytterligare resurser och support för Aspose.Note?**  
A: Du kan hitta omfattande dokumentation, forum och support på den [Aspose Forum](https://forum.aspose.com/c/note/28).

---

**Last Updated:** 2026-04-13  
**Tested With:** Aspose.Note 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}