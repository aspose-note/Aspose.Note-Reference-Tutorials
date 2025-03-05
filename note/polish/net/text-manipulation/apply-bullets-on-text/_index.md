---
title: Zastosuj punktory na tekście w Aspose.Note
linktitle: Zastosuj punktory na tekście w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak stosować punktory w tekście w Aspose.Note dla .NET, aby ulepszyć dokumenty OneNote. Postępuj zgodnie z tym przewodnikiem krok po kroku, aby uzyskać skuteczne formatowanie.
type: docs
weight: 10
url: /pl/net/text-manipulation/apply-bullets-on-text/
---
## Wstęp
Witamy w tym przewodniku krok po kroku dotyczącym stosowania punktorów w tekście za pomocą Aspose.Note dla .NET. Aspose.Note to potężna biblioteka, która umożliwia programistom bezproblemową pracę z plikami Microsoft OneNote w aplikacjach .NET. W tym samouczku przeprowadzimy Cię przez proces stosowania punktorów w tekście, poprawiając atrakcyjność wizualną dokumentów programu OneNote.
## Warunki wstępne
Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
- Podstawowa znajomość programowania w C# i .NET.
-  Zainstalowana biblioteka Aspose.Note dla .NET. Możesz go pobrać[Tutaj](https://releases.aspose.com/note/net/).
## Importuj przestrzenie nazw
W kodzie C# pamiętaj o uwzględnieniu niezbędnych przestrzeni nazw:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Krok 1: Skonfiguruj swój dokument
```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";
//Utwórz obiekt klasy Dokument
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Krok 2: Zainicjuj stronę i konspekt
```csharp
// Zainicjuj obiekt klasy Page
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Zainicjuj obiekt klasy Outline
Outline outline = new Outline(doc);
```
## Krok 3: Ustaw domyślny styl tekstu
```csharp
// Zainicjuj obiekt klasy TextStyle i ustaw właściwości formatowania
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Krok 4: Utwórz elementy konturu za pomocą punktorów
```csharp
// Zainicjuj obiekty klasy OutlineElement i zastosuj punktory
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Powtórz dla pozostałych elementów konturu
```
## Krok 5: Dodaj elementy konspektu do konspektu
```csharp
// Dodaj elementy konturu
outline.AppendChildLast(outlineElem1);
// Powtórz dla pozostałych elementów konturu
```
## Krok 6: Dodaj kontur do strony
```csharp
// Dodaj węzeł Konspekt
page.AppendChildLast(outline);
```
## Krok 7: Dodaj stronę do dokumentu
```csharp
//Dodaj węzeł strony
doc.AppendChildLast(page);
```
## Krok 8: Zapisz dokument OneNote
```csharp
// Zapisz dokument programu OneNote
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## Wniosek
Gratulacje! Pomyślnie nauczyłeś się, jak stosować punktory do tekstu za pomocą Aspose.Note dla .NET. Ta funkcja może znacznie ulepszyć formatowanie dokumentów programu OneNote, czyniąc je bardziej atrakcyjnymi wizualnie.
## Często zadawane pytania
### Czy mogę zastosować różne style punktorów do każdego elementu na liście?
 Tak, możesz dostosować style punktorów, modyfikując plik`NumberList` właściwości dla każdego`OutlineElement`.
### Czy Aspose.Note jest kompatybilny z najnowszą wersją Microsoft OneNote?
Aspose.Note obsługuje różne wersje Microsoft OneNote, zapewniając kompatybilność zarówno ze starszymi, jak i nowszymi wersjami.
### Czy mogę używać Aspose.Note do celów komercyjnych?
 Tak, możesz używać Aspose.Note dla .NET w projektach komercyjnych. Aby uzyskać licencję, odwiedź stronę[Tutaj](https://purchase.aspose.com/buy).
### Czy dostępna jest wersja próbna Aspose.Note dla .NET?
 Tak, możesz pobrać bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).
### Gdzie mogę znaleźć dodatkowe wsparcie i zasoby?
 Możesz odwiedzić forum społeczności Aspose.Note[Tutaj](https://forum.aspose.com/c/note/28) za wsparcie i dyskusje.