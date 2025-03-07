---
title: Spara dokument till OneNote med hjälp av SaveFormat - Aspose.Note
linktitle: Spara dokument till OneNote med hjälp av SaveFormat - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du sparar dokument i OneNote-format med Aspose.Note för Java. Följ denna steg-för-steg handledning för sömlös integration i dina Java-applikationer.
weight: 12
url: /sv/java/onenote-document-saving/save-document-to-onenote-format-using-saveformat/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara dokument till OneNote med hjälp av SaveFormat - Aspose.Note

## Introduktion

Aspose.Note för Java är ett kraftfullt bibliotek som gör det möjligt för utvecklare att arbeta med Microsoft OneNote-filer programmatiskt. Att spara ett dokument i OneNote-format med SaveFormat är en enkel process. I den här självstudien går vi igenom de steg som krävs för att utföra denna uppgift.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. Java Development Kit (JDK) installerat på ditt system.
2.  Aspose.Note för Java-bibliotek nedladdat. Du kan få det från[här](https://releases.aspose.com/note/java/).
3. Grundläggande förståelse för programmeringsspråket Java.

## Importera paket

 Först måste du importera de nödvändiga paketen till ditt Java-projekt. Detta inkluderar import av`com.aspose.note` paket för att arbeta med Aspose.Note-funktioner.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## Steg 1: Konfigurera dokumentkatalog

Definiera katalogen där ditt dokument finns och där du vill spara utdatafilen.

```java
String dataDir = "Your Document Directory";
```

## Steg 2: Ladda dokument

 Ladda dokumentet i din Java-applikation med hjälp av`Document` klass tillhandahållen av Aspose.Note.

```java
Document document = new Document(dataDir + "Sample1.one");
```

## Steg 3: Spara dokument i OneNote-format

Spara det laddade dokumentet i OneNote-formatet med hjälp av`save` metod och ange önskat utdatafilformat som`SaveFormat.One`.

```java
document.save(dataDir + "SaveDocToOneNoteFormatUsingSaveformat_out.one", SaveFormat.One);
```

## Slutsats

I den här handledningen har vi lärt oss hur man sparar ett dokument i OneNote-format med hjälp av SaveFormat i Aspose.Note för Java. Genom att följa dessa enkla steg kan du sömlöst integrera denna funktion i dina Java-applikationer.

## FAQ's

### F1: Är Aspose.Note för Java kompatibel med alla versioner av Microsoft OneNote?

S1: Aspose.Note för Java stöder olika versioner av Microsoft OneNote, vilket säkerställer kompatibilitet mellan olika miljöer.

### F2: Kan jag prova Aspose.Note för Java innan jag köper det?

 S2: Ja, du kan ladda ner en gratis testversion av Aspose.Note för Java från[här](https://releases.aspose.com/).

### F3: Var kan jag hitta dokumentation för Aspose.Note för Java?

 S3: Detaljerad dokumentation för Aspose.Note för Java finns[här](https://reference.aspose.com/note/java/).

### F4: Hur kan jag få teknisk support för Aspose.Note för Java?

 S4: För teknisk assistans och support kan du besöka Aspose.Note-forumet[här](https://forum.aspose.com/c/note/28).

### F5: Finns det ett tillfälligt licensalternativ tillgängligt för Aspose.Note för Java?

 S5: Ja, du kan få en tillfällig licens för Aspose.Note för Java från[här](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
