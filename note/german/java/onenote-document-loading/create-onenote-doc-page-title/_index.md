---
date: 2025-12-02
description: Erfahren Sie, wie Sie in Java mit Aspose.Note für Java eine OneNote‑Seite
  mit einem Titel erstellen. Dieser Leitfaden zeigt, wie Sie den Titel einer OneNote‑Seite
  festlegen und die Schriftart des Titels anpassen.
language: de
linktitle: How to Create OneNote Page with Title - Java
second_title: Aspose.Note Java API
title: Wie man eine OneNote‑Seite mit Titel erstellt – Java
url: /java/onenote-document-loading/create-onenote-doc-page-title/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man eine OneNote‑Seite mit Titel erstellt – Java

## Einführung

Wenn Sie **wie man programmgesteuert eine OneNote‑Seite erstellt**, macht Aspose.Note für Java das ganz einfach. In diesem Tutorial lernen Sie, wie Sie eine OneNote‑Datei erzeugen, den Seitentitel festlegen und sogar die Schriftart des Titels anpassen – alles aus Java‑Code. Am Ende haben Sie ein einsatzbereites OneNote‑Dokument, das Sie in jede Java‑Anwendung integrieren können.

## Schnelle Antworten
- **Welche Bibliothek wird benötigt?** Aspose.Note für Java.  
- **Kann ich eine benutzerdefinierte Schriftart für den Titel festlegen?** Ja – verwenden Sie `ParagraphStyle`, um Schriftname, Größe und Farbe zu definieren.  
- **Welche Java‑Version wird unterstützt?** Jede JDK 8+ (die API ist abwärtskompatibel).  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion reicht für Tests; für den Produktionseinsatz ist eine Lizenz erforderlich.  
- **Wo wird die Ausgabe gespeichert?** Sie geben den Pfad in der Variable `dataDir` an.

## Was ist ein OneNote‑Seitentitel?
Ein OneNote‑Seitentitel ist die Kopfzeile, die oben auf jeder Seite angezeigt wird. Er enthält typischerweise den Seitennamen, das Erstellungsdatum und die Uhrzeit. Das programmgesteuerte Festlegen dieses Titels hilft Ihnen, konsistente, gut strukturierte Notizbücher zu erstellen.

## Warum den OneNote‑Seitentitel programmgesteuert setzen?
- **Automatisierung:** Berichte oder Besprechungsnotizen ohne manuelle Bearbeitung erzeugen.  
- **Konsistenz:** Eine Namenskonvention für alle Seiten durchsetzen.  
- **Integration:** OneNote mit anderen Systemen (z. B. CRM, Projektmanagement‑Tools) verbinden.  

## Voraussetzungen

- **Java Development Kit (JDK)** – Version 8 oder höher.  
- **Aspose.Note für Java** – herunterladen von der offiziellen Seite **[hier](https://releases.aspose.com/note/java/)**.  
- **IDE** – IntelliJ IDEA, Eclipse oder NetBeans (nach Wahl).

## Pakete importieren

Zuerst importieren wir die Klassen, die wir aus der Aspose.Note‑Bibliothek benötigen.

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

### Schritt 1: Dokumentverzeichnis einrichten  
Definieren Sie, wo die erzeugte OneNote‑Datei gespeichert werden soll.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

### Schritt 2: Dokumentobjekt erstellen  
Instanziieren Sie ein neues `Document` – das repräsentiert die OneNote‑Datei, die Sie bauen.

```java
// Create an object of the Document class
Document doc = new Document();
```

### Schritt 3: Seitenobjekt initialisieren  
Erzeugen Sie ein `Page`‑Objekt, das den Titel und beliebigen Inhalt aufnehmen wird.

```java
// Initialize Page class object
Page page = new Page();
```

### Schritt 4: Standardschriftstil festlegen  
Definieren Sie einen Standard‑`ParagraphStyle`, der auf den Titeltext angewendet wird. Hier **passen wir die OneNote‑Titelschrift an**.

```java
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

### Schritt 5: Eigenschaften des Seitentitels setzen  
Hier **setzen wir die OneNote‑Seiten‑Titel‑Details** – Titeltext, Datum und Uhrzeit. Passen Sie die Zeichenketten nach Bedarf an.

```java
// Set page title properties
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

### Schritt 6: Titel der Seite zuweisen  
Jetzt **fügen wir den Titel zu OneNote hinzu**, indem wir das `Title`‑Objekt mit der `Page` verknüpfen.

```java
page.setTitle(title);
```

### Schritt 7: Seite zum Dokument hinzufügen  
Fügen Sie die konfigurierte Seite zur Dokumentstruktur hinzu.

```java
doc.appendChildLast(page);
```

### Schritt 8: OneNote‑Dokument speichern  
Geben Sie den Ausgabedateinamen an und speichern Sie das Notizbuch. Damit ist der **java create onenote file**‑Prozess abgeschlossen.

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// Save OneNote document
doc.save(dataDir);
```

## Häufige Probleme & Tipps

| Problem | Lösung |
|---------|--------|
| **Ungültiger Dateipfad** | Stellen Sie sicher, dass `dataDir` mit einem korrekten Trennzeichen (`/` oder `\\`) endet und dass der Ordner existiert. |
| **Titel nicht sichtbar** | Prüfen Sie, ob `ParagraphStyle` auf jedes `RichText`‑Element angewendet wurde. |
| **Lizenz‑Ausnahme** | Verwenden Sie für Tests eine Testlizenz; setzen Sie vor dem Deployment eine Voll‑Lizenz. |
| **Datum zeigt falschen Monat** | Java‑Monate sind nullbasiert; `cal.set(2018, 04, 03)` setzt tatsächlich Mai. Passen Sie entsprechend an. |

## Häufig gestellte Fragen

**F: Ist Aspose.Note für Java mit verschiedenen Java‑Versionen kompatibel?**  
A: Ja, die Bibliothek funktioniert mit Java 8 und neueren Versionen und bietet Ihnen Flexibilität in unterschiedlichen Umgebungen.

**F: Kann ich die Schriftart und -größe des Seitentitels anpassen?**  
A: Absolut! Verwenden Sie `ParagraphStyle` (wie in Schritt 4 gezeigt), um beliebigen Schriftname, Größe und Farbe festzulegen.

**F: Wie füge ich weiteren Inhalt (z. B. Absätze, Bilder) zur Seite hinzu?**  
A: Erzeugen Sie zusätzliche `RichText`‑ oder `Image`‑Objekte, setzen Sie deren Stile und fügen Sie sie mit `page.appendChildLast(yourObject)` zur `Page` hinzu.

**F: Gibt es eine Testversion von Aspose.Note für Java?**  
A: Ja, Sie können eine kostenlose Testversion von der Aspose‑Website herunterladen, um alle Funktionen zu evaluieren.

**F: Wo bekomme ich Unterstützung, wenn Probleme auftreten?**  
A: Besuchen Sie das [Aspose.Note‑Forum](https://forum.aspose.com/c/note/28) für Community‑Hilfe oder eröffnen Sie ein Support‑Ticket bei Aspose.

---

**Zuletzt aktualisiert:** 2025‑12‑02  
**Getestet mit:** Aspose.Note für Java 24.12 (zum Zeitpunkt der Erstellung)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}