---
date: 2026-01-28
description: Dowiedz się, jak konwertować OneNote na PDF i zarządzać licencją rozliczaną
  w Java przy użyciu Aspose.Note. Kontroluj użycie, monitoruj kredyty i utrzymuj niskie
  koszty.
linktitle: Manage Metered License for OneNote in Java
second_title: Aspose.Note Java API
title: Konwertuj OneNote na PDF i zarządzaj licencją metrową w Javie
url: /pl/java/licensing-java/manage-metered-license/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj OneNote na PDF i zarządzaj licencją metrową w Javie

## Wprowadzenie

W tym samouczku dowiesz się, jak **konwertować OneNote na PDF** przy użyciu licencji metrowej z biblioteką Aspose.Note for Java. Licencjonowanie metrowe pozwala śledzić zużycie kredytów w czasie rzeczywistym, dając elastyczność płacenia tylko za to, co wykorzystasz. Przejdziemy przez cały proces — od ustawienia kluczy licencyjnych, przez wczytanie pliku OneNote, konwersję do PDF i sprawdzenie zużycia kredytów.

## Szybkie odpowiedzi
- **Co oznacza „konwertować OneNote na PDF”?** Przekształca plik .one w przenośny dokument PDF.  
- **Która biblioteka obsługuje konwersję?** Aspose.Note for Java udostępnia prosty interfejs API do tego zadania.  
- **Czy potrzebna jest licencja do konwersji?** Tak, wymagana jest licencja metrowa do użytku produkcyjnego.  
- **Jak mogę monitorować zużycie?** Użyj `Metered.getConsumptionCredit()` i `Metered.getConsumptionQuantity()`.  
- **Czy wymagana jest dodatkowa konfiguracja?** Tylko Java JDK i plik JAR Aspose.Note.

## Co to jest „konwertować OneNote na PDF”?

Konwersja OneNote do PDF tworzy statyczną, szeroko wspieraną reprezentację stron notatnika. PDF-y są idealne do udostępniania, drukowania lub archiwizacji, ponieważ zachowują układ, czcionki i obrazy na różnych platformach.

## Dlaczego używać licencji metrowej do tej konwersji?

Licencja metrowa nalicza opłaty w oparciu o rzeczywiste zużycie kredytów, a nie stałą opłatę. Ten model jest idealny, gdy masz sporadyczne potrzeby konwersji lub chcesz, aby koszty były przewidywalne, jednocześnie korzystając z pełnej mocy Aspose.Note.

## Wymagania wstępne

1. **Java Development Kit (JDK)** – dowolna aktualna wersja (zalecany JDK 11+). Pobierz go z [tutaj](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Biblioteka Aspose.Note for Java** – pobierz najnowszy plik JAR z [oficjalnej strony](https://releases.aspose.com/note/java/).  

> **Wskazówka:** Dodaj plik JAR Aspose.Note do classpath swojego projektu lub użyj narzędzia budującego takiego jak Maven/Gradle, aby zarządzać zależnością.

## Importowanie pakietów

Najpierw zaimportuj potrzebne klasy. Zachowaj ten blok dokładnie tak, jak jest — nie wprowadzaj zmian w kodzie.

```java
import com.aspose.note.Document;
import com.aspose.note.Metered;



import java.nio.file.Paths;
```

## Krok 1: Konfiguracja licencji metrowej

```java
Metered metered = new Metered();
metered.setMeteredKey("MyPublicKey", "MyPrivateKey");
```

Tutaj tworzymy obiekt `Metered` i wprowadzamy klucze publiczny/prywatny otrzymane od Aspose. Ten krok aktywuje tryb licencjonowania metrowego dla wszystkich kolejnych operacji, w tym wywołania **convert OneNote to PDF**.

## Krok 2: Wczytaj dokument OneNote i konwertuj do PDF

```java
String dataDir = "Your Document Directory";
Document doc = new Document(Paths.get(dataDir,"Sample1.one").toString());
doc.save(Paths.get(dataDir,"MeteredLicense.pdf").toString());
```

- **Wczytaj**: `Document` odczytuje plik `.one` znajdujący się w `dataDir`. To klasyczny sposób **wczytywania dokumentu OneNote** do przetwarzania.  
- **Konwertuj i zapisz**: Wywołanie `save` z rozszerzeniem `.pdf` automatycznie **konwertuje .one na .pdf**. Operacja także **zapisuje PDF z OneNote** w tym samym folderze. Zastąp `"Your Document Directory"` rzeczywistą ścieżką na swoim komputerze.

## Krok 3: Sprawdź zużycie kredytów przed i po konwersji

```java
System.out.println(String.format("Credit before operation: %.02f", Metered.getConsumptionCredit()));
System.out.println(String.format("Consumption quantity before operation: %.02f", Metered.getConsumptionQuantity()));
```

Te dwie linie wyświetlają pozostały balans kredytów oraz ilość kredytów użytych przy konwersji. Uruchomienie tych samych wywołań po operacji `save` pokaże zaktualizowane wartości, pozwalając zweryfikować, że licencja metrowa prawidłowo śledzi zużycie.

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|-------|----------------|-----|
| **Nieprawidłowe klucze metrowe** | Klucze są błędnie wpisane lub wygasły. | Sprawdź dokładnie klucze w swoim koncie Aspose; w razie potrzeby wygeneruj nowe. |
| **Plik nie znaleziony** | Ścieżka `dataDir` jest nieprawidłowa. | Użyj ścieżki bezwzględnej lub zweryfikuj ścieżkę względną względem katalogu głównego projektu. |
| **Niewystarczająca liczba kredytów** | Wszystkie kredyty zostały zużyte. | Kup dodatkowe kredyty lub przejdź na stałą licencję przy dużych obciążeniach. |

## Najczęściej zadawane pytania

**Q: Czym jest licencja metrowa?**  
A: Licencja metrowa pozwala płacić za użycie API w oparciu o kredyty, zapewniając precyzyjną kontrolę kosztów.

**Q: Jak uzyskać klucz metrowy do produktów Aspose?**  
A: Kup licencję na stronie Aspose lub poproś o tymczasowy klucz ewaluacyjny w panelu swojego konta.

**Q: Czy mogę używać licencji metrowej w wielu aplikacjach?**  
A: Tak, ale całe zużycie jest sumowane pod tym samym kluczem, więc należy uważnie monitorować łączne zużycie.

**Q: Czy dostępna jest darmowa wersja próbna Aspose.Note for Java?**  
A: Tak, możesz pobrać darmową wersję próbną z [tutaj](https://releases.aspose.com/).

**Q: Gdzie mogę uzyskać wsparcie dla Aspose.Note for Java?**  
A: Zadawaj pytania na forum społeczności Aspose [tutaj](https://forum.aspose.com/c/note/28).

## Zakończenie

Masz teraz kompletny, gotowy do produkcji przepływ pracy, aby **konwertować OneNote na PDF** przy zarządzaniu licencją metrową w Javie. Sprawdzając zużycie kredytów przed i po konwersji, możesz zapewnić, że aplikacja mieści się w budżecie i skaluje się efektywnie.

---

**Last Updated:** 2026-01-28  
**Tested With:** Aspose.Note for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}