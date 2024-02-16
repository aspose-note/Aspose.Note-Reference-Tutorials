---
title: Kontrollera om OneNote-dokumentet är krypterat - Java
linktitle: Kontrollera om OneNote-dokumentet är krypterat - Java
second_title: Aspose.Note Java API
description: Lär dig hur du kontrollerar om ett OneNote-dokument är krypterat i Java med Aspose.Note. Följ vår steg-för-steg-guide för effektiv dokumenthantering.
type: docs
weight: 10
url: /sv/java/onenote-document-loading/check-document-encrypted/
---
## Introduktion

När du arbetar med OneNote-dokument i Java är det avgörande att se till att dokumentet inte är krypterat innan du bearbetar det. Att kryptera dokument kan lägga till ett extra lager av säkerhet, men det kan också komplicera bearbetningsstegen om det inte hanteras på rätt sätt. I den här handledningen guidar vi dig genom processen att kontrollera om ett OneNote-dokument är krypterat med Aspose.Note för Java.

## Förutsättningar

Innan du börjar, se till att du har följande förutsättningar på plats:

1.  Java Development Kit (JDK): Se till att du har Java installerat på ditt system. Du kan ladda ner den från[här](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

2.  Aspose.Note for Java Library: Ladda ner och ställ in Aspose.Note for Java-biblioteket. Du hittar nedladdningslänken[här](https://releases.aspose.com/note/java/).

## Importera paket

För att börja, importera de nödvändiga paketen i ditt Java-projekt:

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```

Låt oss dela upp processen i flera steg:

## Steg 1: Kontrollera om dokument från Stream är krypterat

```java
public static void CheckIfDocumentFromStreamIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromStreamIsEncrypted
    String dataDir = "Your Document Directory";

    LoadOptions loadOptions = new LoadOptions();
    loadOptions.setDocumentPassword("password");

    FileInputStream stream = new FileInputStream(Paths.get(dataDir, "Sample1.one").toString());

    try {
        Document ref[] = { null };
        if (!Document.isEncrypted(stream, loadOptions, ref)) {
            System.out.println("The document is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Provide a password.");
        }
    } finally {
        stream.close();
    }
    // ExEnd:CheckIfDocumentFromStreamIsEncrypted
}
```

Förklaring:

- Den här metoden kontrollerar om ett dokument som laddats från en ström är krypterat.
-  Den ställer in dokumentlösenordet med`setDocumentPassword` metod av`LoadOptions` klass.
-  De`Document.isEncrypted` metod används för att avgöra om dokumentet är krypterat eller inte.

## Steg 2: Kontrollera om dokument från fil är krypterat

```java
public static void CheckIfDocumentFromFileIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromFileIsEncrypted
    String dataDir = "Your Document Directory";

    Document ref[] = { null };
    if (!Document.isEncrypted(Paths.get(dataDir, "Sample1.one").toString(), "VerySecretPassword", ref)) {
        if (ref[0] != null) {
            System.out.println("The document is decrypted. It is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Invalid password was provided.");
        }
    } else {
        System.out.println("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
    // ExEnd:CheckIfDocumentFromFileIsEncrypted
}
```

Förklaring:

- Denna metod kontrollerar om ett dokument som laddats från en fil är krypterat.
-  Den använder`Document.isEncrypted` metod på samma sätt som föregående steg men med en filsökväg och lösenordsparameter.

## Slutsats

I den här handledningen lärde vi oss hur man kontrollerar om ett OneNote-dokument är krypterat i Java med Aspose.Note. Genom att följa den steg-för-steg-guide och använda de medföljande kodexemplen kan du effektivt fastställa krypteringsstatusen för dina dokument, vilket säkerställer smidig bearbetning i dina Java-applikationer.

## FAQ's

### F1: Kan jag kontrollera krypteringsstatus utan att ange ett lösenord?

S1: Ja, du kan kontrollera krypteringsstatusen utan att ange ett lösenord. De`Document.isEncrypted` metoden låter dig göra det.

### F2: Vad händer om jag anger ett felaktigt lösenord?

 S2: Om du anger ett felaktigt lösenord när du kontrollerar krypteringsstatus kommer metoden att återkomma`true`, vilket indikerar att dokumentet är krypterat, men det angivna lösenordet är felaktigt.

### F3: Är det möjligt att dekryptera ett krypterat dokument programmatiskt?

S3: Ja, du kan dekryptera ett krypterat dokument programmatiskt genom att ange rätt lösenord under dokumentladdningen.

### F4: Kan jag använda Aspose.Note för andra dokumentformat än OneNote?

S4: Nej, Aspose.Note är speciellt utformad för att endast arbeta med OneNote-dokument.

### F5: Var kan jag hitta fler resurser och support för Aspose.Note för Java?

 A5: Du kan besöka[Aspose.Note forum](https://forum.aspose.com/c/note/28) för samhällsstöd och dokumentation.