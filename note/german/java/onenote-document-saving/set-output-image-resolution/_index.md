---
title: Legen Sie die Ausgabebildauflösung in OneNote fest – Aspose.Note
linktitle: Legen Sie die Ausgabebildauflösung in OneNote fest – Aspose.Note
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie die Bildauflösung in OneNote-Dokumenten mit Aspose.Note für Java anpassen. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine einfache Implementierung
type: docs
weight: 23
url: /de/java/onenote-document-saving/set-output-image-resolution/
---
## Einführung

Möchten Sie die Auflösung von Bildern in Ihren OneNote-Dokumenten mit Java manipulieren? Aspose.Note für Java bietet eine robuste Lösung für solche Aufgaben. In diesem Tutorial führen wir die Schritte zum Festlegen der Ausgabebildauflösung mit Aspose.Note durch.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Java Development Kit (JDK): Installieren Sie JDK auf Ihrem System.
2. Aspose.Note für Java: Laden Sie Aspose.Note für Java von herunter und installieren Sie es[Webseite](https://releases.aspose.com/note/java/).
3. Integrierte Entwicklungsumgebung (IDE): Wählen Sie Ihre bevorzugte IDE wie Eclipse oder IntelliJ IDEA.

## Pakete importieren

Importieren Sie in Ihr Java-Projekt die erforderlichen Aspose.Note-Pakete:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Schritt 1: Laden Sie das OneNote-Dokument

Laden Sie zunächst das OneNote-Dokument in Ihre Java-Anwendung:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

 Ersetzen`"Your Document Directory"` mit dem tatsächlichen Verzeichnis, in dem sich Ihr OneNote-Dokument befindet.

## Schritt 2: Legen Sie die Optionen zum Speichern von Bildern fest

Definieren Sie die Bildspeicheroptionen und geben Sie die gewünschte Auflösung an:

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

 Hier stellen wir die Auflösung auf ein`120 dpi`. Sie können diesen Wert entsprechend Ihren Anforderungen anpassen.

## Schritt 3: Speichern Sie das Dokument mit geänderter Auflösung

Speichern Sie das Dokument mit der aktualisierten Bildauflösung:

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

Dadurch wird das geänderte Dokument mit der angegebenen Auflösung gespeichert.

## Abschluss

In diesem Tutorial haben wir untersucht, wie Sie die Ausgabebildauflösung in OneNote-Dokumenten mithilfe von Aspose.Note für Java festlegen. Wenn Sie diese einfachen Schritte befolgen, können Sie die Auflösung von Bildern effizient anpassen, um die Anforderungen Ihrer Anwendung zu erfüllen.


## FAQs

### F1: Kann ich die Bildauflösung auf einen Wert über 120 dpi einstellen?

A1: Ja, Sie können die Auflösung je nach Bedarf auf jeden gewünschten Wert einstellen.

### F2: Unterstützt Aspose.Note neben JPEG auch andere Bildformate?

A2: Ja, Aspose.Note unterstützt verschiedene Bildformate wie PNG, BMP, GIF usw.

### F3: Ist Aspose.Note mit allen Java-Versionen kompatibel?

A3: Aspose.Note ist mit Java 1.6 oder späteren Versionen kompatibel.

### F4: Kann ich mit Aspose.Note andere Aspekte von Bildern in OneNote-Dokumenten bearbeiten?

A4: Ja, Aspose.Note bietet umfassende Funktionen zur Bildbearbeitung, einschließlich Größenänderung, Zuschneiden und Drehen.

### F5: Wo erhalte ich Unterstützung für Aspose.Note-bezogene Abfragen?

 A5: Sie können Hilfe im Aspose.Note-Community-Forum suchen[Hier](https://forum.aspose.com/c/note/28).