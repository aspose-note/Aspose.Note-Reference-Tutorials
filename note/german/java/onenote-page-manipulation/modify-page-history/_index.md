---
date: 2026-01-12
description: Erfahren Sie, wie Sie die OneNote‑Seitenhistorie bearbeiten, den OneNote‑Seitentitel
  ändern und die Seitenhistorie in OneNote mit Aspose.Note für Java löschen.
linktitle: Modify Page History in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Wie man die OneNote‑Seitenhistorie mit Aspose.Note ändert
url: /de/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# So ändern Sie die OneNote‑Seitenhistorie mit Aspose.Note

In diesem Tutorial erfahren Sie **wie Sie OneNote**‑Dokumente programmgesteuert ändern, indem Sie mit der Seitenhistorie arbeiten. Wir zeigen Ihnen, wie Sie eine OneNote‑Datei laden, ihre Historieneinträge bearbeiten, einen Seitentitel ändern und schließlich das aktualisierte Notizbuch speichern – alles mit der Aspose.Note für Java API. Egal, ob Sie alte Revisionen bereinigen oder Seiten umbenennen möchten, die nachfolgenden Schritte bieten Ihnen eine vollständige, produktionsreife Lösung.

## Schnelle Antworten
- **Was bedeutet „Seitenhistorie“ in OneNote?**  
  Es ist die Sammlung vorheriger Seitenversionen, die in einer OneNote‑Datei gespeichert sind.
- **Kann ich einen bestimmten Historieneintrag löschen?**  
  Ja, verwenden Sie die Methoden `removeRange` oder `removeItem` auf dem `PageHistory`‑Objekt.
- **Ist das Ändern eines Seitentitels Teil der Historienmanipulation?**  
  Absolut – jeder Historieneintrag hat seinen eigenen Titel, den Sie ändern können.
- **Benötige ich eine Lizenz, um diesen Code auszuführen?**  
  Eine temporäre Evaluierungslizenz funktioniert für Tests; für die Produktion ist eine Vollversion erforderlich.
- **Welche Java-Version wird unterstützt?**  
  Aspose.Note für Java unterstützt JDK 8 und höher.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Java Development Kit (JDK)** – JDK 8 oder neuer, auf Ihrem Rechner installiert.  
2. **Aspose.Note für Java library** – laden Sie sie von der [download page](https://releases.aspose.com/note/java/).  
3. **Ein Beispiel‑OneNote‑Dokument** – z. B. `Sample1.one`, das Sie sicher ändern können.

## Pakete importieren

Zuerst importieren Sie die Klassen, die Sie benötigen. Der untenstehende Codeblock muss exakt unverändert bleiben.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Laden Sie das OneNote‑Dokument

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### Schritt 2: Das erste Blatt und seine Historie abrufen

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### Schritt 3: Einen Bereich von Historieneinträgen löschen

Wenn Sie **OneNote‑Seitenhistorie**‑Einträge löschen müssen, rufen Sie `removeRange` auf. Das Beispiel entfernt den ersten Eintrag.

```java
pageHistory.removeRange(0, 1);
```

### Schritt 4: Einen Historieneintrag ersetzen

Sie können einen vorhandenen Historieneintrag durch ein neues `Page`‑Objekt ersetzen.

```java
pageHistory.set_Item(0, new Page());
```

### Schritt 5: Den Titel einer Historienseite ändern

Das Ändern des Titels ist eine häufige Anforderung, wenn Sie den **OneNote‑Seitentitel** für eine bestimmte Revision ändern möchten.

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### Schritt 6: Einen neuen Historieneintrag hinzufügen

Fügen Sie der Historien‑Collection eine brandneue Seite hinzu.

```java
pageHistory.addItem(new Page());
```

### Schritt 7: Eine Seite an einer bestimmten Position einfügen

Fügen Sie eine Seite an Index 1 ein, wodurch vorhandene Elemente nach hinten verschoben werden.

```java
pageHistory.insertItem(1, new Page());
```

### Schritt 8: Das geänderte Notizbuch speichern

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## Warum die OneNote‑Seitenhistorie ändern?

- **Versionskontrolle:** Nur relevante Revisionen behalten und störende Entwürfe entfernen.  
- **Konsistenz:** Seitentitel über alle historischen Versionen hinweg angleichen für bessere Navigation.  
- **Performance:** Kleinere Historien‑Sammlungen reduzieren die Dateigröße und verbessern die Ladegeschwindigkeit.

## Häufige Stolperfallen & Tipps

- **Index außerhalb des Bereichs:** Überprüfen Sie stets die Größe der Sammlung, bevor Sie `removeRange` oder `insertItem` aufrufen.  
- **Null‑Titel:** Einige historischen Seiten können keinen Titel haben; prüfen Sie auf `null`, wenn Sie `getTitle()` aufrufen.  
- **Speicherort:** Stellen Sie sicher, dass der Ausgabepfad (`ModifyPageHistory_out.one`) beschreibbar ist; andernfalls wird eine `IOException` ausgelöst.

## Häufig gestellte Fragen

**F: Kann ich Aspose.Note für Java mit anderen Java‑Frameworks verwenden?**  
A: Ja, Aspose.Note für Java ist mit verschiedenen Java‑Frameworks wie Spring, Hibernate usw. kompatibel.

**F: Ist Aspose.Note für Java mit verschiedenen Versionen von OneNote‑Dateien kompatibel?**  
A: Aspose.Note für Java unterstützt die Arbeit mit sowohl alten als auch neuen Versionen von OneNote‑Dateien.

**F: Benötigt Aspose.Note für Java zusätzliche Abhängigkeiten?**  
A: Nein, Aspose.Note für Java ist eine eigenständige Bibliothek und erfordert keine zusätzlichen Abhängigkeiten.

**F: Kann ich Massenänderungen an mehreren OneNote‑Dateien gleichzeitig durchführen?**  
A: Ja, Aspose.Note für Java bietet APIs, um Massenänderungen effizient zu verarbeiten.

**F: Gibt es ein Community‑Forum für Aspose.Note für Java, in dem ich Hilfe erhalten kann?**  
A: Ja, Sie können das [Aspose.Note‑Forum](https://forum.aspose.com/c/note/28) besuchen, um Unterstützung oder Fragen zur Bibliothek zu erhalten.

---

**Zuletzt aktualisiert:** 2026-01-12  
**Getestet mit:** Aspose.Note für Java 24.11 (zum Zeitpunkt der Erstellung aktuell)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}