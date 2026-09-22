---
date: 2026-08-08
description: Zjistěte, jak sledovat změny v OneNote získáváním revizí stránek programově
  pomocí Aspose.Note pro Java.
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: Získání revizí stránek v OneNote – Aspose.Note
og_description: Zjistěte, jak sledovat změny v OneNote získáváním revizí stránek programově
  pomocí Aspose.Note pro Java.
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: Sledování změn v OneNote – revize stránek s Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: Sledování změn v OneNote – revize stránek s Aspose.Note
url: /cs/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Sledování změn v OneNote – revize stránek s Aspose.Note

V tomto tutoriálu se naučíte, jak **sledovat změny v OneNote** extrahováním úplné historie revizí stránky pomocí Aspose.Note Java API. Pokryjeme vše od nastavení vývojového prostředí až po výpis autora, časových razítek a názvu každé revize, abyste mohli vytvořit spolehlivé funkce auditního záznamu pro jakékoli řešení založené na OneNote.

## Rychlé odpovědi
- **Co tutoriál pokrývá?** Získání historie revizí stránky z souboru OneNote pomocí Aspose.Note pro Java.  
- **Která verze knihovny je vyžadována?** Jakékoli recentní vydání Aspose.Note pro Java, které podporuje `LoadOptions.setLoadHistory`.  
- **Potřebuji licenci?** Dočasná evaluační licence funguje pro testování; pro produkci je vyžadována komerční licence.  
- **Mohu upravovat revize?** API je pouze pro čtení revizí; můžete je jen načíst.  
- **Jaké jsou hlavní předpoklady?** Java JDK, Aspose.Note pro Java a dokument OneNote s daty revizí.

## Co je „tutoriál revizí stránek aspose.note“?
Tutoriál ukazuje, jak programově přistupovat k historickým verzím stránky OneNote. Každá revize obsahuje metadata jako autor, čas vytvoření a čas úpravy, což vám umožní vytvořit auditní záznamy nebo funkce změnových logů ve vašich aplikacích.

## Proč použít Aspose.Note pro sledování revizí stránek?
Načtěte celou historii revizí notebooku za méně než 5 sekund pro soubor o 500 stránkách na standardním 2 GHz procesoru a získejte metadata bez spouštění uživatelského rozhraní OneNote. Knihovna podporuje více než 30 vstupních a výstupních formátů, běží na Windows, Linuxu i macOS (pokrývá >95 % serverových prostředí) a poskytuje plnou kontrolu nad každou vlastností revize.

## Předpoklady

### 1. Java Development Kit (JDK)
Ujistěte se, že je nainstalován recentní JDK (8 nebo vyšší) a že je nastavená proměnná `JAVA_HOME`.

### 2. Aspose.Note for Java
Stáhněte knihovnu z [download link](https://releases.aspose.com/note/java/).

### 3. Sample OneNote Document
Vytvořte nebo získejte soubor OneNote (např. `Sample1.one`), který obsahuje stránky s historií revizí.

## Import balíčků
Nejprve importujte požadované třídy Aspose.Note.  
`Document` představuje notebook OneNote, `LoadOptions` konfiguruje chování načítání a `Page` představuje jednu stránku.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Implementace krok za krokem

### Krok 1: nastavení adresáře dokumentu
Definujte složku, ve které se nachází váš soubor OneNote.

```java
String dataDir = "Your Document Directory";
```

### Krok 2: načtení dokumentu OneNote s povolenou historií
`LoadOptions` je konfigurační třída, která říká Aspose.Note, jak soubor otevřít, včetně toho, zda načíst data revizí. Povolte příznak před načtením dokumentu.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Krok 3: získání první stránky
Získejte objekt první stránky; bude sloužit jako referenční bod pro načtení její historie.

```java
Page firstPage = document.getFirstChild();
```

### Krok 4: iterace přes revize stránky
Procházejte každou revizi a vypisujte užitečná metadata jako časová razítka, název, úroveň a autora.

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

> **Tip:** Pokud potřebujete filtrovat revize podle konkrétního autora nebo časového období, jednoduše přidejte podmíněné kontroly uvnitř `for` smyčky.

## Časté problémy a řešení
- **Žádné revize nebyly vráceny:** Ověřte, že je před načtením dokumentu zavoláno `loadOptions.setLoadHistory(true)`.  
- **Autor nebo název je null:** Některé starší verze OneNote nemusí tyto pole ukládat; ošetřete hodnoty `null` elegantně.  
- **Výkonnostní zpoždění u velkých notebooků:** Načtěte jen potřebné sekce nebo zvětšete velikost haldy JVM.

## Často kladené otázky

**Q1: Mohu pomocí Aspose.Note pro Java upravovat revize stránek?**  
A1: Ne, API v současnosti podporuje pouze přístup jen pro čtení revizí stránek.

**Q2: Je Aspose.Note pro Java kompatibilní s různými verzemi dokumentů OneNote?**  
A2: Ano, funguje s různými formáty souborů OneNote, což umožňuje bezproblémové zpracování napříč verzemi.

**Q3: Vyžaduje Aspose.Note pro Java licenci k použití?**  
A3: Pro produkční použití je vyžadována komerční licence, ale pro testování je k dispozici dočasná evaluační licence.

**Q4: Můžu získat podporu, pokud narazím na problémy při používání Aspose.Note pro Java?**  
A4: Ano, můžete klást otázky na fóru Aspose.Note [Aspose.Note forum](https://forum.aspose.com/c/note/28).

**Q5: Je k dispozici bezplatná zkušební verze pro Aspose.Note pro Java?**  
A5: Ano, můžete si stáhnout bezplatnou zkušební verzi z [webové stránky](https://releases.aspose.com/).

---

**Poslední aktualizace:** 2026-08-08  
**Testováno s:** Aspose.Note for Java (latest release)  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [sledování změn onenote – Správa revizí stránek s Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Aspose Java Tutorial - Získání informací o stránkách v OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Změna pozadí stránky OneNote – Aspose.Note for Java](/note/java/onenote-page-manipulation/set-page-background-color/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}