---
date: 2025-12-28
description: Erfahren Sie, wie Sie **OneNote in ein Bild konvertieren** und die Bildauflösung
  in Java mit Aspose.Note festlegen. Diese Schritt‑für‑Schritt‑Anleitung zeigt außerdem,
  wie Sie OneNote‑PNG‑Dateien exportieren.
linktitle: Convert OneNote to Image with Options - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote in Bild konvertieren mit Optionen – Aspose.Note
url: /de/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote in Bild konvertieren mit Optionen – Aspose.Note

## Einleitung

In diesem Tutorial lernen Sie, wie Sie **OneNote in ein Bild** konvertieren können, mit einer Vielzahl von Optionen mithilfe von Aspose.Note für Java. Egal, ob Sie ein hochauflösendes PNG für Berichte benötigen oder ein schnelles JPEG‑Vorschaubild, die nachfolgenden Schritte zeigen Ihnen genau, wie Sie dies erreichen und den Vorgang in Ihre Java‑Anwendungen integrieren.

## Schnelle Antworten
- **Was bedeutet „OneNote in Bild konvertieren“?** Es wandelt ein gesamtes OneNote‑Notizbuch in Raster‑Bilddateien (PNG, JPEG usw.) um.
- **Welches Format wird für verlustfreie Qualität empfohlen?** PNG, weil es alle Details ohne Kompressionsartefakte bewahrt.
- **Wie kann ich die Bildauflösung in Java festlegen?** Verwenden Sie `ImageSaveOptions.setResolution(int dpi)` über `NotebookImageSaveOptions`.
- **Kann ich ein OneNote‑Notizbuch in einem Schritt als PNG exportieren?** Ja, Aspose.Note bietet einen einzelnen `save`‑Aufruf mit den entsprechenden Optionen.
- **Benötige ich eine Lizenz für den Produktionseinsatz?** Für die Produktion ist eine kommerzielle Lizenz erforderlich; ein kostenloser Testzeitraum steht zur Evaluierung bereit.

## Was bedeutet „OneNote in Bild konvertieren“?
Das Konvertieren eines OneNote‑Notizbuchs in ein Bild bedeutet, jede Seite des Notizbuchs als Bitmap‑Datei zu rendern. Dies ist nützlich, um statische Vorschaubilder zu erstellen, Inhalte zu archivieren oder Notizbuchseiten in Berichte einzubetten, in denen das ursprüngliche OneNote‑Format nicht unterstützt wird.

## Warum Aspose.Note für Java verwenden?
- **Vollständige Kontrolle** über Ausgabeformat, Auflösung und Farbtiefe.  
- **Keine Microsoft‑Office‑Abhängigkeit** – funktioniert in jeder serverseitigen Java‑Umgebung.  
- **Unterstützt komplexe Notizbücher** mit eingebetteten Dateien, Handschrift und Rich‑Text.

## Voraussetzungen

1. **Java Development Kit (JDK)** – Version 8 oder höher.  
2. **Aspose.Note für Java JAR‑Dateien** – laden Sie die neueste Bibliothek von [hier](https://releases.aspose.com/note/java/) herunter und fügen Sie sie dem Klassenpfad Ihres Projekts hinzu.  

## Pakete importieren

Importieren Sie zunächst die Klassen, die wir zum Laden des Notizbuchs und zur Konfiguration der Bildausgabe benötigen.

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Schritt 1: Notizbuch laden

Laden Sie das OneNote‑Notizbuch, das Sie konvertieren möchten. Ersetzen Sie den Pfad durch den Speicherort Ihrer `.onetoc2`‑Datei.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## Schritt 2: Speicheroptionen festlegen (Wie man **image resolution java** setzt)

Erstellen Sie eine Instanz von `NotebookImageSaveOptions`, wählen Sie das Ausgabeformat und geben Sie die gewünschte Auflösung an. In diesem Beispiel verwenden wir PNG mit 400 dpi.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

> **Pro tip:** Für eine schnellere Verarbeitung großer Notizbücher reduzieren Sie die Auflösung (z. B. 150 dpi). Erhöhen Sie sie für druckfertige Grafiken.

## Schritt 3: Notizbuch als Bild speichern (Wie man **export OneNote PNG**)

Definieren Sie den Ausgabedateinamen und rufen Sie `save` auf. Die gleichen Optionen werden auf jede Seite des Notizbuchs angewendet.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

Der obige Code erzeugt eine PNG‑Datei (oder eine Reihe von PNG‑Dateien, jeweils eine pro Seite) mit der von Ihnen festgelegten Auflösung.

## Häufige Probleme und Lösungen

| Problem | Lösung |
|-------|----------|
| **OutOfMemoryError** bei großen Notizbüchern | Erhöhen Sie die JVM‑Heap‑Größe (`-Xmx2g`) oder reduzieren Sie die Auflösung. |
| **Leere Seiten in der Ausgabe** | Stellen Sie sicher, dass das Notizbuch nicht passwortgeschützt ist; verwenden Sie ggf. `Notebook.load(path, password)`. |
| **Nicht unterstütztes Bildformat** | Verwenden Sie nur `SaveFormat.Png`, `SaveFormat.Jpeg` oder `SaveFormat.Bmp` – andere Formate werden für den Notizbuch‑Export nicht unterstützt. |

## Häufig gestellte Fragen

**F: Kann Aspose.Note komplexe OneNote‑Dateien verarbeiten?**  
A: Ja, es verarbeitet Notizbücher mit eingebetteten Dateien, Handschrift‑Anmerkungen und umfangreicher Formatierung effizient.

**F: Lässt sich Aspose.Note für Java leicht in bestehende Projekte integrieren?**  
A: Absolut. Die API ist unkompliziert, und Sie müssen lediglich die JAR‑Datei zu Ihrem Klassenpfad hinzufügen.

**F: Kann ich die Bildausgabe beim Konvertieren eines Notizbuchs anpassen?**  
A: Ja. Sie können Auflösung, Format und sogar die Farbtiefe über `ImageSaveOptions` festlegen.

**F: Bietet Aspose.Note Support für Entwickler?**  
A: Ja. Aspose stellt umfangreiche Dokumentation, Foren und reaktionsschnelle Support‑Kanäle bereit.

**F: Gibt es eine kostenlose Testversion von Aspose.Note für Java?**  
A: Ja, Sie können eine Testversion von [hier](https://releases.aspose.com/) herunterladen.

---

**Zuletzt aktualisiert:** 2025-12-28  
**Getestet mit:** Aspose.Note 24.11 für Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}