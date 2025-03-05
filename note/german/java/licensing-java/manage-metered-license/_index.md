---
title: Verwalten Sie die gemessene Lizenz für OneNote in Java
linktitle: Verwalten Sie die gemessene Lizenz für OneNote in Java
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie getaktete Lizenzen für OneNote in Java mithilfe der Aspose.Note-Bibliothek verwalten. Steuern Sie die Nutzung, überwachen Sie Guthaben und optimieren Sie Kosten effizient.
type: docs
weight: 10
url: /de/java/licensing-java/manage-metered-license/
---
## Einführung

In diesem Tutorial erfahren Sie, wie Sie mit Aspose.Note für Java eine getaktete Lizenz für OneNote verwalten. Mit der gebührenpflichtigen Lizenzierung können Sie Ihre Nutzung anhand von Credits überwachen und steuern und bieten so eine flexible und kostengünstige Lösung.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1.  Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem System installiert ist. Sie können es herunterladen unter[Hier](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
   
2. Aspose.Note für Java-Bibliothek: Sie benötigen die Aspose.Note für Java-Bibliothek. Sie können es hier herunterladen[Webseite](https://releases.aspose.com/note/java/).

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt:

```java
import com.aspose.note.Document;
import com.aspose.note.Metered;



import java.nio.file.Paths;
```

## Schritt 1: Metered-Lizenz einrichten

```java
Metered metered = new Metered();
metered.setMeteredKey("MyPublicKey", "MyPrivateKey");
```

 In diesem Schritt initialisieren wir die`Metered` Klasse und legen Sie den gemessenen Schlüssel mit Ihren von Aspose bereitgestellten öffentlichen und privaten Schlüsseln fest.

## Schritt 2: Dokument laden und Vorgänge ausführen

```java
String dataDir = "Your Document Directory";
Document doc = new Document(Paths.get(dataDir,"Sample1.one").toString());
doc.save(Paths.get(dataDir,"MeteredLicense.pdf").toString());
```

 Hier laden wir das OneNote-Dokument aus dem angegebenen Verzeichnis und speichern es als PDF-Datei. Stellen Sie sicher, dass Sie es ersetzen`"Your Document Directory"` mit Ihrem tatsächlichen Verzeichnispfad.

## Schritt 3: Verbrauch prüfen

```java
System.out.println(String.format("Credit before operation: %.02f", Metered.getConsumptionCredit()));
System.out.println(String.format("Consumption quantity before operation: %.02f", Metered.getConsumptionQuantity()));
```

Dieser Schritt ruft das Guthaben und die Verbrauchsmenge vor und nach dem Vorgang ab und druckt sie aus.

## Abschluss

In diesem Tutorial haben wir gelernt, wie man mithilfe der Aspose.Note-Bibliothek eine getaktete Lizenz für OneNote in Java verwaltet. Die gebührenpflichtige Lizenzierung bietet Flexibilität und Kontrolle über Ihre Nutzung und sorgt so für Kosteneffizienz und effizientes Ressourcenmanagement.

## FAQs

### F1: Was ist eine gebührenpflichtige Lizenz?

A1: Mit einer gebührenpflichtigen Lizenz können Sie Ihre Nutzung einer API oder eines Dienstes auf der Grundlage von Credits überwachen und steuern.
   
### F2: Wie erhalte ich einen kostenpflichtigen Schlüssel für Aspose-Produkte?

A2: Sie können einen gemessenen Schlüssel erhalten, indem Sie eine Lizenz auf der Aspose-Website erwerben oder eine temporäre Lizenz zu Testzwecken anfordern.
   
### F3: Kann ich eine getaktete Lizenz für mehrere Anwendungen verwenden?

A3: Ja, eine gemessene Lizenz kann über mehrere Anwendungen hinweg verwendet werden, der Verbrauch wird jedoch aggregiert.
   
### F4: Gibt es eine kostenlose Testversion für Aspose.Note für Java?

 A4: Ja, Sie können eine kostenlose Testversion herunterladen[Hier](https://releases.aspose.com/).
   
### F5: Wo erhalte ich Unterstützung für Aspose.Note für Java?

 A5: Sie können Unterstützung in den Aspose-Community-Foren erhalten[Hier](https://forum.aspose.com/c/note/28).