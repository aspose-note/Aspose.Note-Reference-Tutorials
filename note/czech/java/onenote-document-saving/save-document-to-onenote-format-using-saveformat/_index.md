---
title: Uložit dokument do OneNotu pomocí SaveFormat - Aspose.Note
linktitle: Uložit dokument do OneNotu pomocí SaveFormat - Aspose.Note
second_title: Aspose.Note Java API
description: Naučte se ukládat dokumenty do formátu OneNote pomocí Aspose.Note pro Java. Postupujte podle tohoto podrobného návodu pro bezproblémovou integraci do vašich aplikací Java.
weight: 12
url: /cs/java/onenote-document-saving/save-document-to-onenote-format-using-saveformat/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložit dokument do OneNotu pomocí SaveFormat - Aspose.Note

## Úvod

Aspose.Note for Java je výkonná knihovna, která umožňuje vývojářům pracovat se soubory Microsoft OneNote programově. Uložení dokumentu do formátu OneNote pomocí SaveFormat je jednoduchý proces. V tomto tutoriálu si projdeme kroky potřebné k provedení tohoto úkolu.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1. Java Development Kit (JDK) nainstalovaný ve vašem systému.
2.  Aspose.Note pro knihovnu Java stažena. Můžete to získat od[tady](https://releases.aspose.com/note/java/).
3. Základní znalost programovacího jazyka Java.

## Importujte balíčky

 Nejprve je třeba importovat potřebné balíčky do vašeho projektu Java. To zahrnuje import`com.aspose.note` balíček pro práci s funkcemi Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## Krok 1: Nastavte adresář dokumentů

Definujte adresář, kde je umístěn váš dokument a kam chcete uložit výstupní soubor.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Vložte dokument

 Načtěte dokument do své Java aplikace pomocí`Document` třídy poskytuje Aspose.Note.

```java
Document document = new Document(dataDir + "Sample1.one");
```

## Krok 3: Uložte dokument do formátu OneNote

Uložte načtený dokument do formátu OneNote pomocí`save` metoda a určení požadovaného výstupního formátu souboru jako`SaveFormat.One`.

```java
document.save(dataDir + "SaveDocToOneNoteFormatUsingSaveformat_out.one", SaveFormat.One);
```

## Závěr

V tomto kurzu jsme se naučili, jak uložit dokument do formátu OneNote pomocí SaveFormat v Aspose.Note pro Java. Pomocí těchto jednoduchých kroků můžete tuto funkci hladce integrovat do svých aplikací Java.

## FAQ

### Q1: Je Aspose.Note for Java kompatibilní se všemi verzemi Microsoft OneNote?

Odpověď 1: Aspose.Note for Java podporuje různé verze Microsoft OneNote a zajišťuje kompatibilitu v různých prostředích.

### Q2: Mohu vyzkoušet Aspose.Note pro Java před jeho zakoupením?

 A2: Ano, můžete si stáhnout bezplatnou zkušební verzi Aspose.Note pro Java z[tady](https://releases.aspose.com/).

### Q3: Kde najdu dokumentaci k Aspose.Note pro Java?

 A3: Podrobnou dokumentaci pro Aspose.Note pro Java lze nalézt[tady](https://reference.aspose.com/note/java/).

### Q4: Jak mohu získat technickou podporu pro Aspose.Note pro Java?

 Odpověď 4: Pro technickou pomoc a podporu můžete navštívit fórum Aspose.Note[tady](https://forum.aspose.com/c/note/28).

### Q5: Je k dispozici možnost dočasné licence pro Aspose.Note pro Java?

 A5: Ano, můžete získat dočasnou licenci pro Aspose.Note pro Java od[tady](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
