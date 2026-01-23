---
date: 2026-01-23
description: Dowiedz się, jak programowo dodać tabelę do OneNote przy użyciu Aspose.Note
  dla Javy. Przewodnik krok po kroku do efektywnego tworzenia dokumentów.
linktitle: How to add table to OneNote with Aspose.Note for Java
second_title: Aspose.Note Java API
title: Jak dodać tabelę do OneNote przy użyciu Aspose.Note dla Javy
url: /pl/java/onenote-table-manipulation/compose-table/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dodać tabelę do OneNote przy użyciu Aspose.Note dla Javy

## Wprowadzenie
W tym samouczku dowiesz się, jak **dodać tabelę do OneNote** przy użyciu Aspose.Note dla Javy, co umożliwia programowe tworzenie bogatych, strukturalnych dokumentów zwiększających współpracę i raportowanie. Aspose.Note zapewnia potężne API do budowania stron OneNote, konspektów i tabel bez ręcznej edycji.

## Szybkie odpowiedzi
- **Co obejmuje ten samouczek?** Dodanie tabeli do OneNote przy użyciu Aspose.Note dla Javy.  
- **Ile czasu potrzeba?** Około 10‑15 minut na podstawową implementację.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarcza do oceny; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Jaką wersję Javy obsługuje?** Java 8 i nowsze.  
- **Czy mogę dostosować style tabeli?** Tak – możesz modyfikować czcionki, kolory i obramowania komórek za pomocą API.

## Wymagania wstępne
Przed przystąpieniem do samouczka upewnij się, że spełniasz następujące wymagania:
- Podstawowa znajomość programowania w Javie.  
- Zainstalowana biblioteka Aspose.Note dla Javy. Możesz ją pobrać [tutaj](https://releases.aspose.com/note/java/).  
- Zintegrowane środowisko programistyczne (IDE) skonfigurowane do programowania w Javie.

## Importowanie pakietów
Upewnij się, że importujesz niezbędne pakiety, aby rozpocząć projekt. Dodaj następujące instrukcje importu do swojej klasy w Javie:

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.stream.StreamSupport;
```

## Krok 1: Ustaw katalog dokumentu
```java
String dataDir = "Your Document Directory";
```
Zastąp `"Your Document Directory"` rzeczywistą ścieżką, w której chcesz zapisać dokument OneNote.

## Krok 2: Utwórz nagłówek
```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```
Utwórz przyciągający wzrok nagłówek dla swojego dokumentu. Dostosuj rozmiar czcionki, pogrubienie i wyrównanie w razie potrzeby.

## Krok 3: Utwórz stronę i konspekt
```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```
Utwórz nową stronę i konspekt, a następnie dodaj wcześniej utworzony nagłówek do konspektu.

## Krok 4: Dodaj tekst podsumowania
```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```
Dodaj krótki tekst podsumowujący, aby zapewnić kontekst dla tabeli.

## Krok 5: Dodaj tabelę do OneNote
```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
// Remaining steps are involved in setting up the table structure, header row, and adding empty rows.
// Refer to the provided code for detailed implementation.
```
Zbuduj strukturę tabeli i wypełnij ją odpowiednimi informacjami. Dostarczony kod zawiera dodawanie kolumn, wiersza nagłówka, pustych wierszy oraz szablonowej zawartości dla kolumny „Contacts”.

## Krok 6: Zapisz dokument
```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```
Zapisz utworzony dokument, podając określoną nazwę pliku i ścieżkę katalogu.

## Podsumowanie
Gratulacje! Pomyślnie **dodałeś tabelę do OneNote** przy użyciu Aspose.Note dla Javy. Ten samouczek pokazał proces krok po kroku, umożliwiając programowe zwiększenie możliwości tworzenia dokumentów.

## Najczęściej zadawane pytania
### Q: Gdzie mogę znaleźć dokumentację Aspose.Note dla Javy?
Możesz odwołać się do dokumentacji [tutaj](https://reference.aspose.com/note/java/).

### Q: Jak pobrać Aspose.Note dla Javy?
Możesz ją pobrać z [tego linku](https://releases.aspose.com/note/java/).

### Q: Czy dostępna jest wersja próbna?
Tak, możesz uzyskać dostęp do wersji próbnej [tutaj](https://releases.aspose.com/).

### Q: Gdzie mogę uzyskać wsparcie dla Aspose.Note dla Javy?
Odwiedź forum wsparcia [tutaj](https://forum.aspose.com/c/note/28).

### Q: Czy mogę uzyskać tymczasową licencję?
Tak, możesz otrzymać tymczasową licencję [tutaj](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2026-01-23  
**Tested With:** Aspose.Note for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}