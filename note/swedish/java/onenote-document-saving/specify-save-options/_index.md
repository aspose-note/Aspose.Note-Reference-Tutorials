---
title: Ange Spara alternativ i OneNote - Aspose.Note
linktitle: Ange Spara alternativ i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du anger sparalternativ i OneNote med Aspose.Note för Java. Anpassa inställningarna för sidindex, antal och komprimering utan ansträngning.
weight: 24
url: /sv/java/onenote-document-saving/specify-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ange Spara alternativ i OneNote - Aspose.Note

## Introduktion

den här handledningen kommer vi att lära oss hur du anger sparalternativ i OneNote med Aspose.Note för Java. Aspose.Note är ett kraftfullt Java-bibliotek som låter utvecklare skapa, manipulera och konvertera OneNote-dokument programmatiskt. Med Aspose.Note kan du enkelt styra olika sparalternativ för att anpassa utdata enligt dina krav.

## Förutsättningar

Innan du börjar, se till att du har följande förutsättningar:

1. Grundläggande kunskaper i programmeringsspråket Java.
2. JDK (Java Development Kit) installerat på ditt system.
3.  Aspose.Note för Java-biblioteket installerat. Du kan ladda ner den från[här](https://releases.aspose.com/note/java/).

## Importera paket

För att börja, importera nödvändiga paket i din Java-kod:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

Låt oss dela upp exemplet i flera steg:

## Steg 1: Ladda OneNote-dokumentet

```java
// Sökvägen till dokumentkatalogen.
String dataDir = "Your Document Directory";

// Ladda dokumentet i Aspose.Note.
Document doc = new Document(dataDir + "Aspose.one");
```

 I det här steget anger vi sökvägen till OneNote-dokumentet och laddar in det i`Document` objekt.

## Steg 2: Initiera PdfSaveOptions-objekt

```java
// Initiera PdfSaveOptions-objekt
PdfSaveOptions opts = new PdfSaveOptions();
```

 Här initierar vi en`PdfSaveOptions` objekt som kommer att användas för att ange alternativen för att spara dokumentet som en PDF.

## Steg 3: Ställ in sidindex och antal

```java
// Ställ in sidindex
opts.setPageIndex(2);

// Ställ in sidantal
opts.setPageCount(3);
```

Dessa rader anger indexet och antalet sidor som ska sparas. I det här exemplet sparar vi sidor från index 2 och totalt 3 sidor.

## Steg 4: Ange komprimeringsinställningar

```java
// Ange komprimering vid behov
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

Här anger vi inställningarna för bildkomprimering för PDF:en. Vi ställer in komprimeringen till JPEG-format och anger JPEG-kvaliteten till 90 %.

## Steg 5: Spara dokumentet med alternativ

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

Slutligen sparar vi dokumentet med de angivna alternativen. Utdata-PDF-filen kommer att sparas på den angivna platsen med de givna alternativen.

## Slutsats

I den här handledningen har vi lärt oss hur man anger sparalternativ i OneNote med Aspose.Note för Java. Genom att anpassa sparalternativ kan du styra olika aspekter av utdatadokumentet, såsom sidindex, antal och komprimeringsinställningar.

## FAQ's

### F1: Kan Aspose.Note hantera stora OneNote-dokument?

S1: Ja, Aspose.Note är utformad för att hantera stora OneNote-dokument effektivt.

### F2: Är Aspose.Note kompatibel med de senaste Java-versionerna?

S2: Ja, Aspose.Note är kompatibel med de senaste Java-versionerna.

### F3: Kan jag konvertera OneNote-dokument till andra format med Aspose.Note?

S3: Ja, Aspose.Note stöder konvertering av OneNote-dokument till olika format som PDF, DOCX och HTML.

### F4: Ger Aspose.Note stöd för kryptering och dekryptering av OneNote-dokument?

S4: Ja, Aspose.Note tillhandahåller API:er för kryptering och dekryptering av OneNote-dokument.

### F5: Är Aspose.Note lämplig för kommersiellt bruk?

S5: Ja, Aspose.Note kan användas för kommersiella ändamål genom att köpa en licens.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
