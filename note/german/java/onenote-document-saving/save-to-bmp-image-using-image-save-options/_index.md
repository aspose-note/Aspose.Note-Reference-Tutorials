---
title: Mit den Bildspeicheroptionen in OneNote als BMP-Bild speichern
linktitle: Mit den Bildspeicheroptionen in OneNote als BMP-Bild speichern
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie OneNote-Dokumente mit Aspose.Note für Java programmgesteuert in BMP-Bildern speichern. Schritt-für-Schritt-Anleitung mit Codebeispielen.
type: docs
weight: 16
url: /de/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
---
## Einführung

Aspose.Note für Java ist eine leistungsstarke Bibliothek, die es Java-Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten. Mit Aspose.Note für Java können Sie OneNote-Dokumente nahtlos erstellen, bearbeiten und konvertieren. In diesem Tutorial erfahren Sie, wie Sie ein OneNote-Dokument mithilfe der von Aspose.Note für Java bereitgestellten Bildspeicheroptionen in einem BMP-Bild speichern.

## Voraussetzungen

Bevor Sie mit diesem Tutorial fortfahren, stellen Sie sicher, dass Sie über Folgendes verfügen:

1. Grundkenntnisse der Programmiersprache Java.
2. Installiertes JDK (Java Development Kit) auf Ihrem System.
3. Integrierte Entwicklungsumgebung (IDE) wie Eclipse oder IntelliJ IDEA.
4.  Aspose.Note für Java-Bibliothek. Sie können es herunterladen unter[Hier](https://releases.aspose.com/note/java/).

## Pakete importieren

Zunächst müssen Sie die erforderlichen Pakete aus Aspose.Note für Java importieren, um dessen Funktionen nutzen zu können. Fügen Sie Ihrer Java-Datei die folgende Importanweisung hinzu:

```java
import com.aspose.note.*;
import java.io.IOException;
```

Lassen Sie uns nun das bereitgestellte Beispiel in mehrere Schritte unterteilen:

## Schritt 1: Laden Sie das Dokument

```java
// Der Pfad zum Dokumentenverzeichnis.
String dataDir = "Your Document Directory";

// Laden Sie das Dokument in Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

In diesem Schritt geben wir den Pfad zu dem Verzeichnis an, in dem sich unser OneNote-Dokument befindet. Dann laden wir das Dokument mit`Document` Klasse, bereitgestellt von Aspose.Note für Java.

## Schritt 2: Als BMP-Bild speichern

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Speichern Sie das Dokument.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

 In diesem Schritt geben wir den Ausgabepfad für das BMP-Bild an, das aus dem OneNote-Dokument generiert wird. Wir benutzen das`save` Methode der`Document` Klasse zum Speichern des Dokuments als BMP-Bild, Bereitstellung des Ausgabepfads und einer Instanz von`ImageSaveOptions` mit dem Gewünschten`SaveFormat` (in diesem Fall,`SaveFormat.Bmp`).

## Abschluss

In diesem Tutorial haben wir gelernt, wie man mit Aspose.Note für Java ein OneNote-Dokument in einem BMP-Bild speichert. Wenn Sie der Schritt-für-Schritt-Anleitung folgen, können Sie diese Funktionalität nahtlos in Ihre Java-Anwendungen integrieren und so OneNote-Dokumente problemlos bearbeiten.

## FAQs

### F1: Kann ich OneNote-Dokumente in anderen Bildformaten als BMP speichern?

A1: Ja, Sie können OneNote-Dokumente mit Aspose.Note für Java in verschiedenen Bildformaten wie JPEG, PNG, GIF und TIFF speichern.

### F2: Unterstützt Aspose.Note für Java die Konvertierung zwischen verschiedenen Dokumentformaten?

A2: Ja, Aspose.Note für Java unterstützt die Konvertierung zwischen OneNote-Dokumenten und anderen Formaten wie PDF, DOCX, HTML und mehr.

### F3: Ist Aspose.Note für Java mit den neuesten Versionen von OneNote kompatibel?

A3: Ja, Aspose.Note für Java wird regelmäßig aktualisiert, um die Kompatibilität mit den neuesten Versionen von OneNote sicherzustellen.

### F4: Kann ich den Inhalt von OneNote-Dokumenten programmgesteuert mit Aspose.Note für Java bearbeiten?

A4: Ja, Sie können den Inhalt, die Struktur und die Formatierung von OneNote-Dokumenten programmgesteuert mit Aspose.Note für Java bearbeiten.

### F5: Bietet Aspose.Note für Java technischen Support?

 A5: Ja, Aspose bietet technischen Support für seine Produkte. Sie können die besuchen[Aspose.Note-Forum](https://forum.aspose.com/c/note/28) zur Hilfe.