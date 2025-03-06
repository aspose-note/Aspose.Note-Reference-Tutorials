---
title: Mit den Bildspeicheroptionen in OneNote als TIFF-Bild speichern
linktitle: Mit den Bildspeicheroptionen in OneNote als TIFF-Bild speichern
second_title: Aspose.Note Java API
description: Konvertieren Sie OneNote-Dokumente in TIFF und kontrollieren Sie Dateigröße und -qualität! Wählen Sie Jpeg, PackBits oder Faxkomprimierung in Java. Holen Sie sich Codebeispiele und erfahren Sie, wie! #OneNote #Java #Aspose
weight: 21
url: /de/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mit den Bildspeicheroptionen in OneNote als TIFF-Bild speichern

## Einführung

In diesem Tutorial erfahren Sie, wie Sie ein Dokument mithilfe verschiedener Komprimierungsmethoden in Aspose.Note für Java im TIFF-Bildformat speichern. Wir behandeln die Voraussetzungen, das Importieren von Paketen und stellen eine Schritt-für-Schritt-Anleitung für jede Komprimierungsmethode bereit.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

- Java Development Kit (JDK) auf Ihrem System installiert.
- Aspose.Note für Java-Bibliothek heruntergeladen und konfiguriert.
- Grundlegendes Verständnis der Programmiersprache Java.

## Pakete importieren

Zuerst müssen Sie die erforderlichen Pakete in Ihre Java-Datei importieren:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Schritt 1: Mit JPEG-Komprimierung im TIFF speichern

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // Der Pfad zum Dokumentenverzeichnis.
    String dataDir = "Your Document Directory";

    // Laden Sie das Dokument in Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  Laden Sie das Dokument mit`Document` Klasse.
-  Erstellen Sie eine Instanz von`ImageSaveOptions` und geben Sie als TIFF-Komprimierungstyp JPEG an.
- Stellen Sie die gewünschte Qualität ein (optional).
- Speichern Sie das Dokument mit den angegebenen Optionen im TIFF-Format.

## Schritt 2: Mit der PackBits-Komprimierung im TIFF speichern

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // Der Pfad zum Dokumentenverzeichnis.
    String dataDir = "Your Document Directory";

    // Laden Sie das Dokument in Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  Laden Sie das Dokument mit`Document` Klasse.
-  Erstellen Sie eine Instanz von`ImageSaveOptions` und geben Sie den TIFF-Komprimierungstyp als PackBits an.
- Speichern Sie das Dokument mit den angegebenen Optionen im TIFF-Format.

## Schritt 3: Mit CCITT Group 3 Faxkomprimierung als TIFF speichern

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // Der Pfad zum Dokumentenverzeichnis.
    String dataDir = "Your Document Directory";

    // Laden Sie das Dokument in Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  Laden Sie das Dokument mit`Document` Klasse.
-  Erstellen Sie eine Instanz von`ImageSaveOptions` und geben Sie den TIFF-Komprimierungstyp als CCITT Group 3 Fax an.
- Stellen Sie den Farbmodus auf Schwarzweiß ein.
- Speichern Sie das Dokument mit den angegebenen Optionen im TIFF-Format.

## Abschluss

In diesem Tutorial haben Sie gelernt, wie Sie ein Dokument mithilfe verschiedener Komprimierungsmethoden in Aspose.Note für Java im TIFF-Bildformat speichern. Wenn Sie der Schritt-für-Schritt-Anleitung folgen, können Sie die Funktionen von Aspose.Note effizient nutzen, um Ihre Anforderungen zu erfüllen.

## FAQs

### F1: Kann ich Aspose.Note für Java verwenden, um andere Dokumentformate in TIFF zu konvertieren?

A1: Ja, Aspose.Note für Java unterstützt die Konvertierung verschiedener Dokumentformate in TIFF, einschließlich OneNote-Dokumenten.

### F2: Welche Bedeutung hat die Angabe des Komprimierungstyps beim Speichern in TIFF?

A2: Durch Angabe des Komprimierungstyps können Sie die Bildqualität und Dateigröße steuern. Verschiedene Komprimierungsmethoden bieten Kompromisse zwischen Qualität und Komprimierungsverhältnis.

### F3: Ist Aspose.Note für Java für die Stapelverarbeitung von Dokumenten geeignet?

A3: Ja, Aspose.Note für Java bietet APIs für die Stapelverarbeitung, sodass Sie Dokumentkonvertierungsaufgaben effizient automatisieren können.

### F4: Kann ich die Komprimierungseinstellungen weiter anpassen?

A4: Ja, Sie können Parameter wie Qualität, Auflösung und Komprimierungsmethode anpassen, um die Ausgabe an Ihre Anforderungen anzupassen.

### F5: Bietet Aspose.Note für Java technischen Support?

A5: Ja, Aspose bietet umfassenden technischen Support über Foren und Ticket-basierte Systeme.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
