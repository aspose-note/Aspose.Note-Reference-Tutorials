---
date: 2026-03-03
description: Erfahren Sie, wie Sie in OneNote Gliederungen erstellen und Vorlagen
  für Besprechungsnotizen mit Aspose.Note für Java generieren. Passen Sie den Schriftstil
  an und fügen Sie problemlos Kontrollkästchen hinzu.
linktitle: Create Outline in OneNote – Meeting Notes Template
second_title: Aspose.Note Java API
title: Gliederung in OneNote erstellen – Vorlage für Besprechungsnotizen
url: /de/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Gliederung in OneNote erstellen – Besprechungsnotizen‑Vorlage

## Einführung
In der heutigen schnelllebigen Welt ist das effiziente **Erstellen einer Gliederung in OneNote** entscheidend für eine klare Sitzungsdokumentation. Aspose.Note für Java bietet eine leistungsstarke Möglichkeit, **eine Besprechungsnotizen‑Vorlage zu erzeugen**, die Sie anpassen, Checkboxen hinzufügen und die Schriftarten genau nach Ihren Bedürfnissen formatieren können. In dieser Schritt‑für‑Schritt‑Anleitung zeigen wir, wie man eine wiederverwendbare Sitzungsagenda‑Vorlage erstellt und erklären **wie man Checkboxen hinzufügt**, **eine Checkliste zu OneNote hinzufügt** und **die Schriftart in OneNote anpasst** für ein professionelles Aussehen.

## Schnelle Antworten
- **Was bedeutet „Gliederung in OneNote erstellen“?** Es bedeutet, programmgesteuert eine hierarchische Struktur (Titel, Abschnitte, Aufzählungspunkte) innerhalb einer OneNote‑Datei zu erstellen.  
- **Welche Bibliothek unterstützt dies?** Aspose.Note für Java.  
- **Kann ich Checkboxen zur Gliederung hinzufügen?** Ja – verwenden Sie `NoteCheckBox.createBlueCheckBox()`.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion ist verfügbar; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Welche Java‑Version wird unterstützt?** Java 8 und höher.

## Was bedeutet „Gliederung in OneNote erstellen“?
Eine Gliederung in OneNote zu erstellen bedeutet, eine Seite mit einem Titel, mehreren Gliederungsabschnitten und optionaler Listennummerierung oder Checkboxen zu definieren. Diese Struktur spiegelt wider, wie Sie manuell Überschriften und Aufzählungspunkte in der OneNote‑Benutzeroberfläche eingeben würden, wird jedoch automatisch durch Code erzeugt.

## Warum Aspose.Note für Vorlagen von Sitzungsagenden verwenden?
- **Konsistenz:** Jede Besprechung beginnt mit demselben sauberen Layout.  
- **Automatisierung:** Reduziert manuelles Tippen und stellt sicher, dass alle erforderlichen Abschnitte (Agenda, Aufgaben, Notizen) vorhanden sind.  
- **Anpassbarkeit:** Schriftarten, Farben ändern und interaktive Checkboxen hinzufügen, um Aufgaben zu verfolgen.  
- **Integration:** Funktioniert mit jeder Java‑IDE und kann mit anderen Aspose‑Bibliotheken für PDFs, Tabellenkalkulationen usw. kombiniert werden.

## Voraussetzungen
- Grundlegendes Verständnis der Java‑Programmierung.  
- Aspose.Note für Java Bibliothek installiert. Sie können sie [hier](https://releases.aspose.com/note/java/) herunterladen.  
- Eine IDE wie Eclipse oder IntelliJ IDEA.  

## Pakete importieren
Zuerst importieren wir die benötigten Klassen. Dieser Codeabschnitt bleibt exakt gleich wie im Original‑Tutorial.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Schritt 1: Dokumentstruktur erstellen
Wir beginnen mit dem Erstellen des Dokuments, richten einen Titel ein und bereiten Absatz‑Stile vor, die uns später dabei helfen, **die Schriftart in OneNote anzupassen**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
ParagraphStyle headerStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(16);
ParagraphStyle bodyStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(12);
DateFormat dateFormat = DateFormat.getDateInstance(DateFormat.SHORT, Locale.US);
Document d = new Document();
boolean restartFlag = true;
RichText titleText = new RichText().append(String.format("Weekly meeting %s", dateFormat.format(Date.from(Instant.now()))));
titleText.setParagraphStyle(ParagraphStyle.getDefault());
Title title = new Title();
title.setTitleText(titleText);
Page page = new Page();
page.setTitle(title);
d.appendChildLast(page);
```

*Was wir getan haben:*  
- Zwei `ParagraphStyle`‑Objekte definiert (`headerStyle` für Überschriften, `bodyStyle` für normalen Text).  
- Ein `Document` erstellt und einen `Title` hinzugefügt, der das aktuelle Datum enthält und der Seite eine klare Überschrift verleiht.

## Schritt 2: Wichtige Punkte gliedern
Als Nächstes **erstellen wir eine Gliederung in OneNote**, indem wir ein `Outline`‑Objekt hinzufügen und es mit Abschnitten wie „Wichtig“ füllen. Hier befinden sich die Agendapunkte.

```java
Outline outline = page.appendChildLast(new Outline());
outline.setVerticalOffset(30);
outline.setHorizontalOffset(30);
RichText richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("Important");
richText.setParagraphStyle(headerStyle);
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    restartFlag = false;
}
```

*Warum das wichtig ist:*  
- Das `Outline`‑Objekt stellt die hierarchische Liste dar, die Sie in OneNote sehen.  
- Mit `createListNumberingStyle` erzeugen wir eine nummerierte Liste, die für jeden neuen Abschnitt neu gestartet werden kann.

## Schritt 3: Aktionspunkte hervorheben (Wie man Checkboxen hinzufügt)
Aktionspunkte benötigen einen visuellen Hinweis. Durch das Anhängen eines Checkbox‑Tags an jedes `RichText`‑Element ermöglichen wir **wie man Checkboxen hinzufügt** direkt innerhalb der Gliederung.

```java
richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("TO DO");
richText.setParagraphStyle(headerStyle);
richText.setSpaceBefore(15);
restartFlag = true;
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    richText.getTags().add(NoteCheckBox.createBlueCheckBox());
    restartFlag = false;
}
```

*Pro‑Tipp:* Verwenden Sie `NoteCheckBox.createBlueCheckBox()` für ein blaues Kontrollkästchen; weitere Farben sind verfügbar, falls Sie einen anderen visuellen Stil benötigen.

## Schritt 4: Dokument speichern
Abschließend schreiben wir die OneNote‑Datei auf die Festplatte. Die Datei kann direkt in der OneNote‑Desktop‑App geöffnet werden.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Häufige Probleme und Lösungen
| Problem | Lösung |
|-------|----------|
| **Checkboxen werden nicht angezeigt** | Stellen Sie sicher, dass Sie `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` nach dem Festlegen des Absatzstils aufgerufen haben. |
| **Schriftarten sehen in OneNote anders aus** | Vergewissern Sie sich, dass der Schriftname (z. B. „Calibri“) auf dem Rechner installiert ist, auf dem OneNote die Datei öffnet. |
| **Gliederung ist nicht eingerückt** | `setVerticalOffset` und `setHorizontalOffset` am `Outline`‑Objekt anpassen. |
| **Nummerierung startet unerwartet neu** | `restartFlag` korrekt verwenden; nur für die erste Liste in einem neuen Abschnitt auf `true` setzen. |

## Häufig gestellte Fragen
### Kann ich die Schriftstile in meinen Besprechungsnotizen anpassen?
Ja, Aspose.Note ermöglicht das Definieren benutzerdefinierter Schriftstile für Überschriften und Fließtext.

### Ist Aspose.Note mit anderen Java‑Bibliotheken kompatibel?
Aspose.Note lässt sich nahtlos mit anderen Java‑Bibliotheken integrieren, um erweiterte Funktionen zu ermöglichen.

### Wie kann ich zusätzliche Abschnitte zu meinen Besprechungsnotizen hinzufügen?
Sie können die Gliederungsstruktur ganz einfach erweitern, indem Sie dem im Tutorial gezeigten Muster folgen.

### Gibt es Lizenzhinweise für Aspose.Note?
Siehe die [Aspose.Note‑Dokumentation](https://reference.aspose.com/note/java/) für Lizenzdetails.

### Gibt es eine Testversion von Aspose.Note?
Ja, Sie können die [kostenlose Testversion hier](https://releases.aspose.com/) nutzen.

## FAQ
**F: Wie füge ich eine Checkliste zu OneNote hinzu, ohne Checkboxen zu verwenden?**  
A: Sie können eine Aufzählungsliste erstellen und die Elemente manuell markieren, aber die Verwendung von `NoteCheckBox` liefert interaktive Checkboxen, die mit der OneNote‑Benutzeroberfläche synchronisiert werden.

**F: Kann ich diese Vorlage verwenden, um eine wöchentliche Besprechungsagenda‑Vorlage zu erstellen?**  
A: Auf jeden Fall. Ändern Sie einfach das Datumsformat oder übergeben Sie einen benutzerdefinierten Titel‑String, um dieselbe Struktur jede Woche wiederzuverwenden.

**F: Was ist der beste Weg, **die Schriftart in OneNote für das Branding anzupassen**?**  
A: Definieren Sie `ParagraphStyle`‑Objekte mit Ihrem Unternehmensschriftartnamen, Größe und Farbe und wenden Sie sie dann auf jedes `RichText`‑Element an, wie in Schritt 1 gezeigt.

**F: Unterstützt Aspose.Note das Exportieren der Gliederung nach PDF?**  
A: Ja. Nachdem Sie die OneNote‑Datei gespeichert haben, können Sie sie mit Aspose.Note laden und mit `Document.save("output.pdf", SaveFormat.Pdf)` nach PDF exportieren.

**F: Gibt es eine Möglichkeit, eine Checkbox programmgesteuert als erledigt zu markieren?**  
A: Sie können den Zustand der Checkbox setzen, indem Sie ein `NoteCheckBox`‑Tag mit der Eigenschaft `Checked` auf `true` setzen.

**Zuletzt aktualisiert:** 2026-03-03  
**Getestet mit:** Aspose.Note für Java 24.11 (zum Zeitpunkt des Schreibens aktuell)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}