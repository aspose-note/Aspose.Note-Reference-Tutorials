---
date: 2026-04-03
description: Dowiedz się, jak dodać hiperlink w dokumentach Aspose.Note przy użyciu
  Aspose.Note dla .NET, dostosować wygląd hiperlinku oraz wstawić wiele hiperlinków,
  aby uzyskać bogatsze pliki OneNote.
keywords:
- how to add hyperlink
- insert multiple hyperlinks
- add hyperlink to onenote
- customize hyperlink appearance
- generate one file hyperlink
linktitle: Jak dodać hiperłącze w dokumentach Aspose.Note
second_title: Aspose.Note .NET API
title: Jak dodać hiperłącze w dokumentach Aspose.Note
url: /pl/net/hyperlinks/add-hyperlinks/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dodać hiperłącze w dokumentach Aspose.Note

## Wprowadzenie

W tym samouczku odkryjesz **jak dodać hiperłącze** do tekstu w dokumentach Aspose.Note przy użyciu API .NET. Dodanie hiperłącza zamienia statyczne notatki w interaktywną, klikalną treść — idealną do łączenia z zasobami internetowymi, wewnętrznymi sekcjami lub zewnętrznymi plikami. Przejdziemy krok po kroku, pokażemy, jak **dostosować wygląd hiperłącza**, oraz wyjaśnimy, jak **wstawić wiele hiperłączy**, gdy potrzebujesz bardziej rozbudowanych stron OneNote.

## Szybkie odpowiedzi
- **Jaka jest główna klasa do tworzenia pliku OneNote?** `Document` from Aspose.Note.
- **Która właściwość sprawia, że tekst zachowuje się jak hiperłącze?** `IsHyperlink = true` on `TextStyle`.
- **Czy mogę łączyć się z zewnętrznymi stronami internetowymi?** Tak, ustaw `HyperlinkAddress` na adres URL, np. `https://www.google.com`.
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Wymagana jest ważna licencja Aspose.Note dla wersji nie‑ewaluacyjnych.
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.

## Co oznacza „jak dodać hiperłącze” w Aspose.Note?
Dodanie hiperłącza oznacza dołączenie adresu URL do fragmentu tekstu, tak aby po kliknięciu przez użytkownika w OneNote, połączony zasób otworzył się w przeglądarce lub innej aplikacji. Aspose.Note udostępnia flagę `TextStyle.IsHyperlink` oraz właściwość `HyperlinkAddress`, aby umożliwić to programowo.

## Dlaczego dodawać hiperłącza do dokumentów OneNote?
- **Ulepszona nawigacja:** Przejdź bezpośrednio do powiązanych stron internetowych lub sekcji.
- **Ulepszona dokumentacja:** Dostarczaj odnośniki, samouczki lub pliki źródłowe bez opuszczania notatki.
- **Profesjonalny wygląd:** Dostosowywalne kolory i style pozwalają, aby hiperłącza wpasowały się w projekt dokumentu.

## Wymagania wstępne

1. Podstawowa znajomość C# i Visual Studio.
2. Zainstalowana biblioteka Aspose.Note for .NET – pobierz ją z [here](https://releases.aspose.com/note/net/).
3. Zrozumienie struktury dokumentu Aspose.Note (strony, kontury, tekst sformatowany).

## Importowanie przestrzeni nazw

Najpierw zaimportuj przestrzenie nazw, które dają dostęp do podstawowych klas Aspose.Note oraz podstawowych typów .NET.

```csharp
using System;
using System.Drawing;
```

## Przewodnik krok po kroku

### Krok 1: Utwórz nowy obiekt Document

Utwórz instancję `Document`, która będzie przechowywać wszystkie Twoje strony i zawartość.

```csharp
Document doc = new Document();
```

### Krok 2: Zdefiniuj style tekstu (w tym styl hiperłącza)

Utwórz dwa obiekty `TextStyle` – jeden dla zwykłego tekstu, a drugi dla hiperłącza.  
Tutaj również **dostosowujemy wygląd hiperłącza** ustawiając kolor czcionki.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

> **Wskazówka:** Aby wstawić **wiele hiperłączy**, zdefiniuj dodatkowe obiekty `TextStyle` z różnymi wartościami `HyperlinkAddress` i użyj ich ponownie w późniejszych segmentach `RichText`.

### Krok 3: Utwórz obiekty RichText

Zbuduj akapit, który miesza zwykły tekst i hiperłącze. Metoda `Append` pozwala łączyć fragmenty ze stylami.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

### Krok 4: Utwórz kontur i element konturu

Kontury działają jak kontenery dla elementów wizualnych na stronie. Ustaw rozmiar i pozycję w razie potrzeby.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

### Krok 5: Dodaj elementy do strony

Każdy plik OneNote składa się ze stron. Tworzymy `Title` i `Page`, a następnie dołączamy kontur.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

### Krok 6: Zapisz dokument

Wybierz folder, utwórz pełną nazwę pliku i wywołaj `Save`. Plik wyjściowy będzie prawidłowym plikiem OneNote `.one` zawierającym Twoje hiperłącze.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## Częste problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| Hiperłącze nie otwiera się | Upewnij się, że `HyperlinkAddress` zawiera protokół (`http://` lub `https://`). |
| Kolor tekstu nie jest zastosowany | Ustaw `FontColor` w `TextStyle` używanym dla hiperłącza. |
| Potrzeba kilku linków na jednej stronie | Utwórz wiele obiektów `TextStyle`, każdy z własnym `HyperlinkAddress`, i dołącz je do tego samego lub różnych obiektów `RichText`. |
| Dokument nie ładuje się w OneNote | Zweryfikuj, że używasz obsługiwanej wersji OneNote (2010+). |

## Najczęściej zadawane pytania

**Q: Czy mogę dodać wiele hiperłączy w tym samym dokumencie przy użyciu Aspose.Note?**  
A: Tak, po prostu utwórz dodatkowe instancje `TextStyle` z różnymi wartościami `HyperlinkAddress` i dołącz je do swoich obiektów `RichText`.

**Q: Jak mogę dostosować wygląd hiperłączy?**  
A: Użyj właściwości takich jak `FontColor`, `FontName` i `FontSize` w `TextStyle`, który ma `IsHyperlink = true`. Dzięki temu dopasujesz wygląd do identyfikacji wizualnej dokumentu.

**Q: Czy Aspose.Note obsługuje hiperłącza do zewnętrznych stron internetowych?**  
A: Absolutnie. Ustaw `HyperlinkAddress` na dowolny prawidłowy URL (w tym `http://` lub `https://`), aby połączyć się z zasobami spoza pliku OneNote.

**Q: Czy można wygenerować pojedynczy plik OneNote zawierający wiele hiperłączy?**  
A: Tak. Poprzez wielokrotne dołączanie stylizowanych segmentów `RichText` z różnymi adresami hiperłączy, możesz **wygenerować kolekcję hiperłączy w jednym pliku**.

**Q: Czy Aspose.Note jest kompatybilny z najnowszymi wersjami OneNote?**  
A: Biblioteka działa z OneNote 2010 i nowszymi, w tym z wersją Windows 10 UWP.

---

**Ostatnia aktualizacja:** 2026-04-03  
**Testowano z:** Aspose.Note for .NET 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}