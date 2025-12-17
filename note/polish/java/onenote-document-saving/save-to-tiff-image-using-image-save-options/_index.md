---
date: 2025-12-17
description: „Dowiedz się, jak zapisywać dokumenty OneNote jako pliki TIFF, używając
  kompresji TIFF JPEG, PackBits lub CCITT Group 3 Fax w Javie. Kontroluj jakość obrazu,
  rozmiar pliku i tryb kolorów za pomocą Aspose.Note.”
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Zapisz do obrazu TIFF przy użyciu kompresji TIFF JPEG w OneNote
url: /pl/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz jako obraz TIFF przy użyciu kompresji TIFF JPEG w OneNote

## Wprowadzenie

W tym samouczku poznasz **sposób zapisywania dokumentu OneNote jako pliku TIFF przy użyciu kompresji TIFF JPEG** oraz dwóch innych popularnych metod kompresji. Przeprowadzimy Cię przez niezbędną konfigurację, zaimportujemy wymagane pakiety Java i przedstawimy przejrzysty kod krok po kroku dla każdej opcji kompresji. Po zakończeniu będziesz mógł kontrolować **jakość obrazu TIFF**, zmniejszyć rozmiar pliku i nawet tworzyć czarno‑białe pliki TIFF przeznaczone do faksu.

## Szybkie odpowiedzi
- **Czym jest kompresja TIFF JPEG?** Metoda kompresji stratnej, która zmniejsza rozmiar pliku TIFF przy zachowaniu jakości wizualnej.  
- **Która biblioteka obsługuje konwersję?** Aspose.Note for Java.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarczy do testów; licencja jest wymagana w środowisku produkcyjnym.  
- **Czy mogę zmienić jakość obrazu?** Tak, ustawiając właściwość `quality` w `ImageSaveOptions`.  
- **Czy konwersja wsadowa jest możliwa?** Oczywiście – można iterować po dokumentach i stosować te same opcje.

## Co to jest kompresja TIFF JPEG?
Kompresja TIFF JPEG przechowuje dane obrazu w kontenerze TIFF, ale stosuje algorytm JPEG (stratny) w celu zmniejszenia pliku. Jest idealna, gdy potrzebujesz kompromisu między **jakością obrazu TIFF** a mniejszym rozmiarem pliku, szczególnie w zastosowaniach internetowych lub archiwalnych.

## Dlaczego używać różnych typów kompresji TIFF?
- **JPEG** – Dobre dla fotografii; oferuje regulowaną jakość.  
- **PackBits** – Prosta, bezstratna metoda kodowania długości serii; przydatna przy grafice z dużymi jednolitymi obszarami.  
- **CCITT Group 3 Fax** – Tylko czarno‑białe; idealne dla zeskanowanych dokumentów i transmisji faksowej.  

Wybór odpowiedniej kompresji pozwala spełnić ograniczenia przechowywania bez utraty wymaganego poziomu wierności wizualnej.

## Wymagania wstępne

- Zstalowany Java Development Kit (JDK).  
- Biblioteka Aspose.Note for Java dodana do projektu (Maven/Gradle lub ręcznie jako JAR).  
- Podstawowa znajomość składni języka Java.

## Importowanie pakietów

Najpierw zaimportuj niezbędne klasy Aspose.Note do swojego pliku Java:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Krok 1: Zapisz jako TIFF przy użyciu kompresji TIFF JPEG

Poniżej znajduje się pełna metoda, która wczytuje plik OneNote i zapisuje go jako TIFF z kompresją JPEG. Dostosuj wartość `quality` (0‑100), aby kontrolować **jakość obrazu TIFF**.

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

- `ImageSaveOptions` informuje Aspose.Note, że ma wygenerować plik TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` wybiera kompresję JPEG.  
- `setQuality(93)` (opcjonalnie) precyzuje jakość obrazu; niższe wartości dają mniejsze pliki.

### Jak zapisać TIFF z kompresją JPEG w Javie
1. Ustaw `dataDir` na folder zawierający plik `.one`.  
2. Wywołaj `SaveToTiffUsingJpegCompression()` z metody `main` lub usługi.  
3. Powstały plik `.tiff` pojawi się w tym samym katalogu.

## Krok 2: Zapisz jako TIFF przy użyciu kompresji PackBits

Jeśli potrzebujesz opcji bezstratnej, PackBits to prosty algorytm kodowania długości serii, który sprawdza się przy grafice z jednolitymi kolorami.

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

Dla dokumentów w stylu faksu często potrzebny jest **czarno‑biały TIFF**. CCITT Group 3 zapewnia wysoką kompresję dla obrazów monochromatycznych.

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
| **Plik wyjściowy jest większy niż oczekiwano** | Spróbuj obniżyć wartość `quality` w JPEG lub przełącz się na PackBits, jeśli bezstratność jest dopuszczalna. |
| **Kolory wyglądają wyblakłe** | Upewnij się, że nie ustawiasz przypadkowo `ColorMode.BlackAndWhite`, gdy potrzebny jest pełny kolor. |
| **Błąd nieobsługiwanego formatu obrazu** | Sprawdź, czy używasz najnowszej wersji Aspose.Note; starsze wersje mogą nie zawierać niektórych enumów kompresji. |
| **LicenseException w czasie działania** | Zainstaluj ważną licencję Aspose.Note (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Najczęściej zadawane pytania

**P: Czy mogę konwertować inne typy dokumentów (np. PDF, DOCX) do TIFF przy użyciu tych opcji?**  
O: Tak. Aspose.Note koncentruje się na plikach OneNote, ale inne biblioteki Aspose (PDF, Words) oferują podobne `ImageSaveOptions` dla swoich formatów.

**P: czym różni się kompresja TIFF JPEG od standardowych plików JPEG?**  
O: Dane obrazu są przechowywane wewnątrz kontenera TIFF, co zachowuje metadane i umożliwia wiele stron, podczas gdy algorytm kompresji pozostaje JPEG.

**P: Czy można przetwarzać wsadowo wiele plików `.one`?**  
O: Oczywiście. Przejdź po folderze, wywołaj jedną z trzech metod dla każdego pliku i zbierz powstałe pliki TIFF.

**P: Czy mogę kontrolować DPI/rozdzielczość wyjściowego TIFF?**  
O: Tak. Użyj `options.setResolution(int dpi)` przed zapisem.

**P: Czy Aspose.Note obsługuje przetwarzanie asynchroniczne?**  
O: API jest synchroniczne, ale możesz owinąć wywołania w `CompletableFuture` lub puli wątków Javy, aby uzyskać równoległe wykonywanie.

## Zakończenie

Masz teraz kompletny zestaw narzędzi **java tiff conversion**, który pozwala zapisywać dokumenty OneNote jako pliki TIFF przy użyciu kompresji JPEG, PackBits lub CCITT Group 3 Fax. Dostosuj jakość, tryb kolorów i rozdzielczość, aby spełnić konkretne wymagania **jakości obrazu TIFF**, i włącz te metody do przepływów wsadowych dla maksymalnej wydajności.

---

**Ostatnia aktualizacja:** 2025-12-17  
**Testowano z:** Aspose.Note for Java 23.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}