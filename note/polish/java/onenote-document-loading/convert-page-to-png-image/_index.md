---
date: 2026-02-05
description: Dowiedz się, jak eksportować strony OneNote i zapisywać OneNote jako
  obraz. Ten przewodnik pokazuje, jak konwertować pliki .one na PNG, ustawiać indeks
  strony oraz eksportować obraz strony OneNote przy użyciu Aspose.Note dla Javy.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Jak wyeksportować stronę OneNote do obrazu PNG w Javie przy użyciu Aspose.Note
url: /pl/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportowanie strony OneNote do obrazu PNG w Javie przy użyciu Aspose.Note

## Wprowadzenie

W tym samouczku odkryjesz **jak wyeksportować stronę OneNote** do obrazu PNG przy użyciu biblioteki Aspose.Note for Java. **Jak wyeksportować onenote** strony to powszechna potrzeba, gdy chcesz udostępniać notatki poza ekosystemem OneNote, osadzać je w raportach lub przetwarzać za pomocą narzędzi do przetwarzania obrazów. Przejdziemy przez wszystko, czego potrzebujesz — od przygotowania środowiska, przez ustawienie indeksu strony, konwersję strony, po zapisanie wyniku jako wysokiej jakości plik PNG. Po zakończeniu będziesz mógł **zapisać onenote jako obraz** w dowolnej aplikacji Java.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebujesz?** Aspose.Note for Java.  
- **Czy mogę wyeksportować pojedynczą stronę?** Tak — użyj `setPageIndex`, aby wybrać dokładną stronę.  
- **Obsługiwane formaty obrazów?** PNG, JPEG, GIF, BMP, TIFF (tutaj pokazano PNG).  
- **Czy potrzebna jest licencja?** Dostępna jest darmowa wersja próbna; licencja jest wymagana w środowisku produkcyjnym.  
- **Jak długo trwa implementacja?** Zazwyczaj poniżej 10 minut dla podstawowej konwersji.  
- **Jak przekonwertować .one na png?** Załaduj plik `.one` przy użyciu `Document`, ustaw indeks strony i zapisz przy użyciu `ImageSaveOptions`.  

## Czym jest „eksportowanie strony OneNote”?

Eksportowanie strony OneNote oznacza konwersję konkretnej strony wewnątrz dokumentu `.one` do samodzielnego pliku obrazu (w tym przypadku PNG). Jest to przydatne, gdy potrzebujesz **wyeksportować obraz strony onenote** w celu udostępniania, osadzania lub dalszej analizy opartej na obrazach.

## Dlaczego używać Aspose.Note for Java do konwersji OneNote na PNG?

- **Brak zależności od Microsoft Office** – działa na każdej platformie obsługującej Javę.  
- **Precyzyjna kontrola** – możesz wybrać dowolną stronę za pomocą `setPageIndex`.  
- **Wysokiej jakości wynik** – PNG zachowuje grafikę wektorową i czytelność tekstu.  
- **Gotowość do przetwarzania wsadowego** – łatwo iterować po stronach w celu masowej konwersji, co upraszcza **konwersję onenote do png** wielu stron jednocześnie.  

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

1. **Java Development Kit (JDK)** – wersja 8 lub wyższa.  
2. **Aspose.Note for Java** – pobierz najnowszy plik JAR ze [strony Aspose](https://releases.aspose.com/note/java/).  
3. **Dokument OneNote** (`.one`) zawierający stronę, którą chcesz wyeksportować.

## Importowanie pakietów

Najpierw zaimportuj niezbędne klasy Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

Te importy dają dostęp do podstawowego API Aspose.Note, w tym ładowania dokumentów i konfigurowania opcji zapisu obrazu.

## Przewodnik krok po kroku

### Krok 1: Załaduj dokument OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Używamy klasy `Document`, aby odczytać plik OneNote z dysku. Obiekt `LoadOptions` pozwala w razie potrzeby dostosować zachowanie ładowania. Ten krok jest podstawą dla **konwersji .one do png**.

### Krok 2: Zainicjuj ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` informuje Aspose.Note, że chcemy wyjście w formacie **PNG**. Możesz przełączyć na JPEG, BMP itp., zmieniając `SaveFormat`. Ten obiekt pozwala także kontrolować DPI, głębię kolorów i inne ustawienia specyficzne dla obrazu.

### Krok 3: Ustaw indeks strony (Jak przekonwertować stronę OneNote)

```java
// set page index
opts.setPageIndex(0);
```

Metoda `setPageIndex` wybiera, którą stronę wyeksportować. Numeracja stron zaczyna się od **0**, więc `0` odnosi się do pierwszej strony. Dostosuj tę wartość, aby **wyeksportować inną stronę** lub iterować po stronach, gdy potrzebujesz **zapisać onenote jako obraz** dla każdej z nich.

### Krok 4: Zapisz dokument jako PNG (Zapisz OneNote jako PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Wywołanie `save` zapisuje wybraną stronę do pliku PNG na dysku. Nazwa pliku `ConvertSpecificPageToPngImage_out.png` jest tylko przykładem — możesz nadać jej dowolną nazwę. Ten ostatni krok **eksportuje obraz strony onenote**, gotowy do użycia w raportach, stronach internetowych lub dalszym przetwarzaniu.

## Typowe problemy i wskazówki

- **Nieprawidłowy indeks strony** – Pamiętaj, że numeracja zaczyna się od 0. Jeśli otrzymasz pusty obraz, sprawdź wartość indeksu.  
- **Brak pliku JAR Aspose.Note** – Upewnij się, że JAR znajduje się na classpath; w przeciwnym razie zobaczysz `ClassNotFoundException`.  
- **Duże strony** – Dla bardzo dużych stron rozważ zwiększenie rozmiaru sterty JVM (`-Xmx`), aby uniknąć `OutOfMemoryError`.  
- **Kontrola rozdzielczości** – Użyj `opts.setResolution(300)` (lub dowolnego DPI, którego potrzebujesz) przed wywołaniem `save`, aby poprawić klarowność obrazu.  

## Najczęściej zadawane pytania

### Q1: Czy mogę przekonwertować wiele stron na obrazy PNG jednocześnie przy użyciu Aspose.Note for Java?
**Odp1:** Tak, możesz iterować po stronach dokumentu, aktualizować `opts.setPageIndex(i)` i wywoływać `save` w każdej iteracji.

### Q2: Czy Aspose.Note for Java obsługuje inne formaty obrazów poza PNG?
**Odp2:** Absolutnie. Możesz ustawić `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` lub `SaveFormat.Tiff` w `ImageSaveOptions`.

### Q3: Czy dostępna jest darmowa wersja próbna Aspose.Note for Java?
**Odp3:** Tak, możesz pobrać darmową wersję próbną ze [website](https://releases.aspose.com/).

### Q4: Czy mogę uzyskać pomoc techniczną, jeśli napotkam problemy z Aspose.Note for Java?
**Odp4:** Absolutnie, możesz szukać wsparcia na forum społeczności Aspose [here](https://forum.aspose.com/c/note/28).

### Q5: Gdzie mogę kupić licencję na Aspose.Note for Java?
**Odp5:** Możesz kupić licencję na [purchase page](https://purchase.aspose.com/buy).

### Q6: Jak wyeksportować stronę zawierającą osadzone obrazy?
**Odp6:** Osadzone obrazy są renderowane automatycznie w wyjściu PNG; nie wymaga dodatkowego kodu.

### Q7: Czy mogę ustawić DPI lub rozdzielczość obrazu?
**Odp7:** Tak, użyj `opts.setResolution(int dpi)` przed wywołaniem `save`, aby kontrolować jakość wyjścia.

---

**Ostatnia aktualizacja:** 2026-02-05  
**Testowano z:** Aspose.Note for Java 24.11 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}