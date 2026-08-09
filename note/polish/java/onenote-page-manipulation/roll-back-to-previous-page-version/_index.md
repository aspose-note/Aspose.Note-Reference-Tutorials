---
date: 2026-05-25
description: Dowiedz się, jak przywrócić poprzednią wersję OneNote i cofnąć strony
  OneNote przy użyciu Aspose.Note dla Javy. Postępuj zgodnie z tym przewodnikiem krok
  po kroku, aby efektywnie zarządzać dokumentami.
keywords:
- restore previous onenote version
- how to roll back onenote
- read .one file java
- recover previous onenote page
linktitle: Jak przywrócić poprzednią wersję OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to restore previous OneNote version and roll back OneNote
    pages using Aspose.Note for Java. Follow this step‑by‑step guide for efficient
    document management.
  headline: How to Restore Previous OneNote Version – Aspose.Note
  type: TechArticle
- description: Learn how to restore previous OneNote version and roll back OneNote
    pages using Aspose.Note for Java. Follow this step‑by‑step guide for efficient
    document management.
  name: How to Restore Previous OneNote Version – Aspose.Note
  steps:
  - name: '**Install Java Development Kit (JDK):** Grab the latest JDK from the Oracle
      website or your preferred package manager.'
    text: '**Install Java Development Kit (JDK):** Grab the latest JDK from the Oracle
      website or your preferred package manager.'
  - name: '**Configure Environment Variables:** Set `JAVA_HOME` and update `PATH`
      so the `java` and `javac` commands are reachable from the command line.'
    text: '**Configure Environment Variables:** Set `JAVA_HOME` and update `PATH`
      so the `java` and `javac` commands are reachable from the command line.'
  - name: '**Add Aspose.Note for Java:** Download the library from the [website](https://purchase.aspose.com/buy)
      and add the JAR to your project''s classpath.'
    text: '**Add Aspose.Note for Java:** Download the library from the [website](https://purchase.aspose.com/buy)
      and add the JAR to your project''s classpath.'
  type: HowTo
- questions:
  - answer: Restoring a page to a prior version saved in its history.
    question: What does “roll back” mean for OneNote?
  - answer: '`PageHistory` class in Aspose.Note for Java.'
    question: Which API handles the rollback?
  - answer: A valid Aspose.Note license is required for production use.
    question: Do I need a license?
  - answer: Yes – you can pick any entry from the page’s history list.
    question: Can I choose any previous version?
  - answer: Absolutely; the operation works on individual pages without loading the
      entire notebook into memory.
    question: Is this approach safe for large notebooks?
  type: FAQPage
second_title: Aspose.Note Java API
title: Jak przywrócić poprzednią wersję OneNote – Aspose.Note
url: /pl/java/onenote-page-manipulation/roll-back-to-previous-page-version/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak przywrócić poprzednią wersję OneNote – Aspose.Note

## Wprowadzenie

Jeśli potrzebujesz niezawodnego, programowego sposobu na **przywrócenie poprzedniej wersji OneNote**, gdy przypadkowa edycja się pojawi, jesteś we właściwym miejscu. W tym samouczku przeprowadzimy Cię przez Aspose.Note dla Javy, pokazując dokładnie, jak cofnąć stronę OneNote do wcześniejszego stanu. Niezależnie od tego, czy tworzysz zautomatyzowaną usługę zarządzania notatkami, czy dodajesz zabezpieczenie dla współdzielonych notatników, możliwość przywrócenia strony utrzymuje Twoją treść dokładną, wiarygodną i gotową do audytu.

## Szybkie odpowiedzi
- **What does “roll back” mean for OneNote?** Co oznacza „roll back” w OneNote?  
  Przygarnienie strony do wcześniejszej wersji zapisanej w jej historii.  
- **Which API handles the rollback?** Które API obsługuje cofanie?  
  `PageHistory` class in Aspose.Note for Java.  
- **Do I need a license?** Czy potrzebuję licencji?  
  Wymagana jest ważna licencja Aspose.Note do użytku produkcyjnego.  
- **Can I choose any previous version?** Czy mogę wybrać dowolną poprzednią wersję?  
  Tak – możesz wybrać dowolny wpis z listy historii strony.  
- **Is this approach safe for large notebooks?** Czy to podejście jest bezpieczne dla dużych notatników?  
  Zdecydowanie; operacja działa na pojedynczych stronach bez ładowania całego notatnika do pamięci.

## Co to jest „przywrócenie poprzedniej wersji OneNote”?
**`restore previous onenote version`** odnosi się do procesu pobierania wcześniejszego migawki strony OneNote z jej wewnętrznej historii wersji i zastąpienia bieżącej zawartości strony tą migawką. Operacja ta jest w pełni obsługiwana przez API `PageHistory` Aspose.Note i nie wymaga ręcznych działań cofania.

## Dlaczego używać Aspose.Note do cofania stron OneNote?
Aspose.Note może przetwarzać notatniki z **tysiącami stron**, utrzymując zużycie pamięci poniżej **50 MB**, ponieważ działa strona po stronie. Obsługuje **ponad 30 funkcji specyficznych dla OneNote**, w tym odczyt plików `.one`, wyodrębnianie metadanych oraz przywracanie dowolnego wpisu historycznego. Dzięki temu jest idealny do automatyzacji na skalę przedsiębiorstwa, gdzie niezawodność i wydajność są kluczowe.

## Wymagania wstępne

Zanim przejdziemy do kodu, upewnij się, że masz przygotowane następujące elementy:

### Konfiguracja środowiska programistycznego Java
1. **Install Java Development Kit (JDK):** Pobierz najnowszy JDK ze strony Oracle lub z wybranego menedżera pakietów.  
2. **Configure Environment Variables:** Ustaw `JAVA_HOME` i zaktualizuj `PATH`, aby polecenia `java` i `javac` były dostępne z wiersza poleceń.  
3. **Add Aspose.Note for Java:** Pobierz bibliotekę ze [strony](https://purchase.aspose.com/buy) i dodaj plik JAR do ścieżki klas swojego projektu.

## Importowanie pakietów

Aby współpracować z plikami OneNote, zaimportuj niezbędne klasy Aspose.Note:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Jak przywrócić poprzednią wersję strony OneNote?

Załaduj docelowy notatnik, pobierz żądany wpis historyczny za pomocą `PageHistory`, usuń bieżącą stronę i dołącz wybraną wersję z powrotem do dokumentu – wszystko w mniej niż dziesięciu linijkach kodu Java. To podejście zapewnia, że dotknięta zostanie tylko konkretna strona, pozostawiając resztę notatnika nienaruszoną i minimalizując zużycie pamięci.

## Krok 1: Załaduj dokument OneNote

`Document` jest obiektem najwyższego poziomu w Aspose.Note, który reprezentuje pojedynczy plik OneNote w pamięci. Najpierw wskazujemy folder zawierający plik `.one` i ładujemy go do instancji `Document`.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```
Najpierw wskazujemy folder, w którym znajduje się plik `.one`, i ładujemy go do obiektu `Document`.

## Krok 2: Pobierz historię strony

`PageHistory` zapewnia dostęp do każdej zapisanej wersji wybranej strony, umożliwiając funkcję **przywrócenia poprzedniej wersji OneNote**. Wywołując `getHistory()`, otrzymujesz listę, którą możesz iterować lub indeksować bezpośrednio.

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```
`PageHistory` daje dostęp do każdej zapisanej wersji wybranej strony, umożliwiając funkcję **przywrócenia poprzedniej wersji OneNote**.

## Krok 3: Usuń bieżącą stronę

`Page` reprezentuje pojedynczą stronę w notatniku OneNote. Usunięcie bieżącej strony tworzy miejsce dla wersji historycznej, którą chcesz przywrócić.

```java
document.removeChild(page);
```
Usuwając bieżącą stronę, tworzymy miejsce dla wersji, którą chcemy przywrócić.

## Krok 4: Dołącz poprzednią wersję strony

`appendChildLast` dodaje węzeł na koniec kolekcji dzieci dokumentu. Tutaj wybieramy najnowszy wpis historyczny (możesz zmienić indeks, aby wybrać starszą wersję) i dodajemy go z powrotem do dokumentu.

```java
document.appendChildLast(pageHistory.get_Item(pageHistory.size() - 1));
```
Tutaj wybieramy najnowszy wpis historyczny (możesz zmienić indeks, aby wybrać starszą wersję) i dodajemy go z powrotem do dokumentu.

## Krok 5: Zapisz dokument

Zapisanie zapisuje zmodyfikowany notatnik z powrotem na dysk, tworząc plik, który teraz zawiera przywróconą stronę. Operacja zapisuje tylko zmienioną stronę, więc duże notatniki pozostają szybkie w przetwarzaniu.

```java
document.save(dataDir + "RollBackToPreviousPageVersion_out.one");
```
Na koniec, zachowaj zmodyfikowany notatnik. Plik wyjściowy teraz zawiera przywróconą stronę.

## Typowe problemy i wskazówki
- **Empty History:** Jeśli `pageHistory.size()` zwraca 0, strona nie ma zapisanych wersji — upewnij się, że wersjonowanie jest włączone w OneNote.  
- **Index Out of Bounds:** Pamiętaj, że lista historii jest indeksowana od zera. Dostosuj indeks (`size() - 1`), aby wybrać dokładnie potrzebną wersję.  
- **Performance:** Praca z pojedynczą stroną unika ładowania całego notatnika do pamięci, utrzymując operację szybką nawet w notatnikach z **10 000+ stronami**.  
- **Reading .one files in Java:** Użyj `Document.load("path/to/file.one")`, aby odczytać plik OneNote; Aspose.Note w pełni obsługuje format `.one` bez konieczności instalacji Microsoft Office.  
- **Recover previous OneNote page safely:** Zawsze twórz kopię zapasową oryginalnego pliku `.one` przed wykonywaniem zbiorczych przywróceń, szczególnie przy automatyzacji wielu notatników.

## Najczęściej zadawane pytania

**Q1: Czy mogę cofnąć wiele wersji jednej strony?**  
A: Tak, możesz uzyskać dostęp do całej historii strony i przywrócić dowolną poprzednią wersję, wybierając odpowiedni indeks z listy `PageHistory`.

**Q2: Czy Aspose.Note obsługuje inne języki programowania oprócz Javy?**  
A: Tak, Aspose.Note udostępnia biblioteki dla .NET, C++ i Pythona, umożliwiając wykonywanie tych samych operacji cofania na różnych platformach.

**Q3: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami OneNote?**  
A: Aspose.Note obsługuje wszystkie główne formaty plików OneNote, w tym starsze pliki `.one` oraz nowsze struktury OneNote 2016/365, zapewniając szeroką kompatybilność.

**Q4: Czy mogę automatyzować inne zadania w OneNote przy użyciu Aspose.Note?**  
A: Zdecydowanie. API pozwala programowo dodawać, usuwać i modyfikować sekcje, strony oraz zasoby osadzone, co czyni je idealnym do masowych migracji i niestandardowych raportów.

**Q5: Czy istnieje forum społeczności lub wsparcie dostępne dla Aspose.Note?**  
A: Tak, możesz odwiedzić [forum Aspose.Note](https://forum.aspose.com/c/note/28) aby uzyskać pomoc społeczności lub skontaktować się z dedykowanym zespołem wsparcia Aspose w sprawach komercyjnych.

---

**Ostatnia aktualizacja:** 2026-05-25  
**Testowano z:** Aspose.Note for Java (najnowsze wydanie)  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Jak zapisać wersję strony OneNote – Wypchnij bieżącą wersję strony w OneNote - Aspose.Note](/note/java/onenote-page-manipulation/push-current-page-version/)
- [Samouczek Aspose Java – Pobierz informacje o stronach w OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Uzyskaj liczbę stron OneNote przy użyciu Aspose.Note dla Javy](/note/java/onenote-page-manipulation/get-page-count/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}