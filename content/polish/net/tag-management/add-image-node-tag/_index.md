---
title: Dodaj węzeł obrazu ze znacznikiem w Aspose.Note
linktitle: Dodaj węzeł obrazu ze znacznikiem w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak ulepszyć dokumenty OneNote, dodając obrazy z niestandardowymi znacznikami za pomocą Aspose.Note dla .NET.
type: docs
weight: 10
url: /pl/net/tag-management/add-image-node-tag/
---
## Wstęp

W tym samouczku omówimy, jak dodać węzeł obrazu ze znacznikiem za pomocą Aspose.Note dla .NET. Ta funkcja umożliwia ulepszanie dokumentów OneNote poprzez dodawanie obrazów z niestandardowymi tagami.

## Warunki wstępne

Zanim zaczniesz, upewnij się, że masz następujące elementy:

1. Visual Studio: Zainstaluj Visual Studio IDE w swoim systemie.
2.  Aspose.Note dla .NET: Pobierz i zainstaluj bibliotekę Aspose.Note dla .NET z[link do pobrania](https://releases.aspose.com/note/net/).
3. Podstawowa wiedza: Zapoznaj się z językiem programowania C# i frameworkiem .NET.

## Importuj przestrzenie nazw

Najpierw pamiętaj o uwzględnieniu niezbędnych przestrzeni nazw w kodzie C#:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Krok 1: Zainicjuj obiekty dokumentu i strony

 Rozpocznij od utworzenia instancji`Document` klasa i A`Page` obiekt:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Krok 2: Zainicjuj obiekty Outline i OutlineElement

 Następnie zainicjuj`Outline` I`OutlineElement` obiekty:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## Krok 3: Załaduj i wstaw obraz

Załaduj żądany obraz i wstaw go do węzła dokumentu:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## Krok 4: Dodaj tag do obrazu

Dodaj niestandardowy tag do obrazu:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## Krok 5: Dołącz element konspektu i węzły strony

Dołącz element konspektu i węzły konspektu do strony:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## Krok 6: Zapisz dokument

Zapisz zmodyfikowany dokument OneNote:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## Wniosek

Wykonując te kroki, możesz bezproblemowo dodać węzeł obrazu z niestandardowym znacznikiem za pomocą Aspose.Note dla .NET, wzbogacając dokumenty OneNote o spersonalizowane wizualizacje.

## Często zadawane pytania

### P1: Czy mogę dodać wiele obrazów z różnymi tagami w jednym dokumencie za pomocą Aspose.Note?

Odpowiedź 1: Tak, możesz dodać wiele obrazów z różnymi tagami, wykonując podobne kroki dla każdego obrazu.

### P2: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami OneNote?

O2: Aspose.Note obsługuje różne wersje OneNote, zapewniając kompatybilność w różnych środowiskach.

### P3: Czy mogę dostosować wygląd tagu dodanego do obrazu?

O3: Tak, Aspose.Note zapewnia elastyczność w dostosowywaniu wyglądu znacznika do własnych preferencji.

### P4: Czy Aspose.Note oferuje obsługę dodawania obrazów z adresów URL?

O4: Aspose.Note obsługuje przede wszystkim dodawanie obrazów z katalogów lokalnych, ale możesz dołączyć obrazy zewnętrzne, pobierając je najpierw lokalnie.

### P5: Czy istnieją jakieś ograniczenia dotyczące rozmiaru lub formatu obrazów, które można dodać?

Odpowiedź 5: Aspose.Note obsługuje szeroką gamę formatów obrazów i nie nakłada żadnych ścisłych ograniczeń na rozmiar obrazu, co pozwala na włączenie różnorodnych elementów wizualnych do dokumentów.