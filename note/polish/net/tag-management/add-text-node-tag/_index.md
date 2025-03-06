---
title: Dodaj węzeł tekstowy ze znacznikiem w Aspose.Note
linktitle: Dodaj węzeł tekstowy ze znacznikiem w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak dodawać węzły tekstowe ze znacznikami do dokumentów OneNote przy użyciu Aspose.Note dla .NET.
weight: 12
url: /pl/net/tag-management/add-text-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj węzeł tekstowy ze znacznikiem w Aspose.Note

## Wstęp

Aspose.Note dla .NET to potężna biblioteka, która umożliwia programistom programowe tworzenie, manipulowanie i konwertowanie plików Microsoft OneNote przy użyciu platformy .NET. W tym samouczku omówimy, jak dodać węzeł tekstowy ze znacznikiem do dokumentu OneNote za pomocą Aspose.Note dla .NET.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące wymagania wstępne:

1. Visual Studio: Upewnij się, że masz zainstalowany program Visual Studio w swoim systemie.
2.  Aspose.Note dla .NET: Pobierz i zainstaluj Aspose.Note dla .NET z[strona internetowa](https://releases.aspose.com/note/net/).
3. Podstawowa znajomość języka C#: Zapoznaj się z podstawami języka programowania C#.

## Importuj przestrzenie nazw

Najpierw musisz zaimportować niezbędne przestrzenie nazw, aby uzyskać dostęp do klas i metod wymaganych do pracy z Aspose.Note dla .NET.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Krok 1: Utwórz obiekt dokumentu

Zainicjuj obiekt dokumentu, aby rozpocząć pracę z dokumentem programu OneNote.

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## Krok 2: Zainicjuj obiekty strony i konspektu

Utwórz obiekty Page i Outline, aby uporządkować zawartość dokumentu OneNote.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## Krok 3: Dodaj węzeł tekstowy ze znacznikiem

Utwórz obiekt RichText z żądanym tekstem i stylem, a następnie dodaj go do OutlineElement.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## Krok 4: Dołącz element konspektu i węzły strony

Dołącz element OutlineElement do konspektu, a następnie dołącz konspekt do strony. Na koniec dołącz stronę do dokumentu.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Krok 5: Zapisz dokument

Zapisz zmodyfikowany dokument OneNote w określonej lokalizacji.

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się, jak dodać węzeł tekstowy ze znacznikiem do dokumentu OneNote przy użyciu Aspose.Note dla .NET. Dzięki tej wiedzy możesz teraz programowo dostosowywać i ulepszać pliki programu OneNote.

## Często zadawane pytania

### P1: Czy mogę dodać wiele węzłów tekstowych z różnymi tagami w tym samym dokumencie?

O1: Tak, możesz dodać wiele węzłów tekstowych z różnymi tagami, wykonując ten sam proces dla każdego węzła.

### P2: Czy Aspose.Note dla .NET jest kompatybilny ze wszystkimi wersjami OneNote?

O2: Aspose.Note dla .NET obsługuje różne wersje OneNote, w tym 2010, 2013, 2016 i nowsze.

### P3: Czy mogę dostosować kolory i style tagów?

A3: Tak, możesz dostosować kolory i style tagów zgodnie ze swoimi wymaganiami.

### P4: Czy Aspose.Note dla .NET obsługuje szyfrowanie dokumentów?

O4: Tak, Aspose.Note dla .NET obsługuje szyfrowanie dokumentów, aby zapewnić bezpieczeństwo danych.

### P5: Gdzie mogę znaleźć więcej zasobów i wsparcia dla Aspose.Note dla .NET?

 Odpowiedź 5: Możesz eksplorować[Aspose.Note dla dokumentacji .NET](https://reference.aspose.com/note/net/) zwrócić się o pomoc do[Forum Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
