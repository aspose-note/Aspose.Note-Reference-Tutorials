---
date: 2025-12-18
description: Naučte se, jak **uložit OneNote jako PDF** pomocí specifikovaného podsystému
  písem v Javě s Aspose.Note. Tento průvodce také ukazuje, jak převést OneNote do
  PDF, načíst vlastní soubory písem a určit výchozí písma.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: Uložte OneNote jako PDF pomocí podsystému specifikovaných fontů
url: /cs/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložení OneNote jako PDF pomocí specifikovaného podsystému písem

## Úvod

V mnoha obchodních scénářích potřebujete **uložit OneNote jako PDF** a zachovat přesný vzhled původních stránek. Aspose.Note pro Java to usnadňuje tím, že vám umožní řídit podsystém písem během konverze. V tomto tutoriálu projdeme tři praktické způsoby, jak **převést OneNote do PDF**, včetně **načtení vlastních souborů písem**, **specifikace výchozího písma** a dokonce **použití proudu písma**, když písmo není k dispozici na cílovém stroji.

## Rychlé odpovědi
- **Co znamená „uložit OneNote jako PDF“?** Převádí soubor .one do PDF při zachování rozvržení a stylování.  
- **Které API zpracovává písma?** `DocumentFontsSubsystem` vám umožňuje definovat výchozí písmo nebo načíst vlastní soubor/stream písma.  
- **Potřebuji licenci pro produkční použití?** Ano, pro ne‑zkušební použití je vyžadována komerční licence Aspose.Note.  
- **Mohu převádět více souborů najednou?** Ano – stačí smyčkovat načítání a ukládání `Document`.  
- **Jaká verze Javy je požadována?** Java 15 nebo novější (příklad používá JDK 15).

## Co je „uložit OneNote jako PDF“ s podsystémem písem?

Uložení OneNote jako PDF s podsystémem písem znamená, že během procesu konverze Aspose.Note nahradí chybějící glyfy písmem, které poskytnete. Tím se zajistí, že PDF vypadá identicky na jakémkoli zařízení, i když původní písmo není nainstalováno.

## Proč řídit podsystém písem při **převodu OneNote do PDF**?

- **Konzistentní značka** – firemní dokumenty zachovávají přesný typ písma.  
- **Spolehlivost napříč platformami** – PDF se vykreslují stejně na Windows, macOS, Linuxu i mobilních zařízeních.  
- **Snížené chyby** – varování o chybějících písmenech zmizí, výstup je čistý.

## Požadavky

### 1. Java Development Kit (JDK)

Ujistěte se, že máte nainstalovaný Java Development Kit (JDK). Můžete si jej stáhnout z [here](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html), pokud jej ještě nemáte.

### 2. Aspose.Note for Java Library

Stáhněte a nastavte knihovnu Aspose.Note pro Java. Můžete ji stáhnout z [website](https://releases.aspose.com/note/java/).

## Import balíčků

Ujistěte se, že ve svém Java projektu importujete potřebné balíčky:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Nyní si rozložíme každý příklad do několika kroků, abychom lépe pochopili proces.

## Jak **uložit OneNote jako PDF** pomocí Document Fonts Subsystem s výchozím písmem

### Krok 1: Uložení pomocí Document Fonts Subsystem s názvem výchozího písma

Tento krok demonstruje, jak **uložit OneNote jako PDF** jednoduchým způsobem zadáním názvu výchozího písma.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

V tomto kroku:
- Dokument OneNote je načten pomocí Aspose.Note.
- **Výchozí písmo** je nastaveno na **"Times New Roman"**.
- Dokument je uložen ve formátu PDF s vybraným písmem.

### Krok 2: Uložení pomocí Document Fonts Subsystem s výchozím písmem ze souboru

Zde **načteme vlastní soubor písma** a použijeme jej jako náhradní při konverzi do PDF.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Klíčové body:
- Vlastní soubor písma `geo_1.ttf` je načten z disku.
- `usingDefaultFontFromFile` **specifikuje výchozí písmo ze souboru**, což zajišťuje, že PDF použije toto písmo, pokud originál chybí.
- Výsledné PDF zachovává zamýšlený vzhled.

### Krok 3: Uložení pomocí Document Fonts Subsystem s výchozím písmem z proudu

Někdy může být písmo uloženo v databázi nebo přijato přes síť. Tento příklad ukazuje, jak **použít proud písma**.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Co se zde děje:
- Soubor písma je otevřen jako **InputStream**, což je užitečné, když je písmo uloženo v ne‑souborovém zdroji.
- `usingDefaultFontFromStream` **používá stream písma** k definování záložního písma.
- Soubor OneNote je uložen jako PDF s fontem založeným na streamu.

## Časté problémy a řešení

| Problém | Proč k tomu dochází | Jak opravit |
|---------|---------------------|-------------|
| **Upozornění na chybějící písmo** | Zdrojový soubor .one odkazuje na písmo, které není na počítači nainstalováno. | Poskytněte výchozí písmo pomocí `usingDefaultFont`, `usingDefaultFontFromFile` nebo `usingDefaultFontFromStream`. |
| **Soubor vlastního písma nebyl nalezen** | Nesprávná cesta k souboru `.ttf`. | Použijte absolutní cesty nebo ověřte relativní cestu vzhledem k pracovnímu adresáři. |
| **Stream není uzavřen** | Výjimka nastane před voláním `close()`. | Použijte try‑with‑resources (`try (InputStream stream = ...) { ... }`) pro automatické uzavření. |

## Často kladené otázky

**Q: Mohu specifikovat různá písma pro různé části dokumentu?**  
A: Ano, můžete použít vlastní nastavení písma pro jednotlivé prvky bohatého textu pomocí třídy `Font` v Aspose.Note.

**Q: Je Aspose.Note kompatibilní se všemi verzemi OneNote?**  
A: Aspose.Note podporuje soubory OneNote z nedávných desktopových a mobilních verzí, což zajišťuje širokou kompatibilitu.

**Q: Jak mohu řešit chybějící písma při ukládání dokumentů?**  
A: Použijte metody podsystému písem uvedené výše (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`) k poskytnutí náhradního písma.

**Q: Mohu přizpůsobit vlastnosti písma, jako je velikost a styl?**  
A: Rozhodně – API vám umožní nastavit velikost, styl, barvu a další atributy na úrovni jednotlivých běhů textu.

**Q: Je k dispozici zkušební verze pro Aspose.Note pro Java?**  
A: Ano, bezplatnou zkušební verzi lze stáhnout z webu Aspose.

## Závěr

V tomto tutoriálu jsme se naučili, jak **uložit OneNote jako PDF** a zároveň řídit podsystém písem v Javě pomocí Aspose.Note. Dodržením tří přístupů – zadání názvu výchozího písma, načtení vlastního souboru písma nebo použití proudu písma – můžete zajistit konzistentní zobrazení písem napříč platformami při exportu nebo ukládání vašich dokumentů OneNote.

---

**Poslední aktualizace:** 2025-12-18  
**Testováno s:** Aspose.Note for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}