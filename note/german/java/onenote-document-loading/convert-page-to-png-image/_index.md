---
date: 2025-11-29
description: Erfahren Sie, wie Sie eine OneNote‑Seite mit Aspose.Note für Java in
  PNG exportieren. Befolgen Sie die Schritt‑für‑Schritt‑Anleitung, um den Seitenindex
  festzulegen, die Seite zu konvertieren und das Bild zu speichern.
language: de
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: OneNote‑Seite nach PNG‑Bild in Java mit Aspose.Note exportieren
url: /java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren einer OneNote‑Seite als PNG‑Bild in Java mit Aspose.Note

## Introduction

In diesem Tutorial erfahren Sie **wie man eine OneNote‑Seite** in ein PNG‑Bild exportiert, indem Sie die Aspose.Note‑Bibliothek für Java verwenden. Wir führen Sie durch alles, was Sie benötigen – von der Vorbereitung Ihrer Umgebung über das Festlegen des Seitenindex bis hin zum Speichern der Seite als hochqualitatives PNG‑Datei. Am Ende können Sie diese Funktion in jede Java‑Anwendung integrieren, die mit OneNote‑Dokumenten arbeitet.

## Quick Answers
- **Welche Bibliothek wird benötigt?** Aspose.Note für Java.  
- **Kann ich eine einzelne Seite exportieren?** Ja – verwenden Sie `setPageIndex`, um die gewünschte Seite zu adressieren.  
- **Unterstützte Bildformate?** PNG, JPEG, GIF, BMP, TIFF (hier wird PNG gezeigt).  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion ist verfügbar; für den Produktionseinsatz ist eine Lizenz erforderlich.  
- **Wie lange dauert die Implementierung?** In der Regel unter 10 Minuten für eine grundlegende Konvertierung.

## Was bedeutet „export OneNote page“?
Das Exportieren einer OneNote‑Seite bedeutet, eine bestimmte Seite innerhalb eines `.one`‑Dokuments in eine eigenständige Bilddatei (hier PNG) zu konvertieren. Das ist nützlich, wenn Sie OneNote‑Inhalte außerhalb der OneNote‑Umgebung teilen, einbetten oder weiterverarbeiten möchten.

## Warum Aspose.Note für Java verwenden, um OneNote nach PNG zu konvertieren?
- **Keine Abhängigkeit von Microsoft Office** – funktioniert auf jeder Plattform, die Java ausführt.  
- **Fein abgestimmte Kontrolle** – Sie können jede Seite über `setPageIndex` auswählen.  
- **Hochwertige Ausgabe** – PNG bewahrt Vektorgrafiken und Textschärfe.  
- **Batch‑fähig** – einfache Schleifen über Seiten für Massenkonvertierungen.

## Prerequisites

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Java Development Kit (JDK)** – Version 8 oder höher.  
2. **Aspose.Note für Java** – laden Sie das aktuelle JAR von der [Aspose‑Website](https://releases.aspose.com/note/java/) herunter.  
3. **Ein OneNote‑Dokument** (`.one`), das die Seite enthält, die Sie exportieren möchten.

## Import Packages

Zuerst importieren Sie die notwendigen Java‑Klassen:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

### Step 1: Load the OneNote Document

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Wir verwenden die Klasse `Document`, um die OneNote‑Datei von der Festplatte zu lesen. Das Objekt `LoadOptions` ermöglicht es Ihnen, das Ladeverhalten bei Bedarf anzupassen.

### Step 2: Initialize ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` teilt Aspose.Note mit, dass wir die Ausgabe im **PNG**‑Format wünschen. Durch Ändern von `SaveFormat` können Sie zu JPEG, BMP usw. wechseln.

### Step 3: Set the Page Index (How to convert OneNote page)

```java
// set page index
opts.setPageIndex(0);
```

Die Methode `setPageIndex` wählt aus, welche Seite exportiert werden soll. Die Seitennummerierung beginnt bei **0**, sodass `0` die erste Seite bezeichnet. Passen Sie diesen Wert an, um eine andere Seite zu exportieren.

### Step 4: Save the Document as PNG (Save OneNote as PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Durch Aufrufen von `save` wird die ausgewählte Seite als PNG‑Datei auf die Festplatte geschrieben. Der Dateiname `ConvertSpecificPageToPngImage_out.png` ist nur ein Beispiel – Sie können ihn beliebig benennen.

## Common Issues & Tips

- **Falscher Seitenindex** – Denken Sie daran, dass die Indizierung bei 0 beginnt. Wenn Sie ein leeres Bild erhalten, prüfen Sie den Indexwert.  
- **Fehlendes Aspose.Note‑JAR** – Stellen Sie sicher, dass das JAR im Klassenpfad liegt; sonst erhalten Sie `ClassNotFoundException`.  
- **Große Seiten** – Bei sehr großen Seiten sollten Sie die JVM‑Heap‑Größe (`-Xmx`) erhöhen, um `OutOfMemoryError` zu vermeiden.

## Frequently Asked Questions

### Q1: Kann ich mehrere Seiten in einem Durchgang mit Aspose.Note für Java in PNG‑Bilder konvertieren?
A1: Ja, Sie können über die Seiten des Dokuments iterieren, `opts.setPageIndex(i)` aktualisieren und für jede Iteration `save` aufrufen.

### Q2: Unterstützt Aspose.Note für Java andere Bildformate neben PNG?
A2: Absolut. Sie können in `ImageSaveOptions` `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` oder `SaveFormat.Tiff` festlegen.

### Q3: Gibt es eine kostenlose Testversion für Aspose.Note für Java?
A3: Ja, Sie können eine kostenlose Testversion von der [Website](https://releases.aspose.com/) herunterladen.

### Q4: Kann ich technische Unterstützung erhalten, wenn ich Probleme mit Aspose.Note für Java habe?
A4: Absolut, Sie können im Aspose‑Community‑Forum [hier](https://forum.aspose.com/c/note/28) Unterstützung finden.

### Q5: Wo kann ich eine Lizenz für Aspose.Note für Java erwerben?
A5: Sie können eine Lizenz über die [Kaufseite](https://purchase.aspose.com/buy) erwerben.

### Q6: Wie exportiere ich eine Seite, die eingebettete Bilder enthält?
A6: Eingebettete Bilder werden automatisch im PNG‑Ausgabeformat gerendert; zusätzlicher Code ist nicht erforderlich.

### Q7: Kann ich DPI oder Bildauflösung festlegen?
A7: Ja, verwenden Sie `opts.setResolution(int dpi)` vor dem Aufruf von `save`, um die Ausgabequalität zu steuern.

---

**Zuletzt aktualisiert:** 2025-11-29  
**Getestet mit:** Aspose.Note für Java 24.11 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
