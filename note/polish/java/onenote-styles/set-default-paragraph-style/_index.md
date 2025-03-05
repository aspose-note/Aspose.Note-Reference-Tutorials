---
title: Ustaw domyślny styl akapitu w programie OneNote - Aspose.Note
linktitle: Ustaw domyślny styl akapitu w programie OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Dowiedz się, jak ustawić domyślne style akapitów w programie OneNote przy użyciu programu Aspose.Note dla języka Java. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby efektywnie formatować tekst w aplikacjach Java.
type: docs
weight: 11
url: /pl/java/onenote-styles/set-default-paragraph-style/
---
## Wstęp

Aspose.Note dla Java oferuje zaawansowane możliwości manipulowania formatowaniem tekstu, w tym ustawianie domyślnych stylów akapitów. Ten samouczek poprowadzi Cię przez proces ustawiania domyślnych stylów akapitów w programie OneNote przy użyciu Aspose.Note.

## Warunki wstępne

Zanim zaczniesz, upewnij się, że masz następujące elementy:

1. Zestaw Java Development Kit (JDK): Upewnij się, że masz zainstalowany pakiet JDK w swoim systemie.
2.  Biblioteka Aspose.Note dla Java: Pobierz i zainstaluj Aspose.Note dla Java z[strona pobierania](https://releases.aspose.com/note/java/).
3. Zintegrowane środowisko programistyczne (IDE): dla wygody kodowania powinieneś mieć zainstalowane środowisko IDE, takie jak Eclipse lub IntelliJ IDEA.

## Importuj pakiety

Najpierw zaimportuj niezbędne pakiety, aby rozpocząć kodowanie:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

Podzielmy teraz przykładowy kod na kilka kroków:

## Krok 1: Zainicjuj dokument, stronę i konspekt

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## Krok 2: Utwórz element konspektu

```java
OutlineElement outlineElem = new OutlineElement();
```

## Krok 3: Zdefiniuj domyślny styl akapitu

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## Krok 4: Utwórz tekst sformatowany w stylu domyślnym

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## Krok 5: Dołącz tekst sformatowany do elementu konspektu

```java
outlineElem.appendChildLast(text);
```

## Krok 6: Dołącz element konspektu do konspektu

```java
outline.appendChildLast(outlineElem);
```

## Krok 7: Dołącz konspekt do strony

```java
page.appendChildLast(outline);
```

## Krok 8: Dołącz stronę do dokumentu

```java
document.appendChildLast(page);
```

## Krok 9: Zapisz dokument

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

Ten kod ustawi domyślny styl akapitu w OneNote przy użyciu Aspose.Note dla Java.

## Wniosek

Programowe ustawianie domyślnych stylów akapitów w OneNote można efektywnie osiągnąć dzięki Aspose.Note dla Java. Wykonując kroki opisane w tym samouczku, możesz bezproblemowo zintegrować tę funkcjonalność z aplikacjami Java.

## Często zadawane pytania

### P1: Czy mogę bardziej dostosować domyślny styl akapitu?

O1: Tak, możesz dostosować różne parametry, takie jak nazwa czcionki, rozmiar, kolor i wyrównanie, aby dostosować je do swoich wymagań.

### P2: Czy Aspose.Note obsługuje inne operacje formatowania tekstu?

Odpowiedź 2: Oczywiście, Aspose.Note zapewnia szerokie wsparcie dla manipulowania formatowaniem tekstu, w tym stylami czcionek, punktorami i wcięciami.

### P3: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami OneNote?

O3: Aspose.Note został zaprojektowany do współpracy z plikami Microsoft OneNote w różnych wersjach, zapewniając szeroką kompatybilność.

### P4: Czy mogę zintegrować Aspose.Note z moim istniejącym projektem Java?

O4: Tak, możesz łatwo zintegrować Aspose.Note ze swoimi projektami Java, dodając niezbędne zależności i importując wymagane pakiety.

### P5: Czy dostępna jest wersja próbna Aspose.Note?

 O5: Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej Aspose.Note z poziomu[strona internetowa](https://releases.aspose.com/).