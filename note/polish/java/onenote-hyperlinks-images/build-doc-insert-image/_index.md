---
title: Utwórz dokument i wstaw obraz w programie OneNote przy użyciu języka Java
linktitle: Utwórz dokument i wstaw obraz w programie OneNote przy użyciu języka Java
second_title: Aspose.Note API Java
description: Dowiedz się, jak tworzyć dokumenty OneNote i wstawiać obrazy za pomocą Aspose.Note dla Java. Samouczek krok po kroku dotyczący bezproblemowej integracji.
weight: 12
url: /pl/java/onenote-hyperlinks-images/build-doc-insert-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz dokument i wstaw obraz w programie OneNote przy użyciu języka Java

## Wstęp

W tym samouczku omówimy, jak używać Aspose.Note dla Java do tworzenia dokumentów OneNote i wstawiania do nich obrazów. Aspose.Note to potężny interfejs API Java, który umożliwia programistom programową pracę z plikami Microsoft OneNote. Szczegółowo opiszemy każdy krok, aby poprowadzić Cię przez proces.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące wymagania wstępne:

1. Zestaw Java Development Kit (JDK): Upewnij się, że masz zainstalowany pakiet JDK w swoim systemie.
2.  Biblioteka Aspose.Note dla Java: Pobierz i zainstaluj bibliotekę Aspose.Note dla Java z[strona internetowa](https://releases.aspose.com/note/java/).
3. IDE (Zintegrowane środowisko programistyczne): Do kodowania używaj dowolnego środowiska IDE obsługującego język Java, takiego jak IntelliJ IDEA lub Eclipse.

## Importuj pakiety

Zacznij od zaimportowania niezbędnych pakietów do kodu Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Krok 1: Skonfiguruj dokument

Najpierw utwórz nowy dokument OneNote i zainicjuj niezbędne obiekty:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Krok 2: Zainicjuj kontur

Skonfiguruj kontur dokumentu i określ właściwości przesunięcia:

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## Krok 3: Dodaj obraz

Załaduj obraz i określ jego wyrównanie:

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Krok 4: Dodaj obraz do elementu konspektu

Dołącz obraz do elementu konturu:

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## Krok 5: Dodaj węzły konspektu i strony

Dodaj węzły konspektu i strony do dokumentu:

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Krok 6: Zapisz dokument

Na koniec zapisz dokument OneNote:

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się tworzyć dokumenty OneNote i wstawiać do nich obrazy za pomocą Aspose.Note dla Java. Wykonując poniższe kroki, możesz efektywnie zarządzać plikami OneNote i manipulować nimi w aplikacjach Java.

## Często zadawane pytania

### P1: Gdzie mogę znaleźć dokumentację Aspose.Note dla Java?

 Odpowiedź 1: Możesz uzyskać dostęp do dokumentacji[Tutaj](https://reference.aspose.com/note/java/).

### P2: Jak pobrać Aspose.Note dla Java?

 O2: Możesz pobrać Aspose.Note dla Java z[strona pobierania](https://releases.aspose.com/note/java/).

### P3: Czy dostępna jest bezpłatna wersja próbna Aspose.Note dla Java?

 Odpowiedź 3: Tak, możesz uzyskać bezpłatną wersję próbną w witrynie[strona internetowa](https://releases.aspose.com/).

### P4: Gdzie mogę uzyskać pomoc dotyczącą Aspose.Note dla Java?

 A4: Aby uzyskać pomoc, odwiedź stronę[Forum Aspose.Note](https://forum.aspose.com/c/note/28).

### P5: Czy mogę uzyskać tymczasową licencję na Aspose.Note dla Java?

 Odpowiedź 5: Tak, możesz poprosić o licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
