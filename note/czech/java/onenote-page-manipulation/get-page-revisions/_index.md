---
title: Získejte revize stránky ve OneNotu – Aspose.Note
linktitle: Získejte revize stránky ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Přečtěte si, jak načíst revize stránek ve OneNotu pomocí Aspose.Note pro Java. Postupujte podle našeho podrobného průvodce pro efektivní sledování změn.
weight: 14
url: /cs/java/onenote-page-manipulation/get-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Získejte revize stránky ve OneNotu – Aspose.Note

## Úvod

OneNote je výkonný nástroj pro organizování a správu poznámek, ale někdy potřebujete sledovat změny a revize provedené na vašich stránkách. S Aspose.Note pro Java můžete snadno programově načíst revize stránek. V tomto kurzu vás provedeme procesem získávání revizí stránek ve OneNotu pomocí Aspose.Note pro Java.

## Předpoklady

Než začneme, ujistěte se, že máte splněny následující předpoklady:

### 1. Java Development Kit (JDK)

Ujistěte se, že máte v systému nainstalovanou sadu Java Development Kit (JDK). JDK si můžete stáhnout a nainstalovat z webu Oracle.

### 2. Aspose.Note for Java

Stáhněte a nainstalujte Aspose.Note for Java z[odkaz ke stažení](https://releases.aspose.com/note/java/).

### 3. Ukázkový dokument OneNotu

Připravte si ukázkový dokument OneNotu (`Sample1.one`), který obsahuje stránky, ze kterých chcete načíst revize.

## Importujte balíčky

Nejprve je třeba importovat potřebné balíčky z Aspose.Note pro Javu.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Nyní rozdělme poskytnutý příklad do několika kroků:

## Krok 1: Nastavte adresář dokumentů

Definujte cestu k adresáři, kde se nachází váš dokument OneNotu.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Načtěte dokument OneNotu

 Načtěte dokument OneNotu pomocí`LoadOptions` pro povolení historie načítání.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Krok 3: Získejte první stránku

Načtěte první stránku z načteného dokumentu.

```java
Page firstPage = document.getFirstChild();
```

## Krok 4: Iterujte revizemi stránky

Procházejte každou revizi stránky a získejte relevantní informace, jako je čas poslední úpravy, čas vytvoření, název, úroveň a autor.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Závěr

V tomto kurzu jsme se naučili, jak načíst revize stránek ve OneNotu pomocí Aspose.Note pro Java. Pomocí těchto kroků můžete efektivně sledovat změny provedené na stránkách OneNotu programově.

## FAQ

### Q1: Mohu použít Aspose.Note pro Java k úpravě revizí stránek?

Odpověď 1: Ne, Aspose.Note for Java aktuálně podporuje načítání revizí stránek, ale nemění je.

### Q2: Je Aspose.Note for Java kompatibilní s různými verzemi dokumentů OneNotu?

Odpověď 2: Ano, Aspose.Note pro Java podporuje různé verze dokumentů OneNotu, což vám umožňuje bezproblémově pracovat s různými formáty souborů.

### Q3: Vyžaduje Aspose.Note pro Java licenci?

Odpověď 3: Ano, k použití Aspose.Note pro Java v komerčních projektech si musíte zakoupit licenci. Můžete však také získat dočasnou licenci pro účely hodnocení.

### Q4: Mohu vyhledat podporu, pokud při používání Aspose.Note pro Java narazím na nějaké problémy?

 A4: Ano, můžete požádat o podporu na fóru Aspose.Note[tady](https://forum.aspose.com/c/note/28).

### Q5: Je k dispozici bezplatná zkušební verze pro Aspose.Note pro Java?

 A5: Ano, máte přístup k bezplatné zkušební verzi Aspose.Note pro Java z[webová stránka](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
