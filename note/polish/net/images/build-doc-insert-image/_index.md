---
date: 2026-04-06
description: Dowiedz się, jak programowo tworzyć dokument OneNote i wstawiać obraz
  przy użyciu Aspose.Note dla .NET. Postępuj prostymi krokami, aby dodawać obrazy,
  ustawiać wyrównanie i więcej.
keywords:
- create onenote document
- how to insert image
- insert image onenote
- set image alignment
- multiple images onenote
linktitle: Utwórz dokument i wstaw obraz w Aspose.Note
second_title: Aspose.Note .NET API
title: Utwórz dokument OneNote i wstaw obraz przy użyciu Aspose.Note
url: /pl/net/images/build-doc-insert-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz dokument OneNote i wstaw obraz przy użyciu Aspose.Note

## Wprowadzenie

W tym samouczku **utworzysz dokument OneNote** i dowiesz się **jak wstawić obraz** przy użyciu Aspose.Note dla .NET. Aspose.Note daje pełną kontrolę nad plikami OneNote, ułatwiając programowe dodawanie bogatych treści, takich jak zdjęcia, tabele i niestandardowe układy.

## Szybkie odpowiedzi
- **Jaki jest główny cel?** Utworzenie dokumentu OneNote i wstawienie obrazu z niestandardowym wyrównaniem.  
- **Jakiej biblioteki potrzebujesz?** Aspose.Note dla .NET (pobierz [tutaj](https://releases.aspose.com/note/net/)).  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarczy do rozwoju; licencja płatna jest wymagana w środowisku produkcyjnym.  
- **Czy mogę dodać wiele obrazów?** Tak – powtórz kroki wstawiania dla każdego obrazu (zobacz wskazówkę „multiple images onenote”).  
- **Czy obsługiwana jest konwersja do PDF?** Oczywiście – później możesz przekonwertować dokument OneNote na PDF, używając metody `Save` Aspose.Note z formatem PDF.

## Wymagania wstępne

Zanim rozpoczniemy, upewnij się, że masz następujące elementy:

1. **Visual Studio** – w pełni wyposażone IDE do programowania w .NET.  
2. **Aspose.Note dla .NET** – pobierz i zainstaluj bibliotekę ze strony producenta.  
3. **Podstawowa znajomość C#** – znajomość składni C# ułatwi śledzenie przykładów kodu.

## Importowanie przestrzeni nazw

Zacznijmy od zaimportowania niezbędnych przestrzeni nazw do projektu C#. Te przestrzenie nazw zawierają klasy i metody, które wykorzystamy do manipulacji dokumentem.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Teraz rozbijmy proces tworzenia dokumentu i wstawiania obrazu na kilka kroków:

## Krok 1: Utwórz obiekt Document

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document();
```

Ten wiersz kodu inicjalizuje nową instancję klasy `Document`, która reprezentuje dokument OneNote.

## Krok 2: Zainicjalizuj obiekt Page

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

Tutaj tworzymy nową instancję klasy `Page`, która reprezentuje stronę w dokumencie OneNote.

## Krok 3: Zainicjalizuj obiekt Outline

```csharp
Outline outline = new Outline(doc);
```

Klasa `Outline` reprezentuje węzeł konspektu w hierarchii dokumentu. Tworzymy nowy obiekt konspektu, aby ustrukturyzować nasz dokument.

## Krok 4: Zainicjalizuj obiekt OutlineElement

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

`OutlineElement` reprezentuje element w obrębie konspektu. Tutaj tworzymy nowy element konspektu, aby dodać treść do dokumentu.

## Krok 5: Załaduj obraz

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg");
```

Ładujemy plik obrazu z podanej ścieżki, używając konstruktora klasy `Image`.

## Krok 6: Ustaw wyrównanie obrazu

```csharp
image.Alignment = HorizontalAlignment.Right;
```

Ten wiersz ustawia **wyrównanie obrazu** po prawej stronie strony. Możesz także wybrać `Left` lub `Center` w zależności od potrzeb układu.

## Krok 7: Dodaj obraz do OutlineElement

```csharp
outlineElem.AppendChildLast(image);
```

Tutaj dodajemy obraz do elementu konspektu, umieszczając go w strukturze dokumentu.

## Krok 8: Dodaj OutlineElement do Outline

```csharp
outline.AppendChildLast(outlineElem);
```

Dodajemy element konspektu wraz z wstawionym obrazem do struktury konspektu dokumentu.

## Krok 9: Dodaj Outline do Page

```csharp
page.AppendChildLast(outline);
```

Konspekt, zawierający obraz, jest dodawany do struktury strony dokumentu.

## Krok 10: Dodaj Page do Document

```csharp
doc.AppendChildLast(page);
```

Na koniec dodajemy stronę, wraz z jej zawartością, do dokumentu.

## Krok 11: Zapisz dokument

```csharp
dataDir = dataDir + "BuildDocAndInsertImage_out.one";
doc.Save(dataDir);
```

Ten wiersz zapisuje zmodyfikowany dokument OneNote w określonej lokalizacji. Później możesz **przekonwertować OneNote na PDF**, wywołując `doc.Save("output.pdf")`.

## Dlaczego to jest ważne

- **Automatyzacja** – Programowe tworzenie dokumentów OneNote oszczędza czas w porównaniu z ręczną edycją.  
- **Spójność** – Kod zapewnia, że każdy dokument ma ten sam układ i zasady formatowania.  
- **Skalowalność** – To samo podejście można rozszerzyć, aby wstawiać **multiple images onenote** lub generować raporty masowo.

## Częste pułapki i wskazówki

- **Problemy ze ścieżkami** – Zawsze sprawdzaj, czy `dataDir` wskazuje na istniejący folder; w przeciwnym razie ładowanie obrazu się nie powiedzie.  
- **Rozmiar obrazu** – Duże obrazy mogą znacznie zwiększyć rozmiar pliku; rozważ zmianę rozmiaru przed wstawieniem.  
- **Wiele obrazów** – Aby dodać więcej niż jedno zdjęcie, powtórz kroki 5‑7 dla każdego obrazu i dołącz je do tego samego lub innego `OutlineElement`.

## Najczęściej zadawane pytania

### P1: Czy mogę wstawić wiele obrazów do jednego dokumentu przy użyciu Aspose.Note dla .NET?

Odp 1: Oczywiście! Możesz wstawić dowolną liczbę obrazów, powtarzając te same kroki wstawiania dla każdego z nich.

### P2: Czy Aspose.Note obsługuje inne formaty plików poza OneNote?

Odp 2: Tak, Aspose.Note zapewnia szerokie wsparcie dla różnych formatów, w tym PDF, DOCX, HTML i wielu innych.

### P3: Czy Aspose.Note nadaje się do rozwiązań zarządzania dokumentami na poziomie przedsiębiorstwa?

Odp 3: Zdecydowanie! Aspose.Note oferuje solidne funkcje i wysoką wydajność, co czyni go doskonałym wyborem dla korporacyjnych systemów zarządzania dokumentami.

### P4: Czy mogę dostosować wygląd wstawionych obrazów w dokumencie?

Odp 4: Tak, Aspose.Note udostępnia rozbudowane opcje dostosowywania wyglądu obrazu, w tym wyrównanie, rozmiar i obrót.

### P5: Gdzie mogę znaleźć dodatkowe zasoby i wsparcie dla Aspose.Note dla .NET?

Odp 5: Dokumentację Aspose.Note znajdziesz [tutaj](https://reference.aspose.com/note/net/), a pomoc uzyskasz na forum społeczności Aspose [tutaj](https://forum.aspose.com/c/note/28/).

---

**Ostatnia aktualizacja:** 2026-04-06  
**Testowano z:** Aspose.Note 24.11 dla .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}