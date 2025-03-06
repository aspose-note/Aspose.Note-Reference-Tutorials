---
title: Vytvořte dokument OneNote a uložte do HTML - Java
linktitle: Vytvořte dokument OneNote a uložte do HTML - Java
second_title: Aspose.Note Java API
description: Naučte se vytvářet a ukládat dokumenty OneNote jako HTML pomocí Aspose.Note pro Java. Integrujte do aplikací Java pro programovou práci se soubory OneNote.

weight: 18
url: /cs/java/onenote-document-loading/create-onenote-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvořte dokument OneNote a uložte do HTML - Java

## Úvod

Aspose.Note for Java je výkonná knihovna, která umožňuje vývojářům pracovat se soubory Microsoft OneNote programově. V tomto tutoriálu prozkoumáme, jak vytvořit dokument OneNote a uložit jej do formátu HTML pomocí Aspose.Note for Java.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1. Java Development Kit (JDK) nainstalovaný ve vašem systému.
2.  Aspose.Note pro knihovnu Java. Můžete si jej stáhnout z[tady](https://releases.aspose.com/note/java/).
3. Základní znalost programování v Javě.

## Importujte balíčky

Nejprve importujte potřebné balíčky do svého projektu Java:

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

## Krok 1: Vytvořte objekt dokumentu OneNotu

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Tento kód inicializuje a`Document` objekt načtením ukázkového souboru OneNotu.

## Krok 2: Uložit jako HTML do Memory Stream

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Zde nastavíme možnosti uložení HTML a uložíme dokument do paměti.

## Krok 3: Uložte jako HTML se zdroji v samostatných souborech

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Tento krok uloží dokument jako HTML se zdroji, jako jsou CSS, písma a obrázky, do samostatných souborů.

## Krok 4: Uložit jako HTML do Memory Stream se zpětnými voláními pro uložení zdrojů

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

Zde dokument uložíme jako HTML do paměťového streamu pomocí zpětných volání, abychom zvládli úsporu zdrojů.

## Závěr

Gratulujeme! Naučili jste se vytvořit dokument OneNote a uložit jej do formátu HTML pomocí Aspose.Note pro Java. Nyní můžete tuto funkci integrovat do svých aplikací Java, abyste mohli programově pracovat se soubory OneNotu.

## FAQ

### Q1: Mohu převést více dokumentů OneNotu do HTML najednou?

Odpověď 1: Ano, můžete procházet více dokumenty a proces ukládání použít iterativně.

### Q2: Podporuje Aspose.Note for Java jiné výstupní formáty kromě HTML?

Odpověď 2: Ano, Aspose.Note for Java podporuje různé výstupní formáty včetně PDF, DOCX a obrazových formátů.

### Q3: Je k dispozici zkušební verze pro Aspose.Note pro Java?

A3: Ano, můžete si stáhnout bezplatnou zkušební verzi z[tady](https://releases.aspose.com/).

### Q4: Kde mohu získat podporu pro Aspose.Note pro Java?

 A4: Můžete získat podporu od[Aspose.Note fórum](https://forum.aspose.com/c/note/28).

### Q5: Jak mohu zakoupit licenci pro Aspose.Note pro Java?

 A5: Můžete si zakoupit licenci z[Aspose webové stránky](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
