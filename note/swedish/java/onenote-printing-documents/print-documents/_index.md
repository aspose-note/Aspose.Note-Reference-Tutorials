---
title: Skriv ut dokument i OneNote - Aspose.Note
linktitle: Skriv ut dokument i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Lär dig hur du skriver ut dokument i OneNote med Aspose.Note för Java. Steg-för-steg-guide med kodexempel och anpassningsbara alternativ.
type: docs
weight: 10
url: /sv/java/onenote-printing-documents/print-documents/
---
## Introduktion

Att skriva ut dokument är ett vanligt krav för olika applikationer, inklusive OneNote. Aspose.Note för Java ger kraftfulla funktioner för att enkelt skriva ut dokument i dina Java-applikationer. I den här handledningen går vi igenom processen att skriva ut dokument i OneNote med Aspose.Note för Java.

## Förutsättningar

Innan du börjar, se till att du har följande förutsättningar på plats:

1. Java Development Kit (JDK): Se till att du har JDK installerat på ditt system.
2.  Aspose.Note for Java JAR: Ladda ner och inkludera Aspose.Note for Java-biblioteket i ditt projekt. Du kan ladda ner den från[här](https://releases.aspose.com/note/java/).
3. OneNote-dokument: Förbered OneNote-dokumentet som du vill skriva ut.

## Importera paket

Först måste du importera de nödvändiga paketen till din Java-klass:

```java
import javax.print.PrintException;

import com.aspose.note.Document;
import com.aspose.note.DocumentPrintAttributeSet;
import com.aspose.note.PrintOptions;
```

## Steg 1: Skriv ut ett dokument

Låt oss börja med att skriva ut ett dokument utan några specifika utskriftsalternativ.

```java
public static void PrintDocument() throws PrintException {
    // Ange katalogen där ditt dokument finns
    String dataDir = "Your Document Directory";
    
    // Ladda OneNote-dokumentet
    Document document = new Document(dataDir + "YourDocument.one");
    
    // Skriv ut dokumentet
    document.print();
}
```

## Steg 2: Skriv ut ett dokument med utskriftsalternativ

Du kan anpassa utskriftsprocessen genom att ange utskriftsalternativ som utskriftsintervall och skrivarinställningar.

```java
public static void PrintDocumentWithPrintOptions() throws PrintException {
    // Ange katalogen där ditt dokument finns
    String dataDir = "Your Document Directory";

    // Ladda OneNote-dokumentet
    Document document = new Document(dataDir + "YourDocument.one");

    // Definiera utskriftsalternativ
    final DocumentPrintAttributeSet asposeAttr = new DocumentPrintAttributeSet("Microsoft XPS Document Writer");
    asposeAttr.setPrintRange(1, 2);

    // Skriv ut dokumentet med angivna alternativ
    document.print(asposeAttr);
}
```

## Steg 3: Skriv ut dokument med en virtuell skrivare

Du kan också använda virtuella skrivare för att skriva ut dokument. Så här skriver du ut dokument med en virtuell PDF-skrivare.

```java
public static void PrintDocumentsWithVirtualPrinter() throws PrintException {
    // Ange katalogen där ditt dokument finns
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "YourDocument.one");
     
    // Definiera utskriftsalternativ för virtuell skrivare
    final DocumentPrintAttributeSet asposeAttr = new DocumentPrintAttributeSet("doPDF 8");
    asposeAttr.setPrintRange(1, 2);
    asposeAttr.setCopies(3);
     
    PrintOptions printOptions = new PrintOptions();
    printOptions.setDocumentName("YourDocument.one");
    printOptions.setPrinterSettings(asposeAttr);
      
    // Skriv ut dokumentet med virtuell skrivare
    doc.print(printOptions);
}
```

## Slutsats

Att skriva ut dokument i OneNote med Aspose.Note för Java är enkelt och flexibelt. Genom att följa stegen som beskrivs i den här handledningen kan du sömlöst integrera dokumentutskriftsfunktioner i dina Java-program.

## FAQ's

### F1: Kan jag skriva ut specifika sidor i ett OneNote-dokument?

S1: Ja, du kan ange utskriftsintervall för att skriva ut specifika sidor i dokumentet.

### F2: Är Aspose.Note för Java kompatibel med virtuella skrivare?

S2: Ja, Aspose.Note för Java stöder utskrift av dokument med virtuella skrivare.

### F3: Kan jag anpassa utskriftsinställningar som antalet kopior?

A3: Absolut, du kan anpassa olika utskriftsinställningar inklusive antal kopior, utskriftsintervall och mer.

### F4: Kräver Aspose.Note för Java en licens för att skriva ut dokument?

S4: Ja, du behöver en giltig licens för att använda Aspose.Note för Java i en produktionsmiljö.

### F5: Var kan jag hitta mer support och resurser för Aspose.Note för Java?

 S5: Du kan hitta dokumentation, forum och ytterligare resurser på[Aspose.Note för Java-supportsida](https://forum.aspose.com/c/note/28).