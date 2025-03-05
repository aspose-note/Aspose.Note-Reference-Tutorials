---
title: Erstellen Sie ein Dokument mit Seitentitel in Aspose.Note
linktitle: Erstellen Sie ein Dokument mit Seitentitel in Aspose.Note
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie mit Aspose.Note für .NET Dokumente mit Titelseiten erstellen. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Integration.
type: docs
weight: 13
url: /de/net/loading-and-saving-operations/create-doc-with-page-title/
---
## Einführung

In diesem Tutorial führen wir Sie durch den Prozess der Erstellung eines Dokuments mit einer Titelseite mit Aspose.Note für .NET. Aspose.Note ist eine leistungsstarke API, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen installiert und eingerichtet haben:

### Visual Studio-Installation

1. Laden Sie Visual Studio herunter: Falls Sie es noch nicht getan haben, laden Sie Visual Studio von der Microsoft-Website herunter und installieren Sie es.

2. .NET-Entwicklungs-Workload installieren: Stellen Sie während des Installationsvorgangs sicher, dass Sie den Workload „.NET-Desktop-Entwicklung“ auswählen, um sicherzustellen, dass Sie über alle erforderlichen Komponenten für die .NET-Entwicklung verfügen.

3. Erstellen Sie ein neues Projekt: Öffnen Sie Visual Studio und erstellen Sie ein neues Projekt (Konsolenanwendung oder einen anderen von Ihnen bevorzugten Typ).

### Aspose.Note-Installation

1.  Holen Sie sich Aspose.Note: Laden Sie die Aspose.Note für .NET-Bibliothek von herunter[Webseite](https://releases.aspose.com/note/net/).

2. Aspose.Note über NuGet installieren: Alternativ können Sie Aspose.Note für .NET über den NuGet Package Manager in Visual Studio installieren. Suchen Sie einfach nach „Aspose.Note“ und installieren Sie die neueste Version.

## Namespaces importieren

Zunächst müssen Sie die erforderlichen Namespaces importieren, um Aspose.Note in Ihrem Projekt verwenden zu können.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

Lassen Sie uns nun den Prozess der Erstellung eines Dokuments mit einem Seitentitel in mehrere Schritte unterteilen:

## Schritt 1: Erstellen Sie ein Dokumentobjekt

```csharp
//Erstellen Sie ein Objekt der Document-Klasse
Document doc = new Aspose.Note.Document();
```

## Schritt 2: Seitenklassenobjekt initialisieren

```csharp
// Initialisieren Sie das Page-Klassenobjekt
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Schritt 3: Legen Sie den Standardstil für Text fest

```csharp
// Standardstil für den gesamten Text im Dokument.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## Schritt 4: Seitentiteleigenschaften festlegen

```csharp
// Legen Sie die Eigenschaften des Seitentitels fest
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## Schritt 5: Seitenknoten im Dokument anhängen

```csharp
// Knoten „Seite“ im Dokument anhängen
doc.AppendChildLast(page);
```

## Schritt 6: OneNote-Dokument speichern

```csharp
// OneNote-Dokument speichern
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## Abschluss

Glückwunsch! Sie haben mit Aspose.Note für .NET erfolgreich ein Dokument mit einer Titelseite erstellt. Dieses Tutorial bietet eine Schritt-für-Schritt-Anleitung, die Ihnen bei der Integration von Aspose.Note in Ihre .NET-Anwendungen hilft, um OneNote-Dateien programmgesteuert zu verwalten.

## FAQs

### F1: Kann ich den Titeltextstil anpassen?

A1: Ja, Sie können die Schriftfarbe, den Schriftnamen und die Schriftgröße des Titeltexts Ihren Anforderungen entsprechend anpassen.

### F2: Ist Aspose.Note mit .NET Core kompatibel?

A2: Ja, Aspose.Note unterstützt .NET Core, sodass Sie plattformübergreifende Anwendungen entwickeln können.

### F3: Kann ich dem Dokument Bilder und Anhänge hinzufügen?

A3: Auf jeden Fall! Aspose.Note bietet APIs zum nahtlosen Hinzufügen von Bildern, Anhängen und anderen Elementen zu Ihren OneNote-Dokumenten.

### F4: Unterstützt Aspose.Note das Lesen vorhandener OneNote-Dateien?

A4: Ja, Sie können Aspose.Note verwenden, um vorhandene OneNote-Dateien problemlos zu lesen, zu ändern und zu bearbeiten.

### F5: Wo finde ich Unterstützung, wenn ich auf Probleme stoße?

 A5: Unterstützung und Hilfe finden Sie auf der[Aspose.Note-Forum](https://forum.aspose.com/c/note/28), wo Experten und Community-Mitglieder Ihnen bei Ihren Fragen helfen können.