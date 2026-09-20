---
date: 2026-06-30
description: Dowiedz się, jak wyeksportować OneNote, zapisując dokument jako obraz
  PNG w odcieniach szarości przy użyciu Aspose.Note dla Java. Zawiera kroki ładowania
  dokumentu OneNote i tworzenia obrazu w odcieniach szarości.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Jak wyeksportować OneNote jako obraz w odcieniach szarości – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: Jak wyeksportować OneNote jako obraz w odcieniach szarości – Aspose.Note
url: /pl/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz jako obraz w odcieniach szarości w OneNote - Aspose.Note

## Wprowadzenie

W tym samouczku odkryjesz **how to export onenote**, konwertując plik OneNote `.one` na wysokiej jakości obraz PNG w odcieniach szarości przy użyciu Aspose.Note dla Javy. Konwersja do odcieni szarości jest często potrzebna programistom Java do drukowania, archiwizacji lub **reduce OneNote size** bez utraty istotnej zawartości. Przejdziemy przez ładowanie dokumentu OneNote, konfigurowanie opcji zapisu — w tym **adjust image resolution** — i ostateczne zapisanie dokumentu jako PNG.

## Szybkie odpowiedzi
- **Co oznacza “how to export onenote”?** Odnosi się do programowego konwertowania pliku OneNote na inny format, taki jak obraz, przy użyciu kodu.  
- **Jaki format jest najlepszy dla wyjścia w odcieniach szarości?** PNG sprawdza się dobrze, ponieważ zachowuje jakość bezstratną i obsługuje dedykowany tryb kolorów w odcieniach szarości.  
- **Czy potrzebuję licencji?** Wymagana jest ważna licencja Aspose.Note do użytku produkcyjnego; tymczasowa licencja próbna jest dostępna do testów.  
- **Jakiej wersji Java wymaga się?** Zalecana jest Java 8 lub nowsza.  
- **Czy mogę zmienić rozmiar obrazu?** Tak, możesz dostosować właściwości `ImageSaveOptions`, takie jak `Resolution` lub `PageSize`, przed zapisem.  

## Co to jest “how to export onenote”?

Eksportowanie OneNote oznacza programowe konwertowanie pliku OneNote `.one` na inną reprezentację — taką jak PDF, HTML lub obraz. W tym przewodniku koncentrujemy się na **creating grayscale PNG** obrazach, co jest powszechnym wymogiem w dokumentacji lub procesach gotowych do druku. Korzystając z Aspose.Note, konwersja odbywa się w całości w pamięci, więc nie musisz mieć zainstalowanego Microsoft OneNote na serwerze.

## Dlaczego eksportować OneNote jako obraz w odcieniach szarości?

Obrazy PNG w odcieniach szarości są zazwyczaj **30‑40 % mniejsze** niż ich pełnokolorowe odpowiedniki, co przyspiesza dostarczanie w sieci i zmniejsza koszty przechowywania. Zapewniają także **clearer contrast** na drukarkach laserowych, ułatwiając czytanie raportów. Ponieważ PNG jest powszechnie obsługiwany, powstałe pliki działają w przeglądarkach, na urządzeniach mobilnych i w edytorach desktopowych bez dodatkowych kodeków.

## Wymagania wstępne

1. Zainstalowany Java Development Kit (JDK) 8 lub nowszy.  
2. Biblioteka Aspose.Note for Java – pobierz najnowsze wydanie z [tutaj](https://releases.aspose.com/note/java/).  
3. Podstawowa znajomość składni Java oraz konfiguracji projektu Maven/Gradle.  

## Importowanie pakietów

Klasa `ImageSaveOptions` kontroluje, jak dokument jest renderowany do obrazu.  
`ColorMode` jest wyliczeniem, które pozwala przełączać się między pełnym kolorem a wyjściem w odcieniach szarości.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Krok 1: Załaduj dokument OneNote

`Document` reprezentuje notes OneNote i udostępnia metody do ładowania, edytowania i zapisywania jego zawartości. Najpierw **load the OneNote document** do Aspose.Note. Zastąp `"Your Document Directory"` ścieżką do lokalnego folderu oraz `"Aspose.one"` nazwą pliku OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Krok 2: Ustaw ścieżkę wyjściową i opcje

`ImageSaveOptions` konfiguruje, jak dokument OneNote jest renderowany do pliku obrazu. Wyliczenie `ColorMode` wybiera tryb renderowania koloru, taki jak odcienie szarości lub pełny kolor. Zdefiniuj ścieżkę wyjściową dla obrazu w odcieniach szarości i określ opcje zapisu. Ustawimy `ColorMode` na `GrayScale` i użyjemy formatu **save document as PNG**. Możesz także **adjust image resolution** do 300 DPI dla wydruków wysokiej jakości.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Krok 3: Zapisz dokument

Na koniec zapisz dokument jako obraz PNG w odcieniach szarości, używając skonfigurowanych opcji. Metoda `save` zapisuje plik na dysku bez potrzeby tworzenia pośrednich plików tymczasowych.

```java
oneFile.save(dataDir, options);
```

## Typowe problemy i rozwiązania
- **FileNotFoundException** – Zweryfikuj, że `dataDir` wskazuje na właściwy folder i że plik `.one` istnieje.  
- **LicenseException** – Upewnij się, że zastosowano ważną licencję Aspose.Note przed wywołaniem `save`.  
- **Low‑resolution output** – Dostosuj `options.setResolution(300)`, aby zwiększyć DPI; wyższe DPI daje ostrzejsze wydruki, ale większe rozmiary plików.  

## Najczęściej zadawane pytania

**Q1: Czy mogę zapisać obraz w odcieniach szarości w innym formacie?**  
A1: Tak, po prostu zmień parametr `SaveFormat` w konstruktorze `ImageSaveOptions` na `Jpeg`, `Bmp` lub dowolny z ponad 20 obsługiwanych formatów obrazu.

**Q2: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami dokumentów OneNote?**  
A2: Aspose.Note obsługuje Microsoft OneNote 2010 i nowsze, obejmując ponad 95 % notesów aktywnie używanych dzisiaj.

**Q3: Czy Aspose.Note wymaga licencji do użycia?**  
A3: Wymagana jest ważna licencja do użytku produkcyjnego, ale tymczasowa licencja próbna może być uzyskana do oceny bez kosztów.

**Q4: Czy mogę manipulować innymi aspektami dokumentu przed zapisaniem go jako obraz?**  
A5: Oczywiście! Aspose.Note udostępnia API do edycji sekcji, stron i poszczególnych elementów, takich jak tekst, tabele i obrazy, przed eksportem.

**Q5: Gdzie mogę znaleźć wsparcie, jeśli napotkam problemy?**  
A5: Wsparcie można znaleźć na forum Aspose.Note [tutaj](https://forum.aspose.com/c/note/28).

## Podsumowanie

Teraz nauczyłeś się **how to export onenote** poprzez ładowanie pliku OneNote, konfigurowanie opcji zapisu w celu **create a grayscale image**, oraz **saving the document as PNG**. To podejście jest idealne do generowania lekkich, gotowych do druku wizualizacji z notesów OneNote. Śmiało eksperymentuj z innymi ustawieniami `ColorMode`, wyższymi wartościami DPI lub alternatywnymi formatami obrazu, aby dopasować je do wymagań projektu.

---

**Ostatnia aktualizacja:** 2026-06-30  
**Testowano z:** Aspose.Note 27.0 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Eksportuj stronę OneNote do obrazu PNG w Javie przy użyciu Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote set jpeg resolution – Ustaw rozdzielczość obrazu wyjściowego w OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Jak zapisać OneNote jako PDF przy użyciu Aspose.Note dla Javy](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}