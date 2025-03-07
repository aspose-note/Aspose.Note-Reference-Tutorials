---
title: Dodaj nowy węzeł obrazu ze znacznikiem w programie OneNote — Aspose.Note
linktitle: Dodaj nowy węzeł obrazu ze znacznikiem w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Dowiedz się, jak dodać nowy węzeł obrazu ze znacznikiem w programie OneNote przy użyciu Aspose.Note dla języka Java. Podnieś swoje umiejętności programowania w języku Java bez wysiłku.
weight: 10
url: /pl/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj nowy węzeł obrazu ze znacznikiem w programie OneNote — Aspose.Note

## Wstęp
dziedzinie programowania w języku Java Aspose.Note wyróżnia się jako potężne narzędzie do łatwej obsługi dokumentów OneNote. Jeśli chcesz udoskonalić swoje umiejętności i dowiedzieć się, jak dodać nowy węzeł obrazu ze znacznikiem w programie OneNote przy użyciu Aspose.Note, trafiłeś we właściwe miejsce. Ten przewodnik krok po kroku przeprowadzi Cię przez proces, zapewniając dokładne zrozumienie każdej koncepcji.
## Warunki wstępne
Zanim przejdziemy do samouczka, upewnijmy się, że masz wszystko, czego potrzebujesz:
1.  Aspose.Note dla Java: Upewnij się, że masz zainstalowaną bibliotekę Aspose.Note. Jeśli nie, możesz go pobrać[Tutaj](https://releases.aspose.com/note/java/).
2. Środowisko programistyczne Java: Upewnij się, że na komputerze jest skonfigurowane działające środowisko programistyczne Java.
Skoro mamy już warunki wstępne, przejdźmy do kolejnych kroków.
## Importuj pakiety
W projekcie Java rozpocznij od zaimportowania niezbędnych pakietów:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Krok 1: Utwórz obiekt dokumentu
```java
// Ścieżka do katalogu dokumentów.
String dataDir = "Your Document Directory";
// utwórz obiekt klasy Dokument
Document doc = new Document();
```
## Krok 2: Zainicjuj obiekt klasy strony
```java
// zainicjuj obiekt klasy Page
Page page = new Page();
```
## Krok 3: Zainicjuj obiekt klasy Outline
```java
// zainicjuj obiekt klasy Outline
Outline outline = new Outline();
```
## Krok 4: Zainicjuj obiekt klasy OutlineElement
```java
// zainicjuj obiekt klasy OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Krok 5: Załaduj i wstaw obraz
```java
// załaduj obraz
Image image = new Image(null, dataDir + "Input.jpg");
// wstaw obraz w węźle dokumentu
outlineElem.appendChildLast(image);
```
## Krok 6: Dodaj etykietę notatki do obrazu
```java
// dodaj do obrazu żółtą etykietę z gwiazdką
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Krok 7: Dodaj węzeł elementu konspektu
```java
// dodaj węzeł elementu konspektu
outline.appendChildLast(outlineElem);
```
## Krok 8: Dodaj węzeł konspektu
```java
// dodaj węzeł konspektu
page.appendChildLast(outline);
```
## Krok 9: Dodaj węzeł strony
```java
// dodaj węzeł strony
doc.appendChildLast(page);
```
## Krok 10: Zapisz dokument OneNote
```java
// zapisz dokument OneNote jako plik PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Gratulacje! Pomyślnie dodałeś nowy węzeł obrazu ze znacznikiem w OneNote przy użyciu Aspose.Note dla Java.
## Wniosek
 Opanowanie Aspose.Note dla Java otwiera ekscytujące możliwości manipulowania dokumentami OneNote. Postępując zgodnie z tym samouczkiem, zdobyłeś praktyczne umiejętności, które można zastosować w różnych projektach. Kontynuuj eksplorację dokumentacji Aspose.Note[Tutaj](https://reference.aspose.com/note/java/)dla bardziej zaawansowanych funkcji i możliwości.
## Często zadawane pytania
### Gdzie mogę znaleźć dokumentację Aspose.Note?
 Można znaleźć dokumentację[Tutaj](https://reference.aspose.com/note/java/).
### Jak pobrać Aspose.Note dla Java?
 Można go pobrać ze strony wydań[Tutaj](https://releases.aspose.com/note/java/).
### Czy dostępny jest bezpłatny okres próbny?
 Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).
### Gdzie mogę uzyskać pomoc dotyczącą Aspose.Note?
 Odwiedź forum społeczności[Tutaj](https://forum.aspose.com/c/note/28) dla wsparcia.
### Czy potrzebuję tymczasowej licencji?
 W razie potrzeby możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
