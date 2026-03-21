---
date: 2026-03-21
description: Lär dig hur du plattar till en anteckningsbok genom att konvertera OneNote
  till PNG med Aspose.Note för Java. Denna guide täcker hur du ställer in bildupplösning,
  sparar OneNote som bild och plattar till anteckningsböcker effektivt.
linktitle: How to Flatten Notebook – Convert OneNote to PNG
second_title: Aspose.Note Java API
title: Hur man plattar till anteckningsboken – Konvertera OneNote till PNG
url: /sv/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man plattar till en anteckningsbok – Konvertera OneNote till PNG

## Introduktion

I den här handledningen kommer du att upptäcka **hur man plattar till en anteckningsbok** genom att konvertera en OneNote‑anteckningsbok till en högkvalitativ PNG‑bild med Aspose.Note för Java. Oavsett om du behöver bädda in en ögonblicksbild av en anteckningsbok i en rapport, dela en skrivskyddad vy med kollegor eller arkivera en efterlevnadsbild, visar denna steg‑för‑steg‑guide exakt hur du sparar OneNote som bild samtidigt som du kontrollerar upplösningen.

## Snabba svar
- **Vad betyder “flatten notebook”?** Det sammanslår alla sidobjekt till en rasterbild.  
- **Vilket format används?** PNG är standard och ger förlustfri kvalitet.  
- **Kan jag ändra DPI?** Ja, använd `setResolution` på `ImageSaveOptions`.  
- **Behöver jag en licens?** En gratis provversion fungerar för utvärdering; en kommersiell licens krävs för produktion.  
- **Stöds detta på alla operativsystem?** Java‑API:et körs där Java körs.

## Vad är konvertering av OneNote till PNG?

Att konvertera OneNote till PNG skapar en bitmaprepresentation av varje sida i anteckningsboken, där text, teckningar och inbäddade objekt bevaras i en enda bildfil. Detta är särskilt användbart för dokumentation, presentationer eller efterlevnadsarkiv.

## Varför konvertera OneNote till PNG med Aspose.Note?

- **Fullständig trohet** – Alla visuella element behålls.  
- **En‑fil‑utdata** – Ingen behov av att hantera flera sidfiler.  
- **Anpassningsbar upplösning** – Justera DPI för att uppfylla kvalitetskrav.  
- **Ingen Office‑installation** – Fungerar helt oberoende av Microsoft OneNote.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. Java Development Kit (JDK) installerat på ditt system.  
2. Aspose.Note för Java‑biblioteket nedladdat och konfigurerat i ditt Java‑projekt. Du kan ladda ner biblioteket från [here](https://releases.aspose.com/note/java/).  
3. Grundläggande kunskap om Java‑programmering.

## Importera paket

För att börja måste du importera de nödvändiga paketen från Aspose.Note för Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Steg‑för‑steg‑guide

### Steg 1: Ställ in dokumentkatalog

Först, definiera katalogen där din anteckningsboksfil finns:

```java
String dataDir = "Your Document Directory";
```

Byt ut `"Your Document Directory"` mot sökvägen till din anteckningsboksfil.

### Steg 2: Ladda notebook

Ladda sedan notebook‑filen med `Notebook`‑klassen:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Se till att ersätta `"test.onetoc2"` med namnet på din notebook‑fil.

### Steg 3: Ställ in bildsparalternativ (set image resolution java)

Nu ställer du in alternativen för att spara notebook som en bild. Vi kommer att ange sparformatet som PNG och sätta upplösningen till 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Du kan justera upplösningen efter dina behov. Detta är där du **ställer in bildens upplösning** för att kontrollera utdata‑kvaliteten.

### Steg 4: Platta till notebook (how to flatten notebook)

För att säkerställa att alla element plattas till en enda bild, sätt `flatten`‑alternativet till `true`:

```java
saveOptions.setFlatten(true);
```

Att sätta `flatten` till `true` garanterar att den resulterande PNG‑filen behåller exakt layout av din notebook.

### Steg 5: Spara bild (save onenote as image)

Slutligen, spara notebook som en plattad bild:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Byt ut `"ExportImageasFlattenedNotebook_out.png"` mot önskat filnamn för utdata. Detta steg **sparar OneNote som en bild** som du kan dela eller bädda in var som helst.

## Vanliga användningsområden

- **Dokumentation:** Bädda in notebook‑bilden i tekniska manualer eller användarguider.  
- **Presentationer:** Använd en högupplöst PNG‑bild i PowerPoint utan att oroa dig för teckensnitt eller objektkompatibilitet.  
- **Arkivering:** Lagra en skrivskyddad ögonblicksbild av en notebook för efterlevnadsgranskningar.

## Felsökningstips

- **Fil ej hittad:** Dubbelkolla `dataDir`‑sökvägen och säkerställ att `.onetoc2`‑filen finns.  
- **Låg bildkvalitet:** Öka DPI genom att ändra `documentSaveOptions.setResolution(600);`.  
- **Saknade element:** Verifiera att `saveOptions.setFlatten(true);` är aktiverat; annars kan vissa lager förbli separata.

## Vanliga frågor

**Q1: Kan jag justera upplösningen på utdata‑bilden?**  
A1: Ja, du kan justera upplösningen enligt dina krav genom att ändra parametern i `setResolution`‑metoden.

**Q2: Stöder Aspose.Note andra bildformat för export?**  
A2: Ja, Aspose.Note stöder olika bildformat som PNG, JPEG, BMP osv. för export av notebooks.

**Q3: Kan jag anpassa utdata‑bilden ytterligare?**  
A3: Ja, Aspose.Note erbjuder omfattande alternativ för att anpassa utdata‑bilden, inklusive sidstorlek, orientering och kvalitetsinställningar.

**Q4: Finns det en provversion av Aspose.Note för Java?**  
A4: Ja, du kan skaffa en gratis provversion från [here](https://releases.aspose.com/).

**Q5: Var kan jag hitta support för Aspose.Note för Java?**  
A5: Du kan hitta support och resurser på Aspose.Note‑forumet [here](https://forum.aspose.com/c/note/28).

---

**Senast uppdaterad:** 2026-03-21  
**Testad med:** Aspose.Note för Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}