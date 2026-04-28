---
date: 2025-12-17
description: Naucz się eksportować OneNote, zapisując dokument jako szarobury obraz
  PNG przy użyciu Aspose.Note dla Javy. Zawiera kroki ładowania dokumentu OneNote
  i tworzenia obrazu w odcieniach szarości.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: Jak wyeksportować OneNote jako obraz w odcieniach szarości – Aspose.Note
url: /pl/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz jako obraz w odcieniach szarości w OneNote - Aspose.Note

## Wstęp

W tym samouczku baterii, **jak wyeksportować onenote** przez zapisanie jako dokumentu w odcieniach szarości przy użyciu Aspose.Note dla Java. Obrazy w odcieniach szarości to monochromatyczne zdjęcia zawierające tylko odcienie szarości, co może być uwalniane przy drukowaniu, archiwizacji lub zmniejszaniu pliku. Przejdziemy przez ładowanie dokumentu OneNote, skonfiguruj kartę zapisu, aby **utworzyć obraz w odcieniach szarości**, i w końcu **zapisz dokument jako PNG**.

## Szybkie odpowiedzi
- **Co oznacza „jak wyeksportować OneNote”?**Odnosi się do konwertowania pliku OneNote w innym formacie, np. obraz, programowo.
- **Jaki format jest alternatywnym rozwiązaniem dla wyjść w odcieniach szarości?**PNG sprawdza się dobrze, sprawdzając jakość bezstratną i obsługując tryby w odcieniach szarości.
- **Czy jest to licencjat?**Wymagana jest ważna licencjat Aspose.Uwaga do produkcyjnego użytku domowego; tymczasowa licencjat jest dostępny do testów.
- **Jaka wersja Javy jest wymagana?**Zalecana jest Java8 lub nowsza.
- **Czy można zmienić rozmiar obrazu?**Tak, można dostosować właściwości `ImageSaveOptions`, takie jak `Resolution` lub `PageSize`, przed zapisem.

## Co to jest „jak wyeksportować OneNote”?

Eksportowanie OneNote oznacza programowe konwertowanie pliku OneNote `.one` na inną reprezentację — taki jak PDF, HTML lub obraz. W tym przewodniku omówimy się na eksporcie do **obraz PNG w odcieniach szarości**, co jest częstym elementem w dokumentacji lub procesach kontrolnych.

## Po co eksportować program OneNote jako obraz w skali szarości?

- **Zmniejszony rozmiar pliku** – PNG w odcieniach szarości są zwykle większe niż obrazy pełnokolorowe.
- **Lepsza czytelność** – W raportach drukowanych odcieni szarości często wyraźniejszego kontrastu.
- ** kompatybilność** – PNG jest szeroko wspierany w przeglądarce, edytorach i urządzeniu mobilnym.

## Warunki wstępne

Zanim uruchomimy, wykonamy, że masz szczegółowe elementy:

1. Zainstalowany zestaw Java Development Kit (JDK) w twoim systemie.
2. Biblioteka Aspose.Note dla Javy. Możesz ją zabrać [tutaj](https://releases.aspose.com/note/java/).
3. Podstawowa przyjemność programowania w Javie.

## Importuj pakiety

Aby skorzystać, zaimportuj niezbędne pakiety:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Krok 1: Załaduj dokument programu OneNote

Najpierw **załaduj dokument onenote** wykonaj Aspose.Note. Zastąp `"Your Document Directory"`` dostępny do lokalnego folderu i ``Aspose.one'` nazwa One FileNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Krok 2: Ustaw ścieżkę wyjściową i opcje

Zdefiniuj ścieżkę wyjściową dla obrazu w odcieniach szarości i określ opcje zapisu. Ustawimy `ColorMode` na `GrayScale` i użyjemy formatu **save document as png**.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Krok 3: Zapisz dokument

Na koniec zapisz dokument jako obraz PNG w odcieniach szarości, używając skonfigurowanych opcji.

```java
oneFile.save(dataDir, options);
```

## Typowe problemy i rozwiązania
- **FileNotFoundException** – Sprawdź, czy `dataDir` wskazuje na odpowiedni folder i czy plik `.one` istnieje.
- **LicenseException** – zastosowanie, które powoduje zastosowanie Aspose.Note przed wywołaniem `save`.
- **Niska rozdzielczość wyjścia** – Dostosuj `options.setResolution(300)`, aby zobaczyć DPI w razie potrzeby.

## Często zadawane pytania

**Q1: ​​Czy mogę być zarejestrowany w innych odcieniach szarości?**
A1: Tak, po prostu zmień parametr `SaveFormat` w konstruktorze `ImageSaveOptions` na `Jpeg`, `Bmp` itp.

**Pyt. 2: Czy Aspose.Note jest stosowany ze stosowaniem wersji dokumentów OneNote?**
A2: Aspose.Note obsługuje Microsoft OneNote 2010 i późniejsze wersje.

**Pytanie 3: Czy Aspose.Note wymaga licencji do użycia?**
A3: Wymagane jest ważne prawo do użytku produkcyjnego, ale tymczasowa licencja może być dostępna do sprawdzenia.

**Q4: Czy mogę zastosować inne elementy dokumentu przed zapisaniem go jako obrazu?**
A4: Oczywiście! Aspose.Note udostępnia rozwinięte API do edycji sekcji, stron i treści przed eksportem.

**Q5: Gdzie mogę znaleźć wsparcie, jeśli występują problemy?**
A5: Wsparcie można znaleźć na forum Aspose.Note [tutaj](https://forum.aspose.com/c/note/28).

## Wniosek

Teraz wiesz, **jak wyeksportować onenote**, ładując plik OneNote, konfigurując zapis, aby **utworzyć obraz w odcieniach szarości**, i **zarejestrować dokument jako PNG**. Ta technika jest dostępna do emisji lekkich, gotowych do druku wizualizacji z notatników OneNote. Śmiało eksperymentuj z innymi urządzeniami `ColorMode` lub formatami obrazu, aby uzyskać dostęp do potrzeb projektu.

---

**Aktualizacja Ostatnia:** 2025-12-17
**Testowano z:** Aspose.Note 26.4 dla Java
**Autor:** Asponuj

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
