---
date: 2025-12-25
description: Dowiedz się, jak konwertować OneNote na PNG przy użyciu Aspose.Note dla
  Javy. Ten przewodnik pokazuje, jak ustawić rozdzielczość obrazu, spłaszczyć notes
  oraz efektywnie zapisać OneNote jako obraz.
linktitle: How to Convert OneNote to PNG – Flatten Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: Jak przekonwertować OneNote na PNG – spłaszczyć notes do obrazu przy użyciu
  Aspose.Note
url: /pl/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj notes na spłaszczony obraz w OneNote - Aspose.Note

## Wprowadzenie

W tym samouczku dowiesz się, jak **przekonwertować OneNote na PNG** poprzez zamianę całego notesu w jeden spłaszczony obraz przy użyciu Aspose.Note dla Javy. To rozwiązanie jest idealne, gdy potrzebujesz udostępnić notes jako statyczny obraz, osadzić go w raportach lub zarchiwizować bez utraty szczegółów wizualnych.

## Szybkie odpowiedzi
- **Co oznacza „spłaszczyć notes”?** Łączy wszystkie elementy stron w jeden obraz rastrowy.  
- **Jaki format jest używany?** Domyślnie PNG, zapewniający jakość bezstratną.  
- **Czy mogę zmienić DPI?** Tak, użyj `setResolution` w `ImageSaveOptions`.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarczy do oceny; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Czy jest to obsługiwane na wszystkich systemach operacyjnych?** API Javy działa wszędzie tam, gdzie działa Java.

## Co to jest konwersja OneNote na PNG?

Konwersja OneNote na PNG tworzy bitmapową reprezentację każdej strony w notesie, zachowując tekst, rysunki i osadzone obiekty w jednym pliku obrazu. Jest to szczególnie przydatne w dokumentacji, prezentacjach lub archiwach zgodności.

## Dlaczego konwertować OneNote na PNG przy użyciu Aspose.Note?

- **Pełna wierność** – Wszystkie elementy wizualne są zachowane.  
- **Jednoplikowy wynik** – Nie ma potrzeby zarządzania wieloma plikami stron.  
- **Konfigurowalna rozdzielczość** – Dostosuj DPI, aby spełnić wymagania jakościowe.  
- **Brak instalacji Office** – Działa całkowicie niezależnie od Microsoft OneNote.

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz następujące elementy:

1. Zainstalowany Java Development Kit (JDK) na swoim systemie.  
2. Bibliotekę Aspose.Note dla Javy pobraną i skonfigurowaną w projekcie Java. Bibliotekę możesz pobrać [tutaj](https://releases.aspose.com/note/java/).  
3. Podstawową znajomość programowania w Javie.

## Importowanie pakietów

Aby rozpocząć, musisz zaimportować niezbędne pakiety z Aspose.Note dla Javy:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Krok 1: Ustaw katalog dokumentu

Najpierw określ katalog, w którym znajduje się plik notesu:

```java
String dataDir = "Your Document Directory";
```

Zastąp `"Your Document Directory"` ścieżką do swojego pliku notesu.

## Krok 2: Załaduj notes

Następnie załaduj plik notesu przy użyciu klasy `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Upewnij się, że zamieniłeś `"test.onetoc2"` na nazwę swojego pliku notesu.

## Krok 3: Ustaw opcje zapisu obrazu

Teraz skonfiguruj opcje zapisu notesu jako obrazu. Określimy format zapisu jako PNG i ustawimy rozdzielczość na 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Możesz dostosować rozdzielczość według własnych potrzeb. To tutaj **ustawiasz rozdzielczość obrazu**, aby kontrolować jakość wyjściową.

## Krok 4: Spłaszcz notes

Aby zapewnić, że wszystkie elementy zostaną spłaszczone do jednego obrazu, ustaw opcję `flatten` na `true`:

```java
saveOptions.setFlatten(true);
```

Ustawienie `flatten` na `true` gwarantuje, że wynikowy PNG zachowa dokładny układ Twojego notesu.

## Krok 5: Zapisz obraz

Na koniec zapisz notes jako spłaszczony obraz:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Zastąp `"ExportImageasFlattenedNotebook_out.png"` nazwą pliku wyjściowego, której chcesz użyć. Ten krok **zapisuje OneNote jako obraz**, który możesz udostępniać lub osadzać gdziekolwiek.

## Typowe przypadki użycia

- **Dokumentacja:** Osadź obraz notesu w podręcznikach technicznych lub przewodnikach użytkownika.  
- **Prezentacje:** Użyj wysokiej rozdzielczości slajdu PNG w PowerPoint bez obaw o kompatybilność czcionek czy obiektów.  
- **Archiwizacja:** Przechowuj tylko do odczytu migawkę notesu dla audytów zgodności.

## Wskazówki rozwiązywania problemów

- **Plik nie znaleziony:** Sprawdź dokładnie ścieżkę `dataDir` i upewnij się, że plik `.onetoc2` istnieje.  
- **Niska jakość obrazu:** Zwiększ DPI, zmieniając `documentSaveOptions.setResolution(600);`.  
- **Brakujące elementy:** Zweryfikuj, czy `saveOptions.setFlatten(true);` jest włączone; w przeciwnym razie niektóre warstwy mogą pozostać oddzielne.

## Najczęściej zadawane pytania

**P1: Czy mogę dostosować rozdzielczość wyjściowego obrazu?**  
Odp1: Tak, możesz zmienić rozdzielczość zgodnie z wymaganiami, modyfikując parametr metody `setResolution`.

**P2: Czy Aspose.Note obsługuje inne formaty obrazu przy eksporcie?**  
Odp2: Tak, Aspose.Note obsługuje różne formaty obrazu, takie jak PNG, JPEG, BMP itp., przy eksportowaniu notesów.

**P3: Czy mogę dalej dostosowywać wyjściowy obraz?**  
Odp3: Tak, Aspose.Note oferuje rozbudowane opcje dostosowywania obrazu, w tym rozmiar strony, orientację i ustawienia jakości.

**P4: Czy dostępna jest wersja próbna Aspose.Note dla Javy?**  
Odp4: Tak, wersję próbną można pobrać [tutaj](https://releases.aspose.com/).

**P5: Gdzie mogę uzyskać wsparcie dla Aspose.Note dla Javy?**  
Odp5: Wsparcie i zasoby znajdziesz na forum Aspose.Note [tutaj](https://forum.aspose.com/c/note/28).

---

**Ostatnia aktualizacja:** 2025-12-25  
**Testowano z:** Aspose.Note dla Javy 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}