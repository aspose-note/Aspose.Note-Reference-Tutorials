---
date: 2026-04-06
description: Erfahren Sie, wie Sie ein OneNote‑Dokument erstellen und ein Bild programmgesteuert
  mit Aspose.Note für .NET einfügen. Befolgen Sie einfache Schritte, um Bilder hinzuzufügen,
  die Ausrichtung festzulegen und mehr.
keywords:
- create onenote document
- how to insert image
- insert image onenote
- set image alignment
- multiple images onenote
linktitle: Dokument erstellen und Bild in Aspose.Note einfügen
second_title: Aspose.Note .NET API
title: OneNote-Dokument erstellen und Bild mit Aspose.Note einfügen
url: /de/net/images/build-doc-insert-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote-Dokument erstellen und Bild mit Aspose.Note einfügen

## Einführung

In diesem Tutorial **erstellen Sie ein OneNote-Dokument** und lernen **wie man ein Bild** darin mit Aspose.Note für .NET einfügt. Aspose.Note gibt Ihnen die volle Kontrolle über OneNote-Dateien und erleichtert das programmgesteuerte Hinzufügen von reichhaltigem Inhalt wie Bildern, Tabellen und benutzerdefinierten Layouts.

## Schnelle Antworten
- **Was ist der Hauptzweck?** Ein OneNote-Dokument zu erstellen und ein Bild mit benutzerdefinierter Ausrichtung einzufügen.  
- **Welche Bibliothek wird benötigt?** Aspose.Note für .NET (Download [hier](https://releases.aspose.com/note/net/)).  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine kostenpflichtige Lizenz erforderlich.  
- **Kann ich mehrere Bilder hinzufügen?** Ja – wiederholen Sie die Einfügeschritte für jedes Bild (siehe Tipp „multiple images onenote“).  
- **Wird die PDF-Konvertierung unterstützt?** Absolut – Sie können das OneNote-Dokument später mit der `Save`‑Methode von Aspose.Note im PDF‑Format in PDF konvertieren.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. **Visual Studio** – eine voll ausgestattete IDE für .NET‑Entwicklung.  
2. **Aspose.Note für .NET** – laden Sie die Bibliothek von der offiziellen Website herunter und installieren Sie sie.  
3. **Grundlegendes Verständnis von C#** – Vertrautheit mit der C#‑Syntax hilft Ihnen, den Codebeispielen zu folgen.

## Namespaces importieren

Beginnen wir damit, die erforderlichen Namespaces in Ihr C#‑Projekt zu importieren. Diese Namespaces enthalten Klassen und Methoden, die wir für die Dokumentmanipulation verwenden.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Nun zerlegen wir den Prozess des Erstellens eines Dokuments und Einfügens eines Bildes in mehrere Schritte:

## Schritt 1: Dokumentobjekt erstellen

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document();
```

Diese Codezeile initialisiert eine neue Instanz der `Document`‑Klasse, die ein OneNote-Dokument repräsentiert.

## Schritt 2: Seitenobjekt initialisieren

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

Hier initialisieren wir eine neue Instanz der `Page`‑Klasse, die eine Seite im OneNote-Dokument darstellt.

## Schritt 3: Outline‑Objekt initialisieren

```csharp
Outline outline = new Outline(doc);
```

Die `Outline`‑Klasse repräsentiert einen Gliederungsknoten in der Dokumenthierarchie. Wir erstellen ein neues Outline‑Objekt, um unser Dokument zu strukturieren.

## Schritt 4: OutlineElement‑Objekt initialisieren

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

`OutlineElement` stellt ein Element innerhalb einer Gliederung dar. Hier erstellen wir ein neues OutlineElement, um Inhalt zu unserem Dokument hinzuzufügen.

## Schritt 5: Bild laden

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg");
```

Wir laden eine Bilddatei vom angegebenen Pfad mit dem Konstruktor der `Image`‑Klasse.

## Schritt 6: Bildausrichtung festlegen

```csharp
image.Alignment = HorizontalAlignment.Right;
```

Diese Zeile legt die **Bildausrichtung** auf die rechte Seite der Seite fest. Sie können je nach Layoutbedarf auch `Left` oder `Center` wählen.

## Schritt 7: Bild zum Outline‑Element hinzufügen

```csharp
outlineElem.AppendChildLast(image);
```

Hier fügen wir das Bild dem Outline‑Element hinzu und platzieren es innerhalb der Dokumentstruktur.

## Schritt 8: Outline‑Element zum Outline hinzufügen

```csharp
outline.AppendChildLast(outlineElem);
```

Wir fügen das Outline‑Element zusammen mit dem eingefügten Bild zur Outline‑Struktur des Dokuments hinzu.

## Schritt 9: Outline zur Seite hinzufügen

```csharp
page.AppendChildLast(outline);
```

Das Outline, das das Bild enthält, wird zur Seitenstruktur des Dokuments hinzugefügt.

## Schritt 10: Seite zum Dokument hinzufügen

```csharp
doc.AppendChildLast(page);
```

Schließlich fügen wir die Seite mit ihrem gesamten Inhalt dem Dokument hinzu.

## Schritt 11: Dokument speichern

```csharp
dataDir = dataDir + "BuildDocAndInsertImage_out.one";
doc.Save(dataDir);
```

Diese Zeile speichert das modifizierte OneNote-Dokument am angegebenen Ort. Sie können später **OneNote in PDF konvertieren**, indem Sie `doc.Save("output.pdf")` aufrufen.

## Warum das wichtig ist

- **Automatisierung** – Das programmgesteuerte Erstellen von OneNote-Dokumenten spart Zeit im Vergleich zur manuellen Bearbeitung.  
- **Konsistenz** – Durch Code wird sichergestellt, dass jedes Dokument dieselben Layout‑ und Stilregeln einhält.  
- **Skalierbarkeit** – Der gleiche Ansatz kann erweitert werden, um **multiple images onenote**‑Dokumente einzufügen oder Berichte massenhaft zu erzeugen.

## Häufige Fallstricke & Tipps

- **Pfadprobleme** – Stellen Sie immer sicher, dass `dataDir` auf einen gültigen Ordner verweist; andernfalls schlägt das Laden des Bildes fehl.  
- **Bildgröße** – Große Bilder können die Dateigröße stark erhöhen; erwägen Sie eine Größenanpassung vor dem Einfügen.  
- **Mehrere Bilder** – Um mehr als ein Bild hinzuzufügen, wiederholen Sie die Schritte 5‑7 für jedes Bild und hängen Sie jedes an dasselbe oder ein anderes `OutlineElement` an.

## Häufig gestellte Fragen

### Q1: Kann ich mehrere Bilder in ein einzelnes Dokument mit Aspose.Note für .NET einfügen?

A1: Absolut! Sie können beliebig viele Bilder in ein Dokument einfügen, indem Sie für jedes Bild dieselben Einfügeschritte befolgen.

### Q2: Unterstützt Aspose.Note andere Dateiformate neben OneNote?

A2: Ja, Aspose.Note bietet umfangreiche Unterstützung für verschiedene Dateiformate, darunter PDF, DOCX, HTML und mehr.

### Q3: Ist Aspose.Note für Enterprise‑Document‑Management‑Lösungen geeignet?

A3: Sicherlich! Aspose.Note bietet robuste Funktionen und hervorragende Leistung, wodurch es eine ideale Wahl für das Dokumentenmanagement im Unternehmen ist.

### Q4: Kann ich das Aussehen der eingefügten Bilder im Dokument anpassen?

A4: Ja, Aspose.Note bietet umfassende Optionen zur Anpassung des Bildaussehens, einschließlich Ausrichtung, Größe und Drehung.

### Q5: Wo finde ich zusätzliche Ressourcen und Unterstützung für Aspose.Note für .NET?

A5: Sie können die Aspose.Note‑Dokumentation [hier](https://reference.aspose.com/note/net/) durchsuchen und Unterstützung im Aspose‑Community‑Forum [hier](https://forum.aspose.com/c/note/28/) erhalten.

---

**Zuletzt aktualisiert:** 2026-04-06  
**Getestet mit:** Aspose.Note 24.11 für .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}