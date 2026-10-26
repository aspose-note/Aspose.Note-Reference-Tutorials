---
date: 2026-10-26
description: Dowiedz się, jak dodać pola wyboru w OneNote podczas generowania szablonu
  notatek ze spotkania przy użyciu Aspose.Note for Java oraz łatwo dostosować styl
  czcionki w OneNote.
keywords:
- add checkboxes onenote
- generate meeting notes template
- customize font style onenote
- create outline onenote
lastmod: 2026-10-26
linktitle: Generuj szablon notatek ze spotkania z Aspose.Note for Java – Utwórz konspekt
  w OneNote
og_description: Dowiedz się, jak dodać pola wyboru w OneNote podczas generowania szablonu
  notatek ze spotkania przy użyciu Aspose.Note for Java oraz łatwo dostosować styl
  czcionki w OneNote.
og_image_alt: 'Developer guide: add checkboxes onenote and generate meeting notes
  template using Aspose.Note for Java'
og_title: Dodaj pola wyboru w OneNote i utwórz szablon notatek w Javie
schemas:
- author: Aspose
  dateModified: '2026-10-26'
  description: Learn how to add checkboxes onenote while generating a meeting notes
    template with Aspose.Note for Java, and customize font style onenote easily.
  headline: Add checkboxes onenote and create notes template in Java
  type: TechArticle
- questions:
  - answer: You can create a bulleted list and manually mark items, but using `NoteCheckBox`
      provides interactive checkboxes that sync with OneNote’s UI.
    question: How do I add a checklist to OneNote without using checkboxes?
  - answer: Absolutely. Just change the date formatting or pass a custom title string
      to reuse the same structure for each week.
    question: Can I use this template to create a meeting agenda template for weekly
      repeats?
  - answer: Define `ParagraphStyle` objects with your corporate font name, size, and
      color, then apply them to each `RichText` element as shown in Step 1.
    question: What is the best way to customize font style onenote for branding?
  - answer: Yes. After saving the OneNote file, you can load it with Aspose.Note and
      export to PDF using `Document.save("output.pdf", SaveFormat.Pdf)`.
    question: Does Aspose.Note support exporting the outline to PDF?
  - answer: You can set the checkbox state by adding a `NoteCheckBox` tag with the
      `Checked` property set to `true`.
    question: Is there a way to programmatically mark a checkbox as completed?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote
- Aspose.Note
- Java
- meeting notes template
- checkboxes
title: Dodaj pola wyboru w OneNote i utwórz szablon notatek w Javie
url: /pl/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj pola wyboru OneNote i utwórz szablon notatek w Javie

## Wprowadzenie
W nowoczesnych środowiskach współpracy, **add checkboxes onenote** szybko i generuj dopracowany szablon notatek ze spotkania bez ręcznego formatowania. Aspose.Note for Java daje pełną kontrolę nad tytułami stron, hierarchicznymi konspektami, stylizacją czcionek i interaktywnymi polami wyboru, umożliwiając stworzenie wielokrotnego użytku agendy w kilka sekund. Ten przewodnik przeprowadzi Cię przez każdy krok — od importowania wymaganych klas po zapisanie finalnego pliku OneNote — abyś mógł skupić się na treści spotkania, a nie na żmudnej pracy z interfejsem.

## Szybkie odpowiedzi
- **Co oznacza „add checkboxes onenote”?** Oznacza to programowe wstawianie interaktywnych pól wyboru do konspektu OneNote, tak jak robi to interfejs użytkownika.  
- **Która biblioteka pomaga w tym?** Aspose.Note for Java zapewnia pełne API.  
- **Czy mogę dodać pola wyboru do konspektu?** Tak – użyj `NoteCheckBox.createBlueCheckBox()` lub innych wariantów kolorów.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w trakcie rozwoju; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Jaką wersję Javy obsługuje?** Java 8 i nowsze.

## Co to jest add checkboxes onenote?
Dodawanie pól wyboru onenote wstawia znacznik `NoteCheckBox` do elementu `RichText`, zamieniając zwykłą linię tekstu w interaktywny przycisk wyboru, który użytkownicy mogą zaznaczyć lub odznaczyć bezpośrednio w interfejsie OneNote, zachowując stan pola wyboru na różnych urządzeniach i zapewniając spójność.

## Dlaczego używać Aspose.Note do generowania szablonu notatek ze spotkania?
Aspose.Note obsługuje **ponad 50 formatów wejściowych i wyjściowych** i może radzić sobie ze stronami zawierającymi **do 500 linii** bez ładowania całego dokumentu do pamięci, zapewniając szybkie i oszczędne pod względem pamięci generowanie dużych agend. Dostarcza także płynne API do stylizacji, obsługuje znaki Unicode i integruje się bezproblemowo z innymi bibliotekami Aspose, co czyni go idealnym rozwiązaniem dla dokumentacji spotkań na skalę przedsiębiorstwa.

## Wymagania wstępne
- Podstawowa znajomość programowania w Javie.  
- Zainstalowana biblioteka Aspose.Note for Java. Możesz **pobrać Aspose.Note for Java** ze strony oficjalnej wersji: [Aspose.Note for Java release page](https://releases.aspose.com/note/java/).  
- Środowisko IDE, takie jak Eclipse lub IntelliJ IDEA.  

## Importowanie pakietów
Klasy `Document`, `Outline`, `ParagraphStyle`, `RichText` i `NoteCheckBox` są podstawowymi elementami budulcowymi.  

`Document` reprezentuje cały plik OneNote w pamięci, umożliwiając dodawanie lub modyfikowanie stron i ich zawartości.  
`Outline` modeluje hierarchiczną strukturę listy wyświetlaną w OneNote, umożliwiając zagnieżdżone wypunktowania i numerowanie.  
`ParagraphStyle` definiuje wielokrotnego użytku atrybuty czcionki i akapitu, które mogą być zastosowane do wielu elementów `RichText`.  
`RichText` przechowuje rzeczywistą treść tekstową akapitu i może zawierać tagi takie jak `NoteCheckBox`.  
`NoteCheckBox` tworzy interaktywny znacznik pola wyboru, który może być dołączony do akapitu `RichText`.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Krok 1: utwórz strukturę dokumentu
Najpierw utwórz instancję `Document`, ustaw tytuł strony i zdefiniuj dwa wielokrotnego użytku obiekty `ParagraphStyle` — jeden dla nagłówków i jeden dla tekstu głównego.  

Obiekty `ParagraphStyle` pozwalają zastosować tę samą rodzinę czcionki, rozmiar i kolor w wielu akapitach bez powtarzania kodu.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
ParagraphStyle headerStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(16);
ParagraphStyle bodyStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(12);
DateFormat dateFormat = DateFormat.getDateInstance(DateFormat.SHORT, Locale.US);
Document d = new Document();
boolean restartFlag = true;
RichText titleText = new RichText().append(String.format("Weekly meeting %s", dateFormat.format(Date.from(Instant.now()))));
titleText.setParagraphStyle(ParagraphStyle.getDefault());
Title title = new Title();
title.setTitleText(titleText);
Page page = new Page();
page.setTitle(title);
d.appendChildLast(page);
```

*Co zrobiliśmy:*  
- Zdefiniowano `headerStyle` dla nagłówków oraz `bodyStyle` dla zwykłego tekstu.  
- Utworzono `Document` i dodano `Title` zawierający dzisiejszą datę, co nadaje stronie wyraźny nagłówek.

## Krok 2: zarysuj ważne punkty
Następnie dodaj obiekt `Outline` do strony i wypełnij go sekcjami takimi jak „Agenda”, „Discussion Items” i „Action Items”.  

Obiekt `Outline` reprezentuje hierarchiczną listę widoczną w OneNote. Używając `createListNumberingStyle` generujemy listę numerowaną, którą można zrestartować dla każdej nowej sekcji.

```java
Outline outline = page.appendChildLast(new Outline());
outline.setVerticalOffset(30);
outline.setHorizontalOffset(30);
RichText richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("Important");
richText.setParagraphStyle(headerStyle);
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    restartFlag = false;
}
```

*Dlaczego to ważne:*  
- Hierarchia konspektu odzwierciedla ręczną strukturę, którą wpisywałbyś w OneNote, zapewniając spójność we wszystkich generowanych stronach.  
- Style numeracji utrzymują każdą sekcję agendy w porządku i ułatwiają śledzenie.

## Krok 3: podkreśl elementy akcji (jak dodać pola wyboru)
Elementy akcji wymagają wizualnego wskazania. Dołączając znacznik `NoteCheckBox` do każdego elementu `RichText`, umożliwiasz **add checkboxes onenote** bezpośrednio w konspekcie.  

`NoteCheckBox.createBlueCheckBox()` tworzy niebieskie pole wyboru; dostępne są inne kolory dla potrzeb brandingu.

```java
richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("TO DO");
richText.setParagraphStyle(headerStyle);
richText.setSpaceBefore(15);
restartFlag = true;
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    richText.getTags().add(NoteCheckBox.createBlueCheckBox());
    restartFlag = false;
}
```

*Wskazówka:* Użyj `NoteCheckBox.createBlueCheckBox()` dla niebieskiego pola wyboru; dostępne są inne kolory, jeśli potrzebujesz innego stylu wizualnego.

## Krok 4: dostosuj styl czcionki onenote
Aby utrzymać notatki ze spotkania zgodne z marką, zastosuj wcześniej zdefiniowane obiekty `ParagraphStyle` do każdego elementu `RichText`.  

Ustawienie właściwości `FontName`, `FontSize` i `FontColor` zapewnia, że wygenerowana strona odpowiada wytycznym stylu korporacyjnego.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Krok 5: zapisz dokument
Na koniec zapisz plik OneNote na dysku. Plik może być otwarty bezpośrednio w aplikacji OneNote na komputerze, a w razie potrzeby można go później przekonwertować na PDF.

*Bezpośrednia odpowiedź:* Wywołaj `document.save("MeetingTemplate.one")` — API zapisuje w pełni kompatybilny plik OneNote, który otwiera się natychmiast w kliencie OneNote.

## Typowe problemy i rozwiązania
| Problem | Rozwiązanie |
|-------|----------|
| **Pola wyboru nie wyświetlają się** | Upewnij się, że wywołałeś `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` po ustawieniu stylu akapitu. |
| **Czcionki wyglądają inaczej w OneNote** | Sprawdź, czy nazwa czcionki (np. „Calibri”) jest zainstalowana na komputerze, na którym OneNote otwiera plik. |
| **Konspekt nie jest wcięty** | Dostosuj `setVerticalOffset` i `setHorizontalOffset` w obiekcie `Outline`. |
| **Numeracja restartuje się nieoczekiwanie** | Użyj `restartFlag` prawidłowo; ustaw go na `true` tylko dla pierwszej listy w nowej sekcji. |

## Najczęściej zadawane pytania
### Jak dodać pola wyboru onenote?
Załaduj element `RichText`, a następnie wywołaj `richText.getTags().add(NoteCheckBox.createBlueCheckBox())`. Znacznik zamienia linię w interaktywny przycisk wyboru, który użytkownicy mogą zaznaczyć w OneNote.

### Czy mogę dostosować style czcionek w moich notatkach ze spotkania?
Tak. Utwórz obiekty `ParagraphStyle` z żądanymi `FontName`, `FontSize` i `FontColor`, a następnie przypisz je do każdego elementu `RichText`, jak pokazano w Kroku 1.

### Czy Aspose.Note jest kompatybilny z innymi bibliotekami Java?
Aspose.Note działa razem z innymi produktami Aspose (PDF, Cells, Slides) oraz standardowymi bibliotekami Java, umożliwiając łączenie operacji, takich jak konwersja wygenerowanego pliku OneNote do PDF.

### Jak mogę dodać dodatkowe sekcje do moich notatek ze spotkania?
Użyj tego samego wzorca: utwórz nowy węzeł `Outline`, zastosuj `ParagraphStyle` i opcjonalnie dodaj pola wyboru. API jest w pełni powtarzalne dla dowolnej liczby sekcji.

### Czy istnieją kwestie licencyjne dotyczące Aspose.Note?
Zapoznaj się z [dokumentacją Aspose.Note](https://reference.aspose.com/note/java/) w celu uzyskania pełnych informacji o licencjonowaniu. Darmowa wersja próbna wystarcza do rozwoju; licencja komercyjna jest wymagana w środowiskach produkcyjnych.

### Czy dostępna jest wersja próbna Aspose.Note?
Tak, możesz uzyskać dostęp do **bezpłatnej strony pobierania wersji próbnej Aspose.Note**: [Aspose.Note trial download page](https://releases.aspose.com/).

## FAQ
**Q: Jak dodać listę kontrolną do OneNote bez użycia pól wyboru?**  
A: Możesz stworzyć listę punktowaną i ręcznie oznaczać pozycje, ale użycie `NoteCheckBox` zapewnia interaktywne pola wyboru, które synchronizują się z interfejsem OneNote.

**Q: Czy mogę użyć tego szablonu do tworzenia szablonu agendy spotkania na cotygodniowe powtórzenia?**  
A: Oczywiście. Wystarczy zmienić formatowanie daty lub przekazać własny ciąg tytułu, aby ponownie używać tej samej struktury co tydzień.

**Q: Jaki jest najlepszy sposób dostosowania stylu czcionki onenote pod kątem brandingu?**  
A: Zdefiniuj obiekty `ParagraphStyle` z nazwą, rozmiarem i kolorem czcionki korporacyjnej, a następnie zastosuj je do każdego elementu `RichText`, jak pokazano w Kroku 1.

**Q: Czy Aspose.Note obsługuje eksportowanie konspektu do PDF?**  
A: Tak. Po zapisaniu pliku OneNote możesz go wczytać przy pomocy Aspose.Note i wyeksportować do PDF używając `Document.save("output.pdf", SaveFormat.Pdf)`.

**Q: Czy istnieje sposób, aby programowo oznaczyć pole wyboru jako ukończone?**  
A: Możesz ustawić stan pola wyboru, dodając znacznik `NoteCheckBox` z właściwością `Checked` ustawioną na `true`.

**Ostatnia aktualizacja:** 2026-10-26  
**Testowano z:** Aspose.Note for Java 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose

## Powiązane samouczki

- [Dodaj tagi do OneNote – Utwórz oznaczony dokument OneNote przy użyciu Aspose.Note](/note/java/onenote-tag-operations/)
- [Jak dostosować style OneNote przy użyciu Aspose.Note for Java](/note/java/onenote-styles/)
- [Utwórz dokument OneNote w Javie – Samouczek Aspose Note Java](/note/java/onenote-document-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}