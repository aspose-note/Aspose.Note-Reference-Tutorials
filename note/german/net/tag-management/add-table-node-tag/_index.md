---
title: Tabellenknoten mit Tag in Aspose.Note hinzufügen
linktitle: Tabellenknoten mit Tag in Aspose.Note hinzufügen
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie Tabellen mit Tags in Aspose.Note für .NET hinzufügen. Verbessern Sie Ihre Fähigkeiten zur Dokumentenbearbeitung programmgesteuert.
weight: 11
url: /de/net/tag-management/add-table-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tabellenknoten mit Tag in Aspose.Note hinzufügen

## Einführung

In diesem Tutorial führen wir Sie durch den Prozess des Hinzufügens eines Tabellenknotens mit einem Tag mithilfe von Aspose.Note für .NET. Befolgen Sie die folgenden Schritte, um dies zu erreichen.

## Namespaces importieren

Bevor Sie beginnen, stellen Sie sicher, dass Sie die erforderlichen Namespaces importieren, um mit Aspose zu arbeiten.Hinweis:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Voraussetzungen

Stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind, bevor Sie fortfahren:

1.  Installation: Laden Sie die Aspose.Note für .NET-Bibliothek herunter und installieren Sie sie von[Hier](https://releases.aspose.com/note/net/).
2.  Lizenz: Erwerben Sie eine Lizenz oder nutzen Sie eine[temporäre Lizenz](https://purchase.aspose.com/temporary-license/) die Bibliothek zu nutzen.
3. Entwicklungsumgebung: Richten Sie eine kompatible Entwicklungsumgebung ein, z. B. Visual Studio.

## Schritt 1: Dokument- und Seitenobjekte initialisieren

 Beginnen Sie mit der Erstellung einer Instanz von`Document` Klasse und Initialisierung von a`Page` Objekt:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Schritt 2: Erstellen Sie Tabellen-, Zeilen- und Zellenobjekte

 Initialisieren Sie die`Table`, `TableRow` , Und`TableCell` Objekte:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## Schritt 3: Inhalt in die Zelle einfügen

 Fügen Sie der Zelle Inhalt hinzu, indem Sie verwenden`AppendChildLast` Methode:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## Schritt 4: Tabellenknoten initialisieren

 Initialisieren Sie die`Table` Objekt mit angegebenen Eigenschaften:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## Schritt 5: Zeile zur Tabelle hinzufügen

Fügen Sie den Zeilenknoten zur Tabelle hinzu:

```csharp
table.AppendChildLast(row);
```

## Schritt 6: Tag zum Tabellenknoten hinzufügen

Fügen Sie ein Tag für den Tabellenknoten ein:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## Schritt 7: Tabellenknoten zum Gliederungselement hinzufügen

 Erstelle ein`Outline` Und`OutlineElement` So fügen Sie den Tabellenknoten hinzu:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Schritt 8: Dokument speichern

Speichern Sie das OneNote-Dokument:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

Nachdem Sie diese Schritte ausgeführt haben, sollten Sie mit Aspose.Note für .NET erfolgreich einen Tabellenknoten mit einem Tag hinzugefügt haben.

## Abschluss

In diesem Tutorial haben wir den Prozess des Hinzufügens eines Tabellenknotens mit einem Tag in Aspose.Note für .NET behandelt. Wenn Sie diese Schritte befolgen, können Sie OneNote-Dokumente effizient programmgesteuert bearbeiten und so Ihre Dokumentverwaltungsfunktionen verbessern.

## FAQs

### F1: Ist Aspose.Note mit allen Versionen von .NET kompatibel?

A1: Aspose.Note für .NET unterstützt .NET Framework-Versionen 2.0 und höher, einschließlich .NET Core und .NET Standard.

### F2: Kann ich Aspose.Note testen, bevor ich eine Lizenz kaufe?

 A2: Ja, Sie können eine kostenlose Testversion von Aspose.Note unter erhalten[Hier](https://releases.aspose.com/).

### F3: Wie erhalte ich eine temporäre Lizenz für Aspose.Note?

 A3: Sie können eine temporäre Lizenz erhalten von[dieser Link](https://purchase.aspose.com/temporary-license/), die 30 Tage gültig ist.

### F4: Unterstützt Aspose.Note die Dokumentenverschlüsselung?

A4: Ja, Aspose.Note bietet Unterstützung für die Verschlüsselung von OneNote-Dokumenten, um die Datensicherheit zu gewährleisten.

### F5: Ist technischer Support für Aspose.Note-Benutzer verfügbar?

 A5: Ja, technischer Support wird über die Aspose-Foren bereitgestellt[Hier](https://forum.aspose.com/c/note/28), wo Sie Hilfe von Experten erhalten können.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
