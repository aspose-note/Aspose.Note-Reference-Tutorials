---
date: 2025-11-29
description: Erfahren Sie, wie Sie OneNote‑Seiten mit Java in Bilder exportieren und
  entdecken Sie, wie Sie OneNote‑Seitenbilder mit Aspose.Note konvertieren. Folgen
  Sie unserer Schritt‑für‑Schritt‑Anleitung für eine schnelle Integration.
linktitle: How to Export OneNote Page to Image Using Java
second_title: Aspose.Note Java API
title: Wie man eine OneNote‑Seite mit Java in ein Bild exportiert
url: /de/java/onenote-document-loading/convert-page-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man OneNote-Seite mit Java in ein Bild exportiert

## Einführung

In diesem Tutorial lernen Sie **wie man OneNote**‑Seiten in Bilddateien exportiert, und zwar mit Java und Aspose.Note. Das Konvertieren einer OneNote‑Seite in ein Bild ist praktisch, wenn Sie Notebook‑Inhalte in Berichte einbetten, Schnappschüsse mit Nicht‑OneNote‑Benutzern teilen oder Thumbnails für Dokumenten‑Management‑Systeme erzeugen müssen. Wir gehen Schritt für Schritt durch, erklären, warum jede Zeile wichtig ist, und zeigen Ihnen, wie Sie die Ausgabe anpassen können.

## Kurzantworten
- **Welche Bibliothek wird benötigt?** Aspose.Note für Java  
- **Kann ich das Bildformat wählen?** Ja – JPEG, PNG, BMP usw. über `ImageSaveOptions`  
- **Benötige ich eine Lizenz für die Produktion?** Eine gültige Aspose.Note‑Lizenz ist für die kommerzielle Nutzung erforderlich.  
- **Welche Seite kann ich exportieren?** Jede Seite, indem Sie den `PageIndex` (nullbasiert) setzen.  
- **Wie lange dauert die Konvertierung?** In der Regel unter einer Sekunde für eine Standardseite.

## Was bedeutet das Exportieren von OneNote‑Seiten in Bilder?
Das Exportieren von OneNote‑Seiten bedeutet, den reichen Inhalt der Seite – Text, Zeichnungen, Tabellen – in eine statische Bilddatei (z. B. JPEG) zu rendern. Dieser Vorgang erzeugt eine portable visuelle Darstellung, die überall angezeigt werden kann, selbst dort, wo der OneNote‑Client nicht installiert ist.

## Warum Aspose.Note für die Konvertierung von OneNote‑Seiten verwenden?
- **Vollständige Treue** – bewahrt Layout, Schriftarten und Tintenstriche.  
- **Keine Abhängigkeit von Microsoft Office** – funktioniert auf jeder Plattform, die Java unterstützt.  
- **Fein abgestimmte Kontrolle** – wählen Sie Bildformat, Qualität und spezifischen Seitenindex.  
- **Skalierbar** – geeignet für die Stapelverarbeitung vieler Seiten.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllt haben:

1. **Java Development Kit (JDK)** – Installieren Sie JDK 11 oder höher. Sie können es von [Oracle's official site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) herunterladen, falls Sie es noch nicht getan haben.  
2. **Aspose.Note für Java** – Laden Sie die neueste Bibliothek von der [Aspose.Note download page](https://releases.aspose.com/note/java/) herunter. Fügen Sie die JAR-Datei Ihrem Projekt‑Classpath hinzu.

## Pakete importieren

Zuerst importieren wir die notwendigen Pakete, die uns Zugriff auf die Dokumentenverarbeitung und Bild‑Speicheroptionen geben.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Schritt 1: OneNote‑Dokument laden

Wir beginnen damit, die `.one`‑Datei in ein `Aspose.Note` `Document`‑Objekt zu laden.

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Pro‑Tipp:** Verwenden Sie einen absoluten Pfad oder einen Ressourcen‑Stream, wenn sich Ihre Datei innerhalb eines JAR befindet.

## Schritt 2: Bildspeicheroptionen initialisieren

Erstellen Sie eine `ImageSaveOptions`‑Instanz, um das Ausgabeformat festzulegen (JPEG in diesem Beispiel). Sie können zu PNG, BMP oder GIF wechseln, indem Sie `SaveFormat` ändern.

```java
// Initialize ImageSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
```

## Schritt 3: Seitenindex festlegen

Seiten sind nullbasiert, daher wählt `1` die **zweite** Seite aus. Passen Sie diesen Wert an, um jede gewünschte Seite zu exportieren.

```java
// Specify second page for conversion
options.setPageIndex(1);
```

## Schritt 4: Dokument als Bild speichern

Jetzt rufen wir `save` auf dem `Document`‑Objekt auf und übergeben den Ziel-Dateinamen sowie die konfigurierten Optionen.

```java
// Save the document
oneFile.save(dataDir + "ConvertSpecificPageToImage_out.jpg", options);
```

## Schritt 5: Bestätigung ausgeben

Eine einfache Konsolennachricht bestätigt, dass das Bild erfolgreich erzeugt wurde.

```java
// Print confirmation message
System.out.println("File saved: " + dataDir + "ConvertSpecificPageToImage_out.jpg");
```

## Wie man OneNote‑Seiten in Bilder konvertiert (alternative Szenarien)

Wenn Sie **OneNote‑Seitenbilder** stapelweise konvertieren müssen, platzieren Sie den obigen Code einfach in einer Schleife, die über `Document.getPages()` iteriert. Ändern Sie `options.setPageIndex(i)` für jede Iteration und passen Sie optional `options.setQuality(90)` an, um die JPEG‑Kompression zu steuern.

## Häufige Probleme und Lösungen

| Problem | Grund | Lösung |
|---------|-------|--------|
| **Bild ist leer** | Seitenindex außerhalb des Bereichs oder Dokument nicht korrekt geladen. | Stellen Sie sicher, dass `options.setPageIndex` im Bereich `0 .. document.getPages().size() - 1` liegt. |
| **Nicht unterstütztes Format** | Verwendung einer älteren Aspose.Note‑Version, die bestimmte Formate nicht enthält. | Aktualisieren Sie auf die neueste Aspose.Note‑Version für Java. |
| **OutOfMemoryError** | Konvertierung sehr großer Seiten bei wenig verfügbarem JVM‑Speicher. | Erhöhen Sie die Heap‑Größe (`-Xmx2g`) oder verarbeiten Sie Seiten einzeln. |

## Häufig gestellte Fragen

**F1: Kann ich mehrere Seiten mit dieser Methode in Bilder konvertieren?**  
A: Ja. Packen Sie die Speicherlogik in eine Schleife und ändern Sie `options.setPageIndex(i)` für jede zu exportierende Seite.

**F2: Ist Aspose.Note mit verschiedenen Versionen von OneNote‑Dateien kompatibel?**  
A: Absolut. Aspose.Note unterstützt .one‑Dateien von OneNote 2007, 2010, 2013 und neueren Versionen.

**F3: Kann ich das Bildformat und die Qualität während der Konvertierung anpassen?**  
A: Ja. Wählen Sie `SaveFormat.Png`, `SaveFormat.Bmp` usw. und setzen Sie `options.setQuality(int)` für die JPEG‑Qualität (0‑100).

**F4: Bietet Aspose.Note Unterstützung für andere Programmiersprachen?**  
A: Ja. Bibliotheken sind für .NET, Python, C++ und weitere verfügbar.

**F5: Wo finde ich zusätzlichen Support oder Hilfe?**  
A: Besuchen Sie das [Aspose.Note forum](https://forum.aspose.com/c/note/28) oder lesen Sie die offizielle Dokumentation [hier](https://reference.aspose.com/note/java/).

---

**Zuletzt aktualisiert:** 2025-11-29  
**Getestet mit:** Aspose.Note für Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}