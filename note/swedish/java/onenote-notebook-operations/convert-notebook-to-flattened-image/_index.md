---
title: Konvertera anteckningsbok till tillplattad bild i OneNote - Aspose.Note
linktitle: Konvertera anteckningsbok till tillplattad bild i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du konverterar en anteckningsbok till en tillplattad bild i OneNote med Aspose.Note för Java. Bevara alla element i en enda bildfil utan ansträngning.
type: docs
weight: 13
url: /sv/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---
## Introduktion

den här handledningen kommer vi att guida dig genom processen att konvertera en anteckningsbok till en tillplattad bild i OneNote med Aspose.Note för Java. Detta gör att du kan spara din anteckningsbok som en bildfil, vilket säkerställer att alla element bevaras i ett enda bildformat.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. Java Development Kit (JDK) installerat på ditt system.
2.  Aspose.Note för Java-biblioteket laddat ned och konfigurerat i ditt Java-projekt. Du kan ladda ner biblioteket från[här](https://releases.aspose.com/note/java/).
3. Grundläggande kunskaper i Java-programmering.

## Importera paket

För att börja måste du importera nödvändiga paket från Aspose.Note för Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Steg 1: Konfigurera dokumentkatalog

Först definierar du katalogen där din anteckningsbok-fil finns:

```java
String dataDir = "Your Document Directory";
```

 Byta ut`"Your Document Directory"` med sökvägen till din anteckningsbok-fil.

## Steg 2: Ladda anteckningsboken

 Ladda sedan in notebook-filen med hjälp av`Notebook` klass:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Se till att byta ut`"test.onetoc2"` med namnet på din anteckningsbok.

## Steg 3: Ställ in alternativ för bildspar

Ställ nu in alternativen för att spara anteckningsboken som en bild. Vi kommer att specificera sparformatet som PNG och ställa in upplösningen till 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Du kan justera upplösningen enligt dina önskemål.

## Steg 4: Platta till anteckningsboken

För att säkerställa att alla element är tillplattade till en enda bild, ställ in`flatten` möjlighet att`true`:

```java
saveOptions.setFlatten(true);
```

Detta säkerställer att den resulterande bilden bibehåller layouten på din anteckningsbok.

## Steg 5: Spara bild

Slutligen sparar du anteckningsboken som en tillplattad bild:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Byta ut`"ExportImageasFlattenedNotebook_out.png"` med önskat utdatafilnamn.

## Slutsats

Sammanfattningsvis, med Aspose.Note för Java kan du enkelt konvertera din anteckningsbok till en tillplattad bild i OneNote. Denna process säkerställer att alla element bevaras i ett enda bildformat, vilket underlättar delning och visning.

## FAQ's

### F1: Kan jag justera upplösningen på den utgående bilden?

 S1: Ja, du kan justera upplösningen enligt dina krav genom att ändra`setResolution` metodparameter.

### F2: Stöder Aspose.Note andra bildformat för export?

S2: Ja, Aspose.Note stöder olika bildformat som PNG, JPEG, BMP, etc., för export av bärbara datorer.

### F3: Kan jag anpassa utdatabilden ytterligare?

S3: Ja, Aspose.Note erbjuder omfattande alternativ för att anpassa utdatabilden, inklusive sidstorlek, orientering och kvalitetsinställningar.

### F4: Finns det en testversion tillgänglig för Aspose.Note för Java?

 S4: Ja, du kan få en gratis testversion från[här](https://releases.aspose.com/).

### F5: Var kan jag hitta support för Aspose.Note för Java?

 S5: Du kan hitta support och resurser på Aspose.Note-forumet[här](https://forum.aspose.com/c/note/28).