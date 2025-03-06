---
title: Zapisz w formacie PDF przy użyciu ustawień strony w programie OneNote — Aspose.Note
linktitle: Zapisz w formacie PDF przy użyciu ustawień strony w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Dowiedz się, jak zapisywać dokumenty OneNote w formacie PDF w Javie przy użyciu biblioteki Aspose.Note. Przewodnik krok po kroku z przykładami kodu dla różnych ustawień strony.
weight: 19
url: /pl/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz w formacie PDF przy użyciu ustawień strony w programie OneNote — Aspose.Note

## Wstęp

W tym samouczku nauczymy się, jak zapisywać dokumenty OneNote w formacie PDF przy użyciu różnych ustawień strony w Aspose.Note dla Java. Omówimy dwie metody: zapisywanie z ustawieniami strony Letter i zapisywanie z ustawieniami strony A4 bez ograniczenia wysokości.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że spełnione są następujące wymagania wstępne:

1. Zestaw Java Development Kit (JDK) zainstalowany w systemie.
2. Biblioteka Aspose.Note dla Java pobrana i dołączona do projektu Java.
3. Podstawowa znajomość języka programowania Java.

## Importuj pakiety

Upewnij się, że zaimportowałeś pakiety niezbędne do korzystania z Aspose.Note dla Java w swoim projekcie. Oto instrukcja importu:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Zapisz w formacie PDF, korzystając z ustawień strony listowej

### Krok 1: Załaduj dokument

Najpierw załaduj dokument OneNote do Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Krok 2: Zdefiniuj ścieżkę docelową

Określ ścieżkę docelową pliku PDF:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Krok 3: Zapisz dokument

Zapisz dokument z ustawieniami strony Letter:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Zapisz w formacie PDF przy użyciu ustawień strony A4 bez ograniczenia wysokości

### Krok 1: Załaduj dokument

Podobnie załaduj dokument OneNote do Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Krok 2: Zdefiniuj ścieżkę docelową

Określ ścieżkę docelową pliku PDF:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Krok 3: Zapisz dokument

Zapisz dokument z ustawieniami strony A4 bez ograniczenia wysokości:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Po wykonaniu tych kroków pomyślnie zapiszesz dokument programu OneNote w formacie PDF przy użyciu innych ustawień strony.

## Wniosek

W tym samouczku omówiliśmy, jak zapisywać dokumenty OneNote w formacie PDF przy użyciu biblioteki Aspose.Note dla Java. Postępując zgodnie z przewodnikiem krok po kroku, możesz łatwo zintegrować tę funkcjonalność z aplikacjami Java.

## Często zadawane pytania

### P1: Czy mogę bardziej dostosować ustawienia strony?

Odpowiedź 1: Tak, możesz dostosować ustawienia strony zgodnie ze swoimi wymaganiami, używając Aspose.Note dla Java.

### P2: Czy Aspose.Note obsługuje inne formaty wyjściowe oprócz PDF?

O2: Tak, Aspose.Note obsługuje różne formaty wyjściowe, w tym obrazy i HTML.

### P3: Czy Aspose.Note jest kompatybilny z różnymi wersjami plików OneNote?

O3: Tak, Aspose.Note obsługuje pliki OneNote z różnych wersji, w tym .one i .onetoc2.

### P4: Czy mogę za jednym razem przekonwertować wiele plików OneNote na format PDF?

O4: Tak, możesz przetwarzać wsadowo wiele plików OneNote za pomocą Aspose.Note dla Java.

### P5: Czy dostępna jest wersja próbna do celów testowych?

Odpowiedź 5: Tak, możesz pobrać bezpłatną wersję próbną Aspose.Note dla Java ze strony internetowej.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
