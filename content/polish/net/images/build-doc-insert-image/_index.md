---
title: Zbuduj dokument i wstaw obraz w Aspose.Note
linktitle: Zbuduj dokument i wstaw obraz w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak programowo wstawiać obrazy do dokumentów OneNote przy użyciu Aspose.Note dla .NET. Proste kroki umożliwiające bezproblemową manipulację dokumentami.
type: docs
weight: 10
url: /pl/net/images/build-doc-insert-image/
---
## Wstęp

W tym samouczku zagłębimy się w świat manipulacji dokumentami za pomocą Aspose.Note dla .NET. Aspose.Note to potężny interfejs API, który umożliwia programistom programową pracę z plikami Microsoft OneNote, umożliwiając łatwe wykonywanie takich zadań, jak tworzenie, modyfikowanie i konwertowanie dokumentów. 

## Warunki wstępne

Zanim zaczniemy, upewnij się, że spełniasz następujące wymagania wstępne:

1. Visual Studio: Upewnij się, że masz zainstalowany program Visual Studio w swoim systemie. Aspose.Note dla .NET współpracuje bezproblemowo z Visual Studio, zapewniając solidne środowisko programistyczne.

2.  Aspose.Note dla .NET: Pobierz i zainstaluj Aspose.Note dla .NET. Możesz znaleźć link do pobrania[Tutaj](https://releases.aspose.com/note/net/).

3. Podstawowa znajomość języka C#: Zapoznaj się z podstawami języka programowania C#. Chociaż ten samouczek zawiera wskazówki krok po kroku, korzystna będzie podstawowa znajomość języka C#.

## Importuj przestrzenie nazw

Zacznijmy od zaimportowania niezbędnych przestrzeni nazw do projektu C#. Te przestrzenie nazw zawierają klasy i metody, których będziemy używać do wykonywania zadań związanych z manipulacją dokumentami.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Podzielmy teraz proces tworzenia dokumentu i wstawiania obrazu na kilka etapów:

## Krok 1: Utwórz obiekt dokumentu

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document();
```

 Ta linia kodu inicjuje nową instancję klasy`Document` klasa, która reprezentuje dokument programu OneNote.

## Krok 2: Zainicjuj obiekt strony

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

 Tutaj inicjujemy nową instancję klasy`Page` class, która reprezentuje stronę w dokumencie OneNote.

## Krok 3: Zainicjuj obiekt konspektu

```csharp
Outline outline = new Outline(doc);
```

 The`Outline`klasa reprezentuje węzeł konspektu w hierarchii dokumentu. Tworzymy nowy obiekt konspektu, aby uporządkować nasz dokument.

## Krok 4: Zainicjuj obiekt OutlineElement

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

 Jakiś`OutlineElement` reprezentuje element w obrębie konspektu. Tutaj tworzymy nowy element konspektu, aby dodać treść do naszego dokumentu.

## Krok 5: Załaduj obraz

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg");
```

 Ładujemy plik obrazu z określonej ścieżki za pomocą`Image` konstruktor klasy.

## Krok 6: Ustaw wyrównanie obrazu

```csharp
image.Alignment = HorizontalAlignment.Right;
```

Ta linia kodu ustawia wyrównanie obrazu w dokumencie. W tym przykładzie wyrównujemy obraz do prawej strony.

## Krok 7: Dodaj obraz do elementu konspektu

```csharp
outlineElem.AppendChildLast(image);
```

Tutaj dodajemy obraz do elementu konspektu, umieszczając go w strukturze dokumentu.

## Krok 8: Dodaj element konspektu do konspektu

```csharp
outline.AppendChildLast(outlineElem);
```

Do struktury konspektu dokumentu dodajemy element konspektu wraz z wstawionym obrazem.

## Krok 9: Dodaj kontur do strony

```csharp
page.AppendChildLast(outline);
```

Kontur zawierający obraz zostaje dodany do struktury strony dokumentu.

## Krok 10: Dodaj stronę do dokumentu

```csharp
doc.AppendChildLast(page);
```

Na koniec dodajemy stronę wraz z jej zawartością do dokumentu.

## Krok 11: Zapisz dokument

```csharp
dataDir = dataDir + "BuildDocAndInsertImage_out.one";
doc.Save(dataDir);
```

Ta linia zapisuje zmodyfikowany dokument w określonej lokalizacji.

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się tworzyć dokument i wstawiać obraz za pomocą Aspose.Note dla .NET. Dzięki tej nowo zdobytej wiedzy możesz głębiej eksplorować i wdrażać bardziej zaawansowane zadania manipulacji dokumentami.

## Często zadawane pytania

### P1: Czy mogę wstawić wiele obrazów do jednego dokumentu za pomocą Aspose.Note dla .NET?

A1: Absolutnie! Do dokumentu możesz wstawić dowolną liczbę obrazów, wykonując podobne kroki dla każdego obrazu.

### P2: Czy Aspose.Note obsługuje inne formaty plików oprócz OneNote?

Odpowiedź 2: Tak, Aspose.Note zapewnia szeroką obsługę różnych formatów plików, w tym PDF, DOCX, HTML i innych.

### P3: Czy Aspose.Note nadaje się do rozwiązań do zarządzania dokumentami na poziomie przedsiębiorstwa?

A3: Oczywiście! Aspose.Note oferuje solidne funkcje i doskonałą wydajność, co czyni go idealnym wyborem do zarządzania dokumentami w przedsiębiorstwie.

### P4: Czy mogę dostosować wygląd wstawianych obrazów do dokumentu?

O4: Tak, Aspose.Note zapewnia kompleksowe opcje dostosowywania wyglądu obrazu, w tym wyrównania, rozmiaru i obrotu.

### P5: Gdzie mogę znaleźć dodatkowe zasoby i wsparcie dla Aspose.Note dla .NET?

 O5: Możesz zapoznać się z dokumentacją Aspose.Note[Tutaj](https://reference.aspose.com/note/net/) i poproś o pomoc na forum społeczności Aspose[Tutaj](https://forum.aspose.com/c/note/28).