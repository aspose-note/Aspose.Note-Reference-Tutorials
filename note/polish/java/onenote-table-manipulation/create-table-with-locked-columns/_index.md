---
title: Utwórz tabelę z zablokowanymi kolumnami w programie OneNote — Aspose.Note
linktitle: Utwórz tabelę z zablokowanymi kolumnami w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Wzbogać swoje doświadczenie OneNote dzięki Aspose.Note dla Java. Dowiedz się, jak tworzyć tabele z zablokowanymi kolumnami, korzystając z przewodnika krok po kroku. Pobierz teraz bezpłatną wersję próbną!
weight: 12
url: /pl/java/onenote-table-manipulation/create-table-with-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz tabelę z zablokowanymi kolumnami w programie OneNote — Aspose.Note

## Wstęp
OneNote to potężne narzędzie do organizowania informacji, a Aspose.Note dla Java zwiększa jego możliwości, zapewniając płynny sposób tworzenia tabel z zablokowanymi kolumnami. W tym samouczku przeprowadzimy Cię przez proces używania Aspose.Note dla Java do tworzenia tabeli z zablokowanymi kolumnami w OneNote.
## Warunki wstępne
Zanim zaczniesz, upewnij się, że spełnione są następujące wymagania wstępne:
- [Zestaw programistyczny Java (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)zainstalowany na Twojej maszynie.
- [Aspose.Note dla Javy](https://downloads.aspose.com/note/java) biblioteka pobrana i dodana do projektu.
## Importuj pakiety
W swoim projekcie Java zaimportuj pakiety niezbędne do pracy z Aspose.Uwaga:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Krok 1: Skonfiguruj swój projekt
Zacznij od utworzenia nowego projektu Java i dodania biblioteki Aspose.Note do ścieżki klas. Upewnij się, że projekt jest skonfigurowany do korzystania z pakietu JDK.
## Krok 2: Zainicjuj obiekty dokumentu i strony
```java
// Ścieżka do katalogu dokumentów.
String dataDir = "Your Document Directory";
//Utwórz obiekt klasy Dokument
Document doc = new Document();
// Zainicjuj obiekt klasy Page
Page page = new Page();
```
## Krok 3: Utwórz wiersze i komórki tabeli
```java
// Zainicjuj obiekt klasy TableRow
TableRow row1 = new TableRow();
// Zainicjuj obiekt klasy TableCell i ustaw zawartość tekstową
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Zainicjuj obiekt klasy TableRow
TableRow row2 = new TableRow();
// Zainicjuj obiekt klasy TableCell i ustaw zawartość tekstową
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Krok 4: Utwórz i dostosuj tabelę
```java
// Zainicjuj obiekt klasy Table
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Dodaj wiersze
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Krok 5: Dodaj tabelę do konspektu i strony
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Dodaj węzeł tabeli
outlineElem.appendChildLast(table);
// Dodaj węzeł elementu konspektu
outline.appendChildLast(outlineElem);
// Dodaj węzeł konspektu
page.appendChildLast(outline);
// Dodaj węzeł strony
doc.appendChildLast(page);
```
## Krok 6: Zapisz dokument
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Gratulacje! Pomyślnie utworzyłeś tabelę z zablokowanymi kolumnami w OneNote przy użyciu Aspose.Note dla Java.
## Wniosek
tym samouczku omówiliśmy proces wykorzystania Aspose.Note dla języka Java w celu ulepszenia środowiska programu OneNote poprzez tworzenie tabel z zablokowanymi kolumnami. Ta funkcja dodaje nową warstwę organizacji i struktury do Twoich notatek.
## Często zadawane pytania
### Czy Aspose.Note dla Java jest kompatybilny ze wszystkimi wersjami Java?
Tak, Aspose.Note dla Java jest kompatybilny z Java 6 i nowszymi wersjami.
### Czy mogę jeszcze bardziej dostosować wygląd stołu?
Absolutnie! Aspose.Note dla Java zapewnia rozbudowane opcje dostosowywania tabel, takie jak dostosowywanie obramowań, odstępów między komórkami i inne.
### Czy przed zakupem dostępna jest wersja próbna?
 Tak, możesz[pobierz bezpłatną wersję próbną](https://releases.aspose.com/) aby poznać możliwości Aspose.Note dla Java.
### Gdzie mogę znaleźć dodatkowe wsparcie lub dyskusje społecznościowe?
 Odwiedzić[Forum Aspose.Note](https://forum.aspose.com/c/note/28) za wsparcie i dyskusje społeczne.
### Jak mogę uzyskać tymczasową licencję na Aspose.Note dla Java?
 Odwiedzać[ten link](https://purchase.aspose.com/temporary-license/) w celu uzyskania tymczasowej licencji do celów testowych.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
