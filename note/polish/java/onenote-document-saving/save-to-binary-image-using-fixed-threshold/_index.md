---
date: 2025-12-13
description: Dowiedz się, jak dostosować próg, aby konwertować OneNote na PNG przy
  użyciu Aspose.Note Java, tworząc czarno‑białe obrazy OneNote za pomocą binaryzacji
  obrazu w Javie.
linktitle: Save to Binary Image Using Fixed Threshold in OneNote
second_title: Aspose.Note Java API
title: Jak dostosować próg przy zapisywaniu OneNote jako obrazu binarnego
url: /pl/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dostosować próg przy zapisywaniu OneNote jako obrazu binarnego

## Wprowadzenie

W tym samouczku odkryjesz **jak dostosować próg**, aby wyeksportować stronę Microsoft OneNote jako wysokiego kontrastu, czarno‑białą grafikę PNG. Poprzez regulację stałej wartości progu zyskasz precyzyjną kontrolę nad konwersją, co czyni ją idealną w scenariuszach takich jak wstępne przetwarzanie OCR lub archiwizacja dokumentów. Przejdziemy krok po kroku, używając Aspose.Note Java API, abyś mógł szybko **konwertować OneNote do PNG** przy użyciu niezawodnych technik **image binarization Java**.

## Szybkie odpowiedzi
- **Co oznacza „adjust threshold”?** Ustawia on punkt odcięcia intensywności pikseli używany przy konwersji obrazu kolorowego na czarno‑biały.
- **Jaki format jest tworzony?** Plik PNG, który może otworzyć każdy przeglądarka obrazów.
- **Czy mogę zmienić wartość progu?** Tak – zmodyfikuj wywołanie `setBinarizationThreshold()`.
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.
- **Czy jest to kompatybilne ze wszystkimi wersjami OneNote?** Aspose.Note obsługuje OneNote 2010, 2013, 2016 i nowsze.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

1. Zainstalowany Java Development Kit (JDK).
2. Bibliotekę Aspose.Note for Java pobraną z [here](https://releases.aspose.com/note/java/).
3. Podstawową znajomość składni Java.

## Importowanie pakietów

Najpierw zaimportuj wymagane klasy do swojego pliku źródłowego Java.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Krok 1: Załaduj dokument

Załaduj plik OneNote, który chcesz przetworzyć.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Krok 2: Ustaw opcje binaryzacji

Zdefiniuj ustawienia **image binarization Java** i określ stały próg, którego chcesz użyć.

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

> **Pro tip:** Eksperymentuj z wartościami progu od 0‑255, aby znaleźć optymalny punkt dla konkretnego dokumentu. Niższe wartości dają jaśniejsze obrazy, wyższe – ciemniejsze efekty.

## Krok 3: Ustaw opcje zapisu obrazu

Skonfiguruj format obrazu, tryb kolorów i dołącz opcje binaryzacji.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

Ustawienie `ColorMode.BlackAndWhite` zapewnia, że ostateczny plik będzie **czarno‑białym obrazem OneNote**.

## Krok 4: Zapisz dokument

Wykonaj operację zapisu z wcześniej zdefiniowanymi opcjami.

```java
oneFile.save(dataDir, options);
```

Po uruchomieniu kodu znajdziesz plik PNG o nazwie `SaveToBinaryImageUsingFixedThreshold_out.png` w folderze wyjściowym, gotowy do dalszego przetwarzania lub archiwizacji.

## Podsumowanie

Pokazaliśmy **jak dostosować próg**, aby uzyskać czysty, wysokiego kontrastu PNG z pliku OneNote przy użyciu Aspose.Note for Java. Opanowując opcje **image binarization Java**, możesz niezawodnie **konwertować OneNote do PNG** i tworzyć **czarno‑białe zasoby OneNote** do OCR, druku lub cyfrowej konserwacji.

## FAQ

### Q1: Czy mogę dostosować wartość progu binaryzacji?

A1: Tak, możesz zmienić wartość progu zgodnie z wymaganiami, modyfikując parametr metody `setBinarizationThreshold()`.

### Q2: Czy Aspose.Note for Java jest kompatybilny ze wszystkimi wersjami Microsoft OneNote?

A2: Aspose.Note for Java obsługuje różne wersje Microsoft OneNote, w tym 2010, 2013 i 2016.

### Q3: Czy istnieją ograniczenia co do rozmiaru dokumentów, które można przetworzyć?

A3: Aspose.Note for Java nie ma ograniczeń co do rozmiaru przetwarzanych dokumentów, co pozwala efektywnie obsługiwać duże pliki.

### Q4: Czy mogę konwertować wiele dokumentów OneNote jednocześnie?

A4: Tak, możesz przetwarzać wsadowo wiele dokumentów OneNote, iterując po każdym pliku i stosując niezbędne operacje.

### Q5: Czy dostępne jest wsparcie techniczne dla Aspose.Note for Java?

A5: Tak, wsparcie techniczne jest dostępne poprzez [Aspose.Note forum](https://forum.aspose.com/c/note/28), gdzie możesz zadawać pytania i uzyskać pomoc od ekspertów.

## Często zadawane pytania

**Q: Co się stanie, jeśli ustawiam próg zbyt nisko?**  
A: Uzyskany obraz może wyglądać wyblakło, z wieloma odcieniami szarości zamiast wyraźnego kontrastu czarno‑białego.

**Q: Czy mogę użyć innej metody binaryzacji?**  
A: Tak, Aspose.Note obsługuje także progowanie adaptacyjne; wystarczy zamienić `BinarizationMethod.FixedThreshold` na `BinarizationMethod.Adaptive`.

**Q: Czy można eksportować bezpośrednio do innych formatów, np. JPEG?**  
A: Oczywiście – zmień `SaveFormat.Png` na `SaveFormat.Jpeg` w konstruktorze `ImageSaveOptions`.

**Q: Jak obsłużyć pliki OneNote zabezpieczone hasłem?**  
A: Załaduj dokument przy użyciu odpowiedniego przeciążenia, które przyjmuje ciąg znaków hasła, przed zastosowaniem kroków binaryzacji.

**Q: Czy to podejście działa na Linux/macOS?**  
A: Biblioteka Aspose.Note Java jest niezależna od platformy, więc ten sam kod działa na każdym systemie operacyjnym z kompatybilnym JDK.

**Ostatnia aktualizacja:** 2025-12-13  
**Testowano z:** Aspose.Note for Java 24.12 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}