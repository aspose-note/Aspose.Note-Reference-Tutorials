---
title: Konvertera OneNote-dokument till bild - Java
linktitle: Konvertera OneNote-dokument till bild - Java
second_title: Aspose.Note Java API
description: Lär dig att konvertera OneNote till bild med Aspose.Note för Java. Följ enkla steg, ladda dokument, initiera alternativ och spara som PNG.
type: docs
weight: 14
url: /sv/java/onenote-document-loading/convert-to-image/
---
## Introduktion

I den här handledningen guidar vi dig genom processen att använda Aspose.Note för Java för att konvertera ett OneNote-dokument till en bild. Vi delar upp varje steg i instruktioner som är lätta att följa.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. Java Development Kit (JDK) installerat på ditt system.
2.  Aspose.Note för Java-bibliotek. Du kan ladda ner den från[här](https://releases.aspose.com/note/java/).

## Importera paket

Importera först de nödvändiga paketen i din Java-kod:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Låt oss nu dela upp exempelkoden som tillhandahålls i flera steg:

## Steg 1: Konfigurera dokumentkatalog

Definiera katalogen där ditt OneNote-dokument finns:

```java
String dataDir = "Your Document Directory";
```

 Byta ut`"Your Document Directory"` med sökvägen till ditt OneNote-dokument.

## Steg 2: Ladda dokumentet

Ladda OneNote-dokumentet i Aspose.Note:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 Säkerställa`"Sample1.one"` matchar namnet på din OneNote-dokumentfil.

## Steg 3: Initiera ImageSaveOptions

 Initiera`ImageSaveOptions` objekt för att ange sparformatet:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Här sparar vi dokumentet som en PNG-bild. Du kan välja andra format som JPEG eller BMP om det behövs.

## Steg 4: Spara dokumentet som bild

Spara det laddade dokumentet som en bild:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Den här raden sparar dokumentet som en PNG-bild med de angivna alternativen.

## Steg 5: Skriv ut bekräftelse

Skriv ut ett meddelande för att bekräfta att filen har sparats:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Den här raden meddelar dig om den lyckade konverteringen och platsen för den sparade bildfilen.

## Slutsats

Genom att följa stegen som beskrivs ovan kan du enkelt konvertera ett OneNote-dokument till en bild med Aspose.Note för Java. Det är ett enkelt och effektivt sätt att hantera dokumentkonverteringar i dina Java-applikationer.

## FAQ's

### F1: Kan jag konvertera flera OneNote-dokument på en gång?

S1: Ja, du kan gå igenom en lista med dokument och utföra konverteringen för varje dokument.

### F2: Stöder Aspose.Note andra utdataformat förutom bilder?

S2: Ja, Aspose.Note stöder olika utdataformat som PDF, HTML och Microsoft Word-format.

### F3: Är Aspose.Note kompatibel med alla versioner av OneNote-filer?

S3: Aspose.Note erbjuder kompatibilitet med OneNote-filer skapade i olika versioner av Microsoft OneNote.

### F4: Kan jag anpassa upplösningen på de utgående bilderna?

S4: Ja, du kan justera upplösningen och andra parametrar med hjälp av alternativen i Aspose.Note.

### F5: Kräver Aspose.Note internetanslutning för dokumentkonvertering?

S5: Nej, Aspose.Note fungerar lokalt utan behov av en internetanslutning.