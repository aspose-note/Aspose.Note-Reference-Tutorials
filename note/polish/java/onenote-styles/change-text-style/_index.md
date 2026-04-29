---
date: 2026-01-18
description: Dowiedz się, jak ustawić kolor czcionki w Java w OneNote przy użyciu
  Aspose.Note, podświetlić tekst, zmienić rozmiar czcionki i zapisać OneNote jako
  PDF. Przewodnik krok po kroku z kodem.
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Ustaw kolor czcionki w OneNote przy użyciu Java – Aspose.Note
url: /pl/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustaw kolor czcionki Java w OneNote – Aspose.Note

## Wprowadzenie

W tym samouczku dowiesz się, jak **ustawić kolor czcionki Java** dla tekstu w dokumencie OneNote przy użyciu API Aspose.Note for Java. Przejdziemy przez ładowanie pliku `.one`, dostęp do jego węzłów RichText, zastosowanie zmian koloru, podświetlenia i rozmiaru czcionki, a na koniec **zapisanie OneNote jako PDF**. Niezależnie od tego, czy potrzebujesz **podświetlić tekst w OneNote**, **zmienić rozmiar czcionki w OneNote**, czy po prostu zmienić ogólny styl tekstu, poniższe kroki zapewniają kompletną, gotową do produkcji rozwiązanie.

## Szybkie odpowiedzi
- **Czy mogę zmienić kolor czcionki konkretnych słów?** Tak – iteruj przez obiekty `TextRun` i użyj `setFontColor`.
- **Czy Aspose.Note pozwala zapisać OneNote jako PDF?** Absolutnie; użyj `document.save("output.pdf")`.
- **Jaka wersja Java jest wymagana?** Java 8 lub nowsza.
- **Czy podświetlanie jest obsługiwane?** Użyj `setHighlight(Color)` na `TextStyle`.
- **Czy mogę przekonwertować OneNote do PDF w jednej linii?** Nie bezpośrednio, ale metoda `save` obsługuje konwersję.

## Co to jest „set font color java”?

To wyrażenie odnosi się do programowego przypisywania nowego koloru czcionki elementom tekstowym w pliku OneNote przy użyciu kodu Java. Dzięki Aspose.Note uzyskujesz pełną kontrolę nad atrybutami stylu, takimi jak kolor czcionki, podświetlenie i rozmiar, bez konieczności otwierania interfejsu OneNote.

## Dlaczego zmieniać styl tekstu w OneNote?

- **Lepsza czytelność** – kolorowy lub podświetlony tekst przyciąga uwagę do kluczowych punktów.
- **Spójność marki** – wymuszaj korporacyjne kolory w notatkach ze spotkań.
- **Jakość eksportu** – stylizowane notatki wyglądają profesjonalnie, gdy **konwertujesz OneNote na PDF** w celu udostępnienia.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz:

1. Podstawową wiedzę programistyczną w Javie.  
2. Zainstalowany JDK 8 lub nowszy.  
3. Bibliotekę Aspose.Note for Java dodaną do projektu (Maven/Gradle lub ręczny JAR).  
4. Przykładowy plik OneNote (`Sample1.one`) do eksperymentów.  

## Importowanie pakietów

Najpierw zaimportuj klasy, których będziemy potrzebować:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## Przewodnik krok po kroku

### Krok 1: Załaduj dokument

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

Ładujemy plik OneNote (`Sample1.one`), aby Aspose.Note mógł pracować z jego wewnętrzną strukturą.

### Krok 2: Uzyskaj dostęp do węzłów RichText

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

Obiekty `RichText` zawierają rzeczywiste akapity. Pobierając pierwszy węzeł, uzyskujemy dostęp do tekstu, który chcemy sformatować.

### Krok 3: Zmień styl tekstu (set font color java)

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

Wewnątrz pętli **ustawiamy kolor czcionki Java** na żółty, stosujemy niebieskie podświetlenie (ilustrując **highlight text onenote**) i zwiększamy rozmiar do 20 punktów, co pokazuje **modify font size onenote**.

### Krok 4: Zapisz dokument (save onenote as pdf)

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

Wywołanie `save` z rozszerzeniem `.pdf` automatycznie **convert onenote to pdf**, dając gotowy do udostępnienia plik.

## Częste problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|-------|--------|-----|
| Brak widocznej zmiany koloru | Dokument został otwarty w OneNote przed zapisem | Zamknij OneNote lub przeładuj plik po zakończeniu procesu Java |
| Podświetlenie nie zastosowano | Użyto koloru, który pasuje do tła | Wybierz kontrastowy `Color` (np. `Color.yellow`) |
| `document.save` zgłasza `IOException` | Nieprawidłowa ścieżka wyjściowa | Upewnij się, że katalog istnieje i masz uprawnienia do zapisu |

## Najczęściej zadawane pytania

**P: Czy mogę zastosować te zmiany stylu tylko do niektórych sekcji mojego pliku OneNote?**  
O: Tak – filtruj węzły `RichText` według ich rodzica `Section` lub `Page` przed iteracją po `TextRun`.

**P: Oprócz koloru, podświetlenia i rozmiaru, jakie inne formatowanie obsługuje Aspose.Note?**  
O: Możesz zmienić rodzinę czcionki, pogrubienie/pochylenie/podkreślenie, wyrównanie oraz nawet odstępy między akapitami.

**P: Czy istnieje możliwość przetwarzania wsadowego wielu plików OneNote?**  
O: Absolutnie. Umieść logikę ładowania i stylizacji w pętli, która przetwarza każdy plik `.one` w folderze.

**P: Czy biblioteka obsługuje bezpośrednie zapisywanie do innych formatów, takich jak DOCX?**  
O: Tak – Aspose.Note może eksportować do PDF, DOCX, HTML i kilku formatów obrazów.

**P: Gdzie mogę znaleźć więcej przykładów i referencję API?**  
O: Odwiedź oficjalną stronę dokumentacji Aspose.Note, przeglądaj referencję API i pobierz darmową wersję próbną do praktycznych testów.

## Zakończenie

Masz teraz kompletny, pełny przykład, jak **ustawić kolor czcionki Java**, podświetlić tekst, dostosować rozmiar czcionki i **zapisać OneNote jako PDF** przy użyciu Aspose.Note. Śmiało dostosuj kod, aby celować w konkretne strony, stosować warunkowe formatowanie lub zintegrować go z większymi pipeline'ami przetwarzania dokumentów.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-01-18  
**Testowano z:** Aspose.Note 24.11 for Java  
**Autor:** Aspose  

---