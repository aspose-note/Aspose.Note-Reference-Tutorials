---
date: 2026-11-05
description: Erfahren Sie, wie Sie die TIFF-Dateigröße beim Konvertieren von OneNote-Notizbüchern
  in TIFF in Java mit Aspose.Note reduzieren können. Enthält JPEG-, PackBits- und
  Schwarz‑weiß‑TIFF-Optionen.
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: Wie man die TIFF-Dateigröße beim Konvertieren von OneNote in Java reduziert
og_description: Erfahren Sie, wie Sie die TIFF-Dateigröße beim Konvertieren von OneNote-Notizbüchern
  in TIFF in Java mit Aspose.Note reduzieren können. Enthält JPEG-, PackBits- und
  Schwarz‑weiß‑TIFF-Optionen.
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: Wie man die TIFF-Dateigröße beim Konvertieren von OneNote in Java reduziert
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: Wie man die TIFF-Dateigröße beim Konvertieren von OneNote in Java reduziert
url: /de/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man die TIFF-Dateigröße beim Konvertieren von OneNote in Java reduziert

## Einführung

In diesem Tutorial erfahren Sie, wie Sie **die TIFF-Dateigröße reduzieren** können, während Sie OneNote-Notizbücher in TIFF‑Bilder mit Aspose.Note für Java konvertieren. Wir gehen drei Komprimierungsmethoden durch – TIFF JPEG, PackBits und CCITT Group 3 (schwarz‑weiß TIFF) – und zeigen Ihnen, wie Sie die Bildqualität anpassen, den Farbmodus steuern und die Dateigröße für Web‑, Archivierungs‑ oder Fax‑Szenarien optimal halten.

## Schnellantworten
- **Was ist TIFF JPEG‑Kompression?** Eine verlustbehaftete Kompressionsmethode, die die TIFF‑Dateigröße reduziert und gleichzeitig die visuelle Qualität bewahrt.  
- **Welche Bibliothek führt die Konvertierung durch?** Aspose.Note für Java.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für Tests; für den Produktionseinsatz ist eine Lizenz erforderlich.  
- **Kann ich die Bildqualität ändern?** Ja, setzen Sie die Eigenschaft `quality` bei `ImageSaveOptions`.  
- **Ist eine Batch‑Konvertierung möglich?** Absolut – iterieren Sie über Dokumente und wenden Sie dieselben Optionen an.

## Überblick über TIFF JPEG‑Kompression

TIFF JPEG‑Kompression speichert Bilddaten in einem TIFF‑Container, wendet jedoch den verlustbehafteten JPEG‑Algorithmus an, um die Datei zu verkleinern. Sie ist ideal, wenn Sie ein Gleichgewicht zwischen **tiff Bildqualität** und kleinerer Dateigröße benötigen, insbesondere für Web‑ oder Archivierungsszenarien.

## Warum verschiedene TIFF‑Kompressionstypen verwenden?

Sie wählen den Kompressionstyp basierend auf Inhalt und Speicherbedarf: JPEG eignet sich am besten für Fotos, PackBits liefert verlustfreie Kompression für Grafiken mit großen einheitlichen Bereichen, und CCITT Group 3 bietet eine hohe Kompressionsrate für monochrome Fax‑Dokumente. Die richtige Methode ermöglicht es Ihnen, **die TIFF‑Dateigröße zu reduzieren**, ohne die für Ihre Anwendung erforderliche visuelle Treue zu beeinträchtigen.

## Auswahl der richtigen Kompression

- **JPEG** – Einstellbare Qualität (0‑100) ermöglicht das Abwägen von Größe vs. Detail, perfekt für farbreiche Seiten.  
- **PackBits** – Verlustfreie Run‑Length‑Kodierung; ideal, wenn jedes Pixel exakt erhalten bleiben muss.  
- **CCITT Group 3** – Nur monochrom; maximiert die Kompression für gescannte Texte oder Fax‑Dokumente.  

## OneNote in TIFF mit Aspose.Note konvertieren

Wenn Ihr Ziel ist, **OneNote in TIFF zu konvertieren**, decken die drei Methoden unten die gängigsten Szenarien ab. Jede Methode lädt eine `.one`‑Datei, konfiguriert `ImageSaveOptions` und speichert das Ergebnis als `.tiff`‑Datei.

## Voraussetzungen

- Java Development Kit (JDK) installiert.  
- Aspose.Note für Java Bibliothek zu Ihrem Projekt hinzugefügt (Maven/Gradle oder manuell als JAR).  
- Grundlegende Kenntnisse der Java‑Syntax.

## Pakete importieren

Die Klassen `ImageSaveOptions`, `TiffCompression` und `ColorMode` bilden das Kernstück der Konvertierungs‑API.  

`ImageSaveOptions` definiert die Optionen zum Speichern von Bildern, wie Format und Kompression.  
`TiffCompression` enumeriert die unterstützten TIFF‑Kompressionsalgorithmen.  
`ColorMode` gibt die Farbtiefe an, z. B. Farbe oder Schwarz‑und‑Weiß.  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Schritt 1: Mit TIFF JPEG‑Kompression speichern

### TIFF mit JPEG‑Kompression in Java speichern

Laden Sie die OneNote‑Datei, konfigurieren Sie `ImageSaveOptions` mit JPEG‑Kompression, setzen Sie optional den `quality`‑Wert und rufen Sie die Speicher‑Methode auf. Dieses Zwei‑Schritt‑Muster gibt Ihnen volle Kontrolle über Ausgabegröße und visuelle Treue.

1. Setzen Sie `dataDir` auf den Ordner, der Ihre `.one`‑Datei enthält.  
2. Rufen Sie `SaveToTiffUsingJpegCompression()` aus Ihrer Main‑Methode oder Ihrem Service auf.  
3. Die resultierende `.tiff`‑Datei erscheint im selben Verzeichnis.

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Erklärung**

- `ImageSaveOptions` weist Aspose.Note an, eine TIFF‑Datei auszugeben.  
- `setTiffCompression(TiffCompression.Jpeg)` wählt JPEG‑Kompression.  
- `setQuality(93)` (optional) justiert die Bildqualität; niedrigere Werte erzeugen kleinere Dateien.

## Überblick über TIFF PackBits‑Kompression

PackBits ist ein verlustfreier Kompressionsalgorithmus, der am besten für Bilder mit großen einfarbigen Bereichen funktioniert. In der Dokumentation wird er häufig als **tiff packbits compression** bezeichnet.

## TIFF mit PackBits‑Kompression in Java speichern

Wenn Sie eine verlustfreie Option benötigen, ist PackBits ein einfacher Run‑Length‑Algorithmus, der gut für Grafiken mit einheitlichen Farben geeignet ist. Konfigurieren Sie `ImageSaveOptions` mit `TiffCompression.PackBits` und speichern Sie das Dokument.

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Erklärung**

- `setTiffCompression(TiffCompression.PackBits)` wechselt die Kompressionsmethode.  
- Keine Qualitäts‑Einstellung nötig, da PackBits verlustfrei ist.

## TIFF mit CCITT Group 3‑Kompression in Java speichern

Für Fax‑artige Dokumente benötigen Sie häufig ein **schwarz‑weiß TIFF**. CCITT Group 3 liefert hohe Kompression für monochrome Bilder. Setzen Sie den Farbmodus auf Schwarz‑und‑Weiß und wählen Sie das CCITT 3‑Kompressions‑Enum.

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Erklärung**

- `setColorMode(ColorMode.BlackAndWhite)` erzwingt eine monochrome Ausgabe.  
- `setTiffCompression(TiffCompression.Ccitt3)` wendet die fax‑orientierte Kompression an.

## Häufige Probleme & Tipps

| Problem | Lösung |
|-------|----------|
| **Ausgabedatei ist größer als erwartet** | Reduzieren Sie den JPEG‑`quality`‑Wert oder wechseln Sie zu PackBits, wenn verlustfrei akzeptabel ist. |
| **Farben wirken ausgewaschen** | Stellen Sie sicher, dass Sie nicht versehentlich `ColorMode.BlackAndWhite` gesetzt haben, wenn Farbe nötig ist. |
| **Fehler: Nicht unterstütztes Bildformat** | Prüfen Sie, ob Sie eine aktuelle Version von Aspose.Note verwenden; ältere Builds können bestimmte Kompressions‑Enums fehlen. |
| **LicenseException zur Laufzeit** | Installieren Sie eine gültige Aspose.Note‑Lizenz (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Häufig gestellte Fragen

**F: Kann ich andere Dokumenttypen (z. B. PDF, DOCX) mit diesen Optionen in TIFF konvertieren?**  
A: Ja. Während sich Aspose.Note auf OneNote‑Dateien konzentriert, bieten Aspose.PDF, Aspose.Words und andere Bibliotheken ähnliche `ImageSaveOptions` für ihre Formate.

**F: Wie unterscheidet sich TIFF JPEG‑Kompression von einer normalen JPEG‑Datei?**  
A: Der JPEG‑Algorithmus ist derselbe, aber die Bilddaten befinden sich in einem TIFF‑Container, der mehrere Seiten und umfangreichere Metadaten enthalten kann.

**F: Ist es möglich, viele `.one`‑Dateien stapelweise zu verarbeiten?**  
A: Absolut. Durchlaufen Sie ein Verzeichnis, rufen Sie eine der drei Methoden für jede Datei auf und sammeln Sie die resultierenden TIFFs.

**F: Kann ich die DPI/Auflösung des ausgegebenen TIFFs steuern?**  
A: Ja. Verwenden Sie `options.setResolution(int dpi)` vor dem Speichern.

**F: Unterstützt Aspose.Note asynchrone Verarbeitung?**  
A: Die API selbst ist synchron, Sie können Aufrufe jedoch in Java‑`CompletableFuture` oder einem Thread‑Pool für parallele Ausführung einbinden.

## Fazit

Sie verfügen nun über ein vollständiges **Java‑TIFF‑Konvertierungs‑Toolkit**, mit dem Sie **die TIFF‑Dateigröße reduzieren** können, wenn Sie OneNote‑Dokumente als TIFF‑Dateien mit JPEG, PackBits oder CCITT Group 3 Fax‑Kompression speichern. Passen Sie Qualität, Farbmodus und Auflösung an Ihre spezifischen Anforderungen an und integrieren Sie diese Methoden in Batch‑Workflows für maximale Produktivität.

---

**Zuletzt aktualisiert:** 2026-11-05  
**Getestet mit:** Aspose.Note für Java 26.4 (zum Zeitpunkt der Erstellung)  
**Autor:** Aspose

## Verwandte Tutorials

- [Wie man OneNote‑Seitenbild (JPEG) mit Save‑Format unter Verwendung von Aspose.Note für Java rendert](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Aspose.Note für Java zum Speichern von OneNote als PNG mit Optionen verwenden – Notebook in Bild konvertieren](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [Wie man OneNote als Graustufen‑Bild exportiert – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}