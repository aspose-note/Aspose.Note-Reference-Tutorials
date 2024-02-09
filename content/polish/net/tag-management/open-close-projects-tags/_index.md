---
title: Otwieraj i zamykaj projekty za pomocą tagów w Aspose.Note
linktitle: Otwieraj i zamykaj projekty za pomocą tagów w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak programowo manipulować plikami Microsoft OneNote przy użyciu Aspose.Note dla .NET. Efektywnie otwieraj i zamykaj projekty za pomocą tagów.
type: docs
weight: 15
url: /pl/net/tag-management/open-close-projects-tags/
---
## Wstęp

W tym samouczku nauczymy się używać Aspose.Note dla .NET do otwierania i zamykania projektów za pomocą tagów. Aspose.Note to potężny interfejs API, który umożliwia programistom programową pracę z plikami Microsoft OneNote, umożliwiając wykonywanie takich zadań, jak manipulowanie tekstem, obrazami i znacznikami w dokumentach.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz skonfigurowane następujące wymagania wstępne:

## Importuj przestrzenie nazw

```csharp
using System.IO;
using System.Linq;
```

Podzielmy teraz każdy przykład na wiele kroków:

## Krok 1: Załaduj dokument

Najpierw musimy załadować dokument do Aspose.Note.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Krok 2: Zamknij elementy projektu C

Teraz zamknijmy wszystkie pola wyboru związane z „Projektem C”.

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Krok 3: Zapisz notatki zamkniętego projektu C

Zapisz zmodyfikowany dokument z zamkniętymi elementami „Projektu C”.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Krok 4: Otwórz elementy projektu C

Następnie otwórzmy wszystkie pola wyboru związane z „Projektem C”.

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Krok 5: Zapisz notatki dotyczące otwartego projektu C

Zapisz zmodyfikowany dokument z otwartymi elementami „Projektu C”.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Teraz nauczyłeś się otwierać i zamykać projekty ze znacznikami w Aspose.Note przy użyciu .NET.

## Wniosek

Aspose.Note dla .NET zapewnia wygodny sposób programowego manipulowania dokumentami OneNote. Postępując zgodnie z tym samouczkiem, możesz efektywnie zarządzać swoimi projektami, otwierając i zamykając elementy za pomocą tagów.

## Często zadawane pytania

### P1: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami OneNote?

O1: Aspose.Note obsługuje Microsoft OneNote 2010 i nowsze wersje.

### P2: Czy mogę używać Aspose.Note do projektów komercyjnych?

 Odpowiedź 2: Tak, możesz używać Aspose.Note zarówno do projektów osobistych, jak i komercyjnych. Odwiedzać[Tutaj](https://purchase.aspose.com/buy) do zakupu licencji.

### P3: Czy Aspose.Note oferuje bezpłatną wersję próbną?

A3: Tak, możesz uzyskać bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę znaleźć dokumentację dla Aspose.Note?

 A4: Możesz znaleźć dokumentację[Tutaj](https://reference.aspose.com/note/net/).

### P5: Gdzie mogę uzyskać wsparcie dla Aspose.Note?

O5: Aby uzyskać pomoc, możesz odwiedzić stronę Aspose.Note[forum](https://forum.aspose.com/c/note/28).