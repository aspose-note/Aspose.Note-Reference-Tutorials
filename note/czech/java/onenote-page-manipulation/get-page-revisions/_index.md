---
date: 2026-01-10
description: Naučte se tutoriál revizí stránek aspose.note pro Javu – načtěte revize
  stránek OneNote programově pomocí Aspose.Note. Postupujte podle našeho krok‑za‑krokem
  průvodce.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: 'aspose.note – tutoriál revizí stránek: Získání revizí stránek v OneNote'
url: /cs/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Získání revizí stránek v OneNote - Aspose.Note

OneNote je výkonná platforma pro psaní poznámek a když potřebujete auditovat změny, **aspose.note page revisions tutorial** vám přesně ukáže, jak získat historii revizí pomocí několika řádků Java kódu. V tomto průvodci projdeme vše, co potřebujete – od nastavení prostředí až po výpis podrobností každé revize – abyste mohli snadno sledovat úpravy, příspěvky autorů a časové razítka.

## Rychlé odpovědi
- **Co tutoriál pokrývá?** Získání historie revizí stránky z OneNote souboru pomocí Aspose.Note pro Java.  
- **Která verze knihovny je vyžadována?** Jakékoli nedávné vydání Aspose.Note pro Java, které podporuje `LoadOptions.setLoadHistory`.  
- **Potřebuji licenci?** Dočasná evaluační licence funguje pro testování; pro produkci je vyžadována komerční licence.  
- **Mohu upravovat revize?** API je pro revize jen pro čtení; můžete je pouze načíst.  
- **Jaké jsou hlavní předpoklady?** Java JDK, Aspose.Note pro Java a OneNote dokument s daty revizí.

## Co je “aspose.note page revisions tutorial”?
Tento tutoriál ukazuje, jak programově přistupovat k historickým verzím stránky v OneNote. Každá revize obsahuje metadata jako autor, čas vytvoření a čas úpravy, což vám umožní vytvořit auditní stopy nebo funkce změnových záznamů ve vašich aplikacích.

## Proč používat Aspose.Note pro sledování revizí stránek?
- **Žádná závislost na UI** – funguje zcela v kódu, ideální pro backendové služby.  
- **Cross‑platform** – Java běží na Windows, Linuxu i macOS.  
- **Plná kontrola** – načtěte každou vlastnost revize bez ručního otevírání OneNote.  
- **Výkon** – načítání historie je optimalizováno, takže i velké poznámkové bloky jsou zpracovány rychle.

## Prerequisites

### 1. Java Development Kit (JDK)
Ujistěte se, že je nainstalován aktuální JDK (8 nebo vyšší) a že je nastavená proměnná `JAVA_HOME`.

### 2. Aspose.Note for Java
Stáhněte knihovnu z [odkaz ke stažení](https://releases.aspose.com/note/java/).

### 3. Sample OneNote Document
Vytvořte nebo získejte OneNote soubor (např. `Sample1.one`), který obsahuje stránky s historií revizí.

## Import balíčků
Nejprve importujte požadované třídy Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Krok‑za‑krokem implementace

### Krok 1: Nastavení adresáře dokumentu
Definujte složku, ve které se nachází váš OneNote soubor.

```java
String dataDir = "Your Document Directory";
```

### Krok 2: Načtení OneNote dokumentu s povolenou historií
Povolte příznak `LoadOptions`, aby se načetla data revizí.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Krok 3: Získání první stránky
Získejte objekt první stránky; bude sloužit jako referenční bod pro načtení její historie.

```java
Page firstPage = document.getFirstChild();
```

### Krok 4: Procházení revizí stránky
Projděte každou revizi a vytiskněte užitečná metadata jako časová razítka, název, úroveň a autora.

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

> **Tip:** Pokud potřebujete filtrovat revize podle konkrétního autora nebo časového období, jednoduše přidejte podmínky uvnitř `for` smyčky.

## Časté problémy a řešení
- **Žádné revize nebyly vráceny:** Ověřte, že je před načtením dokumentu zavoláno `loadOptions.setLoadHistory(true)`.  
- **Autor nebo název je null:** Některé starší verze OneNote nemusí tyto pole ukládat; ošetřete `null` hodnoty elegantně.  
- **Zpomalení výkonu u velkých poznámkových bloků:** Načtěte pouze potřebné sekce nebo zvětšete velikost haldy JVM.

## Často kladené otázky

**Q1: Mohu pomocí Aspose.Note pro Java upravovat revize stránek?**  
A1: Ne, API v současnosti podporuje pouze přístup k revizím stránek v režimu jen pro čtení.

**Q2: Je Aspose.Note pro Java kompatibilní s různými verzemi OneNote dokumentů?**  
A2: Ano, funguje s různými formáty OneNote souborů, což umožňuje bezproblémové zpracování napříč verzemi.

**Q3: Vyžaduje Aspose.Note pro Java licenci pro použití?**  
A3: Pro produkční použití je vyžadována komerční licence, ale pro testování je k dispozici dočasná evaluační licence.

**Q4: Můžu získat podporu, pokud narazím na problémy při používání Aspose.Note pro Java?**  
A4: Ano, můžete klást otázky na fóru Aspose.Note [zde](https://forum.aspose.com/c/note/28).

**Q5: Je k dispozici bezplatná zkušební verze pro Aspose.Note pro Java?**  
A5: Ano, můžete si stáhnout bezplatnou zkušební verzi z [webové stránky](https://releases.aspose.com/).

---

**Poslední aktualizace:** 2026-01-10  
**Testováno s:** Aspose.Note pro Java (nejnovější verze)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}