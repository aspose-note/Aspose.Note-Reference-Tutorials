---
title: Zmień styl tabeli w OneNote - Aspose.Note
linktitle: Zmień styl tabeli w OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Ulepsz swoje tabele OneNote bez wysiłku dzięki Aspose.Note dla Java. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby zmienić style tabeli. Pobierz bibliotekę teraz!
type: docs
weight: 10
url: /pl/java/onenote-table-manipulation/change-table-style/
---
## Wstęp
Aspose.Note dla Java to potężna biblioteka, która pozwala programistom na łatwe manipulowanie plikami OneNote. W tym samouczku skupimy się na zmianie stylu tabeli w dokumencie OneNote przy użyciu Aspose.Note dla Java. Postępuj zgodnie z przewodnikiem krok po kroku, aby poprawić atrakcyjność wizualną swoich stołów.
## Warunki wstępne
Zanim zaczniesz, upewnij się, że masz przygotowane następujące elementy:
- Środowisko programistyczne Java: Upewnij się, że na komputerze skonfigurowano środowisko programistyczne Java.
-  Aspose.Note dla biblioteki Java: Pobierz i zainstaluj bibliotekę Aspose.Note dla Java z pliku[strona pobierania](https://releases.aspose.com/note/java/).
- Katalog dokumentów: Przygotuj katalog do przechowywania dokumentów programu OneNote.
## Importuj pakiety
swoim projekcie Java zaimportuj niezbędne pakiety do pracy z Aspose.Uwaga:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```
## Krok 1: Skonfiguruj dokument
Załaduj dokument OneNote do Aspose.Note i pobierz listę węzłów tabeli
```java
// Skonfiguruj dokument i uzyskaj listę węzłów tabeli
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```
## Krok 2: Ustaw style wierszy
Wykonaj iterację po każdej tabeli, ustawiając styl dla każdego wiersza, w tym podświetlając pierwszy wiersz po nagłówku.

```java
// Ustaw style wierszy dla każdej tabeli w dokumencie
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Podświetl pierwszy rząd po głowie.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```
## Metoda setRowStyle
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
## Krok 3: Zapisz dokument
Zapisz zmodyfikowany dokument z nowymi stylami tabeli.
Wykonując te kroki, możesz łatwo zmienić styl tabeli w dokumencie OneNote przy użyciu Aspose.Note dla Java.

```java
// Zapisz zmodyfikowany dokument
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```
## Wniosek
Aspose.Note dla Java upraszcza proces manipulowania plikami OneNote. Wykorzystując możliwości biblioteki, możesz bez wysiłku poprawić wizualną prezentację swoich tabel.

## Często zadawane pytania
### Gdzie mogę znaleźć dokumentację Aspose.Note dla Java?
 Odwiedzić[dokumentacja](https://reference.aspose.com/note/java/) w celu uzyskania kompleksowych wskazówek.
### Jak mogę uzyskać tymczasową licencję na Aspose.Note dla Java?
 Obserwuj to[połączyć](https://purchase.aspose.com/temporary-license/) nabyć licencję tymczasową.
### Czy dostępna jest bezpłatna wersja próbna Aspose.Note dla Java?
 Tak, możesz pobrać bezpłatną wersję próbną ze strony[Tutaj](https://releases.aspose.com/).
### Gdzie mogę uzyskać pomoc dotyczącą Aspose.Note dla Java?
 Dołącz[Forum Aspose.Note](https://forum.aspose.com/c/note/28) zwrócić się o pomoc do społeczeństwa.
### Jak kupić Aspose.Note dla Java?
 Bibliotekę można kupić[Tutaj](https://purchase.aspose.com/buy).