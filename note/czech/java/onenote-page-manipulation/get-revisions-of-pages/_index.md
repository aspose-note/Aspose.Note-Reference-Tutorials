---
date: 2026-08-13
description: Naučte se, jak získat page modified time stránky OneNote a načíst page
  revisions pomocí Aspose.Note pro Java, ideální pro audit a správu dokumentů.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Získat revize stránek v OneNote – Aspose.Note
og_description: Naučte se, jak získat page modified time stránky OneNote a načíst
  revize stránek OneNote pomocí Aspose.Note pro Java. Rychlé kroky, ukázky kódu a
  řešení problémů.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Získat page modified time stránky OneNote pomocí Aspose.Note – Java tutoriál
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Získat page modified time stránky OneNote pomocí Aspose.Note
url: /cs/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Získání času poslední úpravy stránky OneNote pomocí Aspose.Note

## Úvod

V tomto tutoriálu se naučíte, jak **get onenote page modified** časové razítka získat a načíst kompletní historii revizí stránky OneNote pomocí Aspose.Note pro Java. Ať už vytváříte funkci auditního záznamu, prohlížeč změnových logů, nebo potřebujete zobrazit datum poslední úpravy na dashboardu, tento průvodce vás provede všemi kroky – od nastavení prostředí až po řešení běžných problémů.

## Rychlé odpovědi
- **Co vrací “get last modified time”?** Vrací časové razítko nejnovější úpravy na stránce OneNote.  
- **Která třída poskytuje historii revizí?** `PageHistory` přes `Document.getPageHistory(Page)`.  
- **Potřebuji pro tuto funkci licenci?** Ano, pro produkční použití je vyžadována platná licence Aspose.Note.  
- **Jaká verze Javy je podporována?** Java 8 nebo vyšší (JDK 8+).  
- **Mohu filtrovat revize podle autora?** Můžete číst vlastnost `Author` každého objektu `Page` a aplikovat vlastní filtr.

## Co je “get last modified time” v OneNote?

Čas poslední úpravy je uložen jako metadata atribut na každé stránce OneNote, který udává okamžik nejnovější úpravy. Aspose.Note tuto hodnotu zpřístupňuje metodou `Page.getLastModifiedTime()`, která vrací objekt `java.util.Date`, jenž lze formátovat nebo zaznamenávat podle požadavků vaší aplikace.

## Proč získávat revize stránky?

Získání revizí stránky vám poskytne kompletní auditní stopu každé změny provedené na stránce OneNote, což vám umožní sledovat, kdo co a kdy upravil. Tuto historii lze použít k porovnání verzí, obnovení předchozích stavů nebo analýze vzorců spolupráce mezi týmy, což je nezbytné pro soulad s předpisy a kontrolu kvality.

## Požadavky

- **Java Development Kit (JDK) 8 nebo novější** – nainstalujte z webu Oracle nebo od libovolného kompatibilního dodavatele.  
- **Knihovna Aspose.Note pro Java** – stáhněte JAR ze stránky **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** a postupujte podle instalačního průvodce **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Import balíčků

Třída `Document` představuje notebook OneNote načtený do paměti, zatímco `Page` a `PageHistory` poskytují přístup k jednotlivým stránkám a jejich revizním datům.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(Skutečné importy jsou zobrazeny jako prostý text, aby byl zachován původní počet bloků kódu.)*

## Jak získat čas poslední úpravy stránky OneNote?

Pro získání časového razítka poslední úpravy nejprve načtěte dokument OneNote do objektu `Document`, poté vyberte požadovanou `Page`. Zavolejte metodu `getLastModifiedTime()` na této stránce, která vrací `java.util.Date`. Tento datum můžete následně formátovat pomocí `SimpleDateFormat` nebo převést na UTC pro konzistentní reportování napříč časovými pásmy.

## Krok 1: nastavení adresáře dokumentu

Definujte složku, která obsahuje váš soubor OneNote.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Krok 2: načtení dokumentu

Vytvořte instanci `Document` předáním úplné cesty k vašemu souboru `.one`.

```java
String dataDir = "Your Document Directory";
```

## Krok 3: získání první stránky

Získejte první objekt `Page` ze sbírky stránek dokumentu.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Krok 4: získání revizí stránky

Získejte `PageHistory` pro vybranou stránku. Pokud byl notebook nikdy upravován, může tento volání vrátit `null`.

```java
Page firstPage = doc.getFirstChild();
```

## Krok 5: procházení revizí stránky

Iterujte přes každou revizi `Page`, přečtěte její `Author` a `LastModifiedTime` a zobrazte informace.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Časté problémy a řešení
- **Null `PageHistory`** – Ověřte, že notebook skutečně obsahuje revize; jinak `getPageHistory` vrací `null`.  
- **Rozdíly časových pásem** – `getLastModifiedTime()` používá výchozí časové pásmo JVM. Pokud vaše aplikace vyžaduje standardní pásmo, převádějte na UTC pomocí `SimpleDateFormat`.  
- **Licence není načtena** – Bez platné licence běží Aspose.Note v evaluačním režimu, což omezuje zpracování stránek. Načtěte soubor licence při spuštění aplikace, abyste se vyhnuli tomuto omezení.

## Často kladené otázky

**Q1: Mohu použít Aspose.Note pro Java k vytvoření nových dokumentů OneNote?**  
A: Ano, API vám umožňuje programově vytvářet, upravovat a ukládat notebooky OneNote od nuly.

**Q2: Je Aspose.Note pro Java kompatibilní s různými verzemi souborů OneNote?**  
A: Ano, podporuje formáty souborů OneNote 2007‑2021, což zajišťuje širokou kompatibilitu napříč desktopovými i cloudovými prostředími.

**Q3: Mohu přizpůsobit výstupní formát při exportu dokumentů OneNote?**  
A: Rozhodně. Můžete exportovat do PDF, HTML, PNG nebo SVG a řídit možnosti jako rozlišení obrázku a vložení fontů.

**Q4: Vyžaduje Aspose.Note pro Java licenci pro komerční použití?**  
A: Ano, pro produkční nasazení je povinná komerční licence. Pro vyzkoušení je k dispozici bezplatná zkušební verze.

**Q5: Kde mohu získat pomoc, pokud narazím na problémy?**  
A: Navštivte komunitní fórum Aspose.Note **[Aspose.Note forum](https://forum.aspose.com/c/note/28)**, kde můžete klást otázky, sdílet zkušenosti a získat pomoc od komunity i inženýrů Aspose.

---

**Poslední aktualizace:** 2026-08-13  
**Testováno s:** Aspose.Note for Java 23.12 (nejnovější v době psaní)  
**Autor:** Aspose

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

## Související tutoriály

- [Aspose Java Tutorial - Získání informací o stránkách v OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [aspose.note tutoriál revizí stránek – Získání revizí stránek v OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [sledování změn onenote – Správa revizí stránek s Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}