---
title: Utwórz dokument z tytułem strony w Aspose.Note
linktitle: Utwórz dokument z tytułem strony w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak tworzyć dokumenty ze stronami tytułowymi przy użyciu Aspose.Note dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby zapewnić bezproblemową integrację.
type: docs
weight: 13
url: /pl/net/loading-and-saving-operations/create-doc-with-page-title/
---
## Wstęp

W tym samouczku przeprowadzimy Cię przez proces tworzenia dokumentu ze stroną zatytułowaną przy użyciu Aspose.Note dla .NET. Aspose.Note to potężny interfejs API, który umożliwia programistom programową pracę z plikami Microsoft OneNote.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz zainstalowane i skonfigurowane następujące wymagania wstępne:

### Instalacja Visual Studio

1. Pobierz Visual Studio: Jeśli jeszcze tego nie zrobiłeś, pobierz i zainstaluj Visual Studio z witryny Microsoft.

2. Zainstaluj obciążenie programistyczne .NET: podczas procesu instalacji wybierz obciążenie „programowanie .NET desktop”, aby upewnić się, że masz wszystkie niezbędne komponenty do programowania .NET.

3. Utwórz nowy projekt: Otwórz Visual Studio i utwórz nowy projekt (aplikacja konsolowa lub dowolny inny preferowany typ).

### Instalacja Aspose.Note

1.  Pobierz Aspose.Note: Pobierz bibliotekę Aspose.Note dla .NET z[strona internetowa](https://releases.aspose.com/note/net/).

2. Zainstaluj Aspose.Note przez NuGet: Alternatywnie możesz zainstalować Aspose.Note dla .NET poprzez Menedżera pakietów NuGet w Visual Studio. Po prostu wyszukaj „Aspose.Note” i zainstaluj najnowszą wersję.

## Importowanie przestrzeni nazw

Najpierw musisz zaimportować niezbędne przestrzenie nazw, aby móc używać Aspose.Note w swoim projekcie.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

Podzielmy teraz proces tworzenia dokumentu z tytułem strony na kilka kroków:

## Krok 1: Utwórz obiekt dokumentu

```csharp
//Utwórz obiekt klasy Dokument
Document doc = new Aspose.Note.Document();
```

## Krok 2: Zainicjuj obiekt klasy strony

```csharp
// Zainicjuj obiekt klasy Page
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Krok 3: Ustaw domyślny styl tekstu

```csharp
// Domyślny styl całego tekstu w dokumencie.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## Krok 4: Ustaw właściwości tytułu strony

```csharp
// Ustaw właściwości tytułu strony
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## Krok 5: Dołącz węzeł strony do dokumentu

```csharp
// Dołącz węzeł strony w dokumencie
doc.AppendChildLast(page);
```

## Krok 6: Zapisz dokument OneNote

```csharp
// Zapisz dokument programu OneNote
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## Wniosek

Gratulacje! Pomyślnie utworzyłeś dokument ze stroną zatytułowaną przy użyciu Aspose.Note dla .NET. Ten samouczek zawiera przewodnik krok po kroku, który pomoże Ci zintegrować Aspose.Note z aplikacjami .NET w celu programowego zarządzania plikami OneNote.

## Często zadawane pytania

### P1: Czy mogę dostosować styl tekstu tytułu?

O1: Tak, możesz dostosować kolor czcionki, nazwę czcionki i rozmiar czcionki tekstu tytułowego zgodnie ze swoimi wymaganiami.

### P2: Czy Aspose.Note jest kompatybilny z .NET Core?

Odpowiedź 2: Tak, Aspose.Note obsługuje .NET Core, umożliwiając tworzenie aplikacji wieloplatformowych.

### P3: Czy mogę dodać obrazy i załączniki do dokumentu?

A3: Absolutnie! Aspose.Note udostępnia interfejsy API umożliwiające płynne dodawanie obrazów, załączników i innych elementów do dokumentów programu OneNote.

### P4: Czy Aspose.Note obsługuje odczytywanie istniejących plików OneNote?

O4: Tak, możesz używać Aspose.Note do łatwego czytania, modyfikowania i manipulowania istniejącymi plikami OneNote.

### P5: Gdzie mogę znaleźć pomoc, jeśli napotkam jakiekolwiek problemy?

 Odpowiedź 5: Możesz znaleźć wsparcie i pomoc na stronie[Forum Aspose.Note](https://forum.aspose.com/c/note/28), gdzie eksperci i członkowie społeczności mogą odpowiedzieć na Twoje pytania.