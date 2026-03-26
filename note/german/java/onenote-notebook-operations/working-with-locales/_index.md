---
date: 2026-01-05
description: Erfahren Sie, wie Sie die Standardsprache festlegen, ein OneNote‑Dokument
  laden, die Aspose‑Lizenz setzen, OneNote in PNG konvertieren und OneNote als Bild
  mit Aspose.Note für Java speichern.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Standard‑Locale in OneNote festlegen – Aspose.Note Java
url: /de/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Standard‑Locale in OneNote festlegen – Aspose.Note Java

## Einführung

Wenn Sie beim Verarbeiten von OneNote‑Dateien **den Standard‑Locale festlegen** müssen, macht Aspose.Note für Java das ganz einfach. In diesem Tutorial führen wir Sie durch alles, was Sie benötigen – von der Lizenzierung des Produkts über das Laden eines OneNote‑Dokuments, das Ändern des Locale bis hin zur Konvertierung der Datei in ein PNG‑Bild. Am Ende können Sie Spracheinstellungen anpassen und locale‑spezifische Ausgaben mit nur wenigen Codezeilen erzeugen.

## Schnellantworten
- **Was bewirkt „Standard‑Locale festlegen“?** Es definiert die Sprache und das regionale Format, das Aspose.Note beim Lesen oder Schreiben von OneNote‑Dateien verwendet.  
- **Benötige ich eine Lizenz?** Ja – setzen Sie die Aspose‑Lizenz, um die volle Funktionalität freizuschalten.  
- **Welche Java‑Version wird benötigt?** Jede JDK 8+ wird unterstützt.  
- **Kann ich OneNote in PNG konvertieren?** Absolut; die API ermöglicht das Speichern von Seiten als Bilder.  
- **Ist der Vorgang thread‑sicher?** Das Festlegen des Standard‑Locale ist global, daher sollte es einmal beim Anwendungsstart konfiguriert werden.

## Was bedeutet „Standard‑Locale festlegen“ in Aspose.Note?
Das Festlegen des Standard‑Locale teilt Aspose.Note mit, welche Sprach‑ und Kulturkonventionen beim Parsen von Datumsangaben, Zahlen und Text anzuwenden sind. Dies ist für multiregionale Anwendungen wichtig, die über verschiedene Benutzer‑Locales hinweg einheitliche Formatierung benötigen.

## Warum das Standard‑Locale beim Arbeiten mit OneNote festlegen?
- **Genaue Datenrepräsentation:** Datums‑ und Zahlenangaben erscheinen korrekt für die Zielgruppe.  
- **Konsistente UI‑Texte:** Aus OneNote extrahierter Text respektiert die Spracheinstellung.  
- **Vereinfachte Konvertierung:** Beim späteren Konvertieren einer OneNote‑Datei zu PNG oder anderen Formaten stimmt das visuelle Layout mit dem erwarteten Locale überein.

## Voraussetzungen

- **Java‑Entwicklungsumgebung:** JDK installiert und `JAVA_HOME` konfiguriert.  
- **Aspose.Note‑Bibliothek:** Laden Sie die neueste JAR von dem [Download-Link](https://releases.aspose.com/note/java/) herunter.  
- **Eine gültige Aspose‑Lizenzdatei** (eine kostenlose Testlizenz funktioniert für Tests).

## Pakete importieren

Bevor Sie Code schreiben, importieren Sie die Klassen, die die benötigte Funktionalität bereitstellen.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Schritt 1: Aspose‑Lizenz setzen

```java
License license = new License();
license.setLicense("licenseFile");
```

Das Setzen der Aspose‑Lizenz schaltet alle Funktionen frei, einschließlich der Locale‑Verarbeitung und Bildkonvertierung.

## Schritt 2: Standard‑Locale festlegen

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

Hier **setzen wir das Standard‑Locale** auf Englisch (`en`) mit dem Ländercode `rs`. Passen Sie die Sprach‑ und Ländercodes an Ihre Zielregion an.

## Schritt 3: OneNote‑Dokument laden

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

Dieser Schritt **lädt das OneNote‑Dokument** in das `Document`‑Objekt, sodass Sie mit dessen Inhalt arbeiten können.

## Schritt 4: OneNote zu PNG konvertieren (OneNote‑Dateikonvertierung)

```java
oneFile.save("sample.png");
```

Die `save`‑Methode führt eine **OneNote‑Dateikonvertierung** durch und exportiert das Notizbuch (oder eine bestimmte Seite) als PNG‑Bild – im Wesentlichen **OneNote in PNG konvertieren** und **OneNote als Bild speichern**.

## Häufige Probleme & Tipps

- **Lizenz nicht gefunden:** Stellen Sie sicher, dass der Pfad zu `licenseFile` korrekt ist und die Datei Leseberechtigungen hat.  
- **Locale nicht angewendet:** Rufen Sie `Locale.setDefault` **vor** dem Laden des Dokuments auf.  
- **Fehlende Bildausgabe:** Prüfen Sie, ob die OneNote‑Datei tatsächlich renderbare Seiten enthält; leere Notizbücher erzeugen ein leeres PNG.

## Häufig gestellte Fragen

**F: Ist Aspose.Note mit verschiedenen Java‑Versionen kompatibel?**  
A: Ja, Aspose.Note unterstützt Java 8 und höher und gewährleistet damit breite Kompatibilität in Entwicklungsumgebungen.

**F: Kann ich Aspose.Note mit anderen Java‑Bibliotheken integrieren?**  
A: Absolut. Die API arbeitet nahtlos mit gängigen Bibliotheken wie Apache POI, Jackson und Spring zusammen.

**F: Bietet Aspose.Note Unterstützung für verschiedene Dateiformate?**  
A: Während der Schwerpunkt auf OneNote‑Dateien liegt, kann die Bibliothek zu PNG, JPEG, PDF und anderen Bildformaten exportieren.

**F: Gibt es ein Community‑Forum für Aspose.Note‑Nutzer, um Hilfe zu erhalten und Wissen zu teilen?**  
A: Ja, das Aspose‑Community‑Forum bietet eine Plattform, auf der Nutzer mit Experten interagieren, Fragen stellen und Lösungen gemeinsam erarbeiten können. Besuchen Sie das [Support-Forum](https://forum.aspose.com/c/note/28) für Unterstützung.

**F: Kann ich Aspose.Note vor dem Kauf testen?**  
A: Natürlich, Sie können die Funktionen von Aspose.Note im Rahmen einer kostenlosen Testversion auf der Website ausprobieren.

## Fazit

Durch Befolgen dieser Schritte haben Sie gelernt, wie man **den Standard‑Locale festlegt**, **ein OneNote‑Dokument lädt**, **die Aspose‑Lizenz setzt** und **OneNote zu PNG konvertiert** mit Aspose.Note für Java. Dieser Workflow ermöglicht Ihnen, locale‑bewusste Berichte und Bilder zu erzeugen, die ein globales Publikum ansprechen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2026-01-05  
**Getestet mit:** Aspose.Note 24.11 für Java  
**Autor:** Aspose  

---