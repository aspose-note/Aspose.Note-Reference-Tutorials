---
date: 2025-12-25
description: Lär dig hur du konverterar OneNote till PNG med Aspose.Note för Java.
  Den här guiden visar hur du ställer in bildupplösning, plattar till en anteckningsbok
  och sparar OneNote som en bild på ett effektivt sätt.
linktitle: How to Convert OneNote to PNG – Flatten Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: Hur man konverterar OneNote till PNG – Platta ut anteckningsboken till en bild
  med Aspose.Note
url: /sv/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera anteckningsbok till platt bild i OneNote - Aspose.Note

## Introduktion

I den här handledningen kommer du att upptäcka hur du **konverterar OneNote till PNG** genom att göra en hel anteckningsbok till en enda platt bild med Aspose.Note för Java. Detta tillvägagångssätt är perfekt när du behöver dela en anteckningsbok som en statisk bild, bädda in den i rapporter eller arkivera den utan att förlora visuella detaljer.

## Snabba svar
- **Vad betyder “platta notebook”**? Det sammanslår alla sidelement till en rasterbild.  
- **Vilket format används?** PNG är standard och ger förlustfri kvalitet.  
- **Kan jag ändra DPI?** Ja, använd `setResolution` på `ImageSaveOptions`.  
- **Behöver jag en licens?** En gratis provversion fungerar för utvärdering; en kommersiell licens krävs för produktion.  
- **Stöds detta på alla OS?** Java‑API:t körs var Java körs.

## Vad är konvertering av OneNote till PNG?

Att konvertera OneNote till PNG skapar en bitmaprepresentation av varje sida i anteckningsboken och bevarar text, teckningar och inbäddade objekt i en enda bildfil. Detta är särskilt användbart för dokumentation, presentationer eller efterlevnadsarkiv.

## Varför konvertera OneNote till PNG med Aspose.Note?

- **Fullständig trohet** – Alla visuella element behålls.  
- **Enkel filutgång** – Ingen behov av att hantera flera sidfiler.  
- **Anpassningsbar upplösning** – Justera DPI för att möta kvalitetskrav.  
- **Ingen Office‑installation** – Fungerar helt oberoende av Microsoft OneNote.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. Java Development Kit (JDK) installerat på ditt system.  
2. Aspose.Note för Java‑biblioteket nedladdat och konfigurerat i ditt Java‑projekt. Du kan ladda ner biblioteket [här](https://releases.aspose.com/note/java/).  
3. Grundläggande kunskaper i Java‑programmering.

## Importera paket

För att komma igång måste du importera de nödvändiga paketen från Aspose.Note för Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Steg 1: Ställ in dokumentkatalog

Definiera först katalogen där din anteckningsboksfil finns:

```java
String dataDir = "Your Document Directory";
```

Byt ut `"Your Document Directory"` mot sökvägen till din anteckningsboksfil.

## Steg 2: Ladda notebook

Läs sedan in anteckningsboksfilen med klassen `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Se till att ersätta `"test.onetoc2"` med namnet på din anteckningsboksfil.

## Steg 3: Ställ in bildsparalternativ

Ställ nu in alternativen för att spara anteckningsboken som en bild. Vi specificerar sparformatet som PNG och sätter upplösningen till 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Du kan justera upplösningen efter dina behov. Här **ställer du bildens upplösning** för att kontrollera utdata­kvaliteten.

## Steg 4: Platta notebook

För att säkerställa att alla element plattas ut till en enda bild, sätt `flatten`‑alternativet till `true`:

```java
saveOptions.setFlatten(true);
```

Att sätta `flatten` till `true` garanterar att den resulterande PNG‑filen behåller exakt layout av din anteckningsbok.

## Steg 5: Spara bild

Spara slutligen anteckningsboken som en platt bild:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Byt ut `"ExportImageasFlattenedNotebook_out.png"` mot önskat filnamn för utdata. Detta steg **sparar OneNote som en bild** som du kan dela eller bädda in var som helst.

## Vanliga användningsområden

- **Dokumentation:** Bädda in anteckningsboksbilden i tekniska manualer eller användarguider.  
- **Presentationer:** Använd en högupplöst PNG‑slide i PowerPoint utan att oroa dig för teckensnitt eller objektkompatibilitet.  
- **Arkivering:** Lagra ett skrivskyddat ögonblicksbild av en anteckningsbok för efterlevnadsrevisioner.

## Felsökningstips

- **Filen hittades inte:** Dubbelkolla `dataDir`‑sökvägen och säkerställ att `.onetoc2`‑filen finns.  
- **Bild med låg kvalitet:** Öka DPI genom att ändra `documentSaveOptions.setResolution(600);`.  
- **Saknade element:** Verifiera att `saveOptions.setFlatten(true);` är aktiverat; annars kan vissa lager förbli separata.

## Vanliga frågor

**Q1: Kan jag justera upplösningen på utdata‑bilden?**  
A1: Ja, du kan justera upplösningen enligt dina krav genom att ändra parametern i `setResolution`‑metoden.

**Q2: Stöder Aspose.Note andra bildformat för export?**  
A2: Ja, Aspose.Note stödjer olika bildformat såsom PNG, JPEG, BMP osv. för export av anteckningsböcker.

**Q3: Kan jag anpassa utdata‑bilden ytterligare?**  
A3: Ja, Aspose.Note erbjuder omfattande alternativ för att anpassa utdata‑bilden, inklusive sidstorlek, orientering och kvalitetsinställningar.

**Q4: Finns det en provversion av Aspose.Note för Java?**  
A4: Ja, du kan skaffa en gratis provversion [här](https://releases.aspose.com/).

**Q5: Var kan jag hitta support för Aspose.Note för Java?**  
A5: Du kan hitta support och resurser på Aspose.Note‑forumet [här](https://forum.aspose.com/c/note/28).

---

**Senast uppdaterad:** 2025-12-25  
**Testad med:** Aspose.Note för Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}