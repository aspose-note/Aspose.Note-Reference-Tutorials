---
date: 2026-04-03
description: Lär dig hur du ställer in en anpassad ikon och bifogar filer i Aspose.Note
  för .NET, inklusive att spara OneNote‑filer och använda bilder som ikoner.
keywords:
- set custom icon
- attach multiple files
- use image as icon
- save onenote file
- embed text file
linktitle: Bifoga fil och ställ in ikon i Aspose.Note
second_title: Aspose.Note .NET API
title: Ställ in anpassad ikon och bifoga fil i Aspose.Note
url: /sv/net/attachments/attach-file-set-icon/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ange anpassad ikon och bifoga fil i Aspose.Note

## Introduktion

Om du behöver **ange en anpassad ikon** för en bilaga i en OneNote‑sida, gör Aspose.Note för .NET det enkelt. Genom att bifoga en fil och tilldela en bild som dess ikon kan du skapa rikare, mer informativa anteckningar som ser exakt ut som du vill. I den här handledningen går vi igenom hela processen – från ett nytt dokument, lägga till en bilaga, applicera en anpassad JPEG‑ikon och slutligen spara OneNote‑filen.

## Snabba svar
- **Vad betyder “set custom icon”?** Det låter dig ersätta standard‑miniatyren för bilagan med en bild du tillhandahåller.  
- **Kan jag bifoga flera filer?** Ja, upprepa bifogningsstegen för varje fil.  
- **Vilka bildformat stöds för ikoner?** Alla .NET‑kompatibla format såsom JPEG, PNG, BMP eller GIF.  
- **Behöver jag en licens?** En giltig Aspose.Note‑licens krävs för produktionsanvändning; en gratis provversion fungerar för utvärdering.  
- **Hur sparar jag OneNote‑filen?** Använd `Document.Save()` och ange en *.one*-filväg.

## Vad är “set custom icon” i Aspose.Note?
Att ange en anpassad ikon innebär att tilldela en specifik bild (t.ex. en JPEG) för att representera en bifogad fil inom en OneNote‑sida. Detta förbättrar visuella ledtrådar för användare och kan användas för att visa filtyp‑logotyper eller varumärkesbilder.

## Varför ange en anpassad ikon för bilagor?
- **Bättre visuell kontext:** Användare känner omedelbart igen typen eller syftet med den bifogade filen.  
- **Varumärkeskonsekvens:** Använd ditt företags logotyp som ikon för alla relaterade dokument.  
- **Förbättrad användarupplevelse:** Gör anteckningar snygga och professionella, särskilt i delade anteckningsböcker.

## Förutsättningar

- Grundläggande kunskap i C#‑programmering.  
- Aspose.Note för .NET‑biblioteket installerat.  
- Visual Studio (eller någon .NET‑kompatibel IDE) redo för utveckling.

## Importera namnrymder

Först importerar du de nödvändiga namnrymderna så att du kan arbeta med filer, bilder och OneNote‑objekt.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing.Imaging;
```

## Steg‑för‑steg‑guide för att bifoga en fil och ange dess ikon

### Steg 1: Skapa ett Document‑objekt
Ett nytt `Document`‑instans representerar OneNote‑filen du kommer att bygga.

```csharp
Document doc = new Document();
```

### Steg 2: Initiera ett Page‑objekt
Varje OneNote‑fil innehåller en eller flera sidor. Här skapar vi den första sidan.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### Steg 3: Initiera ett Outline‑objekt
Outlines fungerar som behållare för innehållsblock på en sida.

```csharp
Outline outline = new Outline(doc);
```

### Steg 4: Initiera ett OutlineElement‑objekt
Detta element kommer att hålla den bifogade filen och dess anpassade ikon.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

### Steg 5: Läs ikonbilden och initiera AttachedFile‑objektet
Vi öppnar bildströmmen (den anpassade ikonen) och pekar på filen vi vill bädda in.

```csharp
string dataDir = "Your Document Directory";
using (var stream = File.OpenRead(dataDir + "icon.jpg"))
{
    AttachedFile attachedFile = new AttachedFile(doc, dataDir + "attachment.txt", stream, ImageFormat.Jpeg);
}
```

> **Pro tip:** Byt ut `ImageFormat.Jpeg` mot `ImageFormat.Png` om du föredrar en PNG‑ikon.

### Steg 6: Lägg till den bifogade filen i OutlineElement
Nu blir filen (med sin ikon) ett barn till outline‑elementet.

```csharp
outlineElem.AppendChildLast(attachedFile);
```

### Steg 7: Lägg till OutlineElement i Outline
Detta placerar elementet i outline‑behållaren.

```csharp
outline.AppendChildLast(outlineElem);
```

### Steg 8: Lägg till Outline i Page
Fäst hela outline‑hierarkin till sidan.

```csharp
page.AppendChildLast(outline);
```

### Steg 9: Lägg till Page i Document
Lägg till den färdiga sidan i dokumentstrukturen.

```csharp
doc.AppendChildLast(page);
```

### Steg 10: Spara OneNote‑dokumentet
Skriv slutligen dokumentet till disk som en *.one*-fil.

```csharp
dataDir = dataDir + "AttachFileAndSetIcon_out.one";
doc.Save(dataDir);
```

## Vanliga användningsfall
- **Inbäddning av kontrakt:** Bifoga en PDF och använd en kontraktslogotyp som ikon.  
- **Dela kodsnuttar:** Bifoga en `.txt`‑fil med en anpassad “kod”‑ikon.  
- **Projekt‑dokumentation:** Bifoga designfiler och ange en miniatyr som matchar filtypen.

## Vanliga problem och lösningar
| Problem | Lösning |
|-------|----------|
| **Ikonen visas inte** | Verifiera att bildformatet matchar det `ImageFormat` du angav (t.ex. JPEG vs PNG). |
| **Fel i filsökväg** | Använd `Path.Combine(dataDir, "file.ext")` för att undvika saknade snedstreck. |
| **Stora bilagor ger prestandaproblem** | Komprimera filen i förväg eller dela upp i flera mindre bilagor. |

## Vanliga frågor

**Q: Kan jag bifoga flera filer till en enda anteckning med Aspose.Note för .NET?**  
A: Ja. Upprepa helt enkelt blocket “Läs ikonbilden och initiera AttachedFile‑objektet” för varje fil och lägg till varje `AttachedFile` i samma `OutlineElement` eller skapa separata element.

**Q: Är det möjligt att ange anpassade ikoner för filbilagor?**  
A: Absolut. `AttachedFile`‑konstruktorn låter dig skicka en bildström och specificera bildformatet, vilket ger full kontroll över ikonen.

**Q: Stöder Aspose.Note andra bildformat för att ange ikoner?**  
A: Ja. Förutom JPEG kan du använda PNG, BMP, GIF eller vilket format som helst som stöds av `System.Drawing.Imaging.ImageFormat`.

**Q: Kan jag bifoga filer från externa URL:er?**  
A: Även om Aspose.Note arbetar med lokala strömmar kan du ladda ner en fil via `HttpClient`, lagra den i en `MemoryStream` och sedan skicka den strömmen till `AttachedFile`.

**Q: Finns det någon storleksgräns för filbilagor?**  
A: Aspose.Note själv pålägger ingen hård gräns, men mycket stora filer kan påverka minnesanvändning och prestanda. Överväg att komprimera stora bilagor.

**Senast uppdaterad:** 2026-04-03  
**Testad med:** Aspose.Note 24.11 för .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}