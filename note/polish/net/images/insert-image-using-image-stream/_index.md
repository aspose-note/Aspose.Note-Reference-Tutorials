---
date: 2026-04-13
description: Dowiedz się, jak dodawać obrazy do dokumentów OneNote przy użyciu strumieni
  obrazów w .NET z Aspose.Note. Ten przewodnik krok po kroku opisuje ładowanie obrazów
  ze strumienia, dodawanie ich do konturów oraz zapisywanie pliku.
keywords:
- add image to onenote
- how to insert image
- load image from stream
- append image to outline
- image stream .net
linktitle: Dodaj obraz do OneNote za pomocą strumienia obrazu przy użyciu Aspose.Note
second_title: Aspose.Note .NET API
title: Dodaj obraz do OneNote za pomocą strumienia obrazu przy użyciu Aspose.Note
url: /pl/net/images/insert-image-using-image-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj obraz do OneNote za pomocą strumienia obrazu przy użyciu Aspose.Note

## Wprowadzenie

W tym samouczku odkryjesz **jak dodać obraz do OneNote** dokumentów, ładując obraz ze strumienia i dołączając go do konturu przy użyciu Aspose.Note dla .NET. Niezależnie od tego, czy tworzysz narzędzie raportujące, aplikację do notowania, czy automatyzujesz dokumentację, programowe wstawianie obrazów sprawia, że pliki OneNote są znacznie bardziej atrakcyjne i użyteczne.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.Note for .NET (dostępna darmowa wersja próbna).  
- **Które wersje .NET są obsługiwane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Czy mogę wczytać obrazy ze strumienia?** Tak – użyj `FileStream` lub dowolnej implementacji `Stream`.  
- **Jak kontrolować wyrównanie obrazu?** Ustaw właściwość `Alignment` (np. `HorizontalAlignment.Right`).  
- **Jaki format pliku jest tworzony?** Plik OneNote (`.one`), który można otworzyć w Microsoft OneNote.

## Co to jest „dodawanie obrazu do OneNote”?

Dodanie obrazu do pliku OneNote oznacza osadzenie elementu wizualnego bezpośrednio w hierarchii treści strony. Dzięki Aspose.Note pracujesz z obiektami takimi jak `Document`, `Page`, `Outline` i `OutlineElement`. Wstawiając obiekt `Image` do `OutlineElement`, obraz staje się częścią układu strony OneNote.

## Dlaczego używać Aspose.Note do wstawiania obrazów?

- **Brak wymogu instalacji Office** – generuj lub modyfikuj pliki OneNote na serwerze.  
- **Pełna kontrola nad układem** – wyrównuj, zmieniaj rozmiar i pozycjonuj obrazy dokładnie tam, gdzie potrzebujesz.  
- **Przyjazny dla strumieni** – działa z dowolnym `Stream`, idealny dla przechowywania w chmurze lub scenariuszy tylko w pamięci.  
- **Wieloplatformowy** – kompatybilny z środowiskami .NET na Windows, Linux i macOS.

## Wymagania wstępne

1. **Środowisko programistyczne** – Visual Studio 2022 lub dowolne IDE kompatybilne z .NET.  
2. **Biblioteka Aspose.Note** – pobierz ją z oficjalnej strony [tutaj](https://releases.aspose.com/note/net/).  
3. **Pliki graficzne** – co najmniej jeden obraz (JPG, PNG, BMP, GIF lub TIFF), który chcesz osadzić.  
4. **Podstawowa znajomość C#** – znajomość obsługi plików i programowania obiektowego.

## Importowanie przestrzeni nazw
Najpierw zaimportuj przestrzenie nazw, które dają dostęp do klas Aspose.Note oraz standardowych narzędzi I/O .NET.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Teraz przejdźmy krok po kroku przez proces.

### Krok 1: Inicjalizacja obiektu Document
Zaczynamy od utworzenia nowej instancji `Document`, która będzie przechowywać plik OneNote.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

### Krok 2: Utworzenie obiektu Page
Plik OneNote składa się z jednej lub wielu stron. Tutaj tworzymy nową stronę, aby pomieścić naszą zawartość.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### Krok 3: Inicjalizacja obiektów Outline i OutlineElement
Outlines są kontenerami dla bogatej treści (tekst, obrazy, tabele). `OutlineElement` jest elementem podrzędnym, który faktycznie przechowuje elementy.

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```

### Krok 4: Wczytanie obrazu ze strumienia
Używając `FileStream` (lub dowolnego `Stream`) odczytujemy plik obrazu i tworzymy obiekt `Image`. To miejsce, w którym wyróżnia się fraza **load image from stream**.

```csharp
using (FileStream fs = File.OpenRead(dataDir + "image.jpg"))
{
    Aspose.Note.Image image1 = new Aspose.Note.Image(doc, "Penguins.jpg", fs)
    {
        Alignment = HorizontalAlignment.Right
    };
    outlineElem1.AppendChildLast(image1);
}
```

### Krok 5: Dodanie obrazu do OutlineElement
Obraz jest teraz częścią `OutlineElement`. Ten krok demonstruje funkcję **append image to outline**.

```csharp
outlineElem1.AppendChildLast(image1);
```

### Krok 6: Dodanie OutlineElement do Outline
Teraz dołączamy element (z obrazem) do kontenera outline.

```csharp
outline1.AppendChildLast(outlineElem1);
```

### Krok 7: Dodanie Outline do Page
Outline, zawierający obraz, jest dodawany do strony.

```csharp
page.AppendChildLast(outline1);
```

### Krok 8: Dodanie Page do Document
Po przygotowaniu strony wstawiamy ją do hierarchii dokumentu.

```csharp
doc.AppendChildLast(page);
```

### Krok 9: Zapisanie dokumentu
Na koniec zapisujemy plik OneNote na dysku. Powstały plik można otworzyć w Microsoft OneNote.

```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|---------|----------------------|-------------|
| **Obraz nie wyświetla się** | Strumień został zamknięty przed dodaniem obrazu. | Utrzymaj blok `using` wokół wywołania `AppendChildLast` (jak pokazano). |
| **Nieprawidłowe wyrównanie** | Właściwość `Alignment` nie została ustawiona lub została nadpisana później. | Ustaw `Alignment` przy tworzeniu `Image` lub zmodyfikuj `image1.Alignment` przed dołączeniem. |
| **Nieobsługiwany format obrazu** | Próba wczytania formatu nie rozpoznawanego przez Aspose.Note. | Najpierw przekonwertuj obraz do JPG, PNG, BMP, GIF lub TIFF. |
| **Błędy ścieżki pliku** | `dataDir` wskazuje na nieistniejący folder. | Użyj `Path.Combine` i sprawdź, czy folder istnieje przed uruchomieniem. |

## Najczęściej zadawane pytania

**P: Czy mogę wstawić wiele obrazów do jednego dokumentu używając tej metody?**  
O: Tak. Po prostu powtórz kroki *Load Image from Stream* i *Append Image to OutlineElement* dla każdego obrazu.

**P: Czy Aspose.Note obsługuje inne formaty obrazów oprócz JPG?**  
O: Oczywiście. PNG, BMP, GIF i TIFF są wszystkie obsługiwane.

**P: Czy mogę dostosować wyrównanie i rozmiar wstawionych obrazów?**  
O: Tak. Oprócz `Alignment` możesz ustawić właściwości `Width`, `Height` i `Scale` obiektu `Image`.

**P: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami .NET?**  
O: Działa z .NET Framework 4.5+, .NET Core 3.1+, .NET 5 i .NET 6+.

**P: Gdzie mogę znaleźć dodatkowe zasoby i wsparcie dla Aspose.Note?**  
O: Kompleksową dokumentację, fora i wsparcie znajdziesz na [Aspose Forum](https://forum.aspose.com/c/note/28).

---

**Ostatnia aktualizacja:** 2026-04-13  
**Testowano z:** Aspose.Note 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}