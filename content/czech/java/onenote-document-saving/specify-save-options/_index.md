---
title: Určete možnosti uložení ve OneNotu – Aspose.Note
linktitle: Určete možnosti uložení ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Přečtěte si, jak určit možnosti uložení ve OneNotu pomocí Aspose.Note pro Java. Přizpůsobte si index, počet a nastavení komprese bez námahy.
type: docs
weight: 24
url: /cs/java/onenote-document-saving/specify-save-options/
---
## Úvod

tomto tutoriálu se naučíme, jak určit možnosti uložení ve OneNotu pomocí Aspose.Note pro Javu. Aspose.Note je výkonná knihovna Java, která umožňuje vývojářům vytvářet, manipulovat a převádět dokumenty OneNote programově. S Aspose.Note můžete snadno ovládat různé možnosti ukládání a přizpůsobit výstup podle svých požadavků.

## Předpoklady

Než začnete, ujistěte se, že máte následující předpoklady:

1. Základní znalost programovacího jazyka Java.
2. JDK (Java Development Kit) nainstalovaný ve vašem systému.
3.  Nainstalovaná knihovna Aspose.Note pro Java. Můžete si jej stáhnout z[tady](https://releases.aspose.com/note/java/).

## Importujte balíčky

Chcete-li začít, importujte potřebné balíčky do kódu Java:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

Rozdělme si příklad do několika kroků:

## Krok 1: Načtěte dokument OneNotu

```java
// Cesta k adresáři dokumentů.
String dataDir = "Your Document Directory";

// Vložte dokument do Aspose.Note.
Document doc = new Document(dataDir + "Aspose.one");
```

 V tomto kroku určíme cestu k dokumentu OneNotu a načteme jej do`Document` objekt.

## Krok 2: Inicializujte objekt PdfSaveOptions

```java
// Inicializujte objekt PdfSaveOptions
PdfSaveOptions opts = new PdfSaveOptions();
```

 Zde inicializujeme a`PdfSaveOptions` objekt, který bude použit k určení možností pro uložení dokumentu jako PDF.

## Krok 3: Nastavte index a počet stránek

```java
// Nastavit index stránky
opts.setPageIndex(2);

// Nastavte počet stránek
opts.setPageCount(3);
```

Tyto řádky nastavují index a počet stránek, které se mají uložit. V tomto příkladu ukládáme stránky počínaje indexem 2 a celkem 3 stránky.

## Krok 4: Zadejte nastavení komprese

```java
// V případě potřeby zadejte kompresi
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

Zde specifikujeme nastavení komprese obrázků pro PDF. Nastavíme kompresi na formát JPEG a kvalitu JPEG určíme na 90 %.

## Krok 5: Uložte dokument pomocí možností

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

Nakonec dokument uložíme se zadanými možnostmi. Výstupní PDF se uloží na zadané místo s danými možnostmi.

## Závěr

V tomto kurzu jsme se naučili, jak určit možnosti uložení ve OneNotu pomocí Aspose.Note pro Javu. Přizpůsobením voleb ukládání můžete ovládat různé aspekty výstupního dokumentu, jako je index stránky, počet a nastavení komprese.

## FAQ

### Q1: Dokáže Aspose.Note zpracovat velké dokumenty OneNotu?

Odpověď 1: Ano, Aspose.Note je navržen tak, aby efektivně zpracovával velké dokumenty OneNotu.

### Q2: Je Aspose.Note kompatibilní s nejnovějšími verzemi Java?

Odpověď 2: Ano, Aspose.Note je kompatibilní s nejnovějšími verzemi Java.

### Q3: Mohu převést dokumenty OneNote do jiných formátů pomocí Aspose.Note?

Odpověď 3: Ano, Aspose.Note podporuje převod dokumentů OneNote do různých formátů, jako jsou PDF, DOCX a HTML.

### Q4: Poskytuje Aspose.Note podporu pro šifrování a dešifrování dokumentů OneNotu?

Odpověď 4: Ano, Aspose.Note poskytuje rozhraní API pro šifrování a dešifrování dokumentů OneNotu.

### Q5: Je Aspose.Note vhodný pro komerční použití?

A5: Ano, Aspose.Note lze použít pro komerční účely zakoupením licence.