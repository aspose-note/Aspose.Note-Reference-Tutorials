---
date: 2026-03-29
description: Erfahren Sie, wie Sie die Sprache für Text in OneNote mit Aspose.Note
  für Java festlegen. Diese Schritt‑für‑Schritt‑Anleitung zeigt Ihnen, wie Sie ein
  OneNote‑Dokument erstellen, die Textsprache ändern und die OneNote‑Datei effizient
  speichern.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Wie man die Sprache für Text in OneNote festlegt – Aspose.Note
url: /de/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man die Sprache für Text in OneNote festlegt – Aspose.Note

## Einführung
Wenn Sie **wie man die Sprache festlegt** für bestimmte Textabschnitte in einem OneNote‑Notizbuch benötigen, macht Aspose.Note für Java dies unkompliziert. In diesem Tutorial lernen Sie, wie Sie ein OneNote‑Dokument erstellen, die Textsprache für einzelne Wörter oder Phrasen ändern und schließlich die OneNote‑Datei mit der korrekten Korrektursprache speichern. Am Ende verstehen Sie, warum das Festlegen der Sprache für Rechtschreibprüfung und Lokalisierung wichtig ist, und Sie haben ein sofort ausführbares Code‑Beispiel.

## Schnelle Antworten
- **Was beeinflusst das „Sprache festlegen“?** Es teilt OneNote mit, welches Korrekturdictionary für Rechtschreib‑ und Grammatikprüfung verwendet werden soll.
- **Kann ich verschiedene Sprachen im selben Notizbuch festlegen?** Ja, Sie können jeder Textsequenz eine Sprache zuweisen.
- **Benötige ich eine Lizenz für Aspose.Note?** Eine kostenlose Testversion reicht für Tests; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.
- **Welche Java‑Versionen werden unterstützt?** Aspose.Note für Java unterstützt Java 8 und neuer.
- **Ist die Ausgabe eine .one‑Datei?** Ja, das Dokument wird als OneNote‑*.one*-Datei gespeichert.

## Voraussetzungen
Bevor Sie in den Code eintauchen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Java‑Entwicklungsumgebung** – JDK 8 oder höher installiert und konfiguriert.  
2. **Aspose.Note für Java‑Bibliothek** – Laden Sie die Bibliothek über den [Download‑Link](https://releases.aspose.com/note/java/) herunter und installieren Sie sie.  
3. **Dokumentverzeichnis** – Erstellen Sie einen Ordner auf Ihrem Rechner, in dem die erzeugte OneNote‑Datei gespeichert wird.

## Warum die Sprache für Text in OneNote festlegen?
Das Festlegen der Korrektursprache sorgt dafür, dass Rechtschreib‑, Grammatikvorschläge und die Suchindizierung für mehrsprachige Inhalte korrekt funktionieren. Das ist besonders nützlich für:

- **Globale Teams**, die an einem einzigen Notizbuch zusammenarbeiten.  
- **Lokalisierte Dokumentation**, bei der jeder Abschnitt in einer anderen Sprache verfasst sein kann.  
- **Datengetriebene Anwendungen**, die Notizen programmgesteuert für Nutzer weltweit erzeugen.

## Pakete importieren
Importieren Sie die notwendigen Aspose.Note‑Klassen und Java‑Hilfsmittel.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Schritt 1: Dokument und Seite einrichten
Erstellen Sie ein frisches OneNote‑Dokument und eine Seite, die Ihren Inhalt aufnehmen wird. Dieser Schritt demonstriert zudem **create OneNote document**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Schritt 2: Gliederung und Gliederungselement erstellen
Eine Gliederung ist der Container für den Notizbuchinhalt. Hier bauen wir die Struktur, die später den sprachspezifischen Text enthalten wird.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Schritt 3: Rich‑Text mit Spracheinstellungen hinzufügen
Jetzt **ändern wir die Textsprache**, indem wir jedem Textsegment ein `TextStyle` mit einem bestimmten `Locale` anhängen. Dies demonstriert **set language for text**.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Schritt 4: Elemente organisieren und speichern
Setzen Sie die Gliederungshierarchie zusammen, hängen Sie sie an die Seite an und **speichern Sie die OneNote‑Datei** mit den angewendeten Spracheinstellungen.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Häufige Fallstricke & Tipps
- **Locale‑Format** – Verwenden Sie das IETF‑BCP‑47‑Tag (z. B. `en-US`, `de-DE`). Ein falsches Tag führt zur Standardsprache des Dokuments.  
- **Dateipfad** – Stellen Sie sicher, dass `dataDir` auf einen vorhandenen Ordner zeigt; andernfalls wirft `document.save` eine `IOException`.  
- **Pro‑Tipp:** Wenn Sie die Sprache für einen gesamten Absatz festlegen möchten, wenden Sie das `TextStyle` auf das `ParagraphStyle` anstatt auf jeden einzelnen `append`‑Aufruf an.

## Fazit
Sie haben gerade **gelernt, wie man die Sprache** für einzelne Textfragmente in einem OneNote‑Notizbuch mit Aspose.Note für Java festlegt. Diese Möglichkeit ermöglicht es Ihnen, **OneNote‑Dokumente** programmgesteuert zu **erstellen**, **Textsprache** on‑the‑fly zu **ändern** und **OneNote‑Dateien** mit genauen Korrekturdaten zu **speichern**.

## Häufig gestellte Fragen

**F: Kann ich die Korrektursprache für andere Sprachen festlegen, die im Beispiel nicht genannt werden?**  
A: Absolut! Fügen Sie zusätzliche `append`‑Aufrufe mit dem gewünschten `Locale.forLanguageTag("xx-XX")` hinzu.

**F: Ist Aspose.Note für Java mit den neuesten Java‑Versionen kompatibel?**  
A: Ja, die Bibliothek wird regelmäßig aktualisiert, um die neuesten Java‑Releases zu unterstützen.

**F: Wie kann ich Fehler beim Sprach‑Festlegungs‑Prozess behandeln?**  
A: Wickeln Sie den Speicher‑Vorgang in einen `try‑catch`‑Block, um `IOException` oder `AsposeException` abzufangen.

**F: Kann ich diesen Code in eine Web‑Anwendung integrieren?**  
A: Sicherlich. Binden Sie das Aspose.Note‑JAR in den Klassenpfad Ihres Web‑Projekts ein und stellen Sie sicher, dass der Server Schreibrechte für das Zielverzeichnis hat.

**F: Wo finde ich weitere Beispiele und Dokumentation für Aspose.Note für Java?**  
A: Durchstöbern Sie die [Dokumentation](https://reference.aspose.com/note/java/) für eine vollständige Liste der APIs und Beispielprojekte.

---

**Zuletzt aktualisiert:** 2026-03-29  
**Getestet mit:** Aspose.Note für Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}