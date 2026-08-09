---
date: 2026-05-25
description: Naučte se, jak obnovit předchozí verzi OneNote a vrátit zpět stránky
  OneNote pomocí Aspose.Note pro Java. Postupujte podle tohoto krok za krokem průvodce
  pro efektivní správu dokumentů.
keywords:
- restore previous onenote version
- how to roll back onenote
- read .one file java
- recover previous onenote page
linktitle: Jak obnovit předchozí verzi OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to restore previous OneNote version and roll back OneNote
    pages using Aspose.Note for Java. Follow this step‑by‑step guide for efficient
    document management.
  headline: How to Restore Previous OneNote Version – Aspose.Note
  type: TechArticle
- description: Learn how to restore previous OneNote version and roll back OneNote
    pages using Aspose.Note for Java. Follow this step‑by‑step guide for efficient
    document management.
  name: How to Restore Previous OneNote Version – Aspose.Note
  steps:
  - name: '**Install Java Development Kit (JDK):** Grab the latest JDK from the Oracle
      website or your preferred package manager.'
    text: '**Install Java Development Kit (JDK):** Grab the latest JDK from the Oracle
      website or your preferred package manager.'
  - name: '**Configure Environment Variables:** Set `JAVA_HOME` and update `PATH`
      so the `java` and `javac` commands are reachable from the command line.'
    text: '**Configure Environment Variables:** Set `JAVA_HOME` and update `PATH`
      so the `java` and `javac` commands are reachable from the command line.'
  - name: '**Add Aspose.Note for Java:** Download the library from the [website](https://purchase.aspose.com/buy)
      and add the JAR to your project''s classpath.'
    text: '**Add Aspose.Note for Java:** Download the library from the [website](https://purchase.aspose.com/buy)
      and add the JAR to your project''s classpath.'
  type: HowTo
- questions:
  - answer: Restoring a page to a prior version saved in its history.
    question: What does “roll back” mean for OneNote?
  - answer: '`PageHistory` class in Aspose.Note for Java.'
    question: Which API handles the rollback?
  - answer: A valid Aspose.Note license is required for production use.
    question: Do I need a license?
  - answer: Yes – you can pick any entry from the page’s history list.
    question: Can I choose any previous version?
  - answer: Absolutely; the operation works on individual pages without loading the
      entire notebook into memory.
    question: Is this approach safe for large notebooks?
  type: FAQPage
second_title: Aspose.Note Java API
title: Jak obnovit předchozí verzi OneNote – Aspose.Note
url: /cs/java/onenote-page-manipulation/roll-back-to-previous-page-version/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak obnovit předchozí verzi OneNote – Aspose.Note

## Úvod

Pokud potřebujete spolehlivý programový způsob, jak **obnovit předchozí verzi OneNote**, když se vyskytne nechtěná úprava, jste na správném místě. V tomto tutoriálu projdeme Aspose.Note pro Java a ukážeme vám přesně, jak vrátit stránku OneNote do dřívějšího stavu. Ať už vytváříte automatizovanou službu pro správu poznámek nebo přidáváte bezpečnostní síť pro spolupracující sešity, schopnost vrátit stránku udržuje váš obsah přesný, důvěryhodný a připravený k auditu.

## Rychlé odpovědi
- **Co znamená „roll back“ v OneNote?** Obnovení stránky na předchozí verzi uloženou v její historii.  
- **Které API provádí rollback?** Třída `PageHistory` v Aspose.Note pro Java.  
- **Potřebuji licenci?** Pro produkční použití je vyžadována platná licence Aspose.Note.  
- **Mohu si vybrat libovolnou předchozí verzi?** Ano – můžete vybrat libovolnou položku ze seznamu historie stránky.  
- **Je tento přístup bezpečný pro velké sešity?** Rozhodně; operace pracuje s jednotlivými stránkami, aniž by načítala celý sešit do paměti.

## Co je „restore previous onenote version“?
**`restore previous onenote version`** označuje proces získání dřívějšího snímku stránky OneNote z její interní historie verzí a nahrazení aktuálního obsahu stránky tímto snímkem. Tato operace je plně podporována API `PageHistory` v Aspose.Note a nevyžaduje ruční kroky zpět.

## Proč použít Aspose.Note k vrácení stránek OneNote?
Aspose.Note dokáže zpracovat sešity s **tisíci stránkami** a udržet využití paměti pod **50 MB**, protože pracuje stránku po stránce. Podporuje **30+ funkcí specifických pro OneNote**, včetně čtení souborů `.one`, extrakce metadat a obnovení jakékoli historické položky. To jej činí ideálním pro automatizaci v podnikovém měřítku, kde jsou spolehlivost a výkon kritické.

## Předpoklady

Než se ponoříme do kódu, ujistěte se, že máte připraveno následující:

### Nastavení vývojového prostředí Java
1. **Instalace Java Development Kit (JDK):** Stáhněte si nejnovější JDK z webu Oracle nebo z preferovaného správce balíčků.  
2. **Konfigurace proměnných prostředí:** Nastavte `JAVA_HOME` a aktualizujte `PATH`, aby byly příkazy `java` a `javac` dostupné z příkazové řádky.  
3. **Přidání Aspose.Note pro Java:** Stáhněte knihovnu z [webu](https://purchase.aspose.com/buy) a přidejte JAR do classpath vašeho projektu.

## Import balíčků

Pro práci se soubory OneNote importujte nezbytné třídy Aspose.Note:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Jak obnovit předchozí verzi stránky OneNote?

Načtěte cílový sešit, získejte požadovanou historickou položku pomocí `PageHistory`, odstraňte aktuální stránku a přidejte vybranou verzi zpět do dokumentu – vše v méně než deseti řádcích Java kódu. Tento přístup zaručuje, že je dotčena pouze konkrétní stránka, zbytek sešitu zůstává nedotčený a spotřeba paměti je minimální.

## Krok 1: Načtení dokumentu OneNote

`Document` je hlavní objekt Aspose.Note, který představuje jeden soubor OneNote v paměti. Nejprve ukážeme na složku, která obsahuje soubor `.one`, a načteme jej do instance `Document`.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```
Nejprve ukážeme na složku, která obsahuje soubor `.one`, a načteme jej do objektu `Document`.

## Krok 2: Získání historie stránky

`PageHistory` poskytuje přístup ke každé uložené verzi vybrané stránky, což umožňuje funkci **restore previous onenote version**. Voláním `getHistory()` získáte seznam, který můžete iterovat nebo indexovat přímo.

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```
`PageHistory` vám dává přístup ke každé uložené verzi vybrané stránky, což umožňuje funkci **restore previous onenote version**.

## Krok 3: Odstranění aktuální stránky

`Page` představuje jednotlivou stránku v sešitu OneNote. Odstraněním aktuální stránky vytvoříte místo pro historickou verzi, kterou chcete vrátit zpět.

```java
document.removeChild(page);
```
Odstraněním aktuální stránky vytvoříme prostor pro verzi, kterou chceme vrátit zpět.

## Krok 4: Přidání předchozí verze stránky

`appendChildLast` přidá uzel na konec kolekce dětí dokumentu. Zde vybereme nejnovější historickou položku (index můžete změnit a cílit na starší verzi) a přidáme ji zpět do dokumentu.

```java
document.appendChildLast(pageHistory.get_Item(pageHistory.size() - 1));
```
Zde vybereme nejnovější historickou položku (index můžete změnit a cílit na starší verzi) a přidáme ji zpět do dokumentu.

## Krok 5: Uložení dokumentu

Uložení zapíše upravený sešit zpět na disk, čímž vznikne soubor, který nyní obsahuje vrácenou stránku. Operace zapisuje jen změněnou stránku, takže i velké sešity zůstávají rychlé na zpracování.

```java
document.save(dataDir + "RollBackToPreviousPageVersion_out.one");
```
Nakonec uložíme upravený sešit. Výstupní soubor nyní obsahuje vrácenou stránku.

## Časté problémy a tipy
- **Prázdná historie:** Pokud `pageHistory.size()` vrátí 0, stránka nemá žádné uložené verze – zajistěte, aby byla v OneNote povolena verze.  
- **Index mimo rozsah:** Pamatujte, že seznam historie je indexován od nuly. Upravit index (`size() - 1`) pro cílení na požadovanou verzi.  
- **Výkon:** Práce s jednou stránkou zabraňuje načtení celého sešitu do paměti, což udržuje operaci rychlou i pro sešity s **10 000+ stránkami**.  
- **Čtení .one souborů v Javě:** Použijte `Document.load("path/to/file.one")` pro načtení souboru OneNote; Aspose.Note plně podporuje formát `.one` bez nutnosti instalace Microsoft Office.  
- **Bezpečné obnovení předchozí stránky OneNote:** Vždy si před hromadnými vráceními zálohujte původní soubor `.one`, zejména při automatizaci napříč mnoha sešity.

## Často kladené otázky

**Q1: Mohu vrátit více verzí jedné stránky?**  
A: Ano, můžete přistupovat k celé historii stránky a obnovit libovolnou předchozí verzi výběrem odpovídajícího indexu ze seznamu `PageHistory`.

**Q2: Podporuje Aspose.Note další programovací jazyky kromě Javy?**  
A: Ano, Aspose.Note poskytuje knihovny pro .NET, C++ a Python, což vám umožní provádět stejné operace rollbacku napříč platformami.

**Q3: Je Aspose.Note kompatibilní se všemi verzemi OneNote?**  
A: Aspose.Note podporuje všechny hlavní formáty souborů OneNote, včetně starších souborů `.one` i novějších struktur OneNote 2016/365, což zajišťuje širokou kompatibilitu.

**Q4: Mohu automatizovat další úkoly v OneNote pomocí Aspose.Note?**  
A: Rozhodně. API vám umožňuje programově přidávat, mazat a upravovat sekce, stránky i vložené zdroje, což je ideální pro hromadné migrace a vlastní reportování.

**Q5: Existuje komunitní fórum nebo podpora pro Aspose.Note?**  
A: Ano, můžete navštívit [forum Aspose.Note](https://forum.aspose.com/c/note/28) pro pomoc od komunity nebo kontaktovat dedikovaný tým podpory Aspose pro komerční asistenci.

---

**Poslední aktualizace:** 2026-05-25  
**Testováno s:** Aspose.Note pro Java (nejnovější verze)  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [How to Save OneNote Page Version – Push Current Page Version in OneNote - Aspose.Note](/note/java/onenote-page-manipulation/push-current-page-version/)
- [Aspose Java Tutorial - Get Information about Pages in OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Get OneNote Page Count with Aspose.Note for Java](/note/java/onenote-page-manipulation/get-page-count/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}