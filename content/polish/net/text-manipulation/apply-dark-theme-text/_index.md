---
title: Transformacja ciemnego motywu za pomocą Aspose.Note dla .NET
linktitle: Zastosuj ciemny motyw do tekstu w Aspose.Note
second_title: Aspose.Note .NET API
description: Przekształć swoje dokumenty OneNote za pomocą Aspose.Note dla .NET! Bez wysiłku zastosuj elegancki ciemny motyw. Pobierz teraz i zwiększ swoje możliwości robienia notatek.
type: docs
weight: 11
url: /pl/net/text-manipulation/apply-dark-theme-text/
---
## Wstęp
Witamy w naszym przewodniku krok po kroku dotyczącym stosowania ciemnego motywu do tekstu w Aspose.Note dla .NET. Aspose.Note to potężny interfejs API .NET, który umożliwia programistom programową pracę z plikami Microsoft OneNote. W tym samouczku dowiemy się, jak nadać dokumentom OneNote elegancki i nowoczesny wygląd, stosując ciemny motyw do tekstu.
## Warunki wstępne
Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
-  Aspose.Note dla .NET: Upewnij się, że masz zainstalowany Aspose.Note dla .NET. Jeśli nie, możesz pobrać go ze strony[Dokumentacja Aspose.Note](https://reference.aspose.com/note/net/).
- Środowisko programistyczne: skonfiguruj preferowane środowisko programistyczne .NET, takie jak Visual Studio.
- Katalog dokumentów: Przygotuj katalog, w którym znajduje się dokument programu OneNote.
## Importuj przestrzenie nazw
W swoim projekcie .NET zaimportuj niezbędne przestrzenie nazw do pracy z Aspose.Uwaga:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## Krok 1: Załaduj dokument OneNote
Załaduj dokument OneNote do Aspose.Note, używając następującego kodu:
```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";
// Załaduj dokument do Aspose.Note.
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## Krok 2: Ustaw kolor tła
Ustaw kolor tła każdej strony na czarny:
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## Krok 3: Dostosuj kolor tekstu
Dostosuj kolor czcionki tekstu do białego dla lepszej widoczności:
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## Krok 4: Zapisz dokument
Zapisz zmodyfikowany dokument OneNote jako plik PDF:
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## Wniosek
Gratulacje! Pomyślnie zastosowałeś ciemny motyw do tekstu w dokumencie Aspose.Note. To proste, ale skuteczne ulepszenie może nadać plikom programu OneNote bardziej wyrafinowany wygląd.
## Często Zadawane Pytania
### Czy mogę zastosować ciemny motyw do określonych sekcji mojego dokumentu programu OneNote?
Tak, możesz dostosować kod, aby kierować reklamy na określone strony lub sekcje w dokumencie.
### Czy Aspose.Note obsługuje inne formaty eksportu oprócz PDF?
Absolutnie! Aspose.Note obsługuje różne formaty eksportu, w tym obrazy i Microsoft Word.
### Czy istnieje ograniczenie rozmiaru dokumentu, jaki może obsłużyć Aspose.Note?
Aspose.Note może obsługiwać dokumenty o różnych rozmiarach, a jego wydajność jest zoptymalizowana pod kątem wydajności.
### Czy mogę powrócić do oryginalnego motywu po zastosowaniu ciemnego motywu?
Tak, możesz zmodyfikować kod, aby przełączać się między motywami w zależności od preferencji.
### Gdzie mogę uzyskać pomoc dotyczącą zapytań związanych z Aspose.Note?
 Aby uzyskać pomoc, odwiedź stronę[Forum Aspose.Note](https://forum.aspose.com/c/note/28) lub eksploruj[dokumentacja](https://reference.aspose.com/note/net/).