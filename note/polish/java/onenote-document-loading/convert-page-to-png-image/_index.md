---
title: Konwertuj określoną stronę na obraz PNG w programie OneNote — Java
linktitle: Konwertuj określoną stronę na obraz PNG w programie OneNote — Java
second_title: Aspose.Note API Java
description: Naucz się korzystać z Aspose.Note dla Java, konwertując stronę OneNote do formatu PNG. Wykonaj proste kroki, załaduj dokument i ustaw opcje. Ulepsz aplikacje Java dzięki tej funkcjonalności.
weight: 13
url: /pl/java/onenote-document-loading/convert-page-to-png-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj określoną stronę na obraz PNG w programie OneNote — Java

## Wstęp

W tym samouczku dowiesz się, jak używać Aspose.Note dla Java do konwertowania określonej strony z dokumentu OneNote na obraz PNG. Podzielimy ten proces na łatwe do wykonania kroki, które pomogą Ci bezproblemowo zintegrować tę funkcjonalność z aplikacją Java.

## Warunki wstępne

Zanim zaczniesz, upewnij się, że masz następujące elementy:

1. Zestaw Java Development Kit (JDK): Upewnij się, że masz zainstalowany pakiet JDK w swoim systemie.
2.  Aspose.Note dla biblioteki Java: Pobierz i zainstaluj bibliotekę Aspose.Note dla Java z pliku[strona internetowa](https://releases.aspose.com/note/java/).
3. Dokument OneNote: przygotuj dokument OneNote, z którego chcesz przekonwertować określoną stronę do formatu PNG.

## Importuj pakiety

Najpierw musisz zaimportować niezbędne pakiety do pliku Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Krok 1: Załaduj dokument OneNote

```java
// Załaduj dokument do Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

 Na tym etapie ładujemy dokument OneNote przy użyciu Aspose.Note`Document` klasa.

## Krok 2: Zainicjuj obiekt ImageSaveOptions

```java
// Zainicjuj obiekt ImageSaveOptions
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

 Tutaj inicjujemy an`ImageSaveOptions` obiekt i określ format zapisu jako PNG.

## Krok 3: Ustaw indeks strony

```java
// ustaw indeks strony
opts.setPageIndex(0);
```

Ustaw indeks strony, którą chcesz przekonwertować. Pamiętaj, że indeksowanie strony zaczyna się od 0.

## Krok 4: Zapisz dokument jako PNG

```java
// Zapisz dokument jako PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Na koniec zapisz dokument z określoną stroną przekonwertowaną na obraz PNG.

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się, jak przekonwertować określoną stronę z dokumentu OneNote na obraz PNG za pomocą Aspose.Note dla Java. Zintegrowanie tej funkcji z aplikacjami Java umożliwi programowe manipulowanie dokumentami programu OneNote, zwiększając produktywność i rozszerzając możliwości oprogramowania.

## Często zadawane pytania

### P1: Czy mogę za jednym razem przekonwertować wiele stron na obrazy PNG, używając Aspose.Note dla Java?

Odpowiedź 1: Tak, możesz dokonać konwersji wsadowej, przeglądając strony i zapisując je indywidualnie.

### P2: Czy Aspose.Note dla Java obsługuje inne formaty obrazów oprócz PNG?

O2: Tak, Aspose.Note obsługuje różne formaty obrazów, takie jak JPEG, GIF, BMP i TIFF.

### P3: Czy dostępna jest bezpłatna wersja próbna Aspose.Note dla Java?

 Odpowiedź 3: Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego w witrynie[strona internetowa](https://releases.aspose.com/).

### P4: Czy mogę uzyskać pomoc techniczną, jeśli napotkam jakiekolwiek problemy z Aspose.Note dla Java?

 Odpowiedź 4: Oczywiście możesz szukać wsparcia na forum społeczności Aspose[Tutaj](https://forum.aspose.com/c/note/28).

### P5: Gdzie mogę kupić licencję na Aspose.Note dla Java?

 Odpowiedź 5: Możesz kupić licencję w witrynie[strona zakupu](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
