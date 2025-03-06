---
title: Mit den Seiteneinstellungen in OneNote – Aspose.Note – als PDF speichern
linktitle: Mit den Seiteneinstellungen in OneNote – Aspose.Note – als PDF speichern
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie OneNote-Dokumente mithilfe der Aspose.Note-Bibliothek in Java als PDF speichern. Schritt-für-Schritt-Anleitung mit Codebeispielen für verschiedene Seiteneinstellungen.
weight: 19
url: /de/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mit den Seiteneinstellungen in OneNote – Aspose.Note – als PDF speichern

## Einführung

In diesem Tutorial erfahren Sie, wie Sie OneNote-Dokumente mithilfe verschiedener Seiteneinstellungen mit Aspose.Note für Java im PDF-Format speichern. Wir behandeln zwei Methoden: Speichern mit den Seiteneinstellungen im Letter-Format und Speichern mit den Seiteneinstellungen im A4-Format ohne Höhenbeschränkung.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Java Development Kit (JDK) auf Ihrem System installiert.
2. Aspose.Note für Java-Bibliothek heruntergeladen und in Ihr Java-Projekt eingebunden.
3. Grundlegendes Verständnis der Programmiersprache Java.

## Pakete importieren

Stellen Sie sicher, dass Sie die erforderlichen Pakete für die Verwendung von Aspose.Note für Java in Ihrem Projekt importiert haben. Hier ist die Importanweisung:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Mit den Letter-Seiteneinstellungen als PDF speichern

### Schritt 1: Laden Sie das Dokument

Laden Sie zunächst das OneNote-Dokument in Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Schritt 2: Zielpfad definieren

Geben Sie den Zielpfad für die PDF-Datei an:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Schritt 3: Speichern Sie das Dokument

Speichern Sie das Dokument mit den Letter-Seiteneinstellungen:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Mit A4-Seiteneinstellungen ohne Höhenbeschränkung als PDF speichern

### Schritt 1: Laden Sie das Dokument

Laden Sie auf ähnliche Weise das OneNote-Dokument in Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Schritt 2: Zielpfad definieren

Geben Sie den Zielpfad für die PDF-Datei an:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Schritt 3: Speichern Sie das Dokument

Speichern Sie das Dokument mit A4-Seiteneinstellungen ohne Höhenbegrenzung:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Nachdem Sie diese Schritte ausgeführt haben, haben Sie Ihr OneNote-Dokument mit verschiedenen Seiteneinstellungen erfolgreich als PDF gespeichert.

## Abschluss

In diesem Tutorial haben wir untersucht, wie man OneNote-Dokumente mithilfe der Aspose.Note für Java-Bibliothek im PDF-Format speichert. Wenn Sie der Schritt-für-Schritt-Anleitung folgen, können Sie diese Funktionalität problemlos in Ihre Java-Anwendungen integrieren.

## FAQs

### F1: Kann ich die Seiteneinstellungen weiter anpassen?

A1: Ja, Sie können die Seiteneinstellungen mit Aspose.Note für Java an Ihre Anforderungen anpassen.

### F2: Unterstützt Aspose.Note neben PDF auch andere Ausgabeformate?

A2: Ja, Aspose.Note unterstützt verschiedene Ausgabeformate, einschließlich Bilder und HTML.

### F3: Ist Aspose.Note mit verschiedenen Versionen von OneNote-Dateien kompatibel?

A3: Ja, Aspose.Note unterstützt OneNote-Dateien verschiedener Versionen, einschließlich .one und .onetoc2.

### F4: Kann ich mehrere OneNote-Dateien in einem einzigen Durchgang in PDF konvertieren?

A4: Ja, Sie können mit Aspose.Note für Java mehrere OneNote-Dateien stapelweise verarbeiten.

### F5: Gibt es eine Testversion zu Testzwecken?

A5: Ja, Sie können auf der Website eine kostenlose Testversion von Aspose.Note für Java herunterladen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
