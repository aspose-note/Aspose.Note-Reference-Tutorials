---
date: 2026-02-07
description: Dowiedz się, jak eksportować czcionki podczas zapisywania OneNote jako
  HTML przy użyciu Aspose.Note dla Javy. Ten przewodnik pokazuje, jak programowo tworzyć
  OneNote i osadzać czcionki, CSS oraz obrazy.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Jak wyeksportować czcionki przy zapisywaniu OneNote jako HTML – Java
url: /pl/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak eksportować czcionki przy zapisywaniu OneNote jako HTML – Java

## Wprowadzenie

W tym samouczku odkryjesz **jak eksportować czcionki**, gdy **zapisujesz OneNote jako HTML** przy użyciu Aspose.Note for Java. Przeprowadzimy Cię przez tworzenie dokumentu OneNote programowo, konfigurowanie opcji zapisu HTML oraz osadzanie wymaganych plików czcionek, tak aby wygenerowany HTML wyglądał dokładnie tak jak oryginalne strony OneNote. To podejście jest idealne, gdy potrzebujesz zachować wizualną wierność treści OneNote w formacie przyjaznym dla sieci.

## Szybkie odpowiedzi
- **Jaka biblioteka obsługuje eksport?** Aspose.Note for Java  
- **Czy czcionki mogą być osadzone w HTML?** Yes – set `ExportFonts` to `ExportEmbedded`  
- **Czy potrzebna jest licencja do produkcji?** A valid Aspose.Note license is required for commercial use  
- **Która wersja Java jest wspierana?** Java 8 or higher  
- **Czy można zapisywać zasoby do osobnych plików?** Absolutely – configure `ResourceExportType` accordingly  

## Co oznacza „jak eksportować czcionki” w kontekście konwersji OneNote do HTML?

Podczas konwersji notatnika OneNote do HTML, wygląd wizualny zależy od CSS, obrazów i szczególnie od czcionek użytych na oryginalnych stronach. **Eksportowanie czcionek** oznacza osadzanie plików czcionek (np. TTF) bezpośrednio w pakiecie HTML, tak aby przeglądarki mogły renderować tekst dokładnie tak, jak wygląda w OneNote, nawet jeśli użytkownik końcowy nie ma tych czcionek zainstalowanych lokalnie.

## Dlaczego tworzyć OneNote programowo i zapisywać go jako HTML?

- **Automatyzacja:** Generuj raporty, dokumentację lub artykuły bazy wiedzy z OneNote bez ręcznego kopiowania i wklejania.  
- **Spójność:** Zachowaj układ, stylizację i niestandardowe czcionki na różnych urządzeniach.  
- **Przenośność:** HTML jest uniwersalnie wyświetlany — nie wymaga klienta OneNote.  

## Wymagania wstępne

1. Java Development Kit (JDK) 8 lub nowszy zainstalowany.  
2. Biblioteka Aspose.Note for Java – pobierz z [tutaj](https://releases.aspose.com/note/java/).  
3. Przykładowy plik OneNote (`.one`) do załadowania, lub możesz utworzyć nowy programowo.  

## Importowanie pakietów

First, import the required classes into your Java project:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Jak eksportować czcionki podczas zapisywania OneNote jako HTML?

Poniżej znajduje się przewodnik krok po kroku, który pokazuje **jak eksportować czcionki** oraz inne zasoby.

### Krok 1: Utwórz dokument OneNote programowo  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Ten wiersz ładuje istniejący plik `.one`. Jeśli potrzebujesz **utworzyć OneNote programowo**, możesz zainicjować nowy obiekt `Document` i dodać sekcje/strony za pomocą API (nie pokazano tutaj, aby skupić się na eksporcie czcionek).

### Krok 2: Zapisz do strumienia pamięci z osadzonymi czcionkami  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` informuje Aspose.Note, aby **eksportował czcionki** bezpośrednio do pakietu HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` zapewnia użycie czcionek TrueType, które mają szerokie wsparcie w przeglądarkach.

### Krok 3: Zapisz jako HTML z oddzielnymi plikami zasobów (wciąż eksportując czcionki)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Mimo że CSS i obrazy są osadzone, możesz zmienić `ResourceExportType` na `ExportExternal`, jeśli wolisz oddzielne pliki dla łatwiejszego buforowania. Kluczowa część — **eksportowanie czcionek** — pozostaje niezmieniona.

### Krok 4: Użyj callbacków, aby kontrolować, gdzie każdy zasób jest przechowywany  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Klasa `UserSavingCallbacks` (musisz zaimplementować `ICssSavingCallback`, `IImageSavingCallback` oraz `IFontSavingCallback`) daje pełną kontrolę nad strukturą folderów, umożliwiając przechowywanie czcionek w dedykowanym katalogu `fonts`, jednocześnie **eksportując czcionki** prawidłowo.

## Jak osadzić niestandardowe czcionki przy konwersji OneNote do HTML

Osadzanie niestandardowych czcionek zapewnia, że renderowanie HTML odpowiada oryginalnemu układowi OneNote, nawet na urządzeniach, które nie mają tych czcionek zainstalowanych. Korzystając z `ExportEmbedded` razem z `FontFaceType.Ttf`, pliki TrueType są kodowane base‑64 i wstawiane bezpośrednio do generowanego CSS, eliminując potrzebę zewnętrznego hostingu czcionek.

## Używanie ResourceExportType do kontrolowania eksportu zasobów

`ResourceExportType` pozwala zdecydować, czy CSS, obrazy i czcionki są przechowywane **wewnątrz** pliku HTML (`ExportEmbedded`) czy zapisywane jako **zewnętrzne** pliki (`ExportExternal`). Wybierz `ExportEmbedded` dla rozwiązania jednoplikowego, lub `ExportExternal`, gdy chcesz wykorzystać buforowanie przeglądarki dla dużych zasobów.

## Tworzenie OneNote programowo dla eksportu do HTML

Jeśli zaczynasz od zera, możesz zbudować dokument OneNote w całości w kodzie, dodać sekcje, strony i tekst sformatowany, a następnie zastosować te same `HtmlSaveOptions` przedstawione powyżej. Daje to pełną automatyzację od generowania danych po w pełni stylowany wynik HTML z osadzonymi niestandardowymi czcionkami.

## Typowe problemy i wskazówki

- **Brak czcionek w wyjściu:** Verify that `setExportFonts(ResourceExportType.ExportEmbedded)` is set and that the source OneNote file actually uses embedded fonts.  
- **Duże pliki HTML:** Embedding fonts can increase size. If bandwidth is a concern, switch `ExportFonts` to `ExportExternal` and host the fonts on a CDN.  
- **Błędy implementacji callbacków:** Ensure your callback classes correctly write the stream and close resources to avoid file corruption.  

## Najczęściej zadawane pytania

**Q:** Czy mogę konwertować wiele dokumentów OneNote do HTML jednorazowo?  
**A:** Tak, przeiteruj każdą instancję `Document` i zastosuj te same `HtmlSaveOptions`.  

**Q:** Czy Aspose.Note for Java obsługuje inne formaty wyjściowe oprócz HTML?  
**A:** Zdecydowanie tak. Możesz eksportować do PDF, DOCX, PNG, JPEG i innych, używając odpowiednich opcji zapisu.  

**Q:** Czy dostępna jest wersja próbna Aspose.Note for Java?  
**A:** Tak, pobierz darmową wersję próbną z [tutaj](https://releases.aspose.com/).  

**Q:** Gdzie mogę uzyskać wsparcie dla Aspose.Note for Java?  
**A:** Odwiedź [forum Aspose.Note](https://forum.aspose.com/c/note/28) dla pomocy społeczności i oficjalnej.  

**Q:** Jak mogę kupić licencję na Aspose.Note for Java?  
**A:** Licencje są dostępne na [stronie Aspose](https://purchase.aspose.com/buy).  

## Podsumowanie

Teraz wiesz **jak eksportować czcionki**, gdy **zapisujesz OneNote jako HTML** przy użyciu Aspose.Note for Java. Konfigurując `HtmlSaveOptions` i opcjonalnie używając callbacków, możesz zachować dokładny wygląd swoich stron OneNote — w tym niestandardowe czcionki — przy udostępnianiu ich w sieci. Śmiało eksperymentuj z różnymi ustawieniami `ResourceExportType`, aby dopasować je do wymagań wydajności i przechowywania Twojego projektu.

**Ostatnia aktualizacja:** 2026-02-07  
**Testowano z:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}