---
date: 2026-01-12
description: Dowiedz się, jak modyfikować historię stron OneNote, zmieniać tytuł strony
  OneNote i usuwać historię stron OneNote przy użyciu Aspose.Note dla Javy.
linktitle: Modify Page History in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Jak zmodyfikować historię stron OneNote przy użyciu Aspose.Note
url: /pl/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak modyfikować historię stron OneNote przy użyciu Aspose.Note

W tym samouczku dowiesz się **jak modyfikować onenote** dokumenty programowo, pracując z historią stron. Przeprowadzimy Cię przez ładowanie pliku OneNote, edycję wpisów historii, zmianę tytułu strony oraz ostateczne zapisanie zaktualizowanego notatnika — wszystko przy użyciu API Aspose.Note dla Javy. Niezależnie od tego, czy potrzebujesz wyczyścić stare wersje, czy zmienić nazwy stron, poniższe kroki dostarczają kompletną, gotową do produkcji rozwiązanie.

## Szybkie odpowiedzi
- **Co oznacza „historia stron” w OneNote?**  
  To zbiór poprzednich wersji stron przechowywanych w pliku OneNote.
- **Czy mogę usunąć konkretny wpis historii?**  
  Tak, użyj metod `removeRange` lub `removeItem` na obiekcie `PageHistory`.
- **Czy zmiana tytułu strony jest częścią manipulacji historią?**  
  Zdecydowanie — każdy element historii ma własny tytuł, który możesz zmodyfikować.
- **Czy potrzebuję licencji, aby uruchomić ten kod?**  
  Tymczasowa licencja ewaluacyjna działa w testach; pełna licencja jest wymagana w środowisku produkcyjnym.
- **Jaką wersję Javy obsługuje?**  
  Aspose.Note dla Javy obsługuje JDK 8 i nowsze.

## Wymagania wstępne

1. **Java Development Kit (JDK)** – JDK 8 lub nowszy zainstalowany na Twoim komputerze.  
2. **Biblioteka Aspose.Note dla Javy** – pobierz ją ze [strony pobierania](https://releases.aspose.com/note/java/).  
3. **Przykładowy dokument OneNote** – np. `Sample1.one`, który możesz bezpiecznie modyfikować.

## Importowanie pakietów

Najpierw zaimportuj klasy, które będą potrzebne. Poniższy blok kodu musi pozostać dokładnie taki sam.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Przewodnik krok po kroku

### Krok 1: Załaduj dokument OneNote

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### Krok 2: Pobierz pierwszą stronę i jej historię

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### Krok 3: Usuń zakres elementów historii

Jeśli potrzebujesz **usunąć wpisy historii stron onenote**, wywołaj `removeRange`. Przykład usuwa pierwszy wpis.

```java
pageHistory.removeRange(0, 1);
```

### Krok 4: Zastąp element historii

Możesz zastąpić istniejący wpis historii nowym obiektem `Page`.

```java
pageHistory.set_Item(0, new Page());
```

### Krok 5: Zmień tytuł strony w historii

Zmiana tytułu jest częstym żądaniem, gdy chcesz **zmienić tytuł strony onenote** dla konkretnej wersji.

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### Krok 6: Dodaj nowy wpis historii

Dodaj zupełnie nową stronę do kolekcji historii.

```java
pageHistory.addItem(new Page());
```

### Krok 7: Wstaw stronę w określonej pozycji

Wstaw stronę pod indeksem 1, przesuwając istniejące elementy do przodu.

```java
pageHistory.insertItem(1, new Page());
```

### Krok 8: Zapisz zmodyfikowany notatnik

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## Dlaczego modyfikować historię stron OneNote?

- **Kontrola wersji:** Zachowuj tylko istotne wersje i odrzucaj niepotrzebne szkice.  
- **Spójność:** Dopasuj tytuły stron we wszystkich wersjach historycznych, aby ułatwić nawigację.  
- **Wydajność:** Mniejsze kolekcje historii zmniejszają rozmiar pliku i przyspieszają ładowanie.

## Częste pułapki i wskazówki

- **Indeks poza zakresem:** Zawsze sprawdzaj rozmiar kolekcji przed wywołaniem `removeRange` lub `insertItem`.  
- **Puste tytuły:** Niektóre strony historyczne mogą nie mieć tytułu; zabezpiecz się przed `null` przy wywoływaniu `getTitle()`.  
- **Lokalizacja zapisu:** Upewnij się, że ścieżka wyjściowa (`ModifyPageHistory_out.one`) jest zapisywalna; w przeciwnym razie zostanie rzucony `IOException`.

## Najczęściej zadawane pytania

**P:** Czy mogę używać Aspose.Note dla Javy z innymi frameworkami Java?  
**O:** Tak, Aspose.Note dla Javy jest kompatybilny z różnymi frameworkami Java, takimi jak Spring, Hibernate itp.

**P:** Czy Aspose.Note dla Javy jest kompatybilny z różnymi wersjami plików OneNote?  
**O:** Aspose.Note dla Javy obsługuje pracę zarówno ze starszymi, jak i nowszymi wersjami plików OneNote.

**P:** Czy Aspose.Note dla Javy wymaga dodatkowych zależności?  
**O:** Nie, Aspose.Note dla Javy jest biblioteką samodzielną i nie wymaga dodatkowych zależności.

**P:** Czy mogę wykonywać masowe modyfikacje wielu plików OneNote jednocześnie?  
**O:** Tak, Aspose.Note dla Javy udostępnia API do efektywnego obsługiwania masowych modyfikacji.

**P:** Czy istnieje forum społecznościowe dla Aspose.Note dla Javy, gdzie mogę poprosić o pomoc?  
**O:** Tak, możesz odwiedzić [forum Aspose.Note](https://forum.aspose.com/c/note/28) w celu uzyskania pomocy lub pytań dotyczących biblioteki.

**Ostatnia aktualizacja:** 2026-01-12  
**Testowano z:** Aspose.Note dla Javy 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}