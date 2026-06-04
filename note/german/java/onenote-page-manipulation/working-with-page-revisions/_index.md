---
date: 2026-01-15
description: Erfahren Sie, wie Sie Änderungen in OneNote verfolgen und Seitenrevisionen
  in OneNote‑Dokumenten mit Aspose.Note für Java verwalten. Enthält ein Beispiel für
  eine Revisionszusammenfassung und Anweisungen zum Ändern des Revisionsdatums.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Änderungen nachverfolgen in OneNote – Seitenrevisionen mit Aspose.Note verwalten
url: /de/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Arbeiten mit Seitenrevisionen in OneNote - Aspose.Note

## Einleitung

OneNote ist ein leistungsstarkes Werkzeug zur Organisation von Notizen, und wenn Sie **track changes onenote** benötigen, wird die Verwaltung von Seitenrevisionen für eine effektive Zusammenarbeit unerlässlich. Mit Aspose.Note für Java können Sie Revisionen programmgesteuert handhaben, sehen, wer eine Seite bearbeitet hat, und sogar Zeitstempel anpassen. Dieses Tutorial führt Sie durch jeden Schritt, vom Laden eines Dokuments bis zum Aktualisieren der Revisionszusammenfassung.

## Quick Answers
- **Was bedeutet “track changes onenote”?** Es bezieht sich auf die Überwachung, wer eine OneNote-Seite bearbeitet hat und wann.
- **Welche Bibliothek wird benötigt?** Aspose.Note für Java.
- **Kann ich den Autor oder das Datum einer Revision ändern?** Ja, mit der RevisionSummary-API (`modify revision date`).
- **Benötige ich vorher eine OneNote-Datei?** Ja, eine Beispiel‑`.one`‑Datei ist erforderlich.
- **Wird für die Produktion eine Lizenz benötigt?** Eine gültige Aspose.Note‑Lizenz ist für die kommerzielle Nutzung erforderlich.

## Was ist ein Beispiel für eine Revisionszusammenfassung?
Eine *Revisionszusammenfassung* liefert Metadaten zu den letzten Änderungen auf einer Seite – Autorname, letzte Änderungszeit und weitere Details. In diesem Leitfaden rufen wir diese Informationen ab und zeigen, wie man **modify revision date** durchführt.

## Warum track changes onenote mit Aspose.Note?
- **Zusammenarbeit:** Schnell sehen, wer die letzten Änderungen vorgenommen hat.
- **Auditierung:** Eine zuverlässige Historie von Änderungen für die Einhaltung von Vorschriften behalten.
- **Automatisierung:** Revisionsverwaltung in Backend‑Dienste oder Migrationstools integrieren.

## Voraussetzungen

### Java-Entwicklungsumgebung
Stellen Sie sicher, dass das Java Development Kit (JDK) auf Ihrem System installiert ist.

### Aspose.Note für Java Bibliothek
Laden Sie die Aspose.Note für Java Bibliothek von [here](https://releases.aspose.com/note/java/) herunter und installieren Sie sie.

### OneNote-Dokument
Haben Sie ein Beispiel‑OneNote‑Dokument für Testzwecke bereit.

## Pakete importieren

Importieren Sie in Ihrem Java‑Projekt die notwendigen Pakete, um mit Aspose.Note für Java zu arbeiten.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Lassen Sie uns das bereitgestellte Beispiel in mehrere Schritte aufteilen, um ein klares Verständnis zu erhalten.

## Schritt 1: OneNote‑Dokument laden

Laden Sie zunächst das OneNote‑Dokument und holen Sie die erste untergeordnete Seite.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Schritt 2: Seiten‑Revisionszusammenfassung lesen

Lesen Sie die Inhalts‑Revisionszusammenfassung für die Seite. Dies ist das **revision summary example**, das zeigt, wer die Seite zuletzt bearbeitet hat.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Schritt 3: Seiten‑Revisionszusammenfassung aktualisieren

Aktualisieren Sie die Seiten‑Revisionszusammenfassung mit einem neuen Autor und einem neuen Änderungsdatum. Dies demonstriert, wie man **modify revision date** programmgesteuert durchführt.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Fazit

Die programmgesteuerte Verwaltung von Seitenrevisionen in OneNote‑Dokumenten kann mit Aspose.Note für Java vereinfacht werden. Durch Befolgen der in diesem Tutorial beschriebenen Schritte können Sie effektiv **track changes onenote**, Revisionsdetails anzeigen und sogar **modify revision date** an Ihren Arbeitsablauf anpassen.

## FAQ's

### Q1: Kann ich Aspose.Note für Java mit anderen Java‑Bibliotheken verwenden?

A: Ja, Aspose.Note für Java kann mit anderen Java‑Bibliotheken integriert werden, um die Funktionalität zu erweitern.

### Q2: Unterstützt Aspose.Note für Java alle Versionen von OneNote‑Dokumenten?

A: Aspose.Note für Java unterstützt verschiedene Versionen von OneNote‑Dokumenten, einschließlich älterer Versionen.

### Q3: Ist Aspose.Note für Java für Unternehmens‑Anwendungen geeignet?

A: Absolut, Aspose.Note für Java ist darauf ausgelegt, den Anforderungen von Unternehmens‑Anwendungen mit robusten Funktionen und Skalierbarkeit gerecht zu werden.

### Q4: Kann ich Seitenrevisionen mit Aspose.Note für Java anpassen?

A: Ja, Sie können Seitenrevisionen nach Ihren Anforderungen mit Aspose.Note für Java anpassen.

### Q5: Wo kann ich Unterstützung für Aspose.Note für Java erhalten?

A: Sie können Unterstützung für Aspose.Note für Java im [Aspose.Note forum](https://forum.aspose.com/c/note/28) erhalten.

---

**Zuletzt aktualisiert:** 2026-01-15  
**Getestet mit:** Aspose.Note für Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}