---
date: 2025-11-29
description: Dowiedz się, jak wyeksportować stronę OneNote do formatu PNG przy użyciu
  Aspose.Note dla Javy. Postępuj zgodnie z instrukcjami krok po kroku, aby ustawić
  indeks strony, przekonwertować stronę i zapisać obraz.
language: pl
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Eksportuj stronę OneNote do obrazu PNG w Javie przy użyciu Aspose.Note
url: /java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportowanie strony OneNote do obrazu PNG w Javie przy użyciu Aspose.Note

## Wprowadzenie

W tym samouczku dowiesz się **jak wyeksportować stronę OneNote** do obrazu PNG przy użyciu biblioteki Aspose.Note dla Javy. Przejdziemy krok po kroku przez wszystko, co jest potrzebne — od przygotowania środowiska, przez ustawienie indeksu strony, aż po zapisanie jej jako wysokiej jakości plik PNG. Po zakończeniu będziesz mógł dodać tę funkcjonalność do dowolnej aplikacji Java pracującej z dokumentami OneNote.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.Note dla Javy.  
- **Czy mogę wyeksportować pojedynczą stronę?** Tak — użyj `setPageIndex`, aby wybrać konkretną stronę.  
- **Jakie formaty obrazu są obsługiwane?** PNG, JPEG, GIF, BMP, TIFF (tutaj pokazano PNG).  
- **Czy potrzebna jest licencja?** Dostępna jest darmowa wersja próbna; licencja jest wymagana w środowisku produkcyjnym.  
- **Jak długo trwa implementacja?** Zazwyczaj mniej niż 10 minut dla podstawowej konwersji.

## Co to jest „export OneNote page”?
Eksportowanie strony OneNote oznacza konwersję konkretnej strony wewnątrz dokumentu `.one` na samodzielny plik obrazu (w tym przypadku PNG). Jest to przydatne, gdy trzeba udostępnić, osadzić lub przetworzyć zawartość OneNote poza środowiskiem OneNote.

## Dlaczego warto używać Aspose.Note dla Javy do konwersji OneNote na PNG?
- **Brak zależności od Microsoft Office** – działa na każdej platformie obsługującej Javę.  
- **Precyzyjna kontrola** – możesz wybrać dowolną stronę za pomocą `setPageIndex`.  
- **Wysokiej jakości wynik** – PNG zachowuje grafikę wektorową i klarowność tekstu.  
- **Gotowość do przetwarzania wsadowego** – łatwo pętlić po stronach w celu masowej konwersji.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

1. **Java Development Kit (JDK)** – wersja 8 lub wyższa.  
2. **Aspose.Note dla Javy** – pobierz najnowszy plik JAR z [strony Aspose](https://releases.aspose.com/note/java/).  
3. **Dokument OneNote** (`.one`) zawierający stronę, którą chcesz wyeksportować.

## Importowanie pakietów

Najpierw zaimportuj niezbędne klasy Javy:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Przewodnik krok po kroku

### Krok 1: Załaduj dokument OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Używamy klasy `Document`, aby odczytać plik OneNote z dysku. Obiekt `LoadOptions` pozwala w razie potrzeby dostosować zachowanie ładowania.

### Krok 2: Zainicjalizuj ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` informuje Aspose.Note, że chcemy uzyskać wynik w formacie **PNG**. Możesz przełączyć się na JPEG, BMP itp., zmieniając `SaveFormat`.

### Krok 3: Ustaw indeks strony (Jak konwertować stronę OneNote)

```java
// set page index
opts.setPageIndex(0);
```

Metoda `setPageIndex` wybiera, którą stronę wyeksportować. Numeracja stron zaczyna się od **0**, więc `0` oznacza pierwszą stronę. Zmień tę wartość, aby wyeksportować inną stronę.

### Krok 4: Zapisz dokument jako PNG (Zapisz OneNote jako PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Wywołanie `save` zapisuje wybraną stronę do pliku PNG na dysku. Nazwa pliku `ConvertSpecificPageToPngImage_out.png` jest tylko przykładem — możesz użyć dowolnej nazwy.

## Typowe problemy i wskazówki

- **Nieprawidłowy indeks strony** – Pamiętaj, że indeksowanie zaczyna się od 0. Jeśli otrzymasz pusty obraz, sprawdź wartość indeksu.  
- **Brak pliku JAR Aspose.Note** – Upewnij się, że JAR znajduje się w classpath; w przeciwnym razie pojawi się `ClassNotFoundException`.  
- **Duże strony** – Dla bardzo dużych stron rozważ zwiększenie pamięci przydzielonej JVM (`-Xmx`), aby uniknąć `OutOfMemoryError`.

## Najczęściej zadawane pytania

### Q1: Czy mogę konwertować wiele stron na obrazy PNG jednocześnie przy użyciu Aspose.Note dla Javy?
A1: Tak, możesz iterować po stronach dokumentu, aktualizować `opts.setPageIndex(i)` i wywoływać `save` dla każdej iteracji.

### Q2: Czy Aspose.Note dla Javy obsługuje inne formaty obrazu poza PNG?
A2: Oczywiście. Możesz ustawić `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` lub `SaveFormat.Tiff` w `ImageSaveOptions`.

### Q3: Czy dostępna jest darmowa wersja próbna Aspose.Note dla Javy?
A3: Tak, możesz pobrać darmową wersję próbną z [strony internetowej](https://releases.aspose.com/).

### Q4: Czy mogę uzyskać pomoc techniczną, jeśli napotkam problemy z Aspose.Note dla Javy?
A4: Oczywiście, wsparcie możesz uzyskać na forum społeczności Aspose [tutaj](https://forum.aspose.com/c/note/28).

### Q5: Gdzie mogę kupić licencję na Aspose.Note dla Javy?
A5: Licencję można nabyć na [stronie zakupu](https://purchase.aspose.com/buy).

### Q6: Jak wyeksportować stronę zawierającą osadzone obrazy?
A6: Osadzone obrazy są renderowane automatycznie w wyjściowym pliku PNG; nie wymaga to dodatkowego kodu.

### Q7: Czy mogę ustawić DPI lub rozdzielczość obrazu?
A7: Tak, użyj `opts.setResolution(int dpi)` przed wywołaniem `save`, aby kontrolować jakość wyjścia.

---

**Ostatnia aktualizacja:** 2025-11-29  
**Testowano z:** Aspose.Note dla Javy 24.11 (najnowsza)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
