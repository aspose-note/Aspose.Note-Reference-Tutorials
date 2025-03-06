---
title: Převést Poznámkový blok na obrázek s možnostmi ve OneNotu – Aspose.Note
linktitle: Převést Poznámkový blok na obrázek s možnostmi ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Naučte se, jak převést notebook na obrázek s možnostmi pomocí Aspose.Note for Java. Postupujte podle našeho podrobného návodu pro bezproblémovou integraci do vašich aplikací Java.
weight: 14
url: /cs/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převést Poznámkový blok na obrázek s možnostmi ve OneNotu – Aspose.Note

## Úvod

V tomto tutoriálu se ponoříme do procesu převodu Notebooku na obrázek s různými možnostmi pomocí Aspose.Note pro Javu. Aspose.Note je výkonné Java API, které umožňuje vývojářům pracovat se soubory Microsoft OneNote programově, což umožňuje bezproblémovou integraci do jejich aplikací Java.

## Předpoklady

Než začneme, ujistěte se, že máte splněny následující předpoklady:

1. Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK.
2. Aspose.Note pro soubory Java JAR: Stáhněte si knihovnu Aspose.Note pro Java z[tady](https://releases.aspose.com/note/java/) a zahrňte jej do cesty třídy vašeho projektu.

## Importujte balíčky

Nejprve importujme potřebné balíčky pro naši aplikaci Java:

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Krok 1: Vložte notebook

Chcete-li začít, musíme načíst poznámkový blok OneNote, který chceme převést na obrázek.

```java
String dataDir = "Your Document Directory";
// Načtěte poznámkový blok OneNotu
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## Krok 2: Nastavte možnosti uložení

Dále definujeme možnosti uložení obrázku, včetně požadovaného formátu (PNG, JPEG atd.) a rozlišení.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

## Krok 3: Uložte notebook jako obrázek

Nyní poznámkový blok uložíme jako obrázek se zadanými možnostmi.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Uložte notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Závěr

V tomto tutoriálu jsme se naučili, jak převést Notebook na obrázek s různými možnostmi pomocí Aspose.Note pro Javu. Podle těchto kroků můžete tuto funkci bez problémů integrovat do svých aplikací Java a otevřít možnosti pro programovou manipulaci se soubory OneNotu.

## FAQ

### Q1: Dokáže Aspose.Note zpracovat složité soubory OneNotu?

Odpověď 1: Ano, Aspose.Note dokáže efektivně zpracovávat složité soubory OneNotu, což vám umožňuje programově s nimi provádět různé operace.

### Q2: Lze Aspose.Note pro Javu snadno integrovat do stávajících projektů?

A2: Rozhodně! Aspose.Note for Java poskytuje přímočaré API, které lze snadno integrovat do vašich projektů Java, což vám ušetří čas a úsilí.

### Otázka 3: Mohu přizpůsobit výstup obrazu při převodu notebooku?

Odpověď 3: Ano, Aspose.Note vám umožňuje přizpůsobit výstup obrazu zadáním možností, jako je rozlišení, formát a další.

### Q4: Nabízí Aspose.Note podporu pro vývojáře?

Odpověď 4: Ano, Aspose poskytuje vynikající podporu vývojářům prostřednictvím jejich fór a dokumentace, což zajišťuje hladkou integraci a odstraňování problémů.

### Q5: Je k dispozici bezplatná zkušební verze pro Aspose.Note pro Java?

 A5: Ano, můžete využít bezplatnou zkušební verzi Aspose.Note pro Java od[tady](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
