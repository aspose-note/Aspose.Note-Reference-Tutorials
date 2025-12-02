---
date: 2025-12-02
description: Dowiedz się, jak eksportować czcionki podczas zapisywania OneNote jako
  HTML przy użyciu Aspose.Note dla Javy. Ten przewodnik pokazuje, jak programowo tworzyć
  OneNote i osadzać czcionki, CSS oraz obrazy.
language: pl
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Jak wyeksportować czcionki przy zapisywaniu OneNote jako HTML – Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak eksportować czcionki przy zapisywaniu OneNote jako HTML – Java

## Introduction

W tym samouczku dowiesz się, **jak eksportować czcionki** podczas **zapisywania OneNote jako HTML** przy użyciu Aspose.Note for Java. Przejdziemy przez tworzenie dokumentu OneNote programowo, konfigurowanie opcji zapisu HTML oraz osadzanie wymaganych plików czcionek, aby wynikowy HTML wyglądał dokładnie tak jak oryginalne strony OneNote. To podejście jest idealne, gdy potrzebujesz zachować wizualną wierność treści OneNote w formacie przyjaznym dla sieci.

## Quick Answers
- **Jaką bibliotekę obsługuje eksport?** Aspose.Note for Java  
- **Czy czcionki mogą być osadzone w HTML?** Tak – ustaw `ExportFonts` na `ExportEmbedded`  
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest ważna licencja Aspose.Note do użytku komercyjnego  
- **Jaką wersję Javy obsługuje?** Java 8 lub wyższa  
- **Czy można zapisywać zasoby do osobnych plików?** Oczywiście – skonfiguruj `ResourceExportType` odpowiednio  

## What is “how to export fonts” in the context of OneNote HTML conversion?

Co oznacza „jak eksportować czcionki” w kontekście konwersji OneNote do HTML?  
Podczas konwersji notesu OneNote do HTML wygląd wizualny zależy od CSS, obrazów i szczególnie od czcionek użytych na oryginalnych stronach. **Eksportowanie czcionek** oznacza osadzenie plików czcionek (np. TTF) bezpośrednio w pakiecie HTML, aby przeglądarki mogły renderować tekst dokładnie tak, jak w OneNote, nawet jeśli użytkownik końcowy nie ma tych czcionek zainstalowanych lokalnie.

## Why create OneNote programmatically and save it as HTML?

- **Automatyzacja:** Generowanie raportów, dokumentacji lub artykułów bazy wiedzy z OneNote bez ręcznego kopiowania‑wklejania.  
- **Spójność:** Zachowanie układu, stylizacji i niestandardowych czcionek na różnych urządzeniach.  
- **Przenośność:** HTML jest uniwersalnie wyświetlany — nie wymaga klienta OneNote.  

## Prerequisites

1. Java Development Kit (JDK) 8 lub nowszy zainstalowany.  
2. Aspose.Note for Java library – download from [here](https://releases.aspose.com/note/java/).  
3. Przykładowy plik OneNote (`.one`) do załadowania, lub możesz utworzyć nowy programowo.  

## Import Packages

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

## How to Export Fonts While Saving OneNote as HTML?

Poniżej znajduje się przewodnik krok po kroku, który pokazuje, **jak eksportować czcionki** oraz inne zasoby.

### Step 1: Create a OneNote document programmatically  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Ten wiersz ładuje istniejący plik `.one`. Jeśli potrzebujesz **utworzyć OneNote programowo**, możesz zainicjować nowy obiekt `Document` i dodać sekcje/strony za pomocą API (nie pokazano tutaj, aby skupić się na eksportowaniu czcionek).

### Step 2: Save to a memory stream with embedded fonts  

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

### Step 3: Save as HTML with separate resource files (still exporting fonts)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Mimo że CSS i obrazy są osadzone, możesz zmienić `ResourceExportType` na `ExportExternal`, jeśli wolisz osobne pliki dla łatwiejszego buforowania. Kluczowa część — **eksportowanie czcionek** — pozostaje niezmieniona.

### Step 4: Use callbacks to control where each resource is stored  

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

## Common Issues & Tips

- **Brak czcionek w wyniku:** Sprawdź, czy ustawiono `setExportFonts(ResourceExportType.ExportEmbedded)` oraz czy źródłowy plik OneNote rzeczywiście używa osadzonych czcionek.  
- **Duże pliki HTML:** Osadzanie czcionek może zwiększyć rozmiar. Jeśli przepustowość jest problemem, przełącz `ExportFonts` na `ExportExternal` i hostuj czcionki na CDN.  
- **Błędy implementacji callbacków:** Upewnij się, że klasy callback poprawnie zapisują strumień i zamykają zasoby, aby uniknąć uszkodzenia pliku.  

## Frequently Asked Questions

**Q:** Czy mogę konwertować wiele dokumentów OneNote do HTML jednocześnie?  
**A:** Tak, przeiteruj każdą instancję `Document` i zastosuj te same `HtmlSaveOptions`.  

**Q:** Czy Aspose.Note for Java obsługuje inne formaty wyjściowe poza HTML?  
**A:** Oczywiście. Możesz eksportować do PDF, DOCX, PNG, JPEG i innych, używając odpowiednich opcji zapisu.  

**Q:** Czy dostępna jest wersja próbna Aspose.Note for Java?  
**A:** Tak, pobierz darmową wersję próbną z [here](https://releases.aspose.com/).  

**Q:** Gdzie mogę uzyskać wsparcie dla Aspose.Note for Java?  
**A:** Odwiedź [Aspose.Note forum](https://forum.aspose.com/c/note/28) w celu uzyskania pomocy społeczności i oficjalnej.  

**Q:** Jak mogę zakupić licencję na Aspose.Note for Java?  
**A:** Licencje są dostępne na [Aspose website](https://purchase.aspose.com/buy).  

## Conclusion

Teraz wiesz, **jak eksportować czcionki**, gdy **zapisujesz OneNote jako HTML** przy użyciu Aspose.Note for Java. Konfigurując `HtmlSaveOptions` i opcjonalnie używając callbacków, możesz zachować dokładny wygląd swoich stron OneNote — w tym niestandardowe czcionki — przy publikacji w sieci. Śmiało eksperymentuj z różnymi ustawieniami `ResourceExportType`, aby dopasować je do wymagań wydajności i przechowywania Twojego projektu.

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
