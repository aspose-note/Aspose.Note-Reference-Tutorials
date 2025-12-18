---
date: 2025-12-18
description: Dowiedz się, jak eksportować strony OneNote do formatu PDF przy użyciu
  Aspose.Note dla Javy. Wybierz algorytmy podziału, ustaw podział stron i łatwo generuj
  pliki PDF.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Eksportowanie stron OneNote metodą algorytmu podziału – Aspose.Note
url: /pl/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportowanie stron OneNote przy użyciu metody algorytmu dzielenia – Aspose.Note

## Wprowadzenie

Jeśli potrzebujesz **eksportować strony OneNote** do dokumentu PDF programowo, Aspose.Note for Java ułatwia to zadanie. W tym samouczku przeprowadzimy Cię przez metodę algorytmu dzielenia, która pozwala kontrolować, jak treść jest rozdzielana na strony, zapewniając czysty i czytelny wynik w PDF. Zobaczysz, jak ustawić opcje zapisu PDF, wybrać odpowiedni algorytm dzielenia stron oraz ostatecznie wygenerować plik PDF — wszystko przy użyciu kilku linii kodu Java.

## Szybkie odpowiedzi
- **Co robi algorytm dzielenia?** Określa, jak obiekty, które przekraczają granice stron, są obsługiwane podczas eksportu stron OneNote do PDF.  
- **Jakiej biblioteki wymaga?** Aspose.Note for Java (pobierz z oficjalnej strony Aspose).  
- **Czy potrzebna jest licencja?** Wymagana jest tymczasowa lub pełna licencja do użytku produkcyjnego; dostępna jest darmowa wersja próbna.  
- **Czy mogę eksportować duże notatniki OneNote?** Tak — biblioteka efektywnie przetwarza duże pliki i pozwala ustawić reguły dzielenia stron.  
- **Jakie formaty wyjściowe są obsługiwane?** PDF, JPEG, PNG, XPS i inne; ten przewodnik koncentruje się na eksporcie do PDF.

## Czym jest **eksportowanie stron OneNote**?
Eksportowanie stron OneNote oznacza konwersję natywnego formatu pliku `.one` do bardziej przenośnego formatu, takiego jak PDF. Jest to przydatne do udostępniania, archiwizacji lub drukowania treści bez konieczności używania aplikacji OneNote.

## Dlaczego używać algorytmu dzielenia przy **eksportowaniu stron OneNote**?
Algorytm daje precyzyjną kontrolę nad tym, jak złożone obiekty (tabele, obrazy, rysunki) są obsługiwane przy podziałach stron. Wybierając odpowiedni algorytm, możesz:

* Zachować wizualny układ każdej strony.  
* Uniknąć przyciętej treści, która w przeciwnym razie zostałaby obcięta.  
* Zmniejszyć liczbę wygenerowanych stron, gdy obiekty mogą być przeniesione na następną stronę w sposób płynny.

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz następujące wymagania wstępne:

1. Java Development Kit (JDK): Upewnij się, że masz zainstalowany JDK w swoim systemie. Możesz go pobrać ze [strony internetowej](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Biblioteka Aspose.Note for Java: Pobierz i zainstaluj bibliotekę Aspose.Note for Java z [linku do pobrania](https://releases.aspose.com/note/java/).

## Importowanie pakietów

W swoim projekcie Java zaimportuj niezbędne pakiety, aby korzystać z funkcji Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Krok 1: Zdefiniuj katalog dokumentu

Ustaw katalog, w którym znajduje się Twój dokument OneNote.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Załaduj dokument OneNote

Załaduj dokument OneNote przy użyciu klasy `Document` z Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Krok 3: Ustaw opcje zapisu PDF

Utwórz instancję `PdfSaveOptions`, aby określić opcje zapisu dokumentu jako PDF. To miejsce, w którym **ustawiasz zachowanie dzielenia stron** oraz inne ustawienia związane z PDF.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Krok 4: Ustaw algorytm dzielenia stron

Wybierz odpowiedni algorytm dzielenia zgodnie z Twoimi wymaganiami. W tym przypadku używamy `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, który zachowuje część obiektu na bieżącej stronie i klonuje pozostałą część na następną stronę.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Krok 5: Zapisz dokument

Zapisz dokument przy użyciu określonych opcji zapisu PDF. Ten krok **generuje wyjście PDF OneNote**, które możesz otworzyć, udostępnić lub wydrukować.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|---------|-------------|
| **Obiekty są obcinane przy granicach stron** | Spróbuj innego algorytmu, takiego jak `AlwaysSplitObjectsAlgorithm`, lub zwiększ wartość progową w `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **Wygenerowany PDF jest pusty** | Sprawdź, czy źródłowy plik `.one` nie jest uszkodzony oraz czy ścieżka `dataDir` jest poprawna. |
| **Wydajność jest niska przy dużych notatnikach** | Użyj `pdfSaveOptions.setCompressImages(true)`, aby zmniejszyć zużycie pamięci, i rozważ przetwarzanie notatnika w mniejszych sekcjach. |

## Najczęściej zadawane pytania

**Q: Czy mogę używać Aspose.Note for Java z innymi językami programowania?**  
A: Tak, Aspose.Note jest dostępny również dla .NET, C++ i Pythona.

**Q: Czy Aspose.Note jest odpowiedni do przetwarzania dużych plików OneNote?**  
A: Zdecydowanie tak. Biblioteka jest zoptymalizowana pod kątem efektywnego obsługiwania dużych notatników.

**Q: Gdzie mogę znaleźć dodatkowe zasoby i wsparcie dla Aspose.Note?**  
A: Możesz odwołać się do [dokumentacji](https://reference.aspose.com/note/java/) oraz [forum](https://forum.aspose.com/c/note/28) w celu uzyskania wsparcia i wskazówek.

**Q: Czy mogę wypróbować Aspose.Note przed zakupem?**  
A: Tak, możesz skorzystać z [bezpłatnej wersji próbnej](https://releases.aspose.com/), aby zapoznać się z funkcjami przed dokonaniem zakupu.

**Q: Jak mogę uzyskać tymczasową licencję na Aspose.Note?**  
A: Możesz złożyć wniosek o [tymczasową licencję](https://purchase.aspose.com/temporary-license/), aby ocenić produkt w okresie próbnym.

---

**Ostatnia aktualizacja:** 2025-12-18  
**Testowano z:** Aspose.Note 24.12 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}