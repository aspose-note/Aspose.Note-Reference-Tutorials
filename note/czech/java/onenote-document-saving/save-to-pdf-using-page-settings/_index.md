---
title: Uložit do PDF pomocí nastavení stránky ve OneNotu – Aspose.Note
linktitle: Uložit do PDF pomocí nastavení stránky ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Naučte se ukládat dokumenty OneNotu do PDF v Javě pomocí knihovny Aspose.Note. Podrobný průvodce s příklady kódu pro různá nastavení stránky.
type: docs
weight: 19
url: /cs/java/onenote-document-saving/save-to-pdf-using-page-settings/
---
## Úvod

V tomto tutoriálu se naučíme, jak uložit dokumenty OneNote do formátu PDF pomocí různých nastavení stránky pomocí Aspose.Note pro Java. Probereme dva způsoby: uložení s nastavením stránky Letter a uložení s nastavením stránky A4 bez omezení výšky.

## Předpoklady

Než začneme, ujistěte se, že máte splněny následující předpoklady:

1. Java Development Kit (JDK) nainstalovaný ve vašem systému.
2. Aspose.Note pro knihovnu Java staženou a zahrnutou do vašeho projektu Java.
3. Základní znalost programovacího jazyka Java.

## Importujte balíčky

Ujistěte se, že jste importovali potřebné balíčky pro použití Aspose.Note for Java ve vašem projektu. Zde je prohlášení o importu:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Uložit do PDF pomocí nastavení stránky Letter

### Krok 1: Vložte dokument

Nejprve načtěte dokument OneNotu do Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Krok 2: Definujte cílovou cestu

Zadejte cílovou cestu pro soubor PDF:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Krok 3: Uložte dokument

Uložte dokument s nastavením stránky Letter:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Uložit do PDF pomocí nastavení stránky A4 bez omezení výšky

### Krok 1: Vložte dokument

Podobně načtěte dokument OneNotu do Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Krok 2: Definujte cílovou cestu

Zadejte cílovou cestu pro soubor PDF:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Krok 3: Uložte dokument

Uložte dokument s nastavením stránky A4 bez omezení výšky:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Po provedení těchto kroků úspěšně uložíte dokument OneNotu do PDF s jiným nastavením stránky.

## Závěr

V tomto tutoriálu jsme prozkoumali, jak uložit dokumenty OneNote do formátu PDF pomocí knihovny Aspose.Note pro Java. Podle podrobného průvodce můžete tuto funkci snadno integrovat do svých aplikací Java.

## FAQ

### Q1: Mohu dále upravit nastavení stránky?

Odpověď 1: Ano, pomocí Aspose.Note pro Java si můžete upravit nastavení stránky podle svých požadavků.

### Q2: Podporuje Aspose.Note jiné výstupní formáty kromě PDF?

A2: Ano, Aspose.Note podporuje různé výstupní formáty včetně obrázků a HTML.

### Q3: Je Aspose.Note kompatibilní s různými verzemi souborů OneNotu?

Odpověď 3: Ano, Aspose.Note podporuje soubory OneNote z různých verzí včetně .one a .onetoc2.

### Q4: Mohu převést více souborů OneNotu do PDF v jednom spuštění?

A4: Ano, můžete dávkově zpracovat více souborů OneNote pomocí Aspose.Note pro Java.

### Q5: Je k dispozici nějaká zkušební verze pro testovací účely?

A5: Ano, můžete získat bezplatnou zkušební verzi Aspose.Note pro Java z webu.