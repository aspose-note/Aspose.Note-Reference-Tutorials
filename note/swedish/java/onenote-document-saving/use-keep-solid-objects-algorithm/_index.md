---
title: Använd Keep Solid Objects Algorithm i OneNote - Aspose.Note
linktitle: Använd Keep Solid Objects Algorithm i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du bevarar solida objekt i dina Aspose.Note-dokument när du konverterar till PDF med hjälp av Keep Solid Objects Algorithm i Java.
weight: 25
url: /sv/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Använd Keep Solid Objects Algorithm i OneNote - Aspose.Note

## Introduktion

den här handledningen kommer vi att utforska hur man använder Keep Solid Objects-algoritmen i Aspose.Note för Java. Denna algoritm är ovärderlig för att upprätthålla integriteten hos solida objekt i dina dokument när du konverterar dem till PDF-format. Vi kommer att bryta ner processen steg för steg, för att säkerställa klarhet och förståelse i varje steg.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. Java Development Kit (JDK) installerat på ditt system.
2.  Aspose.Note för Java-bibliotek. Du kan ladda ner den från[här](https://releases.aspose.com/note/java/).

## Importera paket

Låt oss först importera de nödvändiga paketen:

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Steg 1: Ladda dokumentet

Ladda dokumentet i Aspose.Note med hjälp av följande kodavsnitt:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## Steg 2: Konfigurera PDF-sparalternativ

Definiera PdfSaveOptions och ställ in PageSplittingAlgorithm till KeepSolidObjectsAlgorithm:

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Steg 3: Justera höjdgränsen (valfritt)

Du kan justera höjdgränsen för klonade delar om det behövs:

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## Steg 4: Spara dokumentet

Spara slutligen dokumentet med de angivna PDF-sparalternativen:

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## Slutsats

I den här handledningen har vi lärt oss hur man använder Keep Solid Objects-algoritmen i Aspose.Note för Java. Denna algoritm säkerställer att solida objekt i dina dokument bevaras när du konverterar dem till PDF-format, vilket bibehåller dokumentintegriteten.

## FAQ's

### F1: Kan jag justera höjdgränsen för klonade delar?

 A1: Ja, du kan justera höjdgränsen för klonade delar enligt dina krav med hjälp av`heightLimitOfClonedPart` parameter.

### F2: Var kan jag hitta mer dokumentation?

 S2: Du kan hitta detaljerad dokumentation om Aspose.Note för Java[här](https://reference.aspose.com/note/java/).

### F3: Finns det en gratis provperiod?

 S3: Ja, du kan få en gratis provversion av Aspose.Note för Java[här](https://releases.aspose.com/).

### F4: Hur kan jag få support om jag stöter på några problem?

 S4: Du kan få stöd från Aspose-gemenskapen[här](https://forum.aspose.com/c/note/28).

### F5: Var kan jag köpa en licens?

 S5: Du kan köpa en licens för Aspose.Note för Java[här](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
