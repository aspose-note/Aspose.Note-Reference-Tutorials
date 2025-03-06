---
title: Push aktuell sidversion i OneNote - Aspose.Note
linktitle: Push aktuell sidversion i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Håll OneNote-innehåll fräscht! Lär dig att uppdatera sidhistorik och hantera versioner, steg-för-steg-guide och kod ingår. #OneNote #Java #Aspose
weight: 18
url: /sv/java/onenote-page-manipulation/push-current-page-version/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Push aktuell sidversion i OneNote - Aspose.Note

## Introduktion

I den här handledningen kommer vi att utforska hur man använder Aspose.Note för Java för att driva den aktuella sidversionen i OneNote. Aspose.Note är ett kraftfullt Java-bibliotek som låter utvecklare arbeta med Microsoft OneNote-dokument programmatiskt, vilket möjliggör olika operationer som att skapa, manipulera och konvertera OneNote-filer.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar:
1. Grundläggande kunskaper i programmeringsspråket Java.
2. Installerat Java Development Kit (JDK) på ditt system.
3.  Aspose.Note för Java-bibliotek. Du kan ladda ner den från[här](https://releases.aspose.com/note/java/).
4. Ett exempel på OneNote-dokument att arbeta med.

## Importera paket

Först måste du importera de nödvändiga paketen i ditt Java-projekt för att använda Aspose.Note-funktioner.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Steg 1: Ladda OneNote-dokumentet

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

 Här,`dataDir` ska peka på katalogen där ditt OneNote-dokument finns. Byta ut`"Sample1.one"` med namnet på din OneNote-fil.

## Steg 2: Hämta den aktuella sidan och dess historik

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

 Vi hämtar första sidan av dokumentet med hjälp av`getFirstChild()` och hämta sedan dess historia med hjälp av`getPageHistory()`.

## Steg 3: Tryck på den aktuella sidversionen

```java
pageHistory.addItem(page.deepClone());
```

Här lägger vi till den aktuella versionen av sidan till dess historik genom att klona den och lägga till den som ett nytt objekt.

## Steg 4: Spara dokumentet

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

Slutligen sparar vi det ändrade dokumentet med den uppdaterade sidhistoriken.

## Slutsats

I den här handledningen har vi lärt oss hur man driver den aktuella sidversionen i OneNote med Aspose.Note för Java. Genom att följa dessa steg kan du effektivt hantera versioneringen av dina OneNote-dokument programmatiskt.

## FAQ's

### F1: Kan jag använda Aspose.Note för Java för att arbeta med krypterade OneNote-filer?

S1: Ja, Aspose.Note för Java stöder arbete med både krypterade och okrypterade OneNote-filer.

### F2: Är Aspose.Note för Java kompatibel med den senaste versionen av OneNote?

S2: Aspose.Note för Java strävar efter att upprätthålla kompatibilitet med de senaste versionerna av OneNote-dokument.

### F3: Kan jag manipulera text och bilder i OneNote-dokument med Aspose.Note för Java?

S3: Absolut, Aspose.Note för Java tillhandahåller omfattande funktioner för att manipulera text, bilder och andra element i OneNote-filer.

### F4: Stöder Aspose.Note for Java konvertering av OneNote-filer till andra format?

S4: Ja, Aspose.Note för Java stöder konvertering av OneNote-filer till olika format som PDF, HTML och bildformat.

### F5: Var kan jag få support för Aspose.Note för Java om jag stöter på några problem?

 A5: Du kan besöka[Aspose.Note forum](https://forum.aspose.com/c/note/28) att söka hjälp från samhället eller kontakta Aspose support direkt.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
