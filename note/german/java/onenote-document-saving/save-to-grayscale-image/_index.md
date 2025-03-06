---
title: Als Graustufenbild in OneNote speichern – Aspose.Note
linktitle: Als Graustufenbild in OneNote speichern – Aspose.Note
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Aspose.Note für Java ein Dokument als Graustufenbild in OneNote speichern. Bearbeiten Sie Microsoft OneNote-Dokumente ganz einfach programmgesteuert.
weight: 17
url: /de/java/onenote-document-saving/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Als Graustufenbild in OneNote speichern – Aspose.Note

## Einführung

In diesem Tutorial erfahren Sie, wie Sie mit Aspose.Note für Java ein Dokument als Graustufenbild in OneNote speichern. Graustufenbilder sind monochromatische Bilder, bei denen die Farbinformationen nur durch Graustufen dargestellt werden. Aspose.Note ist eine leistungsstarke Java-API, die die programmgesteuerte Bearbeitung von Microsoft OneNote-Dokumenten ermöglicht.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1. Java Development Kit (JDK) auf Ihrem System installiert.
2.  Aspose.Note für Java-Bibliothek. Sie können es herunterladen unter[Hier](https://releases.aspose.com/note/java/).
3. Grundlegendes Verständnis der Java-Programmierung.

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Schritt 1: Laden Sie das Dokument

 Laden Sie zunächst das Dokument in Aspose.Note. Ersetzen`"Your Document Directory"` mit dem Pfad zu Ihrem Dokumentenverzeichnis und`"Aspose.one"` mit dem Namen Ihres OneNote-Dokuments.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Schritt 2: Ausgabepfad und Optionen festlegen

Definieren Sie den Ausgabepfad für das Graustufenbild und legen Sie die Speicheroptionen fest. Wir stellen den Farbmodus auf Graustufen ein.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Schritt 3: Speichern Sie das Dokument

Speichern Sie abschließend das Dokument mit den angegebenen Optionen als Graustufenbild.

```java
oneFile.save(dataDir, options);
```

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.Note für Java ein Dokument als Graustufenbild in OneNote speichern. Dies kann für verschiedene Anwendungen, bei denen Graustufenbilder erforderlich sind, äußerst nützlich sein.

## FAQs

### F1: Kann ich das Graustufenbild in einem anderen Format speichern?

 A1: Ja, das können Sie. Ändern Sie einfach die`SaveFormat` Parameter in der`ImageSaveOptions` Konstruktor in Ihr gewünschtes Format.

### F2: Ist Aspose.Note mit allen Versionen von OneNote-Dokumenten kompatibel?

A2: Aspose.Note unterstützt Microsoft OneNote 2010 und höher.

### F3: Ist für die Nutzung von Aspose.Note eine Lizenz erforderlich?

A3: Ja, Sie benötigen eine gültige Lizenz, um Aspose.Note in Produktionsumgebungen verwenden zu können. Sie können jedoch zu Testzwecken eine temporäre Lizenz erwerben.

### F4: Kann ich andere Aspekte des Dokuments manipulieren, bevor ich es als Bild speichere?

A4: Auf jeden Fall! Aspose.Note bietet zahlreiche Funktionen zum programmgesteuerten Bearbeiten von OneNote-Dokumenten.

### F5: Wo finde ich Unterstützung, wenn ich auf Probleme stoße?

A5: Unterstützung finden Sie im Aspose.Note-Forum[Hier](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
