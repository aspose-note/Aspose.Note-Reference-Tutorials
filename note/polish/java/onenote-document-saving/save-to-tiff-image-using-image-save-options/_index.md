---
date: 2026-03-14
description: Dowiedz się, jak zapisywać dokumenty OneNote jako pliki TIFF, używając
  kompresji TIFF JPEG, kompresji TIFF PackBits lub CCITT Group 3 Fax w Javie. Kontroluj
  jakość obrazu, rozmiar pliku i tryb kolorów za pomocą Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Zapisz do obrazu TIFF przy użyciu kompresji TIFF JPEG w OneNote
url: /pl/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

b kolorów i rozdzielczość, aby spełnić konkretne wymagania dotyczące **tiff image quality**, i zintegrować te metody w procesach wsadowych dla maksymalnej wydajności."

Then horizontal rule stays.

"**Last Updated:** 2026-03-14" keep same.

"**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)" keep.

"**Author:** Aspose" keep.

Then closing shortcodes.

Finally backtop button shortcode.

Make sure to keep all shortcodes exactly.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz obraz TIFF przy użyciu kompresji TIFF JPEG w OneNote

## Wprowadzenie

W tym samouczku odkryjesz **how to save a OneNote document to a TIFF file using TIFF JPEG compression** oraz dwie inne popularne metody kompresji. Przeprowadzimy Cię przez niezbędną konfigurację, import niezbędnych pakietów Java i dostarczymy przejrzysty kod krok po kroku dla każdej opcji kompresji. Po zakończeniu będziesz mógł kontrolować **TIFF image quality**, zmniejszyć rozmiar pliku i nawet tworzyć czarno‑białe pliki TIFF w stylu faksu.

## Szybkie odpowiedzi
- **What is TIFF JPEG compression?** Metoda kompresji stratnej, która zmniejsza rozmiar pliku TIFF przy zachowaniu jakości wizualnej.  
- **Which library handles the conversion?** Aspose.Note for Java.  
- **Do I need a license?** Darmowa wersja próbna działa do testów; licencja jest wymagana w środowisku produkcyjnym.  
- **Can I change the image quality?** Tak, ustaw właściwość `quality` w `ImageSaveOptions`.  
- **Is batch conversion possible?** Absolutnie – iteruj przez dokumenty i zastosuj te same opcje.

## Co to jest kompresja TIFF JPEG?

Kompresja TIFF JPEG przechowuje dane obrazu w kontenerze TIFF, ale stosuje algorytm JPEG (stratny), aby zmniejszyć plik. Jest idealna, gdy potrzebujesz równowagi między **tiff image quality** a mniejszym rozmiarem pliku, szczególnie w scenariuszach internetowych lub archiwalnych.

## Dlaczego używać różnych typów kompresji TIFF?
- **JPEG** – Dobre dla fotografii; oferuje regulowaną jakość.  
- **PackBits** – Proste, bezstratne kodowanie długości serii; przydatne dla grafiki z dużymi jednolitymi obszarami.  
- **CCITT Group 3 Fax** – Tylko czarno‑białe; idealne dla zeskanowanych dokumentów i transmisji faksu.  

Wybór odpowiedniej kompresji pozwala spełnić ograniczenia przechowywania bez utraty wizualnej wierności wymaganej przez Twoją aplikację.

## Konwertuj One na TIFF przy użyciu Aspose.Note
Jeśli Twoim celem jest **convert OneNote to TIFF**, poniższe trzy metody obejmują najczęstsze scenariusze. Każda metoda ładuje plik `.one`, konfiguruje `ImageSaveOptions` i zapisuje wynik jako plik `.tiff`.

## Wymagania wstępne

- Zainstalowany Java Development Kit (JDK).  
- Biblioteka Aspose.Note for Java dodana do projektu (Maven/Gradle lub ręczny JAR).  
- Podstawowa znajomość składni Java.

## Importowanie pakietów

Najpierw zaimportuj niezbędne klasy Aspose.Note do swojego pliku Java:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Krok 1: Zapisz jako TIFF przy użyciu kompresji TIFF JPEG

Poniżej znajduje się pełna metoda, która ładuje plik OneNote i zapisuje go jako TIFF z kompresją JPEG. Dostosuj wartość `quality` (0‑100), aby kontrolować **tiff image quality**.

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

- `ImageSaveOptions` informuje Aspose.Note, aby wyjściowo generował plik TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` wybiera kompresję JPEG.  
- `setQuality(93)` (opcjonalnie) precyzyjnie dostraja jakość obrazu; niższe wartości generują mniejsze pliki.

### Jak zapisać TIFF z kompresją JPEG w Javie
1. Ustaw `dataDir` na folder zawierający Twój plik `.one`.  
2. Wywołaj `SaveToTiffUsingJpegCompression()` z metody main lub serwisu.  
3. Wynikowy plik `.tiff` pojawi się w tym samym katalogu.

## Przegląd kompresji TIFF PackBits

PackBits to bezstratny algorytm kompresji, który najlepiej sprawdza się w obrazach z dużymi obszarami jednolitego koloru. Często w dokumentacji określany jest jako **tiff packbits compression**.

## Krok 2: Zapisz jako TIFF przy użyciu kompresji PackBits

Jeśli potrzebujesz opcji bezstratnej, PackBits jest prostym algorytmem długości serii, który dobrze działa dla grafiki z jednolitymi kolorami.

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

## Krok 3: Zapisz jako TIFF przy użyciu kompresji CCITT Group 3 Fax (czarno‑biały TIFF)

Dla dokumentów w stylu faksu często potrzebny jest **black and white TIFF**. CCITT Group 3 zapewnia wysoką kompresję dla obrazów monochromatycznych.

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

| Issue | Solution |
|-------|----------|
| **Plik wyjściowy jest większy niż oczekiwano** | Spróbuj zmniejszyć wartość `quality` JPEG lub przełącz się na PackBits, jeśli akceptujesz kompresję bezstratną. |
| **Kolory wyglądają wyblakłe** | Upewnij się, że nie ustawiłeś przypadkowo `ColorMode.BlackAndWhite`, gdy potrzebny jest pełny kolor. |
| **Błąd nieobsługiwanego formatu obrazu** | Sprawdź, czy używasz najnowszej wersji Aspose.Note; starsze kompilacje mogą nie zawierać niektórych enumów kompresji. |
| **LicenseException w czasie wykonywania** | Zainstaluj ważną licencję Aspose.Note (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Najczęściej zadawane pytania

**Q: Czy mogę konwertować inne typy dokumentów (np. PDF, DOCX) na TIFF przy użyciu tych opcji?**  
A: Tak. Choć Aspose.Note koncentruje się na plikach OneNote, biblioteki Aspose.PDF, Aspose.Words i inne oferują podobne `ImageSaveOptions` dla swoich formatów.

**Q: Czym różni się kompresja TIFF JPEG od standardowego pliku JPEG?**  
A: Algorytm JPEG jest taki sam, ale dane obrazu znajdują się wewnątrz kontenera TIFF, który może zawierać wiele stron i bogatsze metadane.

**Q: Czy możliwe jest przetwarzanie wsadowe wielu plików `.one`?**  
A: Absolutnie. Iteruj po katalogu, wywołuj dowolną z trzech metod dla każdego pliku i zbieraj powstałe pliki TIFF.

**Q: Czy mogę kontrolować DPI/rozdzielczość wyjściowego TIFF?**  
A: Tak. Użyj `options.setResolution(int dpi)` przed zapisem.

**Q: Czy Aspose.Note obsługuje przetwarzanie asynchroniczne?**  
A: Sam interfejs API jest synchroniczny, ale możesz owinąć wywołania w `CompletableFuture` Javy lub pulę wątków, aby uzyskać równoległe wykonanie.

## Zakończenie

Masz teraz kompletny zestaw narzędzi **java tiff conversion**, który pozwala zapisywać dokumenty OneNote jako pliki TIFF przy użyciu kompresji JPEG, PackBits lub CCITT Group 3 Fax. Dostosuj jakość, tryb kolorów i rozdzielczość, aby spełnić konkretne wymagania dotyczące **tiff image quality**, i zintegrować te metody w procesach wsadowych dla maksymalnej wydajności.

---

**Last Updated:** 2026-03-14  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}