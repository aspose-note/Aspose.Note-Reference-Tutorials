---
date: 2026-01-31
description: Dowiedz się, jak eksportować strony OneNote i konwertować OneNote na
  PDF, przetwarzając określony zakres stron przy użyciu Aspose.Note dla Javy. Zawiera
  kod krok po kroku oraz wskazówki dotyczące najlepszych praktyk.
linktitle: Export OneNote Pages – Convert Specific Page Range to PDF with Java
second_title: Aspose.Note Java API
title: Jak wyeksportować strony OneNote – konwertuj określony zakres stron na PDF
  przy użyciu Javy
url: /pl/java/onenote-document-loading/convert-page-range-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

 przy użyciu Javy

## Wprowadzenie

Eksportowanie stron OneNote do PDF jest powszechnym wymaganiem, gdy trzeba udostępnić wybrane notatki, zarchiwizować fragment projektu lub stworzyć dokumentację do druku. W tym samouczku dowiesz się **jak wyeksportować onenote** strony z określonego zakresu do pliku PDF przy użyciu Aspose.Note Java API. Przejdziemy przez każdy krok — od wczytania dokumentu źródłowego po dostosowanie wyjścia PDF — abyś mógł szybko i pewnie zintegrować tę funkcję w swoich aplikacjach Java.

## Szybkie odpowiedzi
- **Jaka jest podstawowa klasa do wczytywania pliku OneNote?** `com.aspose.note.Document`
- **Która opcja kontroluje zakres stron przy eksporcie do PDF?** `PdfSaveOptions.setPageIndex()` i `setPageCount()`
- **Czy formatowanie i układ pozostają niezmienione?** Tak, Aspose.Note zachowuje oryginalne formatowanie OneNote.
- **Czy mogę wyeks obsługiwane są tylko ciąg nowsza (dowolny JDK obsługujący bibliotekę Aspose.Note).

## Co to jest „eksport stron onenote”?

Eksportowanie stron OneNote oznacza konwersję wizualnej zawartości wybranych stron do innego przenośnego formatu — najczęściej PDF — przy zachowaniu oryginalnego układu, czcionek i obrazów. Umożliwia to łatwe rozpowszechnianie, drukowanie i długoterminowe przechowywanie notatek.

- **Wysoka wierność** – Biblioteka odtwarza dokładny wygląd stron OneNote.  
- **Programowa kontrola** **Nie wymaga instalacji Office** – Działa w pełni po stronie serwera.  
- **Wieloplatformowość** – Działa na Windows, Linux i macOS z dowolnym standardowym JDK.

## Prerequisites

1. **Java Development Kit (JDK)** – Java 8+ zainstalowane i skonfigurowane na twoim komputerze.  
2. **Aspose.Note for Java** – Pobierz najnowszą wersję strony: [Aspose.Note for Java](https://releases.aspose.com/note/java/).  
3. **Przykładowy dokument OneNote** – Plik `.one` zawierający strony, które chcesz wyeksportować.

## Importowanie pakietów

In your Java project, import the necessary classes for working with OneNote and PDF conversion:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
```

## Krok 1: Wczytaj dokument OneNote

First, point the API to the folder that holds your `.one` file and load it into a `Document` object:

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Wskazówka:** Użyj ścieżki bezwzględnej lub zasobu class‑path, jeśli twoja aplikacja działa w kontenerze.

## Krok 2: Zainicjuj opcje zapisu PDF

Create a `PdfSaveOptions` instance and define the page range you wish to export. The `setPageIndex` method uses a zero‑based index, so `2` refers to the third page in the document.

```java
PdfSaveOptions opts = new PdfSaveOptions();
opts.setPageIndex(2);  // Starting page index (third page)
opts.setPageCount(3);  // Number of consecutive pages to include
```

> **Dlaczego to ważne:** Ustawienie indeksu strony i liczby stron pozwala **konwertować konkretne strony pdf** bez przetwarzania całego notatnika, oszczędzając czas i pamięć.

## Krok 3: Zapisz jako PDF

Finally, call the `save` method with the output file name and the configured options. to disk.

```java
oneFile.save(dataDir + "ConvertSpecificPageRangeToPdf_out.pdf", opts);
System.out.println("File saved: " + dataDir + "ConvertSpecificPageRangeToPdf_out.pdf");
```

Powinieneś i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|----------|
| **Pusty plik PDF** | Nieprawidłowy `pageIndex` (poza zakresem) | Sprawdź całkowitą liczbę stron za pomocą `oneFile.getPages().size()` |
| **Brakujące obrazy** | Obrazy przechowywane jako zasoby zewnętrzne | Upewnij się, że plik źródłowy `.one` i wszystkie powiązaneu |
| **Spowolnienie wydajności przy dużych notatnikach** | Ładowanie całego dokumentu przed podziałem | Użyj `PdfSaveOptions`, aby ograniczyć zakres stron jak pokazano; rozważ przetwarzanie w partiach |

## Często zadawane pytania

**Q: Czy mogę określić wiele nieciągłych zakresów stron do eksportu?**  
A: Obecnie Aspose.Note for Java obsługuje tylko ciągłe zakresy. Należy uruchomić oddzielne operacje eksportu dla każdego zakresu.

**Q: Czy Aspose.Note zachowuje oryginalne formatowanie podczas **konwersji onenote pdf**?**  
A: Tak, biblioteka zachowuje czcionki, kolory, tabele i obrazy dokładnie tak, jak występują w OneNote.

**Q: Czy można wyeksportować zabezpieczony hasłem plik OneNote?**  
A: API nie otwiera bezpośrednio zabezpieczonych hasłem notatnikówniej procedury odszyfrowania przed wczytaniem.

**Q: Jak mogę dostosować wygląd PDF (rozmiar strony, orientacja, nagłówki/stopki)?**  
A: `PdfSaveOptions` udostępnia właściwości takie jak `setPageSize()`, `setOrientation()` i `setHeaderFooter()`, aby dopasować wyjście.

**Q: Czy mogę wsadowo **konwertować dokument onenote** do PDF dla wielu plików?**  
A: Oczywiście. Przejdź pętlą przez kolekcję plików `.one`, zastosuj te same `PdfSaveOptions` i zapisz każdy wynik.

## Jak wyeksportować strony OneNote przy użyciu Javy – Pod`.  
2. **SkonfigurPageCount`, aby określić zakres, który chcesz **wyeksportować onenote do pdf**.  
3. **Zapisz** dokument jako PDF używając `save()`.

Te trzy kroki dają pełną kontrolę nad **jak wyeksportować onenote** zawartość programowo, niezależnie od tego, czy tworzysz narzędzie raportujące, system archiwizacji, czy prostą funkcję udostępniania notatek.

## Conclusion

W strony onenote** poprzez konwersję określonego zakresu stron do PDF przy użyciu Aspose.Note for Java. Masz teraz wielokrotnego użytku fragment kodu, który możesz wbudować w większe przepływy pracy — niezależnie od tego, czy tworzysz narzędzie raportujące, system archiwizacji czy prostą funkcję udostępniania notatek. Eksperymentuj z różnymi ustawieniami `PdfSaveOptions`, aby precyzyjnie dostosować wyjście PDF do swoich potrzeb.

---

**Ostatnia aktualizacja:** 2026-01-31  
**Testowano z:** Aspose.Note for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}