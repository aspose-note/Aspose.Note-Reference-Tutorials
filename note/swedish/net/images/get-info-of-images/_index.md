---
date: 2026-04-09
description: Lär dig hur du extraherar bildmetadata och får bilddimensioner från OneNote‑filer
  med Aspose.Note för .NET. Steg‑för‑steg‑guide för C#‑utvecklare.
keywords:
- extract image metadata
- how to extract images
- get image dimensions
- load onenote document
- c# get image properties
linktitle: Hur man extraherar bildmetadata från OneNote med Aspose.Note
second_title: Aspose.Note .NET API
title: Hur man extraherar bildmetadata från OneNote med Aspose.Note
url: /sv/net/images/get-info-of-images/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extrahera bildmetadata med Aspose.Note för .NET

I den här praktiska handledningen kommer du att lära dig **hur du extraherar bildmetadata**—inklusive bredd, höjd, originalstorlek, filnamn och ändringstid—from Microsoft OneNote-filer med Aspose.Note-biblioteket för C#. Oavsett om du behöver visa bildminiatyrer, validera bildstorlekar eller bygga en katalog över inbäddade resurser, sparar det programatiska extraheringen av denna information dig otaliga manuella steg.

## Snabba svar
- **Vad betyder “extract image metadata”?** Hämta egenskaper såsom dimensioner, filnamn och tidsstämplar från bilder som lagras i ett OneNote-dokument.  
- **Vilket bibliotek hanterar detta?** Aspose.Note för .NET.  
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Stödda plattformar?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **Typisk körtid?** Mindre än en sekund för en standard .one-fil.

## Vad är extrahering av bildmetadata?
Att extrahera bildmetadata innebär att programatiskt läsa de beskrivande attributen (bredd, höjd, originaldimensioner, filnamn, senast ändrad tid osv.) som följer med varje bildobjekt på en OneNote-sida. Dessa data är användbara för validering, rapportering eller vidare bildbehandling.

## Varför extrahera bildmetadata från OneNote?
- **Automation** – Bygg verktyg som automatiskt genererar bildinventarier.  
- **Validering** – Säkerställ att bilder uppfyller storlekskrav innan publicering.  
- **Integration** – Kombinera OneNote-innehåll med andra system som behöver bilddetaljer (CMS, DAM osv.).  
- **Prestanda** – Undvik att ladda fullständiga bildbinärer när endast dimensioner behövs.

## Förutsättningar
1. **C#-grundläggande** – Du bör vara bekväm med att skriva grundläggande C#-kod.  
2. **Aspose.Note för .NET** – Ladda ner och installera biblioteket från den officiella webbplatsen [här](https://releases.aspose.com/note/net/).  
3. **En OneNote (.one)-fil** – Vilket som helst befintligt OneNote-dokument som innehåller bilder.

## Importera namnrymder
Innan vi börjar, importera de nödvändiga namnrymderna:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## Steg 1: Ladda OneNote-dokumentet
Först, ladda den valda OneNote-filen i ett `Aspose.Note.Document`-objekt. Detta är steget **load onenote document** som förbereder API:et för vidare frågor.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Byt ut `"Your Document Directory"` mot den faktiska mappen som innehåller din `.one`-fil.

## Steg 2: Hämta alla bildnoder
Nu kommer vi att **how to extract images** genom att hämta varje `Image`-nod från dokumentet.

```csharp
// Get all Image nodes
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

`GetChildNodes<T>()`-metoden skannar hela notebook-hierarkin och returnerar en samling bildobjekt.

## Steg 3: Iterera genom varje bild och **c# get image properties**
Vi kommer att loopa genom samlingen och skriva ut metadata, inklusive värdena **get image dimensions** och **extract original image size**.

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

Utdata visar varje bilds aktuella bredd/höjd (som renderas på sidan), de originala dimensionerna som lagras i filen, filnamnet och tidsstämpeln för den senaste ändringen.

## Vanliga problem och lösningar
| Problem | Orsak | Lösning |
|-------|--------|-----|
| **NullReferenceException** när `images` är tom | Dokumentet innehåller inga bilder | Verifiera att källfilen `.one` faktiskt har inbäddade bilder. |
| **Felaktiga dimensioner** | Bilder är skalade i OneNote | Använd `OriginalWidth`/`OriginalHeight` för att få den faktiska storleken. |
| **FileName är tom** | Bilden klistrades in från urklipp | API:et kanske inte har ett filnamn; hantera `null` eller tomma strängar i din kod. |

## Vanliga frågor

**Q: Är Aspose.Note kompatibel med alla versioner av Microsoft OneNote?**  
A: Aspose.Note stöder .one, .onepkg och .onetoc2-format, vilket täcker de flesta OneNote-versioner från 2007 och framåt.

**Q: Kan jag ändra bildegenskaperna efter extrahering?**  
A: Ja, du kan ändra egenskaper som `Width`, `Height` eller `FileName` och sedan spara dokumentet.

**Q: Fungerar Aspose.Note med .NET Core?**  
A: Absolut. Biblioteket är fullt kompatibelt med .NET Core, .NET 5 och .NET 6.

**Q: Finns det en gratis provversion tillgänglig?**  
A: Ja, du kan ladda ner en provversion från Aspose-webbplatsen för att utforska alla funktioner.

**Q: Var kan jag få ytterligare hjälp eller community‑support?**  
A: Besök Aspose.Note-forumet [här](https://forum.aspose.com/c/note/28) för tips, exempel på kod och svar från communityn.

---

**Senast uppdaterad:** 2026-04-09  
**Testad med:** Aspose.Note 24.11 för .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}