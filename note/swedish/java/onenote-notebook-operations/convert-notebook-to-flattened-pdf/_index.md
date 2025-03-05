---
title: Konvertera anteckningsbok till tillplattad PDF i OneNote - Aspose.Note
linktitle: Konvertera anteckningsbok till tillplattad PDF i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Konvertera anteckningsböcker till tillplattade PDF-filer utan ansträngning med Aspose.Note för Java. Njut av sömlös integration och anpassningsalternativ.
type: docs
weight: 16
url: /sv/java/onenote-notebook-operations/convert-notebook-to-flattened-pdf/
---
## Introduktion

I den här handledningen kommer vi att utforska hur man konverterar en anteckningsbok till ett tillplattat PDF-format med Aspose.Note för Java. Att konvertera anteckningsböcker till PDF-filer är ett vanligt krav för många applikationer, och Aspose.Note förenklar denna process med sin omfattande uppsättning funktioner och lättanvända API.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. Java Development Kit (JDK): Se till att du har JDK installerat på ditt system.
2.  Aspose.Note for Java Library: Ladda ner och installera Aspose.Note for Java-biblioteket från[här](https://releases.aspose.com/note/java/).
3. Integrated Development Environment (IDE): Välj en IDE som du föredrar, till exempel IntelliJ IDEA eller Eclipse.

## Importera paket

Låt oss först importera de nödvändiga paketen i ditt Java-projekt:

```java
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import java.io.IOException;
```

## Steg 1: Ladda OneNote Notebook

Börja med att ladda OneNote-anteckningsboken som du vill konvertera till PDF:

```java
String dataDir = "Your Document Directory";
Notebook notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## Steg 2: Ställ in konverteringsalternativ

 Definiera alternativen för att konvertera anteckningsboken till PDF. Här, vi sätter`flatten` till`true` för att platta till PDF:en:

```java
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
notebookSaveOptions.setFlatten(true);
```

## Steg 3: Spara anteckningsboken som PDF

Ange utdatakatalogen och spara anteckningsboken som en PDF med de definierade alternativen:

```java
dataDir = dataDir + "ExportNotebookToPDFAsFlattened_out.pdf";
// Spara anteckningsboken
notebook.save(dataDir, notebookSaveOptions);
```

## Slutsats

I den här handledningen har vi lärt oss hur man konverterar en anteckningsbok till ett tillplattat PDF-format med Aspose.Note för Java. Denna process är enkel och kan sömlöst integreras i dina Java-applikationer.

## FAQ's

### F1: Är Aspose.Note för Java kompatibel med olika versioner av OneNote?

S1: Ja, Aspose.Note för Java stöder olika versioner av OneNote, vilket säkerställer kompatibilitet mellan olika miljöer.

### F2: Kan jag anpassa PDF-utdata med Aspose.Note för Java?

S2: Absolut, du kan anpassa PDF-utdata enligt dina krav, inklusive sidlayout, teckensnittsstilar och mer.

### F3: Stöder Aspose.Note for Java batchkonvertering av bärbara datorer?

S3: Ja, du kan batchkonvertera flera anteckningsböcker till PDF-filer effektivt med Aspose.Note för Java.

### F4: Finns det en testversion tillgänglig för Aspose.Note för Java?

 S4: Ja, du kan få tillgång till en gratis testversion av Aspose.Note för Java från[här](https://releases.aspose.com/).

### F5: Var kan jag hitta support för Aspose.Note för Java?

 S5: Du kan hitta support och hjälp för Aspose.Note för Java på[Aspose.Note forum](https://forum.aspose.com/c/note/28).