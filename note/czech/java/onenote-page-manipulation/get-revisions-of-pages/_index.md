---
title: Získejte revize stránek ve OneNotu – Aspose.Note
linktitle: Získejte revize stránek ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Přečtěte si, jak načíst revize stránek v dokumentech OneNotu pomocí Aspose.Note Java. Integrujte to do svých aplikací Java pro efektivní správu dokumentů.
weight: 15
url: /cs/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Získejte revize stránek ve OneNotu – Aspose.Note

## Úvod

tomto tutoriálu se ponoříme do možností Aspose.Note for Java, výkonné knihovny, která vám umožňuje bezproblémově pracovat se soubory Microsoft OneNote v aplikacích Java. Konkrétně se zaměříme na to, jak načíst revize stránek v dokumentu OneNotu. Na konci této příručky budete vybaveni znalostmi pro efektivní extrahování revizí stránek, včetně podrobností, jako je čas poslední úpravy, čas vytvoření, název, úroveň a autor.

## Předpoklady

Než se pustíte do tohoto výukového programu, ujistěte se, že máte nastaveny následující předpoklady:

### Java Development Kit (JDK) nainstalován

Ujistěte se, že máte v systému nainstalovanou sadu Java Development Kit. Můžete si jej stáhnout a nainstalovat z webu Oracle nebo použít správce balíčků, pokud používáte systém založený na Unixu.

### Aspose.Note pro Java Library

 Stáhněte si a nainstalujte knihovnu Aspose.Note for Java z webu. Odkaz ke stažení najdete[tady](https://releases.aspose.com/note/java/) . Postupujte podle pokynů k instalaci uvedených v dokumentaci[tady](https://reference.aspose.com/note/java/).

## Importujte balíčky

Chcete-li začít, importujte potřebné balíčky do svého projektu Java. Tyto balíčky vám umožní využít funkce poskytované Aspose.Note pro Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Nyní si rozeberme poskytnutý příklad kódu do několika kroků, abychom porozuměli jednotlivým komponentám a jejich funkcím.

## Krok 1: Nastavte adresář dokumentů

Definujte adresář, kde se nachází váš dokument OneNotu.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Vložte dokument

Načtěte dokument OneNotu do Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Krok 3: Získejte první stránku

Načtěte první stránku z dokumentu.

```java
Page firstPage = doc.getFirstChild();
```

## Krok 4: Získejte revize stránky

Získejte historii revizí stránky.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Krok 5: Procházení revizí stránek

Procházejte seznam revizí stránek a získejte relevantní informace.

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Závěr

V tomto kurzu jsme prozkoumali, jak načíst revize stránek v dokumentu OneNote pomocí Aspose.Note pro Java. Pokud budete postupovat podle podrobného průvodce a využít poskytnutý ukázkový kód, můžete tuto funkci snadno integrovat do svých aplikací Java a umožnit tak efektivní správu souborů OneNotu.

## FAQ

### Q1: Mohu použít Aspose.Note pro Java k vytváření nových dokumentů OneNotu?

Odpověď 1: Ano, Aspose.Note pro Java poskytuje komplexní podporu pro vytváření, čtení a manipulaci s dokumenty OneNote programově.

### Q2: Je Aspose.Note for Java kompatibilní s různými verzemi souborů OneNote?

Odpověď 2: Ano, Aspose.Note for Java podporuje různé verze souborů Microsoft OneNote, což zajišťuje kompatibilitu v různých prostředích.

### Q3: Mohu přizpůsobit výstupní formát při exportu dokumentů OneNotu?

Odpověď 3: Absolutně, Aspose.Note pro Java nabízí flexibilitu při exportu dokumentů OneNote do různých formátů, jako je PDF, HTML a obrázky, s možnostmi přizpůsobení.

### Q4: Vyžaduje Aspose.Note pro Java licenci pro komerční použití?

A4: Ano, pro komerční použití Aspose.Note pro Java je vyžadována platná licence. Licenci můžete získat z webu Aspose.

### Otázka 5: Kde mohu požádat o pomoc, pokud narazím na problémy nebo mám dotazy ohledně Aspose.Note pro Java?

 Odpověď 5: Pro podporu a pomoc můžete navštívit fórum Aspose.Note[tady](https://forum.aspose.com/c/note/28)kde můžete klást otázky, sdílet zkušenosti a komunikovat s ostatními uživateli a odborníky.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
