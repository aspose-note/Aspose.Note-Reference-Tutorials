---
date: 2026-03-03
description: Dowiedz się, jak tworzyć konspekt w OneNote i generować szablon notatek
  ze spotkania przy użyciu Aspose.Note dla Javy. Dostosuj styl czcionki i łatwo dodawaj
  pola wyboru.
linktitle: Create Outline in OneNote – Meeting Notes Template
second_title: Aspose.Note Java API
title: Utwórz konspekt w OneNote – Szablon notatek ze spotkania
url: /pl/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz konspekt w OneNote – Szablon notatek ze spotkania

## Wprowadzenie
W dzisiejszym szybkim świecie, efektywne **create outline in OneNote** jest niezbędne do jasnej dokumentacji spotkań. Aspose.Note for Java zapewnia potężny sposób na **generate meeting notes template**, który możesz dostosować, dodać pola wyboru i stylizować czcionki dokładnie tak, jak potrzebujesz. W tym przewodniku krok po kroku przeprowadzimy Cię przez tworzenie wielokrotnego użytku szablonu agendy spotkania, wyjaśniając **how to add checkboxes**, **add checklist to OneNote** oraz **customize font style onenote** dla eleganckiego wyglądu.

## Szybkie odpowiedzi
- **What does “create outline in OneNote” mean?** Oznacza to programowe budowanie hierarchicznej struktury (tytuły, sekcje, wypunktowania) wewnątrz pliku OneNote.  
- **Which library helps with this?** Aspose.Note for Java.  
- **Can I add checkboxes to the outline?** Tak – użyj `NoteCheckBox.createBlueCheckBox()`.  
- **Do I need a license?** Dostępna jest darmowa wersja próbna; komercyjna licencja jest wymagana w środowisku produkcyjnym.  
- **What Java version is supported?** Java 8 i nowsze.

## Co to jest „create outline in OneNote”?
Tworzenie konspektu w OneNote oznacza zdefiniowanie strony z tytułem, wieloma sekcjami konspektu oraz opcjonalnym numerowaniem list lub polami wyboru. Ta struktura odzwierciedla sposób, w jaki ręcznie wpisywałbyś nagłówki i wypunktowania w interfejsie OneNote, ale jest generowana automatycznie przez kod.

## Dlaczego warto używać Aspose.Note do szablonów agendy spotkań?
- **Consistency:** Każde spotkanie zaczyna się od tego samego czystego układu.  
- **Automation:** Zmniejsz ręczne pisanie i zapewnij, że wszystkie wymagane sekcje (agenda, zadania, notatki) są obecne.  
- **Customization:** Zmieniaj czcionki, kolory i dodawaj interaktywne pola wyboru, aby śledzić zadania.  
- **Integration:** Działa z dowolnym środowiskiem Java IDE i może być połączony z innymi bibliotekami Aspose, takimi jak PDF, arkusze kalkulacyjne itp.

## Prerequisites
- Podstawowa znajomość programowania w języku Java.  
- Zainstalowana biblioteka Aspose.Note for Java. Możesz ją pobrać [tutaj](https://releases.aspose.com/note/java/).  
- IDE, takie jak Eclipse lub IntelliJ IDEA.  

## Importowanie pakietów
Najpierw zaimportuj klasy, które będą potrzebne. Ten fragment pozostaje dokładnie taki sam jak w oryginalnym poradniku.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Krok 1: Utwórz strukturę dokumentu
Zaczynamy od zbudowania dokumentu, ustawienia tytułu i przygotowania stylów akapitu, które później pomogą nam **customize font style onenote**.

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
- Zdefiniowano dwa obiekty `ParagraphStyle` (`headerStyle` dla nagłówków, `bodyStyle` dla zwykłego tekstu).  
- Utworzono `Document` i dodano `Title`, które zawiera bieżącą datę, nadając stronie wyraźny nagłówek.

## Krok 2: Konspekt ważnych punktów
Następnie **create outline in OneNote** poprzez dodanie obiektu `Outline` i wypełnienie go sekcjami, takimi jak „Important”. To miejsce, w którym znajdują się pozycje agendy.

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
- Obiekt `Outline` reprezentuje hierarchiczną listę, którą widzisz w OneNote.  
- Używając `createListNumberingStyle` generujemy listę numerowaną, którą można zrestartować dla każdej nowej sekcji.

## Krok 3: Wyróżnij elementy akcji (How to add checkboxes)
Elementy akcji potrzebują wizualnego wskazania. Dołączając znacznik pola wyboru do każdego elementu `RichText`, umożliwiamy **how to add checkboxes** bezpośrednio w konspekcie.

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

*Pro tip:* Użyj `NoteCheckBox.createBlueCheckBox()` dla niebieskiego pola wyboru; dostępne są inne kolory, jeśli potrzebujesz innego stylu wizualnego.

## Krok 4: Zapisz dokument
Na koniec zapisz plik OneNote na dysku. Plik może być otwarty bezpośrednio w aplikacji OneNote na komputerze.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Typowe problemy i rozwiązania
| Issue | Solution |
|-------|----------|
| **Pola wyboru nie wyświetlają się** | Upewnij się, że wywołałeś `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` po ustawieniu stylu akapitu. |
| **Czcionki wyglądają inaczej w OneNote** | Sprawdź, czy nazwa czcionki (np. „Calibri”) jest zainstalowana na komputerze, na którym OneNote otwiera plik. |
| **Konspekt nie jest wcięty** | Dostosuj `setVerticalOffset` i `setHorizontalOffset` w obiekcie `Outline`. |
| **Numeracja restartuje się nieoczekiwanie** | Użyj `restartFlag` prawidłowo; ustaw go na `true` tylko dla pierwszej listy w nowej sekcji. |

## Najczęściej zadawane pytania
### Czy mogę dostosować style czcionek w moich notatkach ze spotkania?
Tak, Aspose.Note pozwala zdefiniować własne style czcionek dla nagłówków i tekstu głównego.

### Czy Aspose.Note jest kompatybilny z innymi bibliotekami Java?
Aspose.Note może być bezproblemowo integrowany z innymi bibliotekami Java w celu rozszerzenia funkcjonalności.

### Jak mogę dodać dodatkowe sekcje do moich notatek ze spotkania?
Możesz łatwo rozszerzyć strukturę konspektu, stosując ten sam wzorzec przedstawiony w poradniku.

### Czy istnieją kwestie licencyjne dotyczące Aspose.Note?
Zapoznaj się z [dokumentacją Aspose.Note](https://reference.aspose.com/note/java/) w celu uzyskania szczegółów dotyczących licencji.

### Czy dostępna jest wersja próbna Aspose.Note?
Tak, możesz uzyskać dostęp do [darmowej wersji próbnej tutaj](https://releases.aspose.com/).

## FAQ
**Q: Jak dodać listę kontrolną do OneNote bez użycia pól wyboru?**  
A: Możesz utworzyć listę punktowaną i ręcznie oznaczać pozycje, ale użycie `NoteCheckBox` zapewnia interaktywne pola wyboru, które synchronizują się z interfejsem OneNote.

**Q: Czy mogę używać tego szablonu do tworzenia szablonu agendy spotkania na cotygodniowe powtórzenia?**  
A: Oczywiście. Wystarczy zmienić formatowanie daty lub przekazać własny ciąg tytułu, aby ponownie używać tej samej struktury co tydzień.

**Q: Jaki jest najlepszy sposób na **customize font style onenote** pod kątem brandingu?**  
A: Zdefiniuj obiekty `ParagraphStyle` z nazwą, rozmiarem i kolorem czcionki korporacyjnej, a następnie zastosuj je do każdego elementu `RichText`, jak pokazano w Kroku 1.

**Q: Czy Aspose.Note obsługuje eksportowanie konspektu do PDF?**  
A: Tak. Po zapisaniu pliku OneNote możesz go wczytać przy użyciu Aspose.Note i wyeksportować do PDF używając `Document.save("output.pdf", SaveFormat.Pdf)`.

**Q: Czy istnieje sposób, aby programowo oznaczyć pole wyboru jako ukończone?**  
A: Możesz ustawić stan pola wyboru, dodając znacznik `NoteCheckBox` z właściwością `Checked` ustawioną na `true`.

---

**Ostatnia aktualizacja:** 2026-03-03  
**Testowano z:** Aspose.Note for Java 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}