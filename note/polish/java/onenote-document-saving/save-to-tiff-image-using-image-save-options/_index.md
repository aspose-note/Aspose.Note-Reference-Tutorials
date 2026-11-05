---
date: 2026-11-05
description: Dowiedz się, jak zmniejszyć rozmiar pliku TIFF przy konwertowaniu notatników
  OneNote do formatu TIFF w Javie przy użyciu Aspose.Note. Zawiera opcje JPEG, PackBits
  oraz czarno‑białe TIFF.
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: Jak zmniejszyć rozmiar pliku TIFF przy konwertowaniu OneNote w Javie
og_description: Dowiedz się, jak zmniejszyć rozmiar pliku TIFF przy konwertowaniu
  notatników OneNote do formatu TIFF w Javie przy użyciu Aspose.Note. Zawiera opcje
  JPEG, PackBits oraz czarno‑białe TIFF.
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: Jak zmniejszyć rozmiar pliku TIFF przy konwertowaniu OneNote w Javie
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: Jak zmniejszyć rozmiar pliku TIFF przy konwertowaniu OneNote w Javie
url: /pl/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak zmniejszyć rozmiar pliku TIFF przy konwertowaniu OneNote w Javie

## Wprowadzenie

W tym samouczku odkryjesz, jak **zredukować rozmiar pliku TIFF** podczas konwertowania notatników OneNote na obrazy TIFF przy użyciu Aspose.Note for Java. Przejdziemy przez trzy metody kompresji — TIFF JPEG, PackBits i CCITT Group 3 (czarno‑biały TIFF) — pokażemy, jak dostosować jakość obrazu, kontrolować tryb kolorów i utrzymać rozmiary plików optymalne dla scenariuszy internetowych, archiwalnych lub faksowych.

## Szybkie odpowiedzi
- **Czym jest kompresja TIFF JPEG?** Metoda kompresji stratnej, która zmniejsza rozmiar pliku TIFF przy zachowaniu jakości wizualnej.  
- **Która biblioteka obsługuje konwersję?** Aspose.Note for Java.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa do testów; licencja jest wymagana w środowisku produkcyjnym.  
- **Czy mogę zmienić jakość obrazu?** Tak, ustaw właściwość `quality` w `ImageSaveOptions`.  
- **Czy konwersja wsadowa jest możliwa?** Zdecydowanie – iteruj po dokumentach i zastosuj te same opcje.

## Przegląd kompresji TIFF JPEG

Kompresja TIFF JPEG przechowuje dane obrazu w kontenerze TIFF, ale stosuje stratny algorytm JPEG, aby zmniejszyć plik. Jest idealna, gdy potrzebny jest kompromis między **jakością obrazu TIFF** a mniejszym rozmiarem pliku, szczególnie w scenariuszach internetowych lub archiwalnych.

## Dlaczego używać różnych typów kompresji TIFF?

Wybierasz typ kompresji w zależności od zawartości i potrzeb przechowywania: JPEG sprawdza się najlepiej w przypadku fotografii, PackBits zapewnia bezstratną kompresję dla grafik z dużymi jednolitymi obszarami, a CCITT Group 3 oferuje wysokoratio kompresję dla monochromatycznych dokumentów w stylu faksu. Wybranie odpowiedniej metody pozwala **zredukować rozmiar pliku TIFF** bez uszczerbku dla jakości wizualnej wymaganej przez Twoją aplikację.

## Wybór odpowiedniej kompresji

- **JPEG** – Regulowana jakość (0‑100) pozwala na kompromis między rozmiarem a szczegółowością, idealna dla stron bogatych w kolory.  
- **PackBits** – Bezstratne kodowanie długości serii; idealne, gdy musisz zachować każdy piksel dokładnie.  
- **CCITT Group 3** – Tylko monochromatyczne; maksymalizuje kompresję dla zeskanowanego tekstu lub dokumentów faksowych.  

## Konwertuj OneNote do TIFF przy użyciu Aspose.Note

Jeśli Twoim celem jest **konwersja OneNote do TIFF**, poniższe trzy metody obejmują najczęstsze scenariusze. Każda metoda ładuje plik `.one`, konfiguruje `ImageSaveOptions` i zapisuje wynik jako plik `.tiff`.

## Wymagania wstępne

- Zainstalowany Java Development Kit (JDK).  
- Biblioteka Aspose.Note for Java dodana do projektu (Maven/Gradle lub ręczny JAR).  
- Podstawowa znajomość składni Javy.

## Importowanie pakietów

Klasy `ImageSaveOptions`, `TiffCompression` i `ColorMode` są rdzeniem API konwersji.

`ImageSaveOptions` definiuje opcje zapisu obrazów, takie jak format i kompresja.  
`TiffCompression` wymienia obsługiwane algorytmy kompresji TIFF.  
`ColorMode` określa głębię kolorów, np. kolor lub czarno‑biały.  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Krok 1: zapisz do TIFF przy użyciu kompresji TIFF JPEG

### Zapisywanie TIFF z kompresją JPEG w Javie

Wczytaj plik OneNote, skonfiguruj `ImageSaveOptions` z kompresją JPEG, opcjonalnie ustaw wartość `quality` i wywołaj metodę zapisu. Ten dwustopniowy wzorzec daje pełną kontrolę nad rozmiarem wyjściowym i jakością wizualną.

1. Ustaw `dataDir` na folder zawierający Twój plik `.one`.  
2. Wywołaj `SaveToTiffUsingJpegCompression()` z metody głównej lub serwisu.  
3. Powstały plik `.tiff` pojawi się w tym samym katalogu.

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Wyjaśnienie**

- `ImageSaveOptions` informuje Aspose.Note, aby wyjściowy plik był w formacie TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` wybiera kompresję JPEG.  
- `setQuality(93)` (opcjonalnie) precyzyjnie dostraja jakość obrazu; niższe wartości dają mniejsze pliki.

## Przegląd kompresji TIFF PackBits

PackBits to bezstratny algorytm kompresji, który działa najlepiej dla obrazów z dużymi obszarami jednolitego koloru. Często określany jest w dokumentacji jako **kompresja tiff packbits**.

## Zapisywanie TIFF z kompresją PackBits w Javie

Jeśli potrzebujesz opcji bezstratnej, PackBits jest prostym algorytmem kodowania długości serii, który sprawdza się w grafice o jednolitych kolorach. Skonfiguruj `ImageSaveOptions` z `TiffCompression.PackBits` i zapisz dokument.

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Wyjaśnienie**

- `setTiffCompression(TiffCompression.PackBits)` przełącza metodę kompresji.  
- Ustawienie jakości nie jest potrzebne, ponieważ PackBits jest bezstratny.

## Zapisywanie TIFF z kompresją CCITT Group 3 w Javie

Dla dokumentów w stylu faksu często potrzebny jest **czarno‑biały TIFF**. CCITT Group 3 zapewnia wysoką kompresję dla obrazów monochromatycznych. Ustaw tryb koloru na czarno‑biały i wybierz enum kompresji CCITT 3.

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Wyjaśnienie**

- `setColorMode(ColorMode.BlackAndWhite)` wymusza wyjście monochromatyczne.  
- `setTiffCompression(TiffCompression.Ccitt3)` stosuje kompresję przeznaczoną do faksu.

## Typowe problemy i wskazówki

| Problem | Rozwiązanie |
|-------|----------|
| **Plik wyjściowy jest większy niż oczekiwano** | Spróbuj zmniejszyć wartość `quality` JPEG lub przełącz na PackBits, jeśli akceptowalna jest kompresja bezstratna. |
| **Kolory wyglądają wyblakłe** | Upewnij się, że nie ustawiłeś przypadkowo `ColorMode.BlackAndWhite`, gdy potrzebny jest pełny kolor. |
| **Błąd nieobsługiwanego formatu obrazu** | Sprawdź, czy używasz najnowszej wersji Aspose.Note; starsze kompilacje mogą nie zawierać niektórych enumów kompresji. |
| **LicenseException w czasie działania** | Zainstaluj ważną licencję Aspose.Note (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Najczęściej zadawane pytania

**Q: Czy mogę konwertować inne typy dokumentów (np. PDF, DOCX) do TIFF przy użyciu tych opcji?**  
A: Tak. Choć Aspose.Note koncentruje się na plikach OneNote, biblioteki Aspose.PDF, Aspose.Words i inne oferują podobne `ImageSaveOptions` dla swoich formatów.

**Q: czym różni się kompresja TIFF JPEG od standardowego pliku JPEG?**  
A: Algorytm JPEG jest taki sam, ale dane obrazu znajdują się wewnątrz kontenera TIFF, który może zawierać wiele stron i bogatsze metadane.

**Q: Czy można przetwarzać wsadowo wiele plików `.one`?**  
A: Zdecydowanie. Iteruj po katalogu, wywołaj jedną z trzech metod dla każdego pliku i zbierz powstałe pliki TIFF.

**Q: Czy mogę kontrolować DPI/rozdzielczość wyjściowego TIFF?**  
A: Tak. Użyj `options.setResolution(int dpi)` przed zapisem.

**Q: Czy Aspose.Note obsługuje przetwarzanie asynchroniczne?**  
A: Same API jest synchroniczne, ale możesz owinąć wywołania w `CompletableFuture` Javy lub pulę wątków w celu równoległego wykonania.

## Zakończenie

Masz teraz kompletny zestaw narzędzi **konwersji TIFF w Javie**, który pozwala **zredukować rozmiar pliku TIFF** przy zapisywaniu dokumentów OneNote jako pliki TIFF przy użyciu kompresji JPEG, PackBits lub CCITT Group 3 Fax. Dostosuj jakość, tryb kolorów i rozdzielczość, aby spełnić konkretne wymagania, i zintegrować te metody w procesach wsadowych dla maksymalnej wydajności.

---

**Ostatnia aktualizacja:** 2026-11-05  
**Testowano z:** Aspose.Note for Java 26.4 (latest at time of writing)  
**Autor:** Aspose

## Powiązane samouczki

- [Jak renderować obraz strony OneNote (JPEG) przy użyciu formatu zapisu z Aspose.Note dla Javy](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Użyj Aspose.Note dla Javy, aby zapisać OneNote jako PNG z opcjami – konwersja notatnika na obraz](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [Jak wyeksportować OneNote jako obraz w odcieniach szarości – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}