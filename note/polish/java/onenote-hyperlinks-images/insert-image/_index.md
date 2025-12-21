---
date: 2025-12-21
description: Dowiedz się, jak dodawać obrazy do dokumentów OneNote przy użyciu Javy
  i Aspose.Note for Java. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby
  wstawiać obrazy i opcjonalnie zapisywać OneNote jako PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Jak dodać obraz do OneNote przy użyciu Javy
url: /pl/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wstawianie obrazu w dokumencie OneNote przy użyciu Javy

## Wprowadzenie

W tym samouczku przyjrzymy się, jak wstawić obraz do dokumentu OneNote przy użyciu Javy z pomocą Aspose.Note for Java. Aspose.Note for Java to potężna biblioteka, która umożliwia programistom pracę z plikami Microsoft OneNote w sposób programistyczny, pozwalając na różne operacje, takie jak tworzenie, odczytywanie i manipulowanie dokumentami OneNote.

## Szybkie odpowiedzi
- **Jaki jest najprostszy sposób dodania obrazu do OneNote przy użyciu Javy?**  
  Użyj klasy `Image` z Aspose.Note for Java i dołącz ją do strony.
- **Czy potrzebna jest licencja do użytku produkcyjnego?**  
  Tak, do wdrożeń produkcyjnych wymagana jest licencja komercyjna.
- **Czy mogę ustawić własne wymiary obrazu?**  
  Oczywiście – wywołaj `setWidth()` i `setHeight()` na obiekcie `Image`.
- **Czy można zapisać plik OneNote jako PDF po dodaniu obrazu?**  
  Tak, wywołaj `save(..., SaveFormat.Pdf)`, aby **zapisać OneNote jako PDF**.
- **Jaką wersję Javy obsługuje biblioteka?**  
  Aspose.Note for Java działa z JDK 8 i nowszymi.

## Jak dodać obraz do OneNote przy użyciu Javy?

Zanim przejdziemy do kodu, krótko omówmy, dlaczego warto programowo osadzać obrazy w OneNote. Niezależnie od tego, czy tworzysz protokoły spotkań, generujesz automatyczne raporty, czy budujesz potok dokumentacji, wstawianie obrazów nadaje notatkom kontekst wizualny, którego nie zapewnia sam tekst. Dzięki Aspose.Note for Java możesz zrobić to w całości w kodzie, bez otwierania interfejsu OneNote.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz przygotowane następujące elementy:

### 1. Java Development Kit (JDK)
Upewnij się, że masz zainstalowany Java Development Kit (JDK) na swoim komputerze. Możesz pobrać i zainstalować JDK ze strony Oracle.

### 2. Biblioteka Aspose.Note for Java
Pobierz i skonfiguruj bibliotekę Aspose.Note for Java, postępując zgodnie z [dokumentacją](https://reference.aspose.com/note/java/).

## Importowanie pakietów

Rozpocznij od zaimportowania niezbędnych pakietów do swojego projektu Java. Pakiety te obejmują bibliotekę Aspose.Note oraz inne wymagane zależności.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Rozbijmy proces wstawiania obrazu do dokumentu OneNote na kilka kroków:

## Krok 1: Załaduj dokument OneNote

Najpierw załaduj dokument OneNote, do którego chcesz wstawić obraz.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Krok 2: Pobierz stronę

Pobierz stronę w dokumencie, na której chcesz umieścić obraz.

```java
Page page = oneFile.getFirstChild();
```

## Krok 3: Załaduj obraz

Załaduj obraz, który chcesz wstawić do dokumentu OneNote.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Krok 4: Dostosuj atrybuty obrazu (opcjonalnie)

Opcjonalnie możesz dostosować rozmiar, położenie i wyrównanie obrazu zgodnie z wymaganiami. To miejsce, w którym **ustawiasz wymiary obrazu w stylu Java**.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Krok 5: Dodaj obraz do strony

Dodaj obraz do strony w dokumencie OneNote.

```java
page.appendChildLast(image);
```

## Krok 6: Zapisz dokument

Zapisz zmodyfikowany dokument, łącznie z wstawionym obrazem. Na tym etapie możesz także **zapisać OneNote jako PDF**.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Zakończenie

W tym samouczku nauczyliśmy się, jak wstawić obraz do dokumentu OneNote przy użyciu Javy i biblioteki Aspose.Note for Java. Postępując zgodnie z przewodnikiem krok po kroku, możesz bez trudu programowo włączać obrazy do swoich dokumentów OneNote.

## FAQ

### Q1: Czy mogę wstawić wiele obrazów do jednego dokumentu OneNote przy użyciu tej metody?

A1: Tak, możesz wstawić wiele obrazów do jednego dokumentu OneNote, powtarzając opisany w tym samouczku proces dla każdego obrazu.

### Q2: Czy Aspose.Note for Java jest kompatybilny ze wszystkimi wersjami OneNote?

A2: Aspose.Note for Java obsługuje pliki OneNote utworzone w Microsoft OneNote 2010 i nowszych wersjach.

### Q3: Czy mogę wstawiać obrazy w różnych formatach, takich jak PNG czy GIF, do dokumentu OneNote?

A3: Tak, Aspose.Note for Java obsługuje wstawianie obrazów w różnych formatach, w tym PNG, JPEG, GIF i innych.

### Q4: Czy dostępna jest wersja próbna Aspose.Note for Java do testów?

A4: Tak, możesz pobrać darmową wersję próbną Aspose.Note for Java ze strony internetowej w celu oceny.

### Q5: Jak mogę uzyskać wsparcie techniczne dla Aspose.Note for Java?

A5: Wsparcie techniczne dla Aspose.Note for Java możesz uzyskać, odwiedzając [forum](https://forum.aspose.com/c/note/28) poświęcone produktom Aspose.Note.

---

**Ostatnia aktualizacja:** 2025-12-21  
**Testowano z:** Aspose.Note for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}