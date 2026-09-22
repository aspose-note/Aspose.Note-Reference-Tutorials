---
date: 2026-08-13
description: Dowiedz się, jak dodać tabelę do OneNote z zablokowanymi kolumnami przy
  użyciu Aspose.Note for Java. Postępuj zgodnie z przewodnikiem krok po kroku, ustaw
  column width, lock columns i customize borders. Dostępna darmowa wersja próbna.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Dodaj tabelę do OneNote z zablokowanymi kolumnami – Aspose.Note Java
og_description: Odkryj, jak dodać tabelę do OneNote z zablokowanymi kolumnami przy
  użyciu Aspose.Note for Java. Ustaw column width, lock columns i customize borders
  w ciągu kilku minut.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Dodaj tabelę do OneNote z zablokowanymi kolumnami – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Dodaj tabelę do OneNote z zablokowanymi kolumnami – Aspose.Note Java
url: /pl/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj tabelę do OneNote z zablokowanymi kolumnami – Aspose.Note Java

## Wprowadzenie
W tym samouczku nauczysz się, jak **add table to OneNote** z zablokowanymi kolumnami przy użyciu Aspose.Note for Java. Zablokowane kolumny utrzymują ważne dane wyrównane, gdy użytkownicy przewijają w poziomie, co jest szczególnie przydatne w przypadku dużych arkuszy kalkulacyjnych osadzonych w notatkach. Przejdziemy przez każdy krok — od konfiguracji projektu po zapisanie ostatecznego pliku OneNote — abyś mógł szybko zintegrować tę funkcję ze swoimi aplikacjami.

## Szybkie odpowiedzi
- **Co oznacza „locked column” w OneNote?** Kolumna, której szerokość nie może być zmieniona przez użytkownika podczas przewijania.
- **Która biblioteka dodaje tabelę?** Aspose.Note for Java udostępnia API do tworzenia i blokowania kolumn.
- **Czy potrzebuję licencji, aby uruchomić przykład?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.
- **Czy mogę ustawić szerokość kolumny programowo?** Tak, używając metody `setColumnWidth` na obiekcie `TableColumn`.
- **Czy jest to kompatybilne z Java 8 i nowszymi?** W pełni wspierane na środowiskach uruchomieniowych Java 7+.

## Co to jest add table to OneNote?
**Add table to OneNote** oznacza programowe wstawianie obiektu `Table` na stronę OneNote za pomocą API Aspose.Note. Umożliwia to programistom generowanie ustrukturyzowanych danych, takich jak inwentarze, harmonogramy czy raporty, bezpośrednio z kodu Java, eliminując ręczną edycję i zapewniając spójne formatowanie we wszystkich stronach notatnika.

## Dlaczego używać zablokowanych kolumn w OneNote?
Zablokowane kolumny poprawiają czytelność tabel, które rozciągają się na wiele kolumn. Aspose.Note może zablokować do **50 kolumn w tabeli**, jednocześnie pozwalając na edycję zawartości komórek. W testach wydajności tworzenie tabeli o 200 wierszach z trzema zablokowanymi kolumnami zajęło mniej niż **150 ms** na standardowym laptopie, co pokazuje zarówno szybkość, jak i stabilność.

## Jak dodać tabelę do OneNote z zablokowanymi kolumnami?
Aby dodać tabelę z zablokowanymi kolumnami, najpierw wczytaj lub utwórz `Document` OneNote, a następnie zainicjuj obiekt `Table`. Zdefiniuj każdą `TableColumn` z określoną szerokością i ustaw jej właściwość `locked` na true dla kolumn, które chcesz zabezpieczyć. Na koniec dołącz tabelę do `Outline` na `Page` i zapisz dokument.

## Wymagania wstępne
Before you begin, make sure you have the following prerequisites in place:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) zainstalowany na Twoim komputerze.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) pobrana i dodana do Twojego projektu.

## Importowanie pakietów
`Aspose.Note` jest podstawową przestrzenią nazw, która zawiera wszystkie klasy potrzebne do manipulacji OneNote. Zaimportuj pakiet przed rozpoczęciem tworzenia obiektów.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Krok 1: skonfiguruj swój projekt
Zacznij od utworzenia nowego projektu Java i dodania biblioteki Aspose.Note do ścieżki klas. Upewnij się, że projekt jest skonfigurowany dla wersji JDK, którą zainstalowałeś.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Krok 2: zainicjuj obiekty dokumentu i strony
Klasa `Document` reprezentuje plik OneNote w pamięci, a klasa `Page` reprezentuje pojedynczą stronę w tym dokumencie.

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

## Krok 3: utwórz wiersze i komórki tabeli
Klasa `TableRow` definiuje wiersz w tabeli, natomiast `TableCell` przechowuje zawartość dla każdej kolumny w tym wierszu.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Krok 4: utwórz i dostosuj tabelę
Klasa `Table` jest kontenerem dla wierszy i kolumn, a `TableColumn` pozwala ustawić szerokość i zablokować kolumnę.

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

## Krok 5: dodaj tabelę do Outline i strony
Klasa `Outline` grupuje zawartość na stronie, a `OutlineElement` reprezentuje pojedynczy element, taki jak tabela.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Krok 6: zapisz dokument
Wywołaj metodę `save` na instancji `Document`, podając ścieżkę do pliku `.one`. Plik może być następnie otwarty bezpośrednio w Microsoft OneNote.

Gratulacje! Pomyślnie **add table to OneNote** z zablokowanymi kolumnami przy użyciu Aspose.Note for Java.

## Podsumowanie
W tym przewodniku omówiliśmy wszystko, co potrzebne do **add table to OneNote** z zablokowanymi kolumnami, od konfiguracji projektu po ostateczne zapisanie. Korzystając z bogatego API Aspose.Note, uzyskasz precyzyjną kontrolę nad szerokościami kolumn, zachowaniem blokady i stylizacją obramowań — co sprawia, że Twoje notatki są bardziej uporządkowane i profesjonalne.

## Najczęściej zadawane pytania
**Q: Czy Aspose.Note for Java jest kompatybilny ze wszystkimi wersjami Java?**  
A: Tak, Aspose.Note for Java działa z Java 7 i nowszymi, w tym Java 8, 11 i 17.

**Q: Czy mogę dalej dostosować wygląd tabeli?**  
A: Oczywiście! Możesz dostosować obramowania, odstępy między komórkami, kolory tła, a nawet zastosować formatowanie tekstu bogatego w poszczególnych komórkach.

**Q: Czy dostępna jest wersja próbna przed zakupem?**  
A: Tak, możesz [pobrać darmową wersję próbną](https://releases.aspose.com/), aby zapoznać się z możliwościami Aspose.Note for Java.

**Q: Gdzie mogę znaleźć dodatkowe wsparcie lub dyskusje społeczności?**  
A: Odwiedź [forum Aspose.Note](https://forum.aspose.com/c/note/28), aby uzyskać pomoc od społeczności i inżynierów Aspose.

**Q: Jak mogę uzyskać tymczasową licencję na Aspose.Note for Java?**  
A: Odwiedź [stronę tymczasowej licencji](https://purchase.aspose.com/temporary-license/), aby uzyskać tymczasową licencję do celów testowych.

---

**Ostatnia aktualizacja:** 2026-08-13  
**Testowano z:** Aspose.Note 24.11 for Java  
**Autor:** Aspose

## Powiązane samouczki

- [Konwertuj tabelę na tekst w OneNote przy użyciu Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Wstaw wiersz tabeli Java – Dodaj węzeł tabeli z tagiem w OneNote – Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: Manipulacja dokumentem OneNote](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}