---
title: Przeglądaj wersje stron w dokumentach Aspose.Note
linktitle: Przeglądaj wersje stron w dokumentach Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak przeglądać wersje stron w dokumentach Aspose.Note przy użyciu platformy .NET ze wskazówkami krok po kroku.
type: docs
weight: 14
url: /pl/net/note-manipulation/page-revisions-exploration/
---
## Wstęp

W tym samouczku zagłębimy się w odkrywanie wersji stron w dokumentach Aspose.Note przy użyciu platformy .NET. Aspose.Note to potężna biblioteka, która umożliwia programistom programową pracę z plikami Microsoft OneNote, oferując różne funkcje manipulowania i wyodrębniania danych z tych plików.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz skonfigurowane następujące wymagania wstępne:

### 1. Pobierz i zainstaluj Aspose.Note dla .NET

 Odwiedzić[strona pobierania](https://releases.aspose.com/note/net/) i pobierz bibliotekę Aspose.Note dla .NET. Postępuj zgodnie z dostarczonymi instrukcjami instalacji, aby skonfigurować bibliotekę w środowisku programistycznym.

### 2. Załaduj niezbędne przestrzenie nazw

Pamiętaj, aby zaimportować wymagane przestrzenie nazw do swojego projektu .NET, aby bezproblemowo uzyskać dostęp do funkcjonalności Aspose.Note.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

Podzielmy teraz proces przeglądania wersji stron na instrukcje krok po kroku:

## Krok 1: Załaduj dokument

W pierwszej kolejności musimy załadować dokument Aspose.Note, pamiętając o umożliwieniu ładowania historii dokumentów.

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## Krok 2: Pobierz wersje strony

Po załadowaniu dokumentu możemy pobrać wersje dla określonej strony. W tym przykładzie otrzymamy poprawki dla pierwszej strony.

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## Krok 3: Iteruj po wersjach

W pętli możesz przeglądać każdą wersję strony i uzyskać dostęp do jej właściwości, takich jak czas ostatniej modyfikacji, czas utworzenia, tytuł, poziom i autor.

## Wniosek

Eksplorowanie wersji stron w dokumentach Aspose.Note przy użyciu platformy .NET jest prostym procesem. Wykonując kroki opisane w tym samouczku, możesz skutecznie programowo pobierać i analizować historię wersji plików programu OneNote.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.Note dla .NET do tworzenia nowych dokumentów OneNote?

O1: Tak, Aspose.Note dla .NET umożliwia programowe tworzenie, edytowanie i manipulowanie dokumentami OneNote.

### P2: Czy Aspose.Note obsługuje historię ładowania wszystkich typów plików OneNote?

O2: Aspose.Note obsługuje historię ładowania zarówno dla formatów plików .one, jak i .onepkg.

### P3: Czy dostępna jest bezpłatna wersja próbna Aspose.Note dla .NET?

 A3: Tak, możesz pobrać bezpłatną wersję próbną Aspose.Note dla .NET ze strony[Tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać tymczasową licencję na Aspose.Note dla .NET?

 Odpowiedź 4: Możesz poprosić o licencję tymczasową od[ten link](https://purchase.aspose.com/temporary-license/).

### P5: Gdzie mogę znaleźć wsparcie dla Aspose.Note dla .NET?

 Odpowiedź 5: Wsparcie i zasoby można znaleźć na stronie[Forum Aspose.Note](https://forum.aspose.com/c/note/28).