---
date: 2026-01-10
description: Naučte se, jak získat čas poslední úpravy a načíst revize stránek OneNote
  pomocí Aspose.Note pro Javu. Začleňte to do svých Java aplikací pro efektivní správu
  dokumentů.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Jak získat čas poslední úpravy stránek OneNote – Aspose.Note
url: /cs/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Získání revizí stránek v OneNote - Aspose.Note

## Úvod

V tomto tutoriálu **získáte čas poslední úpravy** pro stránky uvnitř dokumentu OneNote a prozkoumáte, jak získat úplnou historii revizí pomocí Aspose.Note pro Java. Ať už vytváříte systém pro správu dokumentů, provádíte audit změn, nebo jen potřebujete zobrazit, kdy byla stránka naposledy upravena, tento průvodce vám přesně ukáže, jak tuto informaci programově získat.

## Rychlé odpovědi
- **Co vrací “get last modified time”?** Časové razítko nejnovější úpravy na stránce OneNote.  
- **Která třída poskytuje historii revizí?** `PageHistory` přes `Document.getPageHistory(Page)`.  
- **Potřebuji licenci pro tuto funkci?** Ano, pro produkční použití je vyžadována platná licence Aspose.Note.  
- **Jaká verze Javy je podporována?** Java 8 nebo vyšší (JDK 8+).  
- **Mohu filtrovat revize podle autora?** Můžete číst vlastnost `Author` každého objektu `Page` a aplikovat vlastní filtr.

## Co je “get last modified time” v OneNote?

**Čas poslední úpravy** je metadata uložená u každé stránky, která zaznamenává, kdy byla stránka naposledy změněna. Aspose.Note tuto hodnotu zpřístupňuje metodou `Page.getLastModifiedTime()`, což usnadňuje zobrazování nebo zaznamenávání dat změn.

## Proč získávat revize stránek?

- **Auditní stopy:** Uchovávejte záznam o tom, kdo co a kdy změnil.  
- **Porovnání verzí:** Vytvořte funkce, které porovnávají dvě revize vedle sebe.  
- **Přehled o spolupráci uživatelů:** Pochopte vzorce úprav ve sdílených poznámkových blocích.  

## Požadavky

Než začnete, ujistěte se, že máte následující:

### Java Development Kit (JDK) nainstalován
Nainstalujte JDK 8 nebo novější z webu Oracle nebo z vašeho preferovaného správce balíčků.

### Knihovna Aspose.Note pro Java
Stáhněte knihovnu z oficiálního webu. Stahovací odkaz najdete **[zde](https://releases.aspose.com/note/java/)**. Postup instalace najdete v dokumentaci **[zde](https://reference.aspose.com/note/java/)**.

## Import balíčků

Pro začátek importujte potřebné balíčky do svého Java projektu. Tyto balíčky vám umožní využít funkčnost poskytovanou Aspose.Note pro Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Nyní si rozložíme ukázkový kód do několika kroků, abychom pochopili každou součást a její funkci.

## Jak získat čas poslední úpravy stránky OneNote

### Krok 1: Nastavte adresář dokumentu
Definujte adresář, kde se nachází váš OneNote dokument.

```java
String dataDir = "Your Document Directory";
```

### Krok 2: Načtěte dokument
Načtěte OneNote dokument do Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Krok 3: Získejte první stránku
Získejte první stránku z dokumentu.

```java
Page firstPage = doc.getFirstChild();
```

### Krok 4: Získejte revize stránky
Získejte historii revizí stránky.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Krok 5: Procházejte revize stránky
Iterujte přes seznam revizí stránky a získejte relevantní informace, včetně **last modified time**.

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

## Časté problémy a řešení
- **Null `PageHistory`:** Ujistěte se, že dokument skutečně obsahuje revize; jinak může `getPageHistory` vrátit `null`.  
- **Rozdíly časových pásem:** `getLastModifiedTime()` vrací `java.util.Date` v výchozím časovém pásmu systému. V případě potřeby jej převedete na UTC.  
- **Licence není načtena:** Bez platné licence může Aspose.Note fungovat v evaluačním režimu, který omezuje počet zpracovávaných stránek.

## Často kladené otázky

### Q1: Mohu pomocí Aspose.Note pro Java vytvářet nové dokumenty OneNote?
**A1:** Ano, Aspose.Note pro Java poskytuje komplexní podporu pro vytváření, čtení a manipulaci s OneNote dokumenty programově.

### Q2: Je Aspose.Note pro Java kompatibilní s různými verzemi souborů OneNote?
**A2:** Ano, Aspose.Note pro Java podporuje různé verze souborů Microsoft OneNote, což zajišťuje kompatibilitu napříč různými prostředími.

### Q3: Mohu přizpůsobit výstupní formát při exportu dokumentů OneNote?
**A3:** Rozhodně, Aspose.Note pro Java nabízí flexibilitu při exportu OneNote dokumentů do různých formátů, jako jsou PDF, HTML a obrázky, s možnostmi přizpůsobení.

### Q4: Vyžaduje Aspose.Note pro Java licenci pro komerční použití?
**A4:** Ano, pro komerční použití Aspose.Note pro Java je vyžadována platná licence. Licenci můžete získat na webu Aspose.

### Q5: Kde mohu získat pomoc, pokud narazím na problémy nebo mám otázky ohledně Aspose.Note pro Java?
**A5:** Pro podporu a pomoc můžete navštívit fórum Aspose.Note **[zde](https://forum.aspose.com/c/note/28)**, kde můžete klást otázky, sdílet zkušenosti a komunikovat s ostatními uživateli a odborníky.

---

**Last Updated:** 2026-01-10  
**Testováno s:** Aspose.Note pro Java 23.12 (nejnovější v době psaní)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}