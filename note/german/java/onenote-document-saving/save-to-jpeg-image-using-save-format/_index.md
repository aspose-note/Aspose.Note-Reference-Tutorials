---
title: Mit dem Speicherformat in OneNote als JPEG-Bild speichern
linktitle: Mit dem Speicherformat in OneNote als JPEG-Bild speichern
second_title: Aspose.Note Java API
description: Konvertieren Sie ein OneNote-Dokument ganz einfach in ein JPEG-Bild! Dieses Java-Tutorial zeigt, wie Aspose.Note verwendet wird. Konvertieren und automatisieren Sie mit Codebeispielen! #OneNote #Java #Aspose
weight: 18
url: /de/java/onenote-document-saving/save-to-jpeg-image-using-save-format/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mit dem Speicherformat in OneNote als JPEG-Bild speichern

## Einführung

In diesem Tutorial befassen wir uns mit dem Prozess des Speicherns eines Dokuments im JPEG-Bildformat mit Aspose.Note für Java. Aspose.Note ist eine leistungsstarke Java-API, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten und verschiedene Vorgänge wie Konvertierung, Bearbeitung und Extraktion von Inhalten zu ermöglichen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem System das Java Development Kit (JDK) installiert ist.
2.  Aspose.Note für Java-Bibliothek: Laden Sie die Aspose.Note für Java-Bibliothek herunter und installieren Sie sie. Sie können es herunterladen unter[Hier](https://releases.aspose.com/note/java/).

## Pakete importieren

Importieren wir zunächst die notwendigen Pakete, die für unseren Java-Code erforderlich sind:

```java
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Schritt 1: Laden Sie das Dokument

 Der erste Schritt besteht darin, das Dokument in Aspose.Note zu laden. Dies kann mit der erreicht werden`Document` Klasse, bereitgestellt von Aspose.Note.

```java
// Der Pfad zum Dokumentenverzeichnis.
String dataDir = "Your Document Directory";

// Laden Sie das Dokument in Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Schritt 2: Als JPEG-Bild speichern

 Als nächstes geben wir den Pfad der Ausgabedatei an und speichern das Dokument im JPEG-Bildformat mit`save()` Methode zusammen mit der`SaveFormat.Jpeg` Parameter.

```java
// Geben Sie den Pfad der Ausgabedatei an.
dataDir = dataDir + "SaveToJpegImageUsingSaveFormat_out.jpg";

// Speichern Sie das Dokument.
oneFile.save(dataDir, SaveFormat.Jpeg);
```

## Abschluss

In diesem Tutorial haben wir gelernt, wie man ein Dokument mit Aspose.Note für Java als JPEG-Bild speichert. Wenn Sie die bereitgestellten Schritte befolgen, können Sie Ihre OneNote-Dateien nahtlos programmgesteuert in das JPEG-Format konvertieren und so verschiedene Möglichkeiten zur Integration und Automatisierung in Ihre Java-Anwendungen ermöglichen.

## FAQs

### F1: Kann Aspose.Note komplexe OneNote-Dateien verarbeiten?

A1: Ja, Aspose.Note ist darauf ausgelegt, komplexe OneNote-Dateien effizient zu verarbeiten und eine genaue Konvertierung und Bearbeitung sicherzustellen.

### F2: Gibt es eine Testversion für Aspose.Note für Java?

 A2: Ja, Sie können eine kostenlose Testversion von Aspose.Note für Java erhalten von[Hier](https://releases.aspose.com/).

### F3: Wie erhalte ich Unterstützung für Aspose.Note für Java?

 A3: Sie können Unterstützung für Aspose.Note für Java erhalten, indem Sie die besuchen[Aspose.Note-Forum](https://forum.aspose.com/c/note/28).

### F4: Kann ich eine temporäre Lizenz für Aspose.Note für Java erwerben?

 A4: Ja, Sie können eine temporäre Lizenz erwerben bei[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Wo finde ich eine ausführliche Dokumentation für Aspose.Note für Java?

A5: Eine ausführliche Dokumentation zu Aspose.Note für Java finden Sie hier[Hier](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
