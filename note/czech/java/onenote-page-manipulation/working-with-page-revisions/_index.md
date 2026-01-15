---
date: 2026-01-15
description: Naučte se sledovat změny v OneNote a spravovat revize stránek v dokumentech
  OneNote pomocí Aspose.Note pro Javu. Obsahuje příklad souhrnu revizí a návod, jak
  upravit datum revize.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: sledování změn v OneNote – Správa revizí stránek pomocí Aspose.Note
url: /cs/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Práce s revizemi stránek v OneNote – Aspose.Note

## Úvod

OneNote je výkonný nástroj pro organizaci poznámek a když potřebujete **track changes onenote**, správa revizí stránek se stává nezbytnou pro efektivní spolupráci. S Aspose.Note pro Java můžete programově pracovat s revizemi, zobrazit, kdo stránku upravil, a dokonce upravit časová razítka. Tento tutoriál vás provede každým krokem, od načtení dokumentu až po aktualizaci souhrnu revizí.

## Rychlé odpovědi
- **Co znamená “track changes onenote”?** Odkazuje na sledování, kdo upravil stránku OneNote a kdy.
- **Která knihovna je vyžadována?** Aspose.Note pro Java.
- **Mohu změnit autora nebo datum revize?** Ano, pomocí RevisionSummary API (`modify revision date`).
- **Potřebuji mít předem soubor OneNote?** Ano, je vyžadován ukázkový soubor `.one`.
- **Je pro produkci potřeba licence?** Pro komerční použití je vyžadována platná licence Aspose.Note.

## Co je příklad souhrnu revizí?
*revision summary* poskytuje metadata o nejnovějších změnách na stránce — jméno autora, čas poslední úpravy a další podrobnosti. V tomto průvodci získáme a zobrazíme tyto informace a poté ukážeme, jak **modify revision date**.

## Proč sledovat změny onenote pomocí Aspose.Note?
- **Spolupráce:** Rychle zjistíte, kdo provedl poslední úpravy.
- **Audit:** Uchovávejte spolehlivou historii změn pro soulad s předpisy.
- **Automatizace:** Integrujte zpracování revizí do backendových služeb nebo migračních nástrojů.

## Požadavky

### Vývojové prostředí Java
Ujistěte se, že máte na svém systému nainstalovaný Java Development Kit (JDK).

### Knihovna Aspose.Note pro Java
Stáhněte a nainstalujte knihovnu Aspose.Note pro Java z [zde](https://releases.aspose.com/note/java/).

### Dokument OneNote
Mějte připravený ukázkový dokument OneNote pro testovací účely.

## Import balíčků

Ve svém Java projektu importujte potřebné balíčky pro práci s Aspose.Note pro Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Rozdělme poskytnutý příklad do několika kroků pro lepší pochopení.

## Krok 1: Načtení dokumentu OneNote

Nejprve načtěte dokument OneNote a získejte první podřízenou stránku.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Krok 2: Přečtení souhrnu revize stránky

Přečtěte souhrn revize obsahu pro stránku. Toto je **revision summary example**, který ukazuje, kdo stránku naposledy upravil.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Krok 3: Aktualizace souhrnu revize stránky

Aktualizujte souhrn revize stránky novým autorem a novým datem úpravy. Toto ukazuje, jak programově **modify revision date**.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Závěr

Programové řízení revizí stránek v dokumentech OneNote lze zjednodušit pomocí Aspose.Note pro Java. Dodržením kroků uvedených v tomto tutoriálu můžete efektivně **track changes onenote**, zobrazit podrobnosti revizí a dokonce **modify revision date** přizpůsobit svému pracovnímu postupu.

## Často kladené otázky

### Q1: Mohu použít Aspose.Note pro Java s jinými Java knihovnami?

A: Ano, Aspose.Note pro Java lze integrovat s jinými Java knihovnami pro rozšíření funkčnosti.

### Q2: Podporuje Aspose.Note pro Java všechny verze dokumentů OneNote?

A: Aspose.Note pro Java podporuje různé verze dokumentů OneNote, včetně starších verzí.

### Q3: Je Aspose.Note pro Java vhodný pro podnikovou úroveň aplikací?

A: Rozhodně, Aspose.Note pro Java je navržen tak, aby vyhovoval potřebám podnikově úrovňových aplikací s robustními funkcemi a škálovatelností.

### Q4: Mohu přizpůsobit revize stránek pomocí Aspose.Note pro Java?

A: Ano, můžete přizpůsobit revize stránek podle svých požadavků pomocí Aspose.Note pro Java.

### Q5: Kde mohu získat podporu pro Aspose.Note pro Java?

A: Podporu pro Aspose.Note pro Java můžete získat na [fóru Aspose.Note](https://forum.aspose.com/c/note/28).

---

**Poslední aktualizace:** 2026-01-15  
**Testováno s:** Aspose.Note pro Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}