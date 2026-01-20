---
date: 2026-01-20
description: Dowiedz się, jak zmienić styl tabeli w OneNote przy użyciu Aspose.Note
  dla Javy i ustawić kolory tła wierszy tabeli. Postępuj zgodnie z przewodnikiem krok
  po kroku, aby zastosować kolor tła, pogrubić tekst i zapisać dokument OneNote.
linktitle: Change Table Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Jak zmienić styl tabeli w OneNote przy użyciu Aspose.Note
url: /pl/java/onenote-table-manipulation/change-table-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak zmienić styl tabeli w OneNote przy użyciu Aspose.Note

## Wprowadzenie
Jeśli potrzebujesz **jak zmienić styl tabeli** w notesie OneNote, Aspose.Note for Java zrobi to za Ciebie w mgnieniu oka. W tym samouczku przeprowadzimy Cię przez cały proces — od załadowania pliku OneNote, ustawienia kolorów tła wierszy tabeli, zastosowania pogrubienia i kursywy, po ostateczne zapisanie zaktualizowanego dokumentu. Po zakończeniu będziesz pewnie formatować tabele w OneNote, wiedzieć, jak zastosować kolor tła do wierszy oraz rozumieć, jak zapisać dokument OneNote z nowymi stylami.

## Szybkie odpowiedzi
- **Jaka biblioteka jest najlepsza do stylizacji tabel w OneNote?** Aspose.Note for Java.  
- **Czy mogę ustawić kolory tła wierszy tabeli?** Tak, używając metody pomocniczej `setRowStyle`.  
- **Jak pogrubić tekst w tabeli OneNote?** Ustaw flagę `bold` w `setRowStyle`.  
- **Co jest wymagane do zapisania zmodyfikowanego pliku?** Wywołaj `document.save(...)` z prawidłową ścieżką.  
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Tak, wymagana jest licencja komercyjna.

## Czym jest „jak zmienić styl tabeli” w OneNote?
Zmiana stylu tabeli oznacza modyfikację kolorów wierszy, formatowania tekstu oraz ogólnego wyglądu, aby dane były łatwiejsze do odczytania i bardziej atrakcyjne wizualnie. Aspose.Note udostępnia płynne API do programowego manipulowania tymi właściwościami.

## Dlaczego używać Aspose.Note for Java?
- **Pełna kontrola** nad strukturami OneNote bez ręcznej pracy w interfejsie użytkownika.  
- **Wsparcie wieloplatformowe**; działa na każdym systemie operacyjnym, na którym działa Java.  
- **Bogate opcje formatowania** takie jak kolory tła, pogrubienie i kursywa.  

## Wymagania wstępne
Zanim rozpoczniesz, upewnij się, że masz:
- **Środowisko programistyczne Java** – zainstalowany JDK 8 lub wyższy.  
- **Biblioteka Aspose.Note for Java** – pobierz ze [strony pobierania](https://releases.aspose.com/note/java/).  
- **Katalog dokumentów** – folder, w którym będą przechowywane pliki `.one`.  

## Importowanie pakietów
W swoim projekcie Java zaimportuj niezbędne pakiety do pracy z Aspose.Note:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

## Krok 1: Przygotowanie dokumentu
Załaduj dokument OneNote do Aspose.Note i pobierz listę węzłów tabel.
```java
// Set up the document and get the list of table nodes
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```

## Krok 2: Ustawianie stylów wierszy
Iteruj po każdej tabeli, ustawiając styl dla każdego wiersza, w tym podświetlając pierwszy wiersz po nagłówku. To demonstruje **ustawienie tła wiersza tabeli** i **jak zastosować kolor tła**.
```java
// Set row styles for each table in the document
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Highlight first row after the head.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```

## Metoda setRowStyle
Metoda pomocnicza stosuje kolor tła, pogrubienie i kursywę do każdej komórki w wierszu. To miejsce, w którym implementowane jest **jak pogrubić tekst w onenote**.
```java
    private static void setRowStyle(TableRow row, Color highlightColor, boolean bold, boolean italic) {
        for (TableCell cell: row)
        {
            cell.setBackgroundColor(highlightColor);
            for (RichText node: cell.getChildNodes(RichText.class))
            {
                node.getParagraphStyle().setBold(bold);
                node.getParagraphStyle().setItalic(italic);
                for (TextRun run: node.getTextRuns())
                {
                    run.getStyle().setBold(bold);
                    run.getStyle().setItalic(italic);
                }
            }
        }
    }
```

## Krok 3: Zapisanie dokumentu
Po sformatowaniu tabel, zapisz zmodyfikowany dokument. To pokazuje **jak zapisać dokument onenote** z zastosowanym nowym formatowaniem.
```java
// Save the modified document
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```

## Podsumowanie
Aspose.Note for Java upraszcza proces manipulacji plikami OneNote. Wykorzystując możliwości biblioteki, możesz łatwo zmienić style tabel, ustawić kolory tła wierszy, pogrubić tekst i zapisać dokument OneNote — wszystko w kilku linijkach kodu.

## Najczęściej zadawane pytania
### Gdzie mogę znaleźć dokumentację Aspose.Note for Java?
Odwiedź [dokumentację](https://reference.aspose.com/note/java/) po kompleksowe wskazówki.

### Jak mogę uzyskać tymczasową licencję dla Aspose.Note for Java?
Skorzystaj z tego [linku](https://purchase.aspose.com/temporary-license/), aby uzyskać tymczasową licencję.

### Czy dostępna jest bezpłatna wersja próbna Aspose.Note for Java?
Tak, możesz pobrać bezpłatną wersję próbną [tutaj](https://releases.aspose.com/).

### Gdzie mogę uzyskać wsparcie dla Aspose.Note for Java?
Dołącz do [forum Aspose.Note](https://forum.aspose.com/c/note/28), aby uzyskać pomoc od społeczności.

### Jak mogę kupić Aspose.Note for Java?
Możesz zakupić bibliotekę [tutaj](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-01-20  
**Testowano z:** Aspose.Note for Java 24.11  
**Autor:** Aspose  

---