---
title: Převést dokument OneNote do PDF - Java
linktitle: Převést dokument OneNote do PDF - Java
second_title: Aspose.Note Java API
description: Naučte se převádět dokumenty OneNotu do PDF pomocí Aspose.Note pro Java. Vylepšete své možnosti zpracování dokumentů pomocí tohoto podrobného průvodce.
weight: 16
url: /cs/java/onenote-document-loading/convert-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převést dokument OneNote do PDF - Java

## Úvod

V tomto tutoriálu prozkoumáme, jak převést dokumenty OneNote do PDF pomocí Aspose.Note pro Java. Aspose.Note je výkonná Java knihovna, která umožňuje bezproblémovou manipulaci se soubory OneNote a poskytuje různé funkce pro práci s různými prvky v rámci těchto dokumentů. Jedním z běžných požadavků je převod těchto souborů do formátu PDF, čehož lze snadno dosáhnout pomocí Aspose.Note.

## Předpoklady

Než začneme, ujistěte se, že máte splněny následující předpoklady:

1.  Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK. Můžete si jej stáhnout z[tady](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Aspose.Note for Java: Musíte mít knihovnu Aspose.Note for Java. Pokud jste tak ještě neučinili, můžete si jej stáhnout z[tady](https://releases.aspose.com/note/java/).

## Importujte balíčky

Chcete-li začít, importujte potřebné balíčky do svého projektu Java. Budete potřebovat`com.aspose.note.Document` a`com.aspose.note.PdfSaveOptions` třídy.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
```

Pojďme si proces převodu dokumentu OneNotu do PDF rozdělit do několika kroků:

## Krok 1: Načtěte dokument OneNotu

Nejprve načtěte dokument OneNotu do Aspose.Note.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

 Nahradit`"Your Document Directory"` s cestou k vašemu dokumentu OneNotu.

## Krok 2: Inicializujte objekt PdfSaveOptions

 Inicializovat a`PdfSaveOptions` objekt, který určí možnosti pro uložení dokumentu jako PDF.

```java
PdfSaveOptions options = new PdfSaveOptions();
```

## Krok 3: Nastavte index stránky a počet (volitelné)

Pokud chcete převést pouze konkrétní stránky dokumentu OneNotu, můžete volitelně nastavit index a počet stránek.

```java
// Nastavit index stránky
// options.setPageIndex(2);

// Nastavte počet stránek
// options.setPageCount(3);
```

Odkomentujte a upravte tyto řádky podle potřeby.

## Krok 4: Uložte dokument jako PDF

Uložte načtený dokument OneNotu jako soubor PDF pomocí zadaných možností.

```java
oneFile.save(dataDir + "ConvertToPdf_out.pdf", options);
```

## Krok 5: Zobrazte zprávu o úspěchu

Nakonec vytiskněte zprávu o úspěšném převodu dokumentu do PDF.

```java
System.out.println("File saved: " + dataDir + "ConvertToPdf_out.pdf");
```

## Závěr

tomto tutoriálu jsme se naučili, jak převést dokumenty OneNote do PDF pomocí Aspose.Note pro Java. Podle tohoto podrobného průvodce můžete snadno integrovat tuto funkci do svých aplikací Java a vylepšit tak možnosti zpracování dokumentů.

## FAQ

### Q1: Je Aspose.Note kompatibilní se všemi verzemi OneNotu?

Odpověď 1: Aspose.Note podporuje různé verze OneNotu a zajišťuje kompatibilitu s většinou dokumentů OneNotu.

### Q2: Mohu přizpůsobit nastavení převodu PDF?

 A2: Ano, můžete upravit nastavení převodu PDF pomocí`PdfSaveOptions` třídy dle vašich požadavků.

### Q3: Vyžaduje Aspose.Note licenci pro komerční použití?

 A3: Ano, Aspose.Note vyžaduje licenci pro komerční použití. Licenci můžete získat od[tady](https://purchase.aspose.com/buy).

### Q4: Je pro uživatele Aspose.Note k dispozici technická podpora?

 A4: Ano, pro uživatele Aspose.Note je k dispozici technická podpora. Můžete vstoupit do fóra podpory[tady](https://forum.aspose.com/c/note/28).

### Q5: Mohu vyzkoušet Aspose.Note před nákupem?

A5: Ano, můžete požádat o bezplatnou zkušební verzi Aspose.Note od[tady](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
