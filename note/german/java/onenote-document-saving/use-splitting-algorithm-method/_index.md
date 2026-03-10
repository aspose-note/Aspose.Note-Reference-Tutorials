---
date: 2025-12-18
description: Erfahren Sie, wie Sie OneNote‑Seiten mit Aspose.Note für Java in PDF
  exportieren. Wählen Sie Aufteilungsalgorithmen, legen Sie die Seitenteilung fest
  und erstellen Sie PDF‑Dateien ganz einfach.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: OneNote‑Seiten mit Splitting‑Algorithmus‑Methode exportieren – Aspose.Note
url: /de/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren von OneNote‑Seiten mit der Splitting‑Algorithmus‑Methode – Aspose.Note

## Einleitung

Wenn Sie **OneNote‑Seiten** programmgesteuert in ein PDF‑Dokument exportieren müssen, macht Aspose.Note für Java das ganz einfach. In diesem Tutorial führen wir Sie durch die Splitting‑Algorithmus‑Methode, mit der Sie steuern können, wie Inhalte über Seiten hinweg aufgeteilt werden, um ein sauberes und gut lesbares PDF‑Ergebnis zu erzielen. Sie sehen, wie Sie die PDF‑Speicheroptionen festlegen, den passenden Seiten‑Splitting‑Algorithmus wählen und schließlich die PDF‑Datei erzeugen – alles mit nur wenigen Zeilen Java‑Code.

## Schnelle Antworten
- **Was macht der Splitting‑Algorithmus?** Er bestimmt, wie Objekte, die Seiten­grenzen überschreiten, beim Export von OneNote‑Seiten nach PDF behandelt werden.  
- **Welche Bibliothek wird benötigt?** Aspose.Note für Java (Download von der offiziellen Aspose‑Website).  
- **Benötige ich eine Lizenz?** Für den Produktionseinsatz ist eine temporäre oder vollständige Lizenz erforderlich; ein kostenloser Testzeitraum ist verfügbar.  
- **Kann ich große OneNote‑Notizbücher exportieren?** Ja – die Bibliothek verarbeitet große Dateien effizient und ermöglicht das Festlegen von Seiten‑Splitting‑Regeln.  
- **Welche Ausgabeformate werden unterstützt?** PDF, JPEG, PNG, XPS und mehr; dieser Leitfaden konzentriert sich auf den PDF‑Export.

## Was ist **Exportieren von OneNote‑Seiten**?
Das Exportieren von OneNote‑Seiten bedeutet, das native `.one`‑Dateiformat in ein portableres Format wie PDF zu konvertieren. Das ist nützlich zum Teilen, Archivieren oder Drucken von Inhalten, ohne die OneNote‑Anwendung zu benötigen.

## Warum den Splitting‑Algorithmus für **Exportieren von OneNote‑Seiten** verwenden?
Der Algorithmus gibt Ihnen eine feinkörnige Kontrolle darüber, wie komplexe Objekte (Tabellen, Bilder, Zeichnungen) an Seitenumbrüchen behandelt werden. Durch die Auswahl des passenden Algorithmus können Sie:

* Das visuelle Layout jeder Seite erhalten.  
* Abgeschnittene Inhalte vermeiden, die sonst abgeschnitten würden.  
* Die Anzahl der erzeugten Seiten reduzieren, wenn Objekte sauber auf die nächste Seite verschoben werden können.  

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Java Development Kit (JDK): Stellen Sie sicher, dass das JDK auf Ihrem System installiert ist. Sie können es von der [Website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) herunterladen.  
2. Aspose.Note für Java‑Bibliothek: Laden Sie die Aspose.Note für Java‑Bibliothek herunter und installieren Sie sie über den [Download‑Link](https://releases.aspose.com/note/java/).

## Pakete importieren

In Ihrem Java‑Projekt importieren Sie die notwendigen Pakete, um die Funktionalitäten von Aspose.Note zu nutzen.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Schritt 1: Dokumentverzeichnis festlegen

Richten Sie das Verzeichnis ein, in dem sich Ihr OneNote‑Dokument befindet.

```java
String dataDir = "Your Document Directory";
```

## Schritt 2: OneNote‑Dokument laden

Laden Sie das OneNote‑Dokument mit der `Document`‑Klasse von Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Schritt 3: PDF‑Speicheroptionen festlegen

Erzeugen Sie eine Instanz von `PdfSaveOptions`, um Optionen für das Speichern des Dokuments als PDF festzulegen. Hier bestimmen Sie das **Seiten‑Splitting**‑Verhalten und weitere PDF‑bezogene Einstellungen.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Schritt 4: Seiten‑Splitting‑Algorithmus festlegen

Wählen Sie den geeigneten Splitting‑Algorithmus nach Ihren Anforderungen aus. Hier verwenden wir `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, das einen Teil eines Objekts auf der aktuellen Seite belässt und den Rest auf die nächste Seite klont.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Schritt 5: Dokument speichern

Speichern Sie das Dokument mit den angegebenen PDF‑Speicheroptionen. Dieser Schritt **generiert PDF‑OneNote**‑Ausgabe, die Sie öffnen, teilen oder drucken können.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Häufige Probleme und Lösungen

| Problem | Lösung |
|-------|----------|
| **Objekte werden an Seiten­grenzen abgeschnitten** | Probieren Sie einen anderen Algorithmus wie `AlwaysSplitObjectsAlgorithm` oder erhöhen Sie den Schwellenwert in `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **Ausgabe‑PDF ist leer** | Stellen Sie sicher, dass die Quell‑`.one`‑Datei nicht beschädigt ist und der Pfad `dataDir` korrekt ist. |
| **Leistung ist bei großen Notizbüchern langsam** | Verwenden Sie `pdfSaveOptions.setCompressImages(true)`, um den Speicherverbrauch zu reduzieren, und erwägen Sie, das Notizbuch in kleineren Abschnitten zu verarbeiten. |

## Häufig gestellte Fragen

**F: Kann ich Aspose.Note für Java mit anderen Programmiersprachen verwenden?**  
A: Ja, Aspose.Note ist ebenfalls für .NET, C++ und Python verfügbar.

**F: Ist Aspose.Note für die Verarbeitung großer OneNote‑Dateien geeignet?**  
A: Absolut. Die Bibliothek ist darauf optimiert, große Notizbücher effizient zu handhaben.

**F: Wo finde ich zusätzliche Ressourcen und Support für Aspose.Note?**  
A: Sie können die [Dokumentation](https://reference.aspose.com/note/java/) und das [Forum](https://forum.aspose.com/c/note/28) für Unterstützung und Anleitungen konsultieren.

**F: Kann ich Aspose.Note vor dem Kauf testen?**  
A: Ja, Sie können einen [kostenlosen Test](https://releases.aspose.com/) nutzen, um die Funktionen vor dem Kauf zu erkunden.

**F: Wie kann ich eine temporäre Lizenz für Aspose.Note erhalten?**  
A: Sie können eine [temporäre Lizenz](https://purchase.aspose.com/temporary-license/) anfordern, um das Produkt im Testzeitraum zu evaluieren.

---

**Zuletzt aktualisiert:** 2025-12-18  
**Getestet mit:** Aspose.Note 24.12 für Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}