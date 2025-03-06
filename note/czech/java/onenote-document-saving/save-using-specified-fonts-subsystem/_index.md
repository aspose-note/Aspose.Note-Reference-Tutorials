---
title: Uložit pomocí zadaného podsystému písem ve OneNotu
linktitle: Uložit pomocí zadaného podsystému písem ve OneNotu
second_title: Aspose.Note Java API
description: Naučte se ukládat dokumenty OneNotu pomocí specifikovaného subsystému písem v Javě pomocí Aspose.Note. Zajistěte bez námahy konzistentní reprezentaci písem napříč platformami.
weight: 22
url: /cs/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložit pomocí zadaného podsystému písem ve OneNotu

## Úvod

Aspose.Note for Java poskytuje robustní možnosti pro práci s dokumenty OneNotu. Jedním společným požadavkem při práci s takovými dokumenty je zajištění správné údržby písem, zejména pokud má být dokument exportován nebo uložen v různých formátech, jako je PDF. Tento výukový program vás provede procesem ukládání dokumentů OneNotu při specifikaci podsystému písem, což zajistí konzistentní a přesnou reprezentaci textu na různých platformách.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte nastaveny následující předpoklady:

### 1. Java Development Kit (JDK)

 Ujistěte se, že máte v systému nainstalovanou sadu Java Development Kit (JDK). Můžete si jej stáhnout z[tady](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) pokud jste to ještě neudělali.

### 2. Aspose.Note for Java Library

 Stáhněte a nastavte knihovnu Aspose.Note for Java. Můžete si jej stáhnout z[webová stránka](https://releases.aspose.com/note/java/).

## Importujte balíčky

Ujistěte se, že do svého projektu Java importujete potřebné balíčky:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Nyní si každý příklad rozdělíme do několika kroků, abychom procesu lépe porozuměli.

## Krok 1: Uložení pomocí podsystému písem dokumentu s výchozím názvem písma

Tento krok ukazuje, jak uložit dokument ve formátu PDF pomocí zadaného výchozího názvu písma.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Vložte dokument do Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Zadejte výchozí písmo.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Uložte dokument jako PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

V tomto kroku:
- Dokument OneNotu se načte pomocí Aspose.Note.
- Výchozí písmo je určeno jako "Times New Roman".
- Dokument se uloží ve formátu PDF se zadaným písmem.

## Krok 2: Uložte pomocí podsystému písem dokumentu s výchozím písmem ze souboru

Tento krok ukazuje, jak uložit dokument ve formátu PDF pomocí výchozího písma načteného ze souboru.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Vložte dokument do Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Zadejte cestu k souboru písma.
    String fontFile = "geo_1.ttf";

    // Zadejte výchozí písmo ze souboru.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Uložte dokument jako PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

V tomto kroku:
- Načte se soubor fontu "geo_1.ttf".
- Výchozí písmo je určeno z načteného souboru písma.
- Dokument se uloží ve formátu PDF se zadaným písmem.

## Krok 3: Uložte pomocí subsystému písem dokumentu s výchozím písmem ze streamu

Tento krok ukazuje, jak uložit dokument ve formátu PDF pomocí výchozího písma načteného ze streamu.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Vložte dokument do Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Zadejte cestu k souboru písma.
    String fontFile = "geo_1.ttf";

    // Načtěte soubor písma jako proud.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Zadejte výchozí písmo ze streamu.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Uložte dokument jako PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

V tomto kroku:
- Soubor fontu "geo_1.ttf" se načte jako proud.
- Výchozí písmo je určeno z načteného streamu.
- Dokument se uloží ve formátu PDF se zadaným písmem.

## Závěr

V tomto tutoriálu jsme se naučili ukládat dokumenty OneNote pomocí specifikovaného subsystému písem v Javě pomocí Aspose.Note. Pomocí těchto kroků můžete zajistit konzistentní reprezentaci písem na různých platformách při exportu nebo ukládání dokumentů.

## FAQ

### Q1: Mohu zadat různá písma pro různé části dokumentu?

Odpověď 1: Ano, pomocí Aspose.Note pro Javu můžete určit různá písma pro různé části dokumentu.

### Q2: Je Aspose.Note kompatibilní se všemi verzemi OneNotu?

Odpověď 2: Aspose.Note podporuje různé verze OneNotu a zajišťuje kompatibilitu v různých prostředích.

### Q3: Jak mohu vyřešit chybějící písma při ukládání dokumentů?

A3: Aspose.Note poskytuje možnosti pro určení výchozích písem, aby bylo možné efektivně zpracovat chybějící písma během ukládání dokumentu.

### Q4: Mohu přizpůsobit vlastnosti písma, jako je velikost a styl?

Odpověď 4: Ano, pomocí Aspose.Note pro Java můžete upravit vlastnosti písma, jako je velikost, styl a barva.

### Q5: Je k dispozici zkušební verze pro Aspose.Note pro Java?

A5: Ano, můžete získat bezplatnou zkušební verzi Aspose.Note pro Java z webu.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
