---
title: Převést Poznámkový blok na sloučený PDF ve OneNotu – Aspose.Note
linktitle: Převést Poznámkový blok na sloučený PDF ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Převádějte notebooky na sloučené PDF bez námahy pomocí Aspose.Note pro Java. Užijte si bezproblémovou integraci a možnosti přizpůsobení.
weight: 16
url: /cs/java/onenote-notebook-operations/convert-notebook-to-flattened-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převést Poznámkový blok na sloučený PDF ve OneNotu – Aspose.Note

## Úvod

V tomto tutoriálu prozkoumáme, jak převést notebook do sloučeného formátu PDF pomocí Aspose.Note pro Java. Převod poznámkových bloků do PDF je běžným požadavkem mnoha aplikací a Aspose.Note tento proces zjednodušuje pomocí komplexní sady funkcí a snadno použitelného rozhraní API.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1. Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK.
2.  Aspose.Note for Java Library: Stáhněte si a nainstalujte knihovnu Aspose.Note for Java z[tady](https://releases.aspose.com/note/java/).
3. Integrované vývojové prostředí (IDE): Vyberte si IDE podle svých preferencí, jako je IntelliJ IDEA nebo Eclipse.

## Importujte balíčky

Nejprve importujme potřebné balíčky do vašeho projektu Java:

```java
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import java.io.IOException;
```

## Krok 1: Načtěte OneNote Notebook

Chcete-li začít, načtěte poznámkový blok OneNotu, který chcete převést do PDF:

```java
String dataDir = "Your Document Directory";
Notebook notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## Krok 2: Nastavte možnosti převodu

 Definujte možnosti pro převod poznámkového bloku do PDF. Tady, nastavíme`flatten` na`true` pro sloučení PDF:

```java
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
notebookSaveOptions.setFlatten(true);
```

## Krok 3: Uložte Poznámkový blok jako PDF

Určete výstupní adresář a uložte zápisník jako PDF s definovanými možnostmi:

```java
dataDir = dataDir + "ExportNotebookToPDFAsFlattened_out.pdf";
// Uložte notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Závěr

V tomto tutoriálu jsme se naučili, jak převést notebook do sloučeného formátu PDF pomocí Aspose.Note pro Javu. Tento proces je přímočarý a lze jej bez problémů integrovat do vašich aplikací Java.

## FAQ

### Q1: Je Aspose.Note for Java kompatibilní s různými verzemi OneNotu?

Odpověď 1: Ano, Aspose.Note pro Java podporuje různé verze OneNotu, což zajišťuje kompatibilitu v různých prostředích.

### Q2: Mohu přizpůsobit výstup PDF pomocí Aspose.Note pro Java?

A2: Absolutně můžete upravit výstup PDF podle svých požadavků, včetně rozvržení stránky, stylů písem a dalších.

### Q3: Podporuje Aspose.Note pro Java dávkovou konverzi notebooků?

Odpověď 3: Ano, pomocí Aspose.Note pro Java můžete dávkově převést více poznámkových bloků do PDF efektivně.

### Q4: Je k dispozici zkušební verze pro Aspose.Note pro Java?

 A4: Ano, máte přístup k bezplatné zkušební verzi Aspose.Note pro Java od[tady](https://releases.aspose.com/).

### Q5: Kde najdu podporu pro Aspose.Note pro Java?

 A5: Podporu a pomoc pro Aspose.Note pro Java najdete na[Aspose.Note fórum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
