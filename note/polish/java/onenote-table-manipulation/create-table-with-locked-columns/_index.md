---
date: 2026-01-23
description: Dowiedz się, jak zablokować szerokość kolumny podczas dodawania tabeli
  do OneNote przy użyciu Aspose.Note dla Javy. Przewodnik krok po kroku z kodem, wskazówkami
  i najczęściej zadawanymi pytaniami.
linktitle: How to Lock Column in OneNote Table – Aspose.Note
second_title: Aspose.Note Java API
title: Jak zablokować kolumnę w tabeli OneNote – Aspose.Note
url: /pl/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak zablokować kolumnę w tabeli OneNote – Aspose.Note

## Wprowadzenie
OneNote to wszechstronna platforma do robienia notatek, a Aspose.Note for Java ułatwia **zablokowanie szerokości kolumny**, gdy dodajesz tabelę do OneNote. W tym samouczku zobaczysz kompletny, praktyczny przykład, który pokazuje, jak ustawić szerokość kolumny tabeli, zablokować tę szerokość i dostosować obramowania tabeli OneNote — wszystko przy użyciu kilku linii kodu Java.

## Szybkie odpowiedzi
- **Co oznacza „lock column”?** Ustawia stałą szerokość kolumny, tak aby użytkownik nie mógł jej zmienić w OneNote.  
- **Która biblioteka udostępnia tę funkcję?** Aspose.Note for Java.  
- **Czy potrzebna jest licencja do uruchomienia przykładu?** Darmowa wersja próbna wystarczy do oceny; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Czy mogę dodać więcej wierszy po zablokowaniu kolumny?** Tak, możesz dalej dodawać wiersze; zablokowana szerokość pozostaje zastosowana.  
- **Jaką wersję Javy obsługuje?** Java 6 i nowsze.

## Co to jest „zablokowanie kolumny” w tabeli OneNote?
Zablokowanie kolumny oznacza przypisanie stałej szerokości obiektowi `TableColumn` i ustawienie jego właściwości `LockedWidth` na `true`. Zapobiega to przypadkowej zmianie rozmiaru przez użytkowników i utrzymuje spójny układ.

## Dlaczego blokować szerokość kolumny w OneNote?
- **Spójny układ** – Twoje notatki wyglądają tak samo na każdym urządzeniu.  
- **Lepsza czytelność** – Długi tekst jest łamany w przewidywalnym rozmiarze kolumny.  
- **Profesjonalny wygląd** – Zablokowane kolumny nadają wykończenie podobne do raportu.

## Wymagania wstępne
Zanim rozpoczniesz, upewnij się, że następujące elementy są gotowe:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) zainstalowany na Twoim komputerze.  
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) pobrana i dodana do ścieżki klas Twojego projektu.

## Importowanie pakietów
W swoim projekcie Java zaimportuj niezbędne pakiety do pracy z Aspose.Note:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Krok 1: Konfiguracja projektu
Utwórz nowy projekt Java (lub użyj istniejącego) i dodaj pliki JAR Aspose.Note do ścieżki budowania. Upewnij się, że projekt jest kompilowany przy użyciu zainstalowanego JDK.

## Krok 2: Inicjalizacja obiektów Document i Page
Zaczynamy od utworzenia nowego `Document` oraz `Page`, na której będzie znajdować się tabela.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Krok 3: Tworzenie wierszy i komórek tabeli
Tutaj budujemy dwa wiersze, każdy z jedną komórką zawierającą przykładowy tekst. Demonstracja pokazuje, jak zachowuje się zablokowana kolumna przy krótkiej i długiej treści.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Krok 4: Tworzenie i dostosowanie tabeli
Teraz tworzymy tabelę, **ustawiamy szerokość kolumny tabeli**, **blokujemy kolumnę** oraz **dostosowujemy obramowania tabeli OneNote**.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);               // customize onenote table borders
TableColumn col = new TableColumn();
col.setWidth(200);                           // set table column width
col.setLockedWidth(true);                    // onenote table locked width
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Krok 5: Dodanie tabeli do Outline i strony
Teraz dołączamy tabelę do `OutlineElement`, a na końcu dodajemy ją do strony — jest to krok **add outline element java**.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Krok 6: Zapisanie dokumentu
Zapisz plik OneNote (`.one`) w katalogu, który określiłeś wcześniej.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

Gratulacje! Pomyślnie **dodano tabelę do OneNote** z zablokowaną kolumną, stałą szerokością i dostosowanymi obramowaniami przy użyciu Aspose.Note for Java.

## Typowe problemy i rozwiązania
| Problem | Rozwiązanie |
|-------|----------|
| Table appears with no borders | Ensure `table.setBordersVisible(true);` is called. |
| Column width changes after adding rows | Verify `col.setLockedWidth(true);` is set **before** rows are appended. |
| File not saved | Check that `dataDir` points to a writable folder and ends with a valid filename. |

## Najczęściej zadawane pytania

**Q: Czy Aspose.Note for Java jest kompatybilny ze wszystkimi wersjami Javy?**  
A: Tak, działa z Java 6 i nowszymi, w tym Java 11 i Java 17.

**Q: Czy mogę dalej dostosowywać wygląd tabeli?**  
A: Oczywiście! Możesz modyfikować style obramowań, wypełnienie komórek, kolory tła i wiele innych poprzez właściwości `Table` i `TableCell`.

**Q: Czy dostępna jest wersja próbna przed zakupem?**  
A: Tak, możesz [pobrać darmową wersję próbną](https://releases.aspose.com/), aby zapoznać się z możliwościami Aspose.Note for Java.

**Q: Gdzie mogę znaleźć dodatkowe wsparcie lub dyskusje społeczności?**  
A: Odwiedź [forum Aspose.Note](https://forum.aspose.com/c/note/28), aby uzyskać pomoc i uczestniczyć w dyskusjach społeczności.

**Q: Jak mogę uzyskać tymczasową licencję dla Aspose.Note for Java?**  
A: Odwiedź [ten link](https://purchase.aspose.com/temporary-license/), aby uzyskać tymczasową licencję do celów testowych.

**Ostatnia aktualizacja:** 2026-01-23  
**Testowano z:** Aspose.Note for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}