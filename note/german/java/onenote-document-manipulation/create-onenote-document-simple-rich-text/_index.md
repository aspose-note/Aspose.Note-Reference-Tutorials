---
date: 2026-02-18
description: Erfahren Sie, wie Sie beim Erstellen von OneNote‑Dokumenten in Java mit
  Aspose.Note den Absatzstil festlegen und ein Gliederungselement hinzufügen. Exportieren
  Sie OneNote nach PDF, speichern Sie OneNote als PDF und erstellen Sie mühelos OneNote‑Dateien.
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: OneNote nach PDF exportieren – Absatzstil beim Erstellen eines OneNote‑Dokuments
  in Java festlegen
url: /de/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Absatzstil festlegen beim Erstellen eines OneNote‑Dokuments in Java

## Einführung

In der heutigen schnelllebigen Entwicklungslandschaft ist es unerlässlich, **OneNote programmgesteuert nach PDF zu exportieren**, um professionell aussehende, teilbare Dokumente zu erzeugen. Dieses Tutorial führt Sie durch das Erstellen einer OneNote‑Datei, das Anwenden eines benutzerdefinierten Absatzstils und schließlich das **Exportieren von OneNote nach PDF** mit Aspose.Note für Java. Egal, ob Sie eine Reporting‑Engine, eine automatisierte Notiz‑Lösung oder einen Dokument‑Konvertierungs‑Service bauen – die hier behandelten Techniken helfen Ihnen, **OneNote als PDF zu speichern** mit genauer Formatierungskontrolle.

## Schnelle Antworten
- **Was bedeutet „Absatzstil festlegen“?** Es wendet Schriftart, Größe, Farbe und weitere Formatierungen auf einen Textabsatz an.  
- **Kann ich das Ergebnis nach PDF exportieren?** Ja – das Tutorial endet mit dem Speichern der OneNote‑Datei als PDF.  
- **Benötige ich eine Lizenz für Aspose.Note?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine Lizenz erforderlich.  
- **Welche IDEs werden unterstützt?** Jede Java‑IDE – Eclipse, IntelliJ IDEA, NetBeans usw.  
- **Wie lange dauert die Implementierung?** Ungefähr 10‑15 Minuten für ein Basis‑Dokument.

## Was bedeutet „Absatzstil festlegen“ in Aspose.Note?
Das Festlegen des Absatzstils bezieht sich auf die Konfiguration eines `ParagraphStyle`‑Objekts (Schriftname, Größe, Farbe usw.) und dessen Anbindung an einen `RichText`‑Knoten. Damit haben Sie die volle Kontrolle darüber, wie Text innerhalb einer OneNote‑Seite erscheint.

## Wie legt man den Absatzstil in OneNote fest?
Das Anwenden eines Stils ist so einfach wie das Erstellen einer `ParagraphStyle`‑Instanz, das Anpassen ihrer Eigenschaften und das Zuweisen zu einem `RichText`‑Element. Die API macht dies zu einer einzeiligen Operation, sobald das Stil‑Objekt bereit ist.

## Warum OneNote nach PDF exportieren?
- **Konsistente Markenführung:** Bewahren Sie Unternehmensschriftarten und -farben, wenn Sie Notizen extern teilen.  
- **Lesbarkeit:** PDF behält das genaue Layout bei und ist ideal zum Drucken oder Archivieren.  
- **Plattformübergreifender Zugriff:** Empfänger können das PDF auf jedem Gerät ansehen, ohne OneNote zu benötigen.  

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Java Development Kit (JDK) 1.8+** – jedes aktuelle JDK funktioniert.  
2. **Aspose.Note für Java** – laden Sie das neueste JAR von der [Aspose.Note‑Download‑Seite](https://releases.aspose.com/note/java/) herunter.  
3. **Eine IDE** (Eclipse, IntelliJ IDEA oder NetBeans) zum Kompilieren und Ausführen des Beispiels.  

> **Pro Tipp:** Fügen Sie das Aspose.Note‑JAR Ihrem Projekt‑Classpath via Maven hinzu oder referenzieren Sie das JAR manuell in Ihrer IDE.

## Pakete importieren

Zuerst importieren wir die Klassen, die wir benötigen. Dieser Block bleibt unverändert.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> Die Klasse `ParagraphStyle` ist der Schlüssel, um später im Tutorial **Absatzstil festzulegen**.

## Schritt‑für‑Schritt‑Anleitung

Im Folgenden finden Sie einen kompakten Durchlauf jeder Operation. Die Code‑Blöcke entsprechen exakt dem Original‑Beispiel; wir fügen nur erläuternden Text hinzu.

### Schritt 1: Dokumentverzeichnis festlegen
Definieren Sie, wo die erzeugten Dateien gespeichert werden.

```java
String dataDir = "Your Document Directory";
```

Ersetzen Sie `"Your Document Directory"` durch einen absoluten oder relativen Pfad auf Ihrem Rechner.

### Schritt 2: Dokumentobjekt initialisieren
Erzeugen Sie das Root‑`Document`, das die OneNote‑Datei repräsentiert.

```java
Document doc = new Document();
```

### Schritt 3: Seitenobjekt initialisieren
Eine OneNote‑Datei besteht aus einer oder mehreren Seiten; wir beginnen mit einer einzelnen Seite.

```java
Page page = new Page();
```

### Schritt 4: Outline‑Objekt initialisieren
Outlines fungieren als Container für Outline‑Elemente (sozusagen Abschnitte).

```java
Outline outline = new Outline();
```

### Schritt 5: OutlineElement‑Objekt initialisieren
Hier **fügen wir ein Outline‑Element hinzu**, das unseren Rich‑Text enthält.

```java
OutlineElement outlineElem = new OutlineElement();
```

### Schritt 6: Textstil festlegen (Absatzstil setzen)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

Die `ParagraphStyle`‑Instanz definiert Schriftart, Größe und Farbe – hier setzen wir den **Absatzstil** für den kommenden Textknoten.

### Schritt 7: RichText‑Objekt initialisieren

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Wir erstellen einen `RichText`‑Knoten, fügen einen einfachen String ein und binden den zuvor definierten Stil an.

### Schritt 8: RichText‑Knoten zum OutlineElement hinzufügen

```java
outlineElem.appendChildLast(text);
```

Jetzt befindet sich der formatierte Text im Outline‑Element.

### Schritt 9: OutlineElement‑Knoten zum Outline hinzufügen

```java
outline.appendChildLast(outlineElem);
```

Das Outline enthält nun das Element, das unseren Absatz hält.

### Schritt 10: Outline‑Knoten zur Seite hinzufügen

```java
page.appendChildLast(outline);
```

Wir platzieren das Outline auf der Seite.

### Schritt 11: Seiten‑Knoten zum Dokument hinzufügen

```java
doc.appendChildLast(page);
```

Das Dokument besitzt nun eine einzelne Seite mit unserem formatierten Text.

### Schritt 12: Dokument speichern (OneNote‑PDF exportieren)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

Die `save`‑Methode schreibt die OneNote‑Datei und **exportiert OneNote nach PDF** in einem Schritt. Sie können auch als `.one` speichern, indem Sie `SaveFormat.One` verwenden, falls das native Format benötigt wird.

## Häufige Probleme & Lösungen

| Problem | Ursache | Lösung |
|---------|----------|--------|
| **Datei nicht gefunden** | `dataDir` verweist auf einen nicht existierenden Ordner. | Stellen Sie sicher, dass das Verzeichnis existiert, oder erstellen Sie es programmgesteuert (`new File(dataDir).mkdirs();`). |
| **Leeres PDF** | Vor dem Speichern wurde kein Inhalt hinzugefügt. | Prüfen Sie, ob der `RichText`‑Knoten angehängt und der Stil gesetzt ist. |
| **Nicht unterstützte Schriftart** | Schriftname ist nicht auf dem System installiert. | Verwenden Sie eine gängige Schrift wie `"Arial"` oder betten Sie die Schrift im Projekt ein. |

## Häufig gestellte Fragen

**F: Kann Aspose.Note komplexe Formatierungen wie Tabellen oder Bilder verarbeiten?**  
A: Ja, die API unterstützt Tabellen, Bilder, Hyperlinks und weitere erweiterte Layout‑Funktionen.

**F: Ist es möglich, **OneNote‑PDF zurück in eine OneNote‑Datei** zu konvertieren?**  
A: Eine direkte Konvertierung wird nicht bereitgestellt, aber Sie können PDF‑Inhalte extrahieren und ein OneNote‑Dokument mit der API neu aufbauen.

**F: Arbeitet die Bibliothek auf Linux/macOS?**  
A: Absolut. Aspose.Note für Java ist plattformunabhängig; stellen Sie lediglich sicher, dass das JDK installiert ist.

**F: Wie füge ich mehrere Seiten oder Outlines hinzu?**  
A: Erzeugen Sie zusätzliche `Page`‑ und `Outline`‑Objekte und hängen Sie sie wie im Ein‑Seiten‑Beispiel an das `Document` an.

**F: Wo finde ich weitere Beispiele?**  
A: In der offiziellen Aspose.Note‑Dokumentation und im [Support‑Forum](https://forum.aspose.com/c/note/28) gibt es zahlreiche Code‑Beispiele.

## Fazit

Sie haben nun gesehen, wie man **Absatzstil festlegt**, **Outline‑Elemente hinzufügt** und eine **OneNote‑Datei erzeugt**, die **nach PDF exportiert** werden kann – alles mit Aspose.Note für Java. Das frühzeitige Einbinden von formatiertem Text sorgt dafür, dass das Enddokument professionell wirkt und jede nachfolgende **OneNote‑PDF‑Konvertierung** die Formatierung beibehält. Erweitern Sie diese Basis gerne um Bilder, Tabellen oder benutzerdefinierte Metadaten, um den Anforderungen Ihres Projekts gerecht zu werden.

---

**Zuletzt aktualisiert:** 2026-02-18  
**Getestet mit:** Aspose.Note für Java 24.11 (neueste Version)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}