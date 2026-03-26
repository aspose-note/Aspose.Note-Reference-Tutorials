---
date: 2026-01-05
description: Dowiedz się, jak ustawić domyślną lokalizację, załadować dokument OneNote,
  ustawić licencję Aspose, przekonwertować OneNote na PNG oraz zapisać OneNote jako
  obraz przy użyciu Aspose.Note dla Javy.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Ustaw domyślną lokalizację w OneNote – Aspose.Note Java
url: /pl/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustaw domyślną lokalizację w OneNote – Aspose.Note Java

## Wprowadzenie

Jeśli potrzebujesz **ustawić domyślną lokalizację** podczas przetwarzania plików OneNote, Aspose.Note dla Javy robi to w mig. W tym samouczku przeprowadzimy Cię przez wszystkie kroki — od licencjonowania produktu, po wczytanie dokumentu OneNote, zmianę lokalizacji i w końcu konwersję pliku do obrazu PNG. Po zakończeniu będziesz mógł dostosować ustawienia językowe i generować wyniki specyficzne dla danej lokalizacji przy użyciu kilku linii kodu.

## Szybkie odpowiedzi
- **Co robi „ustaw domyślną lokalizację”?** Definiuje język i formatowanie regionalne używane przez Aspose.Note przy odczycie lub zapisie plików OneNote.  
- **Czy potrzebna jest licencja?** Tak — ustaw licencję Aspose, aby odblokować pełną funkcjonalność.  
- **Jakiej wersji Javy wymaga?** Wspierane są wszystkie wersje JDK 8+.  
- **Czy mogę konwertować OneNote do PNG?** Oczywiście; API umożliwia zapisywanie stron jako obrazy.  
- **Czy proces jest bezpieczny wątkowo?** Ustawienie domyślnej lokalizacji jest globalne, więc konfiguruje się je raz przy uruchamianiu aplikacji.

## Co to jest „ustaw domyślną lokalizację” w Aspose.Note?
Ustawienie domyślnej lokalizacji informuje Aspose.Note, którego języka i konwencji kulturowych ma używać przy parsowaniu dat, liczb i tekstu. Jest to niezbędne w aplikacjach wieloregionalnych, które wymagają spójnego formatowania niezależnie od lokalizacji użytkownika.

## Dlaczego warto ustawić domyślną lokalizację przy pracy z OneNote?
- **Precyzyjna reprezentacja danych:** Daty i liczby wyświetlane są prawidłowo dla docelowej grupy odbiorców.  
- **Spójne ciągi UI:** Tekst wyodrębniony z OneNote respektuje ustawienia językowe.  
- **Uproszczona konwersja:** Gdy później konwertujesz plik OneNote na PNG lub inne formaty, układ wizualny odpowiada oczekiwanej lokalizacji.

## Wymagania wstępne

- **Środowisko programistyczne Java:** Zainstalowany JDK i skonfigurowana zmienna `JAVA_HOME`.  
- **Biblioteka Aspose.Note:** Pobierz najnowszy plik JAR z [download link](https://releases.aspose.com/note/java/).  
- **Ważny plik licencji Aspose** (bezpłatna wersja próbna wystarczy do testów).

## Importowanie pakietów

Zanim napiszesz jakikolwiek kod, zaimportuj klasy zapewniające wymaganą funkcjonalność.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Krok 1: Ustaw licencję Aspose

```java
License license = new License();
license.setLicense("licenseFile");
```

Ustawienie licencji Aspose odblokowuje wszystkie funkcje, w tym obsługę lokalizacji i konwersję obrazów.

## Krok 2: Ustaw domyślną lokalizację

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

Tutaj **ustawiamy domyślną lokalizację** na angielski (`en`) z kodem kraju `rs`. Dostosuj kody języka i kraju do swojej docelowej regionu.

## Krok 3: Wczytaj dokument OneNote

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

Ten krok **wczytuje dokument OneNote** do obiektu `Document`, abyś mógł pracować z jego zawartością.

## Krok 4: Konwertuj OneNote na PNG (konwersja pliku OneNote)

```java
oneFile.save("sample.png");
```

Metoda `save` wykonuje **konwersję pliku OneNote**, eksportując notes (lub konkretną stronę) jako obraz PNG — w praktyce **konwertuje onenote na png** i **zapisuje onenote jako obraz**.

## Typowe problemy i wskazówki

- **Licencja nie znaleziona:** Upewnij się, że ścieżka do `licenseFile` jest poprawna i plik ma uprawnienia do odczytu.  
- **Lokalizacja nie zastosowana:** Wywołaj `Locale.setDefault` **przed** wczytaniem dokumentu.  
- **Brak wyjściowego obrazu:** Sprawdź, czy plik OneNote rzeczywiście zawiera renderowalne strony; puste notesy wygenerują pusty PNG.

## Najczęściej zadawane pytania

**P: Czy Aspose.Note jest kompatybilny z różnymi wersjami Javy?**  
O: Tak, Aspose.Note obsługuje Javę 8 i nowsze, zapewniając szeroką kompatybilność w różnych środowiskach programistycznych.

**P: Czy mogę integrować Aspose.Note z innymi bibliotekami Java?**  
O: Oczywiście. API współpracuje płynnie z popularnymi bibliotekami takimi jak Apache POI, Jackson i Spring.

**P: Czy Aspose.Note oferuje obsługę różnych formatów plików?**  
O: Choć jego głównym celem są pliki OneNote, biblioteka może eksportować do PNG, JPEG, PDF i innych formatów graficznych.

**P: Czy istnieje forum społecznościowe dla użytkowników Aspose.Note, gdzie można uzyskać pomoc i dzielić się wiedzą?**  
O: Tak, forum społeczności Aspose zapewnia platformę, na której użytkownicy mogą kontaktować się z ekspertami, zadawać pytania i współpracować nad rozwiązaniami. Odwiedź [support forum](https://forum.aspose.com/c/note/28) po pomoc.

**P: Czy mogę wypróbować Aspose.Note przed zakupem?**  
O: Oczywiście, możesz zapoznać się z możliwościami Aspose.Note, korzystając z darmowej wersji próbnej dostępnej na stronie.

## Zakończenie

Postępując zgodnie z tymi krokami, nauczyłeś się **ustawiać domyślną lokalizację**, **wczytywać dokument OneNote**, **ustawiać licencję Aspose** oraz **konwertować OneNote na PNG** przy użyciu Aspose.Note dla Javy. Ten przepływ pracy umożliwia generowanie raportów i obrazów uwzględniających lokalizację, które są dostosowane do globalnych odbiorców.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-01-05  
**Testowano z:** Aspose.Note 24.11 dla Javy  
**Autor:** Aspose  

---