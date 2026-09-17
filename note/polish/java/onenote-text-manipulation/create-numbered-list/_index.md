---
date: 2026-03-05
description: Dowiedz się, jak zapisać OneNote jako PDF, tworząc listę numerowaną przy
  użyciu Aspose.Note dla Javy. Zawiera kroki ustawiania domyślnego stylu tekstu i
  dostosowywania numeracji.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: Zapisz OneNote jako PDF – Utwórz listę numerowaną przy użyciu Aspose.Note
url: /pl/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz OneNote jako PDF – Utwórz listę numerowaną przy użyciu Aspose.Note

## Wprowadzenie
Aspose.Note for Java umożliwia programistom Java **zapisanie OneNote jako PDF** i wzbogacenie dokumentu o zaawansowane formatowanie, takie jak listy numerowane. W tym samouczku przeprowadzimy Cię przez cały proces — od ustawienia domyślnego stylu tekstu po dostosowanie formatu numeracji — abyś mógł wyeksportować OneNote do PDF z profesjonalnym wyglądem.

## Szybkie odpowiedzi
- **Co obejmuje ten samouczek?** Tworzenie listy numerowanej w OneNote i zapisywanie pliku jako PDF przy użyciu Aspose.Note for Java.  
- **Jakie główne słowo kluczowe jest celem?** *save onenote as pdf*  
- **Czy potrzebna jest licencja?** Dostępna jest darmowa wersja próbna; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Jakiej wersji Javy wymaga?** JDK 8 lub nowsza.  
- **Jak długo trwa implementacja?** Około 10–15 minut dla podstawowej listy.

## Co to jest „zapisanie OneNote jako PDF”?
Zapisanie OneNote jako PDF konwertuje bogatą tekstowo stronę OneNote na przenośny dokument o stałym układzie, który może być udostępniany na różnych platformach bez konieczności posiadania OneNote. Jest to szczególnie przydatne do archiwizacji, raportowania lub dystrybucji treści do użytkowników, którzy nie mają zainstalowanego OneNote.

## Dlaczego tworzyć listę numerowaną przed eksportem?
Lista numerowana dodaje struktury i czytelności, sprawiając, że wyeksportowany PDF wygląda jak dopracowany raport. Dzięki Aspose.Note możesz **dostosować format numeracji**, ustawić czcionki i kontrolować odstępy — wszystko przy zachowaniu oryginalnego układu OneNote.

## Wymagania wstępne
Zanim zaczniesz, upewnij się, że masz:

- Zainstalowany Java Development Kit (JDK) na swoim komputerze.  
- Bibliotekę Aspose.Note for Java pobraną z [tutaj](https://releases.aspose.com/note/java/).

## Importowanie pakietów
Najpierw zaimportuj wymagane klasy, aby móc pracować z obiektami OneNote i konwersją do PDF.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```

## Jak zapisać OneNote jako PDF z listą numerowaną?
Poniżej znajduje się przewodnik krok po kroku, który pokazuje **jak tworzyć elementy listy**, **ustawiać domyślny styl tekstu**, a na końcu **eksportować OneNote do PDF**.

### Krok 1: Inicjalizacja obiektów Document, Page i Outline
Zaczynamy od utworzenia podstawowych struktur OneNote. To także demonstruje użycie **add outline element java**.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Wskazówka:** Utrzymuj ścieżkę `dataDir` jako absolutną lub użyj `System.getProperty("user.dir")`, aby uniknąć problemów ze ścieżkami.

### Krok 2: Ustaw domyślny styl tekstu
Spójny styl zapewnia, że lista wygląda jednolicie we wszystkich elementach.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### Krok 3: Utwórz elementy Outline (lista numerowana)
Tutaj **dostosowujemy format numeracji** przy użyciu `NumberList`. Wzorzec `"{0})"` generuje „1)”, „2)”, itd.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **Dlaczego to ważne:** Dołączając `NumberList` do każdego `OutlineElement`, uzyskujesz pełną kontrolę nad stylem numeracji, czcionką i rozmiarem.

### Krok 4: Dodaj elementy Outline do Outline
Teraz grupujemy poszczególne elementy listy w jedną strukturę outline.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Krok 5: Dołącz Outline do strony
Outline staje się częścią hierarchii strony OneNote.

```java
page.appendChildLast(outline);
```

### Krok 6: Zapisz dokument jako PDF
Na koniec **zapisujemy OneNote jako PDF**. Plik wyjściowy będzie zawierał listę numerowaną dokładnie tak, jak została zdefiniowana.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

Uruchomienie powyższego kodu generuje plik PDF o nazwie `CreateNumberedList_out.pdf` w wybranym katalogu, zachowując format listy numerowanej.

## Typowe problemy i rozwiązania
| Problem | Rozwiązanie |
|-------|----------|
| **PDF jest pusty** | Upewnij się, że `doc.appendChildLast(page);` jest wywoływane przed `doc.save()`. |
| **Numeracja nie wyświetla się** | Sprawdź, czy wzorzec `NumberList` i `NumberFormat` są ustawione prawidłowo. |
| **Błąd pliku nie znaleziono** | Użyj ścieżki absolutnej dla `dataDir` lub utwórz katalog wcześniej. |
| **Niezgodność czcionki** | Zainstaluj czcionkę (np. Arial) na maszynie, na której uruchamiany jest kod. |

## Najczęściej zadawane pytania
### Q: Czy mogę dostosować format numeracji w mojej liście OneNote?
A: Oczywiście! Możesz dostosować format numeracji używając klasy `NumberList` dostarczonej przez Aspose.Note for Java.

### Q: Czy dostępna jest wersja próbna Aspose.Note for Java?
A: Tak, możesz pobrać darmową wersję próbną [tutaj](https://releases.aspose.com/).

### Q: Jak mogę uzyskać wsparcie dla Aspose.Note for Java?
A: Odwiedź [forum Aspose.Note for Java](https://forum.aspose.com/c/note/28), aby uzyskać wsparcie społeczności.

### Q: Gdzie mogę znaleźć szczegółową dokumentację Aspose.Note for Java?
A: Zapoznaj się z [dokumentacją](https://reference.aspose.com/note/java/), aby uzyskać pełne informacje.

### Q: Jak mogę zakupić licencję na Aspose.Note for Java?
A: Możesz kupić licencję [tutaj](https://purchase.aspose.com/buy).

## Podsumowanie
W tym samouczku pokazaliśmy, jak **zapisanie OneNote jako PDF** jednocześnie tworząc czystą, numerowaną listę przy użyciu Aspose.Note for Java. Ustawiając domyślny styl tekstu, dostosowując format numeracji i podążając za przewodnikiem krok po kroku, możesz szybko i niezawodnie generować profesjonalne pliki PDF ze stron OneNote.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose