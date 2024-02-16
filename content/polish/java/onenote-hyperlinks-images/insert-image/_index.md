---
title: Wstaw obraz do dokumentu programu OneNote za pomocą języka Java
linktitle: Wstaw obraz do dokumentu programu OneNote za pomocą języka Java
second_title: Aspose.Note API Java
description: Dowiedz się, jak wstawiać obrazy do dokumentów OneNote przy użyciu języka Java z biblioteką Aspose.Note for Java. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby zapewnić bezproblemową integrację.
type: docs
weight: 16
url: /pl/java/onenote-hyperlinks-images/insert-image/
---
## Wstęp

W tym samouczku omówimy, jak wstawić obraz do dokumentu programu OneNote przy użyciu języka Java i Aspose.Note dla języka Java. Aspose.Note dla Java to potężna biblioteka, która umożliwia programistom programową pracę z plikami Microsoft OneNote, umożliwiając różne operacje, takie jak tworzenie, czytanie i manipulowanie dokumentami OneNote.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz skonfigurowane następujące wymagania wstępne:

### 1. Zestaw programistyczny Java (JDK)
Upewnij się, że w systemie jest zainstalowany zestaw Java Development Kit (JDK). Możesz pobrać i zainstalować JDK ze strony internetowej Oracle.

### 2. Aspose.Note dla biblioteki Java
 Pobierz i skonfiguruj bibliotekę Aspose.Note dla Java, postępując zgodnie z instrukcją[dokumentacja](https://reference.aspose.com/note/java/).

## Importuj pakiety

Zacznij od zaimportowania niezbędnych pakietów do projektu Java. Pakiety te obejmują bibliotekę Aspose.Note i inne wymagane zależności.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Podzielmy proces wstawiania obrazu do dokumentu programu OneNote na kilka kroków:

## Krok 1: Załaduj dokument OneNote

Najpierw załaduj dokument programu OneNote, do którego chcesz wstawić obraz.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Krok 2: Pobierz stronę

Pobierz stronę w dokumencie, na której chcesz wstawić obraz.

```java
Page page = oneFile.getFirstChild();
```

## Krok 3: Załaduj obraz

Załaduj obraz, który chcesz wstawić do dokumentu OneNote.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Krok 4: Dostosuj atrybuty obrazu (opcjonalnie)

Opcjonalnie możesz dostosować rozmiar, położenie i wyrównanie obrazu zgodnie ze swoimi wymaganiami.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Krok 5: Dodaj obraz do strony

Dodaj obraz do strony w dokumencie programu OneNote.

```java
page.appendChildLast(image);
```

## Krok 6: Zapisz dokument

Zapisz zmodyfikowany dokument, łącznie z wstawionym obrazem.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Wniosek

W tym samouczku nauczyliśmy się, jak wstawić obraz do dokumentu OneNote przy użyciu języka Java i biblioteki Aspose.Note for Java. Postępując zgodnie ze szczegółowym przewodnikiem, możesz bez wysiłku programowo włączać obrazy do dokumentów programu OneNote.

## Często zadawane pytania

### P1: Czy przy użyciu tej metody mogę wstawić wiele obrazów do jednego dokumentu programu OneNote?

O1: Tak, możesz wstawić wiele obrazów do jednego dokumentu OneNote, powtarzając proces opisany w tym samouczku dla każdego obrazu.

### P2: Czy Aspose.Note dla Java jest kompatybilny ze wszystkimi wersjami OneNote?

O2: Aspose.Note for Java obsługuje pracę z plikami OneNote utworzonymi w Microsoft OneNote 2010 i nowszych wersjach.

### Pyt. 3: Czy mogę wstawiać obrazy w różnych formatach, takich jak PNG lub GIF, do dokumentu programu OneNote?

O3: Tak, Aspose.Note dla Java obsługuje wstawianie obrazów w różnych formatach, w tym PNG, JPEG, GIF i innych.

### P4: Czy dostępna jest wersja próbna Aspose.Note dla Java do celów testowych?

O4: Tak, możesz pobrać bezpłatną wersję próbną Aspose.Note dla Java ze strony internetowej w celu sprawdzenia.

### P5: Jak mogę uzyskać pomoc techniczną dla Aspose.Note dla Java?

 O5: Możesz uzyskać pomoc techniczną dla Aspose.Note dla Java, odwiedzając stronę[forum](https://forum.aspose.com/c/note/28) dedykowane produktom Aspose.Note.