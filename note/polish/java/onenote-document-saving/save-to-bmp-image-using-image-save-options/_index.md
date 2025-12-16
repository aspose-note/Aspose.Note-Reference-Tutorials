---
date: 2025-12-16
description: Dowiedz się, jak zapisywać dokumenty OneNote jako obrazy BMP przy użyciu
  opcji zapisu obrazu w Aspose.Note dla Javy. Zobacz także, jak zapisać OneNote jako
  PDF lub PNG.
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: jak zapisać OneNote jako obraz BMP przy użyciu opcji zapisu obrazu
url: /pl/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# jak zapisać OneNote jako obraz BMP przy użyciu opcji zapisu obrazu

## Wprowadzenie

Aspose.Note for Java jest potężną biblioteką, która umożliwia programistom Java pracę z plikami Microsoft OneNote programowo. **W tym samouczku dowiesz się, jak zapisać dokumenty OneNote jako obrazy BMP** przy użyciu funkcji Image Save Options w Aspose.Note for Java. Przejdziemy przez każdy krok, wyjaśnimy, dlaczego możesz wybrać BMP zamiast innych formatów, i pokażemy, jak zintegrować tę funkcję w własnych aplikacjach.

## Szybkie odpowiedzi
- **Co robi klasa Image Save Options?** Umożliwia określenie formatu wyjściowego obrazu (BMP, PNG, JPEG itp.) przy konwertowaniu strony OneNote.  
- **Czy potrzebuję licencji, aby uruchomić przykład?** Darmowa wersja próbna działa w celach oceny, ale licencja komercyjna jest wymagana do użytku produkcyjnego.  
- **Czy mogę przekonwertować stronę OneNote na PDF lub PNG zamiast BMP?** Tak – wystarczy zmienić enum `SaveFormat` (np. `SaveFormat.Pdf` lub `SaveFormat.Png`).  
- **Jaką wersję Javy obsługuje?** Java 8 i nowsze są w pełni obsługiwane.  
- **Czy istnieje specjalne przetwarzanie dużych dokumentów?** Możesz strumieniować wyjście, aby uniknąć dużego zużycia pamięci.

## Co to jest „Image Save Options” w Aspose.Note?
Klasa `ImageSaveOptions` zapewnia precyzyjną kontrolę nad tym, jak strony OneNote są renderowane jako obrazy rastrowe. Możesz ustawić format obrazu, rozdzielczość, głębię kolorów i inne. Ta elastyczność ułatwia generowanie plików BMP dla starszych systemów lub plików PNG/JPEG do użytku w sieci.

## Wymagania wstępne

1. Podstawowa znajomość języka programowania Java.  
2. Zainstalowany JDK (Java Development Kit) na komputerze.  
3. IDE, takie jak Eclipse lub IntelliJ IDEA.  
4. Biblioteka Aspose.Note for Java – pobierz ją z [here](https://releases.aspose.com/note/java/).

## Importowanie pakietów

Najpierw zaimportuj niezbędne klasy Aspose.Note oraz standardowe narzędzia I/O Javy:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Krok 1: Załaduj dokument OneNote

Tutaj wskazujemy folder zawierający źródłowy plik OneNote (`Aspose.one`) i ładujemy go do obiektu `Document`. Ten obiekt zapewnia pełny dostęp do stron, sekcji i innych elementów w notesie.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Krok 2: Zapisz dokument jako obraz BMP

Łączymy nazwę pliku wyjściowego, a następnie wywołujemy `save` z instancją `ImageSaveOptions` skonfigurowaną dla **BMP** (`SaveFormat.Bmp`).  
Jeśli chcesz **zapisać stronę OneNote** jako PNG, po prostu zamień `SaveFormat.Bmp` na `SaveFormat.Png`. Analogicznie, `SaveFormat.Pdf` umożliwia konwersję **OneNote do PDF**.

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

## Dlaczego wybrać BMP?

- **Lossless quality** – BMP przechowuje surowe dane pikseli, zachowując dokładny wygląd oryginalnej strony.  
- **Compatibility** – Starsze aplikacje Windows często wymagają plików BMP.  
- **Simplicity** – Brak artefaktów kompresji, co czyni go idealnym do dalszego przetwarzania obrazu.

## Typowe problemy i wskazówki

- **File path errors** – Upewnij się, że `dataDir` kończy się odpowiednim separatorem plików (`/` lub `\`).  
- **Large notebooks** – W przypadku bardzo dużych plików OneNote rozważ zapisywanie każdej strony osobno, aby utrzymać niskie zużycie pamięci.  
- **License exceptions** – Uruchomienie kodu bez ważnej licencji doda znak wodny do wygenerowanego obrazu.

## Podsumowanie

W tym przewodniku pokazaliśmy **jak zapisać dokumenty OneNote** jako obrazy BMP przy użyciu `ImageSaveOptions` w Aspose.Note for Java. Zmieniając enum `SaveFormat`, możesz także generować PNG, JPEG, PDF lub inne obsługiwane formaty, co daje elastyczny sposób eksportu treści OneNote do dowolnego scenariusza.

## Najczęściej zadawane pytania

**Q1: Czy mogę zapisać dokumenty OneNote w innych formatach obrazu niż BMP?**  
A: Tak, możesz użyć `ImageSaveOptions` z `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` lub `SaveFormat.Tiff`, aby wyeksportować do tych formatów.

**Q2: Czy Aspose.Note for Java obsługuje konwersję między różnymi formatami dokumentów?**  
A: Zdecydowanie. Oprócz formatów obrazu możesz konwertować pliki OneNote na PDF, DOCX, HTML i inne, używając odpowiedniego `SaveFormat`.

**Q3: Czy Aspose.Note for Java jest kompatybilny z najnowszymi wersjami OneNote?**  
A: Tak, biblioteka jest regularnie aktualizowana, aby nadążać za najnowszymi wydaniami OneNote.

**Q4: Czy mogę programowo manipulować zawartością dokumentów OneNote?**  
A: Tak, możesz dodawać, edytować lub usuwać strony, sekcje i bogatą zawartość (tekst, obrazy, tabele) za pomocą API.

**Q5: Czy Aspose.Note for Java zapewnia wsparcie techniczne?**  
A: Tak, Aspose oferuje wsparcie techniczne oraz dedykowane forum. Odwiedź [forum Aspose.Note](https://forum.aspose.com/c/note/28), aby uzyskać pomoc.

---

**Last Updated:** 2025-12-16  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
