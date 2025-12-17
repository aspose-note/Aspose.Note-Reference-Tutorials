---
date: 2025-12-17
description: Learn how to save OneNote documents as TIFF files using TIFF JPEG compression,
  PackBits, or CCITT Group 3 Fax in Java. Control image quality, file size, and color
  mode with Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Speichern als TIFF‑Bild mit TIFF‑JPEG‑Kompression in OneNote
url: /de/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Speichern eines TIFF-Bildes mit TIFF JPEG-Kompression in OneNote

## Einleitung

In diesem Tutorial entdecken Sie **wie Sie ein OneNote‑Dokument mit TIFF JPEG‑Kompression in eine TIFF‑Datei speichern** und zwei weitere beliebte Kompressionsmethoden verwenden. Wir führen Sie durch die erforderliche Einrichtung, importieren die notwendigen Java‑Pakete und bieten klaren Schritt‑für‑Schritt‑Code für jede Kompressionsoption. Am Ende können Sie **die TIFF‑Bildqualität** steuern, die Dateigröße reduzieren und sogar Schwarz‑weiß‑TIFFs für Fax‑ähnliche Ausgaben erzeugen.

## Schnelle Antworten
- **Was ist TIFF JPEG‑Kompression?** Eine verlustbehaftete Kompressionsmethode, die die TIFF‑Dateigröße reduziert und gleichzeitig die visuelle Qualität bewahrt.  
- **Welche Bibliothek führt die Konvertierung durch?** Aspose.Note für Java.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für Tests; für den Produktionseinsatz ist eine Lizenz erforderlich.  
- **Kann ich die Bildqualität ändern?** Ja, setzen Sie die Eigenschaft `quality` bei `ImageSaveOptions`.  
- **Ist eine Batch‑Konvertierung möglich?** Absolut – iterieren Sie über Dokumente und wenden Sie dieselben Optionen an.

## Was ist TIFF JPEG‑Kompression?
TIFF JPEG‑Kompression speichert Bilddaten im TIFF‑Container, wendet jedoch den verlustbehafteten JPEG‑Algorithmus an, um die Datei zu verkleinern. Sie ist ideal, wenn Sie ein Gleichgewicht zwischen **TIFF‑Bildqualität** und kleinerer Dateigröße benötigen, insbesondere für Web‑ oder Archivierungs‑Szenarien.

## Warum verschiedene TIFF‑Kompressionstypen verwenden?
- **JPEG** – Gut für Fotos; bietet einstellbare Qualität.  
- **PackBits** – Einfaches, verlustfreies Run‑Length‑Encoding; nützlich für Grafiken mit großen einheitlichen Bereichen.  
- **CCITT Group 3 Fax** – Nur Schwarz‑weiß; perfekt für gescannte Dokumente und Faxübertragung.  

Die Wahl der richtigen Kompression ermöglicht es Ihnen, Speicherbeschränkungen zu erfüllen, ohne die für Ihre Anwendung erforderliche visuelle Treue zu opfern.

## Voraussetzungen

- Java Development Kit (JDK) installiert.  
- Aspose.Note für Java‑Bibliothek zu Ihrem Projekt hinzugefügt (Maven/Gradle oder manuelles JAR).  
- Grundlegende Kenntnisse der Java‑Syntax.

## Pakete importieren

Zuerst bringen Sie die notwendigen Aspose.Note‑Klassen in Ihre Java‑Datei ein:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Schritt 1: Speichern als TIFF mit TIFF JPEG‑Kompression

Nachfolgend die vollständige Methode, die eine OneNote‑Datei lädt und sie als TIFF mit JPEG‑Kompression speichert. Passen Sie den `quality`‑Wert (0‑100) an, um **die TIFF‑Bildqualität** zu steuern.

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

### So speichern Sie TIFF mit JPEG‑Kompression in Java
1. Setzen Sie `dataDir` auf den Ordner, der Ihre `.one`‑Datei enthält.  
2. Rufen Sie `SaveToTiffUsingJpegCompression()` aus Ihrer Hauptmethode oder Ihrem Service auf.  
3. Die resultierende `.tiff`‑Datei erscheint im selben Verzeichnis.

## Schritt 2: Speichern als TIFF mit PackBits‑Kompression

Wenn Sie eine verlustfreie Option benötigen, ist PackBits ein einfaches Run‑Length‑Verfahren, das gut für Grafiken mit einheitlichen Farben funktioniert.

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

## Schritt 3: Speichern als TIFF mit CCITT Group 3 Fax‑Kompression (Schwarz‑weiß‑TIFF)

Für Fax‑artige Dokumente möchten Sie oft ein **Schwarz‑weiß‑TIFF**. CCITT Group 3 bietet hohe Kompression für monochrome Bilder.

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
- `setTiffCompression(TiffCompression.Ccitt3)` wendet die faxorientierte Kompression an.

## Häufige Probleme & Tipps

| Problem | Lösung |
|---------|--------|
| **Ausgabedatei ist größer als erwartet** | Versuchen Sie, den JPEG‑`quality`‑Wert zu reduzieren oder wechseln Sie zu PackBits, wenn verlustfrei akzeptabel ist. |
| **Farben wirken ausgewaschen** | Stellen Sie sicher, dass Sie nicht versehentlich `ColorMode.BlackAndWhite` setzen, wenn Sie Vollfarbe benötigen. |
| **Fehler: Nicht unterstütztes Bildformat** | Vergewissern Sie sich, dass Sie eine aktuelle Version von Aspose.Note verwenden; ältere Builds können bestimmte Kompressions‑Enums fehlen. |
| **LicenseException zur Laufzeit** | Installieren Sie eine gültige Aspose.Note‑Lizenz (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Häufig gestellte Fragen

**Q: Kann ich andere Dokumenttypen (z. B. PDF, DOCX) mit diesen Optionen in TIFF konvertieren?**  
A: Ja. Aspose.Note konzentriert sich auf OneNote‑Dateien, aber Asposes andere Bibliotheken (PDF, Words) bieten ähnliche `ImageSaveOptions` für ihre jeweiligen Formate.

**Q: Wie unterscheidet sich TIFF JPEG‑Kompression von normalen JPEG‑Dateien?**  
A: Die Bilddaten werden in einem TIFF‑Container gespeichert, wodurch Metadaten erhalten bleiben und mehrere Seiten möglich sind, während der Kompressionsalgorithmus weiterhin JPEG bleibt.

**Q: Ist es möglich, viele `.one`‑Dateien stapelweise zu verarbeiten?**  
A: Absolut. Durchlaufen Sie einen Ordner, rufen Sie eine der drei Methoden pro Datei auf und sammeln Sie die resultierenden TIFFs.

**Q: Kann ich die DPI/Auflösung des ausgegebenen TIFFs steuern?**  
A: Ja. Verwenden Sie `options.setResolution(int dpi)` vor dem Speichern.

**Q: Unterstützt Aspose.Note asynchrones Processing?**  
A: Die API selbst ist synchron, aber Sie können Aufrufe in Java‑`CompletableFuture` oder Thread‑Pools einbetten, um parallele Ausführungen zu ermöglichen.

## Fazit

Sie verfügen nun über ein vollständiges **Java‑TIFF‑Konvertierungs‑Toolkit**, mit dem Sie OneNote‑Dokumente als TIFF‑Dateien mit JPEG, PackBits oder CCITT Group 3 Fax‑Kompression speichern können. Passen Sie Qualität, Farbmodus und Auflösung an, um Ihre spezifischen **TIFF‑Bildqualitäts**‑Anforderungen zu erfüllen, und integrieren Sie diese Methoden in Batch‑Workflows für maximale Produktivität.

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note für Java 23.12 (aktuell zum Zeitpunkt der Erstellung)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}