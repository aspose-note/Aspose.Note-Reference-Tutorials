---
title: Konvertieren Sie ein Notizbuch in ein abgeflachtes Bild in OneNote – Aspose.Note
linktitle: Konvertieren Sie ein Notizbuch in ein abgeflachtes Bild in OneNote – Aspose.Note
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Aspose.Note für Java ein Notizbuch in OneNote in ein reduziertes Bild konvertieren. Bewahren Sie alle Elemente mühelos in einer einzigen Bilddatei auf.
type: docs
weight: 13
url: /de/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---
## Einführung

In diesem Tutorial führen wir Sie durch den Prozess der Konvertierung eines Notizbuchs in ein reduziertes Bild in OneNote mit Aspose.Note für Java. Dadurch können Sie Ihr Notizbuch als Bilddatei speichern und so sicherstellen, dass alle Elemente in einem einzigen Bildformat erhalten bleiben.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1. Java Development Kit (JDK) auf Ihrem System installiert.
2.  Aspose.Note für Java-Bibliothek heruntergeladen und in Ihrem Java-Projekt eingerichtet. Sie können die Bibliothek herunterladen unter[Hier](https://releases.aspose.com/note/java/).
3. Grundkenntnisse der Java-Programmierung.

## Pakete importieren

Zunächst müssen Sie die erforderlichen Pakete aus Aspose.Note für Java importieren:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Schritt 1: Dokumentenverzeichnis einrichten

Definieren Sie zunächst das Verzeichnis, in dem sich Ihre Notebook-Datei befindet:

```java
String dataDir = "Your Document Directory";
```

 Ersetzen`"Your Document Directory"` mit dem Pfad zu Ihrer Notebook-Datei.

## Schritt 2: Notebook laden

 Laden Sie als Nächstes die Notebook-Datei mit`Notebook` Klasse:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Stellen Sie sicher, dass Sie es ersetzen`"test.onetoc2"` mit dem Namen Ihrer Notebook-Datei.

## Schritt 3: Legen Sie die Optionen zum Speichern von Bildern fest

Richten Sie nun die Optionen zum Speichern des Notizbuchs als Bild ein. Als Speicherformat legen wir PNG fest und stellen die Auflösung auf 400 DPI ein:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Sie können die Auflösung entsprechend Ihren Anforderungen anpassen.

## Schritt 4: Notizbuch flach drücken

Um sicherzustellen, dass alle Elemente zu einem einzigen Bild zusammengefasst werden, legen Sie fest`flatten` Option zu`true`:

```java
saveOptions.setFlatten(true);
```

Dadurch wird sichergestellt, dass das resultierende Bild das Layout Ihres Notizbuchs beibehält.

## Schritt 5: Bild speichern

Speichern Sie abschließend das Notizbuch als reduziertes Bild:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Ersetzen`"ExportImageasFlattenedNotebook_out.png"` mit dem gewünschten Namen der Ausgabedatei.

## Abschluss

Zusammenfassend lässt sich sagen, dass Sie mit Aspose.Note für Java Ihr Notizbuch problemlos in ein reduziertes Bild in OneNote konvertieren können. Dieser Prozess stellt sicher, dass alle Elemente in einem einzigen Bildformat erhalten bleiben, was eine einfache Weitergabe und Anzeige erleichtert.

## FAQs

### F1: Kann ich die Auflösung des Ausgabebildes anpassen?

 A1: Ja, Sie können die Auflösung entsprechend Ihren Anforderungen anpassen, indem Sie die ändern`setResolution` Methodenparameter.

### F2: Unterstützt Aspose.Note andere Bildformate für den Export?

A2: Ja, Aspose.Note unterstützt verschiedene Bildformate wie PNG, JPEG, BMP usw. zum Exportieren von Notizbüchern.

### F3: Kann ich das Ausgabebild weiter anpassen?

A3: Ja, Aspose.Note bietet umfangreiche Optionen zum Anpassen des Ausgabebilds, einschließlich Seitengröße, Ausrichtung und Qualitätseinstellungen.

### F4: Gibt es eine Testversion für Aspose.Note für Java?

 A4: Ja, Sie können eine kostenlose Testversion von erhalten[Hier](https://releases.aspose.com/).

### F5: Wo finde ich Unterstützung für Aspose.Note für Java?

 A5: Unterstützung und Ressourcen finden Sie im Aspose.Note-Forum[Hier](https://forum.aspose.com/c/note/28).