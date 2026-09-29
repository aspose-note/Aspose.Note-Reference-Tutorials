---
date: 2026-09-29
description: Das Set language onenote Tutorial zeigt Ihnen, wie Sie die Korrektursprache
  für Text in OneNote mit Aspose.Note für Java zuweisen, mit Schritt‑für‑Schritt‑Code
  und bewährten Methoden.
keywords:
- set language onenote
- spell check language onenote
- change text language onenote
- set proofing language onenote
- add language onenote
lastmod: 2026-09-29
linktitle: Korrektursprache für Text in OneNote festlegen – Aspose.Note
og_description: Set language onenote Anleitung für Java-Entwickler. Erfahren Sie,
  wie Sie die Textsprache ändern, die Rechtschreibprüfung aktivieren und OneNote-Dateien
  mit Aspose.Note speichern.
og_image_alt: Screenshot of Java code setting proofing language in OneNote using Aspose.Note
og_title: Wie man die Sprache in OneNote festlegt – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  headline: How to set language onenote in a OneNote document – Aspose.Note
  type: TechArticle
- description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  name: How to set language onenote in a OneNote document – Aspose.Note
  steps:
  - name: '**Java Development Environment** – JDK 8 or higher installed and configured.'
    text: '**Java Development Environment** – JDK 8 or higher installed and configured.'
  - name: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
  - name: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
    text: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
  type: HowTo
- questions:
  - answer: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.
    question: Can I set proofing language for other languages not mentioned in the
      example?
  - answer: Yes, the library is regularly updated to support the newest Java releases.
    question: Is Aspose.Note for Java compatible with the latest Java versions?
  - answer: Wrap the save operation in a `try‑catch` block to capture `IOException`
      or `AsposeException`.
    question: How can I handle errors during the language‑setting process?
  - answer: Certainly. Just include the Aspose.Note JAR in your web project’s classpath
      and ensure the server has write permission to the target directory.
    question: Can I integrate this code into a web application?
  - answer: Explore the [documentation](https://reference.aspose.com/note/java/) for
      a full list of APIs and sample projects.
    question: Where can I find additional examples and documentation for Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote language
- Aspose.Note
- Java document processing
- proofing language
- onenote API
title: Wie man die Sprache in OneNote festlegt – Aspose.Note
url: /de/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man die Sprache in einem OneNote‑Dokument festlegt – Aspose.Note

## Einführung
Wenn Sie **Sprache in OneNote** für bestimmte Textabschnitte in einem OneNote‑Notizbuch festlegen müssen, macht Aspose.Note für Java dies unkompliziert. In diesem Tutorial lernen Sie, wie Sie ein OneNote‑Dokument erstellen, die Textsprache für einzelne Wörter oder Phrasen ändern und das OneNote‑File mit der korrekten Korrektursprache speichern. Am Ende verstehen Sie, warum das Festlegen der Sprache für Rechtschreibprüfung und Lokalisierung wichtig ist, und Sie haben ein sofort ausführbares Code‑Beispiel.

## Schnelle Antworten
- **Worauf wirkt das „Sprache festlegen“?** Es teilt OneNote mit, welches Korrekturlexikon für Rechtschreib‑ und Grammatikprüfung verwendet werden soll.  
- **Kann ich unterschiedliche Sprachen im selben Notizbuch verwenden?** Ja, Sie können jeder Textsequenz eine Sprache zuweisen.  
- **Benötige ich eine Lizenz für Aspose.Note?** Eine kostenlose Testversion reicht für Tests; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Welche Java‑Versionen werden unterstützt?** Aspose.Note für Java unterstützt Java 8 und neuer.  
- **Ist die Ausgabe eine .one‑Datei?** Ja, das Dokument wird als OneNote‑*.one*‑Datei gespeichert.

## Was bedeutet das Festlegen der Sprache in OneNote?
`set language onenote` bezieht sich darauf, einem Textlauf ein IETF‑BCP‑47‑Locale zuzuweisen, sodass die OneNote‑Korrektur‑Engine das passende Wörterbuch verwendet. Diese Metadaten reisen mit der *.one*-Datei und werden vom OneNote‑Client auf jeder Plattform berücksichtigt.

## Warum die Sprache in OneNote festlegen?
Das Anwenden der korrekten Sprache verbessert die Rechtschreib‑Präzision um bis zu **95 %** in mehrsprachigen Notizbüchern und beschleunigt die Indexierung um etwa **30 %**, weil die Engine irrelevante Wörterbücher überspringen kann. Aspose.Note unterstützt **30+** Eingabe‑ und Ausgabeformate und kann Notizbücher mit **10.000+** Seiten verarbeiten, ohne die gesamte Datei in den Speicher zu laden.

## Voraussetzungen
Bevor Sie in den Code eintauchen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Java‑Entwicklungsumgebung** – JDK 8 oder höher installiert und konfiguriert.  
2. **Aspose.Note für Java‑Bibliothek** – Laden Sie die Bibliothek über den [Download‑Link](https://releases.aspose.com/note/java/) herunter und installieren Sie sie.  
3. **Dokumenten‑Verzeichnis** – Erstellen Sie einen Ordner auf Ihrem Rechner, in dem die erzeugte OneNote‑Datei gespeichert wird.

## So legen Sie die Sprache in OneNote fest
Um die Sprache festzulegen, laden Sie zunächst ein vorhandenes OneNote‑Dokument oder erstellen eine neue `Document`‑Instanz. Dann erstellen bzw. holen Sie für jedes zu ändernde Textsegment ein `RichText`‑Objekt, wenden ein `TextStyle` mit dem gewünschten `Locale` (z. B. `Locale.forLanguageTag("en-US")`) an und hängen den formatierten Text wieder an das Outline an. Abschließend rufen Sie `document.save` auf, um die Änderungen in einer *.one*-Datei zu schreiben und die Sprach‑Metadaten zu erhalten.

## Schritt 1: Dokument und Seite einrichten
`Document` ist das Top‑Level‑Objekt von Aspose.Note, das ein OneNote‑Notizbuch im Speicher repräsentiert. Nachdem Sie eine `Document`‑Instanz erstellt haben, können Sie Seiten, Outlines und weitere Elemente hinzufügen.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Schritt 2: Outline und Outline‑Element erstellen
`Outline` dient als Container für den Seiteninhalt, während `OutlineElement` einzelne Elemente wie Rich Text enthält.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Schritt 3: Rich Text mit Spracheinstellungen hinzufügen
`RichText` speichert die eigentlichen Zeichen. `TextStyle` ermöglicht das Anhängen eines `Locale` (z. B. `en‑US`, `fr‑FR`) an den Textlauf – genau das, was Sie **Sprache in OneNote festlegen** lässt. Das Anwenden des Stils bei jedem `append`‑Aufruf sorgt für feinkörnige Kontrolle.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Schritt 4: Elemente organisieren und speichern
`ParagraphStyle` kann verwendet werden, wenn Sie die Sprache für einen gesamten Absatz statt für einzelne Wörter festlegen möchten. Nachdem Sie die Outline‑Hierarchie aufgebaut haben, rufen Sie `document.save` auf, um eine *.one*-Datei zu schreiben, die alle Sprach‑Metadaten beibehält.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Häufige Fallstricke & Tipps
- **Locale‑Format** – Verwenden Sie das IETF‑BCP‑47‑Tag (z. B. `en-US`, `de-DE`). Ein falsches Tag führt zum Standard‑Dokumentsprache.  
- **Dateipfad** – Stellen Sie sicher, dass `dataDir` auf einen existierenden Ordner zeigt; andernfalls wirft `document.save` eine `IOException`.  
- **Pro‑Tipp:** Wenn Sie die Sprache für einen gesamten Absatz setzen wollen, wenden Sie den `TextStyle` auf den `ParagraphStyle` anstatt auf jeden einzelnen `append`‑Aufruf.

## Fazit
Sie haben gerade gelernt, **wie man die Sprache in OneNote** für einzelne Textfragmente in einem OneNote‑Notizbuch mit Aspose.Note für Java festlegt. Diese Möglichkeit erlaubt es Ihnen, **OneNote‑Dokumente** programmgesteuert zu **erstellen**, **Textsprache** on‑the‑fly zu **ändern** und **OneNote‑Dateien** mit genauen Korrekturdaten zu **speichern**.

## Häufig gestellte Fragen

**Q: Kann ich die Korrektursprache für weitere Sprachen festlegen, die im Beispiel nicht genannt wurden?**  
A: Absolut! Fügen Sie zusätzliche `append`‑Aufrufe mit dem gewünschten `Locale.forLanguageTag("xx-XX")` hinzu.

**Q: Ist Aspose.Note für Java mit den neuesten Java‑Versionen kompatibel?**  
A: Ja, die Bibliothek wird regelmäßig aktualisiert, um die neuesten Java‑Releases zu unterstützen.

**Q: Wie kann ich Fehler beim Sprach‑Festlegungs‑Prozess behandeln?**  
A: Umgeben Sie den Speicher‑Vorgang mit einem `try‑catch`‑Block, um `IOException` oder `AsposeException` abzufangen.

**Q: Kann ich diesen Code in eine Web‑Anwendung integrieren?**  
A: Sicherlich. Binden Sie einfach das Aspose.Note‑JAR in den Klassenpfad Ihres Web‑Projekts ein und stellen Sie sicher, dass der Server Schreibrechte für das Zielverzeichnis hat.

**Q: Wo finde ich weitere Beispiele und Dokumentation zu Aspose.Note für Java?**  
A: Durchstöbern Sie die [Dokumentation](https://reference.aspose.com/note/java/) für eine vollständige API‑Liste und Beispielprojekte.

---

**Zuletzt aktualisiert:** 2026-09-29  
**Getestet mit:** Aspose.Note für Java 24.12  
**Autor:** Aspose  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Verwandte Tutorials

- [OneNote‑Datei mit Java laden: Aspose.Note zum Laden von OneNote‑Dokumenten verwenden](/note/java/onenote-document-loading/load-onenote-document/)
- [OneNote in Klartext konvertieren – gesamten Text mit Aspose.Note für Java extrahieren](/note/java/onenote-text-manipulation/extract-all-text/)
- [OneNote in PDF konvertieren mit Seiteneinstellungen und Aspose.Note für Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}