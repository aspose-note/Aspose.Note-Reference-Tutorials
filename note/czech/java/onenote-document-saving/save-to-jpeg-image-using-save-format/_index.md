---
title: Uložit do obrázku JPEG pomocí Uložit formát ve OneNotu
linktitle: Uložit do obrázku JPEG pomocí Uložit formát ve OneNotu
second_title: Aspose.Note Java API
description: Převeďte dokument OneNote snadno na obrázek JPEG! Tento tutoriál Java ukazuje, jak používat Aspose.Note. Převádějte a automatizujte pomocí příkladů kódu! #OneNote #Java #Aspose
type: docs
weight: 18
url: /cs/java/onenote-document-saving/save-to-jpeg-image-using-save-format/
---
## Úvod

V tomto tutoriálu se ponoříme do procesu ukládání dokumentu do obrazového formátu JPEG pomocí Aspose.Note pro Java. Aspose.Note je výkonné Java API, které umožňuje vývojářům pracovat se soubory Microsoft OneNote programově a umožňuje různé operace, jako je konverze, manipulace a extrakce obsahu.

## Předpoklady

Než začneme, ujistěte se, že máte splněny následující předpoklady:

1. Vývojové prostředí Java: Ujistěte se, že máte v systému nainstalovanou sadu Java Development Kit (JDK).
2.  Aspose.Note for Java Library: Stáhněte si a nainstalujte knihovnu Aspose.Note for Java. Můžete si jej stáhnout z[tady](https://releases.aspose.com/note/java/).

## Importujte balíčky

Nejprve importujme potřebné balíčky potřebné pro náš kód Java:

```java
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Krok 1: Vložte dokument

 Prvním krokem je načtení dokumentu do Aspose.Note. To lze provést pomocí`Document` třídy poskytuje Aspose.Note.

```java
// Cesta k adresáři dokumentů.
String dataDir = "Your Document Directory";

// Vložte dokument do Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Krok 2: Uložit jako obrázek JPEG

 Dále určíme cestu k výstupnímu souboru a uložíme dokument ve formátu obrázku JPEG pomocí`save()` metoda spolu s`SaveFormat.Jpeg` parametr.

```java
// Zadejte cestu k výstupnímu souboru.
dataDir = dataDir + "SaveToJpegImageUsingSaveFormat_out.jpg";

// Uložte dokument.
oneFile.save(dataDir, SaveFormat.Jpeg);
```

## Závěr

V tomto tutoriálu jsme se naučili, jak uložit dokument jako obrázek JPEG pomocí Aspose.Note pro Java. Dodržováním uvedených kroků můžete bez problémů převádět soubory OneNote do formátu JPEG programově, což umožňuje různé možnosti integrace a automatizace ve vašich aplikacích Java.

## FAQ

### Q1: Dokáže Aspose.Note zpracovat složité soubory OneNotu?

Odpověď 1: Ano, Aspose.Note je navržen tak, aby efektivně zpracovával složité soubory OneNote a zajistil přesnou konverzi a manipulaci.

### Q2: Je k dispozici zkušební verze pro Aspose.Note pro Java?

 A2: Ano, můžete získat bezplatnou zkušební verzi Aspose.Note pro Java od[tady](https://releases.aspose.com/).

### Q3: Jak mohu získat podporu pro Aspose.Note pro Java?

 Odpověď 3: Podporu pro Aspose.Note pro Java můžete získat na adrese[Aspose.Note fórum](https://forum.aspose.com/c/note/28).

### Q4: Mohu si zakoupit dočasnou licenci pro Aspose.Note pro Java?

 A4: Ano, můžete si zakoupit dočasnou licenci od[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Kde najdu podrobnou dokumentaci k Aspose.Note pro Java?

A5: Můžete najít podrobnou dokumentaci pro Aspose.Note pro Java[tady](https://reference.aspose.com/note/java/).