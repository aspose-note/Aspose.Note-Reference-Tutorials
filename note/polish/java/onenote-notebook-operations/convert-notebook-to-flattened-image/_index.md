---
date: 2026-03-21
description: Dowiedz się, jak spłaszczyć notes, konwertując OneNote na PNG przy użyciu
  Aspose.Note dla Javy. Ten przewodnik omawia ustawianie rozdzielczości obrazu, zapisywanie
  OneNote jako obrazu oraz efektywne spłaszczanie notesów.
linktitle: How to Flatten Notebook – Convert OneNote to PNG
second_title: Aspose.Note Java API
title: Jak spłaszczyć notatnik – konwertuj OneNote na PNG
url: /pl/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak spłaszczyć notes – konwersja OneNote do PNG

## Wprowadzenie

W tym samouczku odkryjesz **jak spłaszczyć notes** konwertując notes OneNote na wysokiej jakości obraz PNG przy użyciu Aspose.Note for Java. Niezależnie od tego, czy potrzebujesz osadzić migawkę notesu w raporcie, udostępnić widok tylko do odczytu współpracownikom, czy zarchiwizować zgodny obraz, ten przewodnik krok po kroku pokaże Ci dokładnie, jak zapisać OneNote jako obraz, kontrolując rozdzielczość.

## Szybkie odpowiedzi
- **Co oznacza „flatten notebook”?** Łączy wszystkie elementy strony w jeden obraz rastrowy.  
- **Jaki format jest używany?** PNG jest domyślny, zapewniając jakość bezstratną.  
- **Czy mogę zmienić DPI?** Tak, użyj `setResolution` na `ImageSaveOptions`.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w celach oceny; licencja komercyjna jest wymagana w produkcji.  
- **Czy jest to obsługiwane na wszystkich systemach operacyjnych?** API Java działa wszędzie tam, gdzie działa Java.  

## Co to jest konwersja OneNote do PNG?

Konwersja OneNote do PNG tworzy bitmapową reprezentację każdej strony w notesie, zachowując tekst, rysunki i osadzone obiekty w jednym pliku obrazu. Jest to szczególnie przydatne w dokumentacji, prezentacjach lub archiwach zgodności.

## Dlaczego konwertować OneNote do PNG przy użyciu Aspose.Note?

- **Pełna wierność** – Wszystkie elementy wizualne są zachowane.  
- **Jednoplikowy wynik** – Nie ma potrzeby zarządzania wieloma plikami stron.  
- **Konfigurowalna rozdzielczość** – Dostosuj DPI, aby spełnić wymagania jakości.  
- **Brak instalacji Office** – Działa całkowicie niezależnie od Microsoft OneNote.  

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz następujące elementy:

1. Zainstalowany Java Development Kit (JDK) w systemie.  
2. Biblioteka Aspose.Note for Java pobrana i skonfigurowana w projekcie Java. Bibliotekę możesz pobrać [tutaj](https://releases.aspose.com/note/java/).  
3. Podstawowa znajomość programowania w języku Java.

## Importowanie pakietów

Aby rozpocząć, musisz zaimportować niezbędne pakiety z Aspose.Note for Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Przewodnik krok po kroku

### Krok 1: Ustaw katalog dokumentu

Najpierw określ katalog, w którym znajduje się plik notesu:

```java
String dataDir = "Your Document Directory";
```

Zastąp `"Your Document Directory"` ścieżką do swojego pliku notesu.

### Krok 2: Załaduj notes

Następnie załaduj plik notesu przy użyciu klasy `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Upewnij się, że zamieniłeś `"test.onetoc2"` na nazwę swojego pliku notesu.

### Krok 3: Ustaw opcje zapisu obrazu (ustaw rozdzielczość obrazu java)

Teraz skonfiguruj opcje zapisu notesu jako obrazu. Określimy format zapisu jako PNG i ustawimy rozdzielczość na 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Możesz dostosować rozdzielczość według własnych wymagań. To tutaj **ustawiasz rozdzielczość obrazu**, aby kontrolować jakość wyjściową.

### Krok 4: Spłaszcz notes (jak spłaszczyć notes)

Aby zapewnić, że wszystkie elementy zostaną spłaszczone do jednego obrazu, ustaw opcję `flatten` na `true`:

```java
saveOptions.setFlatten(true);
```

Ustawienie `flatten` na `true` gwarantuje, że wynikowy PNG zachowa dokładny układ Twojego notesu.

### Krok 5: Zapisz obraz (zapisz OneNote jako obraz)

Na koniec zapisz notes jako spłaszczony obraz:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Zastąp `"ExportImageasFlattenedNotebook_out.png"` nazwą pliku wyjściowego, której chcesz użyć. Ten krok **zapisuje OneNote jako obraz**, który możesz udostępnić lub osadzić gdziekolwiek.

## Typowe przypadki użycia

- **Dokumentacja:** Osadź obraz notesu w podręcznikach technicznych lub przewodnikach użytkownika.  
- **Prezentacje:** Użyj slajdu PNG wysokiej rozdzielczości w PowerPoint bez obaw o kompatybilność czcionek czy obiektów.  
- **Archiwizacja:** Przechowuj migawkę notesu w trybie tylko do odczytu do audytów zgodności.

## Porady rozwiązywania problemów

- **Plik nie znaleziony:** Sprawdź ponownie ścieżkę `dataDir` i upewnij się, że plik `.onetoc2` istnieje.  
- **Obraz niskiej jakości:** Zwiększ DPI, zmieniając `documentSaveOptions.setResolution(600);`.  
- **Brakujące elementy:** Upewnij się, że `saveOptions.setFlatten(true);` jest włączone; w przeciwnym razie niektóre warstwy mogą pozostać oddzielne.

## Najczęściej zadawane pytania

**Q1: Czy mogę dostosować rozdzielczość obrazu wyjściowego?**  
A1: Tak, możesz dostosować rozdzielczość zgodnie z wymaganiami, modyfikując parametr metody `setResolution`.

**Q2: Czy Aspose.Note obsługuje inne formaty obrazu przy eksporcie?**  
A2: Tak, Aspose.Note obsługuje różne formaty obrazu, takie jak PNG, JPEG, BMP itp., przy eksportowaniu notesów.

**Q3: Czy mogę dalej dostosować obraz wyjściowy?**  
A3: Tak, Aspose.Note oferuje rozbudowane opcje dostosowywania obrazu wyjściowego, w tym rozmiar strony, orientację i ustawienia jakości.

**Q4: Czy dostępna jest wersja próbna Aspose.Note for Java?**  
A4: Tak, możesz uzyskać darmową wersję próbną [tutaj](https://releases.aspose.com/).

**Q5: Gdzie mogę znaleźć wsparcie dla Aspose.Note for Java?**  
A5: Wsparcie i zasoby znajdziesz na forum Aspose.Note [tutaj](https://forum.aspose.com/c/note/28).

---

**Ostatnia aktualizacja:** 2026-03-21  
**Testowano z:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}