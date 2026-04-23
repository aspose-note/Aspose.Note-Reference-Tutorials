---
date: 2026-03-16
description: Dowiedz się, jak eksportować PDF z OneNote przy użyciu Aspose.Note dla
  Javy metodą algorytmu dzielenia, kontrolować podziały stron i efektywnie kompresować
  obrazy w PDF.
linktitle: Export OneNote PDF with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Eksportuj PDF z OneNote metodą algorytmu dzielenia – Aspose.Note
url: /pl/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport PDF z OneNote przy użyciu metody algorytmu dzielenia – Aspose.Note

## Wprowadzenie

Jeśli potrzebujesz **eksportować PDF z OneNote** programowo, Aspose.Note for Java ułatwia to zadanie. W tym samouczku przeprowadzimy Cię przez metodę Splitting Algorithm, która pozwala kontrolować, jak treść jest dzielona na strony, zapewniając czysty i czytelny wynik w formacie PDF. Zobaczysz, jak ustawić opcje zapisu PDF, wybrać odpowiedni algorytm dzielenia stron oraz ostatecznie wygenerować plik PDF — wszystko przy użyciu kilku linii kodu Java.

## Szybkie odpowiedzi
- **Co robi algorytm dzielenia?** Określa, jak obiekty przekraczające granice stron są obsługiwane podczas eksportu stron OneNote do PDF.  
- **Jakiej biblioteki wymaga?** Aspose.Note for Java (pobierz ze strony oficjalnej Aspose).  
- **Czy potrzebna jest licencja?** Wymagana jest tymczasowa lub pełna licencja do użytku produkcyjnego; dostępna jest darmowa wersja próbna.  
- **Czy mogę eksportować duże notatniki OneNote?** Tak — biblioteka efektywnie przetwarza duże pliki i pozwala ustawić reguły dzielenia stron.  
- **Jakie formaty wyjściowe są obsługiwane?** PDF, JPEG, PNG, XPS i inne; ten przewodnik koncentruje się na eksporcie do PDF.  
- **Jak mogę skompresować obrazy w PDF?** Użyj `pdfSaveOptions.setCompressImages(true)`, aby zmniejszyć rozmiar obrazów w generowanym PDF.  

## Jak eksportować PDF z OneNote przy użyciu algorytmu dzielenia
Ta sekcja przeprowadzi Cię przez dokładne kroki potrzebne do **konwersji stron OneNote** do PDF, jednocześnie inteligentnie obsługując podziały stron.

## Czym jest eksport PDF z OneNote?
Eksport PDF z OneNote oznacza konwersję natywnego formatu pliku `.one` do przenośnego dokumentu PDF. Jest to przydatne do udostępniania, archiwizacji lub drukowania treści bez konieczności posiadania aplikacji OneNote.

## Dlaczego używać algorytmu dzielenia przy eksporcie PDF z OneNote?
Algorytm zapewnia precyzyjną kontrolę nad tym, jak złożone obiekty (tabele, obrazy, rysunki) są obsługiwane przy podziałach stron. Wybierając odpowiedni algorytm, możesz:
* Zachować wizualny układ każdej strony.  
* Uniknąć przyciętej treści, która w przeciwnym razie zostałaby obcięta.  
* Zredukować liczbę wygenerowanych stron, gdy obiekty mogą być przeniesione na następną stronę w sposób uporządkowany.  

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz następujące wymagania wstępne:

1. Java Development Kit (JDK): Upewnij się, że masz zainstalowany JDK w swoim systemie. Możesz go pobrać ze [strony internetowej](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Biblioteka Aspose.Note for Java: Pobierz i zainstaluj bibliotekę Aspose.Note for Java z [linku do pobrania](https://releases.aspose.com/note/java/).

## Importowanie pakietów

W swoim projekcie Java zaimportuj niezbędne pakiety, aby korzystać z funkcjonalności Aspose.Note.

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

Wybierz odpowiedni algorytm dzielenia zgodnie z Twoimi wymaganiami. Tutaj używamy `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, który zachowuje część obiektu na bieżącej stronie i klonuje pozostałą część na następną stronę.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Krok 5: Zapisz dokument

Zapisz dokument z określonymi opcjami zapisu PDF. Ten krok **generuje wyjściowy PDF z OneNote**, który możesz otworzyć, udostępnić lub wydrukować.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **Obiekty są przycinane przy granicach stron** | Spróbuj innego algorytmu, takiego jak `AlwaysSplitObjectsAlgorithm`, lub zwiększ wartość progową w `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **Wygenerowany PDF jest pusty** | Sprawdź, czy źródłowy plik `.one` nie jest uszkodzony oraz czy ścieżka `dataDir` jest poprawna. |
| **Wydajność jest niska przy dużych notatnikach** | Użyj `pdfSaveOptions.setCompressImages(true)`, aby zmniejszyć zużycie pamięci, i rozważ przetwarzanie notatnika w mniejszych sekcjach. |

## Najczęściej zadawane pytania

**Q: Czy mogę używać Aspose.Note for Java z innymi językami programowania?**  
A: Tak, Aspose.Note jest dostępny także dla .NET, C++ i Pythona.

**Q: Czy Aspose.Note nadaje się do przetwarzania dużych plików OneNote?**  
A: Zdecydowanie tak. Biblioteka jest zoptymalizowana pod kątem efektywnego obsługiwania dużych notatników.

**Q: Gdzie mogę znaleźć dodatkowe zasoby i wsparcie dla Aspose.Note?**  
A: Możesz odwołać się do [dokumentacji](https://reference.aspose.com/note/java/) i [forum](https://forum.aspose.com/c/note/28) w celu uzyskania pomocy i wskazówek.

**Q: Czy mogę wypróbować Aspose.Note przed zakupem?**  
A: Tak, możesz skorzystać z [bezpłatnej wersji próbnej](https://releases.aspose.com/), aby zapoznać się z funkcjami przed dokonaniem zakupu.

**Q: Jak mogę uzyskać tymczasową licencję dla Aspose.Note?**  
A: Możesz poprosić o [tymczasową licencję](https://purchase.aspose.com/temporary-license/), aby ocenić produkt w okresie próbnym.

---

**Ostatnia aktualizacja:** 2026-03-16  
**Testowano z:** Aspose.Note 24.12 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}