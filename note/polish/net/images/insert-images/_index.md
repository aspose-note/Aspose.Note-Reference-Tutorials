---
date: 2026-05-05
description: Dowiedz się, jak wstawiać obrazy do dokumentów Aspose.Note przy użyciu
  .NET. Ten przewodnik krok po kroku pokazuje, jak wyrównać obraz, dodać obraz do
  strony i wzbogacić treść wizualną.
keywords:
- how to insert image
- how to align image
- append image to page
linktitle: Wstawianie obrazów w dokumentach Aspose.Note
second_title: Aspose.Note .NET API
title: Jak wstawić obraz do dokumentów Aspose.Note przy użyciu .NET
url: /pl/net/images/insert-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak wstawić obraz do dokumentów Aspose.Note przy użyciu .NET

## Wprowadzenie

Jeśli chcesz uczynić swoje pliki Aspose.Note bardziej atrakcyjnymi, **jak wstawić obraz** jest pierwszą umiejętnością, którą będziesz chciał opanować. W tym samouczku przeprowadzimy Cię przez dokładne kroki potrzebne do dodania obrazów, kontrolowania ich rozmiaru, precyzyjnego pozycjonowania oraz wyrównywania ich tak, jak chcesz. Po zakończeniu będziesz swobodnie wstawiać obrazy, je wyrównywać i dołączać obraz do strony — wszystko przy użyciu czystego, czytelnego kodu C#.

## Szybkie odpowiedzi
- **Jakiej biblioteki wymaga?** Aspose.Note for .NET  
- **Czy mogę ustawić rozmiar obrazu programowo?** Tak – użyj właściwości Width i Height.  
- **Jak pozycjonować obraz?** Dostosuj HorizontalOffset, VerticalOffset lub użyj opcji wyrównania.  
- **Czy istnieje limit formatów obrazów?** Obsługiwane są JPG, PNG, BMP, GIF i inne.  
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest ważna licencja Aspose.Note do użytku komercyjnego.

## Co to jest wstawianie obrazu w Aspose.Note?

Wstawianie obrazu oznacza utworzenie obiektu Aspose.Note.Image, skonfigurowanie jego właściwości wizualnych i dołączenie go do strony w pliku .one zgodnym z OneNote. Dzięki temu możesz wzbogacić notatki o zrzuty ekranu, diagramy lub dowolne materiały wizualne.

## Dlaczego wstawiać obrazy przy użyciu Aspose.Note?

- **Lepsza komunikacja:** Wizualizacje wyjaśniają skomplikowane pomysły szybciej niż sam tekst.  
- **Spójny układ:** Kontrola programowa zapewnia, że każdy dokument spełnia te same standardy projektowe.  
- **Przyjazne automatyzacji:** Idealne do generowania raportów, samouczków lub przetwarzania partii notatników.

## Wymagania wstępne

1. Aspose.Note for .NET: Pobierz i zainstaluj Aspose.Note for .NET z [tutaj](https://releases.aspose.com/note/net/).  
2. Pliki graficzne: Przygotuj pliki graficzne (JPG, PNG itp.), które zamierzasz osadzić, na dysku.

## Importowanie przestrzeni nazw

Zaczynamy od zaimportowania przestrzeni nazw, które zapewniają dostęp do operacji we/wy plików oraz API Aspose.Note.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## Krok 1: Załaduj dokument i pobierz stronę

Najpierw otwórz istniejący dokument .one i pobierz stronę, na której będzie znajdować się obraz.

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## Jak wyrównać obraz

Zanim dodamy obraz, zdecyduj, jak ma on być wyrównany względem pozostałej treści. Aspose.Note oferuje opcje wyrównania poziomego (Left, Center, Right). Możesz także precyzyjnie dostosować położenie za pomocą wartości offsetów.

## Krok 2: Załaduj obraz i ustaw właściwości

Utwórz obiekt Image, wskaż na swój plik i określ jego wymiary, offsety oraz wyrównanie.

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // Set image width
    Height = 100,               // Set image height
    HorizontalOffset = 100,     // Set horizontal offset
    VerticalOffset = 400,       // Set vertical offset
    Alignment = HorizontalAlignment.Right  // Set image alignment
};
```

## Dołącz obraz do strony

Teraz, gdy obraz jest w pełni skonfigurowany, dołącz go do drzewa elementów strony.

```csharp
page.AppendChildLast(image);
```

## Typowe pułapki i wskazówki

- **Nieprawidłowe offsety:** Pamiętaj, że offsety mierzone są od lewego górnego rogu strony. Duży offset pionowy może spowodować, że obraz zostanie przesunięty poza ekran.  
- **Nieobsługiwany format:** Jeśli spróbujesz użyć formatu, który nie jest rozpoznawany, Aspose.Note zgłosi wyjątek — najpierw skonwertuj plik do JPG lub PNG.  
- **Ostrzeżenia licencyjne:** Uruchamianie bez licencji dodaje znak wodny do wygenerowanego dokumentu; zawsze stosuj swoją licencję w środowisku produkcyjnym.

## Podsumowanie

Teraz nauczyłeś się **jak wstawić obraz** do dokumentu Aspose.Note, **jak wyrównać obraz** oraz **jak dołączyć obraz do strony** przy użyciu kilku prostych linii C#. Te techniki pozwalają automatycznie tworzyć bogatsze, bardziej profesjonalne notatniki.

## FAQ

### Q1: Czy mogę wstawiać obrazy w dowolnym formacie do dokumentów Aspose.Note?

A1: Tak, Aspose.Note obsługuje różne formaty obrazów, w tym JPG, PNG, BMP, GIF itp.

### Q2: Czy można programowo zmienić rozmiar wstawionych obrazów?

A2: Zdecydowanie! Możesz dostosować szerokość i wysokość obrazów zgodnie z własnymi preferencjami podczas wstawiania.

### Q3: Czy Aspose.Note oferuje opcje modyfikacji wyrównania obrazu?

A3: Tak, możesz wyrównać obrazy do lewej, prawej lub środka na stronach dokumentu.

### Q4: Czy mogę wstawić wiele obrazów na jedną stronę mojego dokumentu?

A4: Oczywiście! Możesz wstawić dowolną liczbę obrazów na jednej stronie przy użyciu Aspose.Note.

### Q5: Czy istnieje limit rozmiaru pliku obrazów, które można wstawić?

A5: Aspose.Note nie nakłada ścisłych ograniczeń na rozmiary plików obrazów, ale zaleca się optymalizację obrazów w celu lepszej wydajności.

## Często zadawane pytania

**Q: Jak załadować obraz ze strumienia zamiast ścieżki pliku?**  
A: Użyj konstruktora Image(Stream, Document) i przekaż MemoryStream zawierający bajty obrazu.

**Q: Czy mogę zmienić obraz po jego dodaniu do strony?**  
A: Tak, możesz modyfikować właściwości Width, Height, HorizontalOffset, VerticalOffset i Alignment istniejącego obiektu Image, a następnie wywołać page.Update().

**Q: Czy można dodać podpis pod obrazem?**  
A: Wstaw element RichText po obrazie i ustaw jego tekst jako podpis.

**Q: Czy Aspose.Note obsługuje animowane GIFy?**  
A: Animowane GIFy są traktowane jako obrazy statyczne; wyświetlana jest tylko pierwsza klatka.

**Q: Co zrobić, gdy obraz jest rozmyty?**  
A: Upewnij się, że źródłowy obraz ma wystarczającą rozdzielczość i unikaj skalowania go powyżej jego oryginalnego rozmiaru.

---

**Ostatnia aktualizacja:** 2026-05-05  
**Testowano z:** Aspose.Note 23.12 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}