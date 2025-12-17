---
date: 2025-12-17
description: Erfahren Sie, wie Sie OneNote exportieren, indem Sie ein Dokument als
  Graustufen‑PNG‑Bild mit Aspose.Note für Java speichern. Enthält Schritte zum Laden
  des OneNote‑Dokuments und zum Erstellen eines Graustufen‑Bildes.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: Wie man OneNote als Graustufenbild exportiert – Aspose.Note
url: /de/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Speichern als Graustufen‑Bild in OneNote – Aspose.Note

## Einleitung

In diesem Tutorial zeigen wir Ihnen **wie man OneNote exportiert**, indem ein Dokument als Graustufen‑Bild mit Aspose.Note für Java gespeichert wird. Graustufen‑Bilder sind monochrome Bilder, die nur Grautöne enthalten und sich für den Druck, die Archivierung oder die Reduzierung der Dateigröße eignen. Wir führen Sie durch das Laden eines OneNote‑Dokuments, die Konfiguration der Speicheroptionen zum **Erstellen eines Graustufen‑Bildes** und schließlich das **Speichern des Dokuments als PNG**.

## Schnelle Antworten
- **Was bedeutet „how to export onenote“?** Es bezieht sich darauf, eine OneNote‑Datei programmgesteuert in ein anderes Format, z. B. ein Bild, zu konvertieren.  
- **Welches Format ist am besten für Graustufenausgabe?** PNG eignet sich gut, weil es verlustfreie Qualität bewahrt und den Graustufen‑Farbmodus unterstützt.  
- **Benötige ich eine Lizenz?** Eine gültige Aspose.Note‑Lizenz ist für den Produktionseinsatz erforderlich; eine temporäre Testlizenz ist zum Ausprobieren verfügbar.  
- **Welche Java‑Version wird benötigt?** Java 8 oder höher wird empfohlen.  
- **Kann ich die Bildgröße ändern?** Ja, Sie können die Eigenschaften von `ImageSaveOptions` wie `Resolution` oder `PageSize` vor dem Speichern anpassen.

## Was bedeutet „how to export onenote“?
Das Exportieren von OneNote bedeutet, eine OneNote‑`.one`‑Datei programmgesteuert in eine andere Darstellung zu konvertieren – beispielsweise PDF, HTML oder ein Bild. In diesem Leitfaden konzentrieren wir uns auf den Export in ein **Graustufen‑PNG**‑Bild, was häufig für Dokumentations‑ oder Druck‑Workflows benötigt wird.

## Warum OneNote als Graustufen‑Bild exportieren?
- **Reduzierte Dateigröße** – Graustufen‑PNGs sind in der Regel kleiner als Vollfarbbilder.  
- **Bessere Lesbarkeit** – Für gedruckte Berichte bietet Graustufen oft einen klareren Kontrast.  
- **Kompatibilität** – PNG wird von den meisten Browsern, Editoren und mobilen Geräten breit unterstützt.  

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. Java Development Kit (JDK) auf Ihrem System installiert.  
2. Aspose.Note für Java‑Bibliothek. Sie können sie von [hier](https://releases.aspose.com/note/java/) herunterladen.  
3. Grundlegendes Verständnis der Java‑Programmierung.  

## Pakete importieren

Um loszulegen, importieren Sie die notwendigen Pakete:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Schritt 1: OneNote‑Dokument laden

Zuerst **laden Sie das OneNote‑Dokument** in Aspose.Note. Ersetzen Sie `"Your Document Directory"` durch den Pfad zu Ihrem lokalen Ordner und `"Aspose.one"` durch den Namen Ihrer OneNote‑Datei.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Schritt 2: Ausgabepfad und Optionen festlegen

Definieren Sie den Ausgabepfad für das Graustufen‑Bild und geben Sie die Speicheroptionen an. Wir setzen `ColorMode` auf `GrayScale` und verwenden das **save document as png**‑Format.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Schritt 3: Dokument speichern

Speichern Sie schließlich das Dokument als Graustufen‑PNG‑Bild mit den konfigurierten Optionen.

```java
oneFile.save(dataDir, options);
```

## Häufige Probleme und Lösungen
- **FileNotFoundException** – Stellen Sie sicher, dass `dataDir` auf den richtigen Ordner verweist und die `.one`‑Datei existiert.  
- **LicenseException** – Stellen Sie sicher, dass Sie vor dem Aufruf von `save` eine gültige Aspose.Note‑Lizenz angewendet haben.  
- **Niedrige Auflösung** – Passen Sie `options.setResolution(300)` an, um bei Bedarf die DPI zu erhöhen.

## Häufig gestellte Fragen

**Q1: Kann ich das Graustufen‑Bild in einem anderen Format speichern?**  
A1: Ja, ändern Sie einfach den `SaveFormat`‑Parameter im `ImageSaveOptions`‑Konstruktor zu `Jpeg`, `Bmp` usw.

**Q2: Ist Aspose.Note mit allen Versionen von OneNote‑Dokumenten kompatibel?**  
A2: Aspose.Note unterstützt Microsoft OneNote 2010 und spätere Versionen.

**Q3: Benötigt Aspose.Note eine Lizenz zur Nutzung?**  
A3: Eine gültige Lizenz ist für den Produktionseinsatz erforderlich, aber eine temporäre Testlizenz kann für Evaluierungszwecke erhalten werden.

**Q4: Kann ich andere Aspekte des Dokuments vor dem Speichern als Bild manipulieren?**  
A4: Absolut! Aspose.Note bietet eine umfassende API zum Bearbeiten von Abschnitten, Seiten und Inhalten vor dem Export.

**Q5: Wo finde ich Unterstützung, wenn ich auf Probleme stoße?**  
A5: Sie finden Unterstützung im Aspose.Note‑Forum [hier](https://forum.aspose.com/c/note/28).

## Fazit

Sie haben nun gelernt **wie man OneNote exportiert**, indem Sie eine OneNote‑Datei laden, die Speicheroptionen zum **Erstellen eines Graustufen‑Bildes** konfigurieren und **das Dokument als PNG speichern**. Diese Technik ist praktisch, um leichte, druckfertige Visualisierungen aus OneNote‑Notizbüchern zu erzeugen. Experimentieren Sie gern mit anderen `ColorMode`‑Einstellungen oder Bildformaten, um den Anforderungen Ihres Projekts gerecht zu werden.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose