---
date: 2026-03-14
description: Erfahren Sie, wie Sie OneNote‑Dokumente in Java als TIFF‑Dateien mit
  TIFF‑JPEG‑Kompression, TIFF‑PackBits‑Kompression oder CCITT Group 3 Fax speichern.
  Steuern Sie Bildqualität, Dateigröße und Farbraum mit Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Speichern als TIFF‑Bild mit TIFF‑JPEG‑Kompression in OneNote
url: /de/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save to TIFF Image Using TIFF JPEG Compression in OneNote

## Introduction

In diesem Tutorial erfahren Sie **wie Sie ein OneNote-Dokument mit TIFF JPEG-Kompression in eine TIFF-Datei speichern** und zwei weitere beliebte Kompressionsmethoden. Wir gehen die erforderliche Einrichtung durch, importieren die notwendigen Java-Pakete und liefern klaren Schritt‑für‑Schritt‑Code für jede Kompressionsoption. Am Ende können Sie **die TIFF-Bildqualität** steuern, die Dateigröße reduzieren und sogar Schwarz‑weiß‑TIFFs für Fax‑Ausgaben erzeugen.

## Quick Answers
- **Was ist TIFF JPEG-Kompression?** Eine verlustbehaftete Kompressionsmethode, die die TIFF-Dateigröße reduziert und dabei die visuelle Qualität beibehält.  
- **Welche Bibliothek übernimmt die Konvertierung?** Aspose.Note for Java.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für Tests; für den Produktionseinsatz ist eine Lizenz erforderlich.  
- **Kann ich die Bildqualität ändern?** Ja, setzen Sie die `quality`‑Eigenschaft von `ImageSaveOptions`.  
- **Ist eine Batch‑Konvertierung möglich?** Absolut – durchlaufen Sie die Dokumente und wenden Sie dieselben Optionen an.

## Was ist TIFF JPEG Compression?
TIFF JPEG-Kompression speichert Bilddaten in einem TIFF‑Container, wendet jedoch den verlustbehafteten JPEG‑Algorithmus an, um die Datei zu verkleinern. Sie ist ideal, wenn Sie ein Gleichgewicht zwischen **tiff image quality** und kleinerer Dateigröße benötigen, insbesondere für Web‑ oder Archivierungs‑Szenarien.

## Warum verschiedene TIFF Compression Types?
- **JPEG** – Gut für Fotos; bietet einstellbare Qualität.  
- **PackBits** – Einfache, verlustfreie Run‑Length‑Kodierung; nützlich für Grafiken mit großen einheitlichen Bereichen.  
- **CCITT Group 3 Fax** – Nur Schwarz‑weiß; perfekt für gescannte Dokumente und Fax‑Übertragung.  

Die richtige Kompression zu wählen, ermöglicht es Ihnen, Speicherbeschränkungen einzuhalten, ohne die für Ihre Anwendung erforderliche visuelle Treue zu opfern.

## OneNote in TIFF konvertieren mit Aspose.Note
Wenn Ihr Ziel ist, **OneNote in TIFF zu konvertieren**, decken die drei untenstehenden Methoden die gängigsten Szenarien ab. Jede Methode lädt eine `.one`‑Datei, konfiguriert `ImageSaveOptions` und speichert das Ergebnis als `.tiff`‑Datei.

## Prerequisites

- Java Development Kit (JDK) installiert.  
- Aspose.Note for Java‑Bibliothek zu Ihrem Projekt hinzugefügt (Maven/Gradle oder manuelles JAR).  
- Grundlegende Kenntnisse der Java‑Syntax.

## Pakete importieren

First, bring the necessary Aspose.Note classes into your Java file:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Schritt 1: TIFF mit TIFF JPEG Compression speichern

Unten finden Sie die vollständige Methode, die eine OneNote‑Datei lädt und sie als TIFF mit JPEG‑Kompression speichert. Passen Sie den `quality`‑Wert (0‑100) an, um die **tiff image quality** zu steuern.

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

**Explanation**

- `ImageSaveOptions` teilt Aspose.Note mit, eine TIFF‑Datei auszugeben.  
- `setTiffCompression(TiffCompression.Jpeg)` wählt JPEG‑Kompression.  
- `setQuality(93)` (optional) justiert die Bildqualität; niedrigere Werte erzeugen kleinere Dateien.

### So speichern Sie TIFF mit JPEG Compression in Java
1. Setzen Sie `dataDir` auf den Ordner, der Ihre `.one`‑Datei enthält.  
2. Rufen Sie `SaveToTiffUsingJpegCompression()` aus Ihrer `main`‑Methode oder Ihrem Service auf.  
3. Die resultierende `.tiff`‑Datei erscheint im selben Verzeichnis.

## Übersicht über TIFF PackBits Compression

PackBits ist ein verlustfreier Kompressionsalgorithmus, der am besten bei Bildern mit großen einfarbigen Bereichen funktioniert. In der Dokumentation wird er häufig als **tiff packbits compression** bezeichnet.

## Schritt 2: TIFF mit PackBits Compression speichern

Wenn Sie eine verlustfreie Option benötigen, ist PackBits ein einfacher Run‑Length‑Algorithmus, der gut für Grafiken mit einfarbigen Bereichen funktioniert.

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

**Explanation**

- `setTiffCompression(TiffCompression.PackBits)` wechselt die Kompressionsmethode.  
- Keine Qualitäts‑Einstellung ist nötig, da PackBits verlustfrei ist.

## Schritt 3: TIFF mit CCITT Group 3 Fax Compression speichern (Schwarz‑weiß‑TIFF)

Für Fax‑artige Dokumente benötigen Sie häufig ein **schwarz‑weiß‑TIFF**. CCITT Group 3 bietet hohe Kompression für monochrome Bilder.

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

**Explanation**

- `setColorMode(ColorMode.BlackAndWhite)` erzwingt eine monochrome Ausgabe.  
- `setTiffCompression(TiffCompression.Ccitt3)` wendet die fax‑orientierte Kompression an.

## Häufige Probleme & Tipps

| Problem | Lösung |
|-------|----------|
| **Ausgabedatei ist größer als erwartet** | Versuchen Sie, den JPEG `quality`‑Wert zu reduzieren oder wechseln Sie zu PackBits, wenn verlustfrei akzeptabel ist. |
| **Farben wirken ausgewaschen** | Stellen Sie sicher, dass Sie nicht versehentlich `ColorMode.BlackAndWhite` gesetzt haben, wenn Sie Vollfarbe benötigen. |
| **Fehler: Nicht unterstütztes Bildformat** | Vergewissern Sie sich, dass Sie eine aktuelle Version von Aspose.Note verwenden; ältere Builds können bestimmte Kompressions‑Enums fehlen. |
| **LicenseException zur Laufzeit** | Installieren Sie eine gültige Aspose.Note‑Lizenz (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Häufig gestellte Fragen

**Q: Kann ich andere Dokumenttypen (z. B. PDF, DOCX) mit diesen Optionen in TIFF konvertieren?**  
A: Ja. Während sich Aspose.Note auf OneNote‑Dateien konzentriert, bieten Aspose.PDF, Aspose.Words und andere Bibliotheken ähnliche `ImageSaveOptions` für ihre Formate.

**Q: Wie unterscheidet sich TIFF JPEG‑Kompression von einer normalen JPEG‑Datei?**  
A: Der JPEG‑Algorithmus ist derselbe, aber die Bilddaten befinden sich in einem TIFF‑Container, der mehrere Seiten und umfangreichere Metadaten enthalten kann.

**Q: Ist es möglich, viele `.one`‑Dateien stapelweise zu verarbeiten?**  
A: Absolut. Durchlaufen Sie ein Verzeichnis, rufen Sie eine der drei Methoden für jede Datei auf und sammeln Sie die resultierenden TIFFs.

**Q: Kann ich die DPI/Auflösung des AusgabetiFFs steuern?**  
A: Ja. Verwenden Sie `options.setResolution(int dpi)` vor dem Speichern.

**Q: Unterstützt Aspose.Note asynchrone Verarbeitung?**  
A: Die API selbst ist synchron, aber Sie können Aufrufe in Java‑`CompletableFuture` oder einen Thread‑Pool einbetten, um parallele Ausführung zu ermöglichen.

## Fazit

Sie haben jetzt ein vollständiges **java tiff conversion**‑Toolkit, mit dem Sie OneNote‑Dokumente als TIFF‑Dateien mit JPEG-, PackBits- oder CCITT Group 3 Fax‑Kompression speichern können. Passen Sie Qualität, Farbmodus und Auflösung an, um Ihre spezifischen **tiff image quality**‑Anforderungen zu erfüllen, und integrieren Sie diese Methoden in Batch‑Workflows für maximale Produktivität.

---

**Zuletzt aktualisiert:** 2026-03-14  
**Getestet mit:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}