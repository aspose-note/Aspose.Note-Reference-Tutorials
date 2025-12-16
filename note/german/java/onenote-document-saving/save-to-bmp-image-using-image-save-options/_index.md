---
date: 2025-12-16
description: Erfahren Sie, wie Sie OneNote‑Dokumente mithilfe der Bildspeicheroptionen
  von Aspose.Note für Java als BMP‑Bilder speichern. Sehen Sie sich auch an, wie Sie
  OneNote in PDF oder PNG speichern.
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: Wie man OneNote als BMP‑Bild speichert, mit Bildspeicheroptionen
url: /de/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# wie man onenote in BMP-Bild speichert mit Image Save Options

## Einleitung

Aspose.Note for Java ist eine leistungsstarke Bibliothek, die Java‑Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote‑Dateien zu arbeiten. **In diesem Tutorial lernen Sie, wie man OneNote‑Dokumente als BMP‑Bilder speichert** mithilfe der Image Save Options‑Funktion von Aspose.Note for Java. Wir gehen jeden Schritt durch, erklären, warum Sie BMP gegenüber anderen Formaten wählen könnten, und zeigen Ihnen, wie Sie diese Fähigkeit in Ihre eigenen Anwendungen integrieren.

## Schnelle Antworten
- **Was macht die Image Save Options‑Klasse?** Sie ermöglicht es Ihnen, das Ausgabe‑Bildformat (BMP, PNG, JPEG usw.) beim Konvertieren einer OneNote‑Seite festzulegen.  
- **Benötige ich eine Lizenz, um das Beispiel auszuführen?** Eine kostenlose Testversion funktioniert für die Evaluierung, aber für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich eine OneNote‑Seite in PDF oder PNG statt BMP konvertieren?** Ja – ändern Sie einfach das `SaveFormat`‑Enum (z. B. `SaveFormat.Pdf` oder `SaveFormat.Png`).  
- **Welche Java‑Version wird unterstützt?** Java 8 und spätere Versionen werden vollständig unterstützt.  
- **Gibt es besondere Handhabungen für große Dokumente?** Sie können die Ausgabe streamen, um einen hohen Speicherverbrauch zu vermeiden.

## Was ist „Image Save Options“ in Aspose.Note?

Die `ImageSaveOptions`‑Klasse bietet feinkörnige Kontrolle darüber, wie OneNote‑Seiten als Rasterbilder gerendert werden. Sie können das Bildformat, die Auflösung, die Farbtiefe und mehr festlegen. Diese Flexibilität erleichtert das Erzeugen von BMP‑Dateien für Altsysteme oder PNG/JPEG‑Dateien für die Web‑Nutzung.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. Grundkenntnisse der Programmiersprache Java.  
2. JDK (Java Development Kit) auf Ihrem Rechner installiert.  
3. Eine IDE wie Eclipse oder IntelliJ IDEA.  
4. Aspose.Note for Java‑Bibliothek – laden Sie sie von [here](https://releases.aspose.com/note/java/) herunter.

## Pakete importieren

Zuerst importieren Sie die notwendigen Aspose.Note‑Klassen und die Standard‑Java‑I/O‑Hilfsmittel:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Schritt 1: OneNote‑Dokument laden

Hier geben wir den Ordner an, der die Quell‑OneNote‑Datei (`Aspose.one`) enthält, und laden sie in ein `Document`‑Objekt. Dieses Objekt gibt Ihnen vollen Zugriff auf Seiten, Abschnitte und andere Elemente im Notizbuch.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Schritt 2: Dokument als BMP‑Bild speichern

Wir verketten den Ausgabedateinamen und rufen dann `save` mit einer `ImageSaveOptions`‑Instanz auf, die für **BMP** (`SaveFormat.Bmp`) konfiguriert ist.  
Wenn Sie die **OneNote‑Seite** als PNG speichern möchten, ersetzen Sie einfach `SaveFormat.Bmp` durch `SaveFormat.Png`. Ebenso ermöglicht `SaveFormat.Pdf` eine **OneNote‑zu‑PDF**‑Konvertierung.

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

## Warum BMP wählen?

- **Verlustfreie Qualität** – BMP speichert Rohpixel‑Daten und bewahrt das genaue Aussehen der Originalseite.  
- **Kompatibilität** – Ältere Windows‑Anwendungen benötigen häufig BMP‑Dateien.  
- **Einfachheit** – Keine Kompressionsartefakte, was es ideal für weitere Bildverarbeitung macht.

## Häufige Probleme & Tipps

- **Dateipfad‑Fehler** – Stellen Sie sicher, dass `dataDir` mit dem passenden Dateiseparator (`/` oder `\`) endet.  
- **Große Notizbücher** – Bei sehr großen OneNote‑Dateien sollten Sie jede Seite einzeln speichern, um den Speicherverbrauch gering zu halten.  
- **Lizenzausnahmen** – Das Ausführen des Codes ohne gültige Lizenz fügt dem erzeugten Bild ein Wasserzeichen hinzu.

## Fazit

In diesem Leitfaden haben wir **wie man OneNote**‑Dokumente als BMP‑Bilder mit `ImageSaveOptions` von Aspose.Note for Java speichert, demonstriert. Durch das Austauschen des `SaveFormat`‑Enums können Sie auch PNG, JPEG, PDF oder andere unterstützte Formate erzeugen, was Ihnen eine flexible Möglichkeit bietet, OneNote‑Inhalte für beliebige nachgelagerte Szenarien zu exportieren.

## Häufig gestellte Fragen

**F1: Kann ich OneNote‑Dokumente in andere Bildformate als BMP speichern?**  
A: Ja, Sie können `ImageSaveOptions` mit `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` oder `SaveFormat.Tiff` verwenden, um in diese Formate zu exportieren.

**F2: Unterstützt Aspose.Note for Java die Konvertierung zwischen verschiedenen Dokumentformaten?**  
A: Absolut. Neben Bildformaten können Sie OneNote‑Dateien mit dem entsprechenden `SaveFormat` in PDF, DOCX, HTML und mehr konvertieren.

**F3: Ist Aspose.Note for Java mit den neuesten Versionen von OneNote kompatibel?**  
A: Ja, die Bibliothek wird regelmäßig aktualisiert, um mit den neuesten OneNote‑Versionen synchron zu bleiben.

**F4: Kann ich den Inhalt von OneNote‑Dokumenten programmgesteuert manipulieren?**  
A: Ja, Sie können über die API Seiten, Abschnitte und Rich‑Content (Text, Bilder, Tabellen) hinzufügen, bearbeiten oder löschen.

**F5: Bietet Aspose.Note for Java technischen Support?**  
A: Ja, Aspose bietet technischen Support und ein dediziertes Forum. Besuchen Sie das [Aspose.Note forum](https://forum.aspose.com/c/note/28) für Unterstützung.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2025-12-16  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

---