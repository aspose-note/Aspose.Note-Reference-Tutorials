---
title: Konwertuj określoną stronę na obraz w Aspose.Note
linktitle: Konwertuj określoną stronę na obraz w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak programowo konwertować określone strony dokumentów Microsoft OneNote na obrazy za pomocą Aspose.Note dla .NET.
type: docs
weight: 11
url: /pl/net/loading-and-saving-operations/convert-specific-page-to-image/
---
## Wstęp

Aspose.Note dla .NET to potężny interfejs API, który umożliwia programistom programową pracę z dokumentami Microsoft OneNote. Niezależnie od tego, czy chcesz wyodrębnić zawartość, przekonwertować dokumenty do innych formatów, czy manipulować elementami w pliku OneNote, Aspose.Note dla .NET zapewnia wszechstronną funkcjonalność usprawniającą Twoje zadania. W tym samouczku omówimy, jak wykorzystać Aspose.Note dla .NET do konwersji określonych stron dokumentu OneNote na obrazy. Omówimy wymagania wstępne, zaimportujemy przestrzenie nazw i zapewnimy wskazówki krok po kroku dotyczące wdrażania procesu konwersji.

## Warunki wstępne

Zanim zagłębimy się w używanie Aspose.Note dla .NET do konwersji stron OneNote na obrazy, upewnij się, że masz następujące elementy:

- Visual Studio: Upewnij się, że masz zainstalowany program Visual Studio w swoim systemie.
-  Aspose.Note dla .NET: Pobierz i zainstaluj Aspose.Note dla .NET z[Tutaj](https://releases.aspose.com/note/net/).
- Microsoft OneNote: Aby tworzyć lub uzyskiwać dokumenty OneNote, musisz mieć zainstalowany program OneNote w swoim systemie.

## Importuj przestrzenie nazw

W projekcie C# zaimportuj niezbędne przestrzenie nazw, aby uzyskać dostęp do klas i metod Aspose.Note dla .NET.

```csharp
using System;
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
```

## Konwertuj określoną stronę na obraz

Przeanalizujmy teraz proces konwertowania określonej strony dokumentu OneNote na obraz za pomocą Aspose.Note dla .NET.

### Krok 1: Załaduj dokument

```csharp
string dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

### Krok 2: Zainicjuj opcje ImageSaveOptions

```csharp
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png)
{
    PageIndex = 1 // Ustaw indeks strony do konwersji
};
```

### Krok 3: Zapisz dokument jako PNG

```csharp
dataDir = dataDir + "ConvertSpecificPageToImage_out.png";
oneFile.Save(dataDir, opts);
```

## Ustaw rozdzielczość obrazu wyjściowego

Można także ustawić rozdzielczość obrazu wyjściowego podczas zapisywania dokumentu jako obrazu.

### Krok 1: Załaduj dokument

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

### Krok 2: Ustaw rozdzielczość obrazu wyjściowego

```csharp
dataDir = dataDir + "SetOutputImageResolution_out.jpg";
doc.Save(dataDir, new ImageSaveOptions(SaveFormat.Jpeg) { Resolution = 220 });
```

## Wniosek

Aspose.Note dla .NET upraszcza zadanie programowej konwersji określonych stron dokumentów OneNote na obrazy. Wykonując kroki opisane w tym samouczku, możesz skutecznie zintegrować tę funkcję z aplikacjami .NET, zwiększając produktywność i poszerzając możliwości dzięki plikom OneNote.

## Często zadawane pytania

### P1: Czy mogę przekonwertować wiele stron jednocześnie za pomocą Aspose.Note dla .NET?

Odpowiedź 1: Tak, możesz przeglądać strony w pętli i konwertować je indywidualnie lub zbiorczo.

### P2: Czy Aspose.Note dla .NET obsługuje inne formaty wyjściowe oprócz PNG i JPEG?

O2: Tak, Aspose.Note dla .NET obsługuje różne formaty wyjściowe do konwersji obrazów.

### P3: Czy dostępna jest wersja próbna Aspose.Note dla .NET?

 Odpowiedź 3: Tak, możesz uzyskać bezpłatną wersję próbną od[Tutaj](https://releases.aspose.com/).

### P4: Czy mogę dostosować jakość obrazu podczas konwersji do formatu JPEG?

A4: Tak, możesz ustawić jakość obrazu zgodnie ze swoimi wymaganiami.

### P5: Gdzie mogę uzyskać wsparcie dla Aspose.Note dla .NET?

 O5: Możesz uzyskać wsparcie od społeczności Aspose.Note dla .NET[forum](https://forum.aspose.com/c/note/28).