---
title: Erstellen Sie ein Dokument und fügen Sie ein Bild in Aspose.Note ein
linktitle: Erstellen Sie ein Dokument und fügen Sie ein Bild in Aspose.Note ein
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie mit Aspose.Note für .NET Bilder programmgesteuert in OneNote-Dokumente einfügen. Einfache Schritte für eine nahtlose Dokumentenbearbeitung.
type: docs
weight: 10
url: /de/net/images/build-doc-insert-image/
---
## Einführung

In diesem Tutorial tauchen wir in die Welt der Dokumentbearbeitung mit Aspose.Note für .NET ein. Aspose.Note ist eine leistungsstarke API, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten und so Aufgaben wie das einfache Erstellen, Ändern und Konvertieren von Dokumenten zu ermöglichen. 

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Visual Studio: Stellen Sie sicher, dass Visual Studio auf Ihrem System installiert ist. Aspose.Note für .NET arbeitet nahtlos mit Visual Studio zusammen und bietet eine robuste Entwicklungsumgebung.

2.  Aspose.Note für .NET: Laden Sie Aspose.Note für .NET herunter und installieren Sie es. Den Download-Link finden Sie hier[Hier](https://releases.aspose.com/note/net/).

3. Grundlegendes Verständnis von C#: Machen Sie sich mit den Grundlagen der Programmiersprache C# vertraut. Während dieses Tutorial eine Schritt-für-Schritt-Anleitung bietet, sind grundlegende Kenntnisse in C# von Vorteil.

## Namespaces importieren

Beginnen wir mit dem Importieren der erforderlichen Namespaces in Ihr C#-Projekt. Diese Namespaces enthalten Klassen und Methoden, die wir zur Durchführung von Dokumentenmanipulationsaufgaben verwenden.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Lassen Sie uns nun den Prozess des Erstellens eines Dokuments und des Einfügens eines Bilds in mehrere Schritte unterteilen:

## Schritt 1: Dokumentobjekt erstellen

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document();
```

 Diese Codezeile initialisiert eine neue Instanz von`Document` Klasse, die ein OneNote-Dokument darstellt.

## Schritt 2: Seitenobjekt initialisieren

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

 Hier initialisieren wir eine neue Instanz von`Page` Klasse, die eine Seite innerhalb des OneNote-Dokuments darstellt.

## Schritt 3: Gliederungsobjekt initialisieren

```csharp
Outline outline = new Outline(doc);
```

 Der`Outline`Die Klasse stellt einen Gliederungsknoten in der Dokumenthierarchie dar. Wir erstellen ein neues Gliederungsobjekt, um unser Dokument zu strukturieren.

## Schritt 4: OutlineElement-Objekt initialisieren

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

 Ein`OutlineElement` stellt ein Element innerhalb einer Gliederung dar. Hier erstellen wir ein neues Gliederungselement, um unserem Dokument Inhalt hinzuzufügen.

## Schritt 5: Bild laden

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg");
```

 Wir laden eine Bilddatei aus dem angegebenen Pfad mit`Image` Klassenkonstruktor.

## Schritt 6: Bildausrichtung festlegen

```csharp
image.Alignment = HorizontalAlignment.Right;
```

Diese Codezeile legt die Ausrichtung des Bildes innerhalb des Dokuments fest. In diesem Beispiel richten wir das Bild rechts aus.

## Schritt 7: Bild zum Gliederungselement hinzufügen

```csharp
outlineElem.AppendChildLast(image);
```

Hier fügen wir das Bild dem Gliederungselement hinzu und platzieren es innerhalb der Dokumentstruktur.

## Schritt 8: Gliederungselement zur Gliederung hinzufügen

```csharp
outline.AppendChildLast(outlineElem);
```

Wir fügen das Gliederungselement zusammen mit dem eingefügten Bild zur Gliederungsstruktur des Dokuments hinzu.

## Schritt 9: Gliederung zur Seite hinzufügen

```csharp
page.AppendChildLast(outline);
```

Die Gliederung, die das Bild enthält, wird zur Seitenstruktur des Dokuments hinzugefügt.

## Schritt 10: Seite zum Dokument hinzufügen

```csharp
doc.AppendChildLast(page);
```

Abschließend fügen wir die Seite mit ihrem Inhalt dem Dokument hinzu.

## Schritt 11: Dokument speichern

```csharp
dataDir = dataDir + "BuildDocAndInsertImage_out.one";
doc.Save(dataDir);
```

Diese Zeile speichert das geänderte Dokument am angegebenen Speicherort.

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.Note für .NET ein Dokument erstellen und ein Bild einfügen. Mit diesem neu gewonnenen Wissen können Sie weiter forschen und komplexere Dokumentenmanipulationsaufgaben implementieren.

## FAQs

### F1: Kann ich mit Aspose.Note für .NET mehrere Bilder in ein einzelnes Dokument einfügen?

A1: Auf jeden Fall! Sie können beliebig viele Bilder in ein Dokument einfügen, indem Sie für jedes Bild ähnliche Schritte ausführen.

### F2: Unterstützt Aspose.Note neben OneNote auch andere Dateiformate?

A2: Ja, Aspose.Note bietet umfassende Unterstützung für verschiedene Dateiformate, darunter PDF, DOCX, HTML und mehr.

### F3: Ist Aspose.Note für Dokumentenmanagementlösungen auf Unternehmensebene geeignet?

A3: Auf jeden Fall! Aspose.Note bietet robuste Funktionen und hervorragende Leistung und ist damit die ideale Wahl für die Dokumentenverwaltung in Unternehmen.

### F4: Kann ich das Erscheinungsbild eingefügter Bilder im Dokument anpassen?

A4: Ja, Aspose.Note bietet umfassende Optionen zum Anpassen der Bilddarstellung, einschließlich Ausrichtung, Größe und Drehung.

### F5: Wo finde ich zusätzliche Ressourcen und Unterstützung für Aspose.Note für .NET?

 A5: Sie können die Aspose.Note-Dokumentation durchsuchen[Hier](https://reference.aspose.com/note/net/) und bitten Sie das Aspose-Community-Forum um Hilfe[Hier](https://forum.aspose.com/c/note/28).