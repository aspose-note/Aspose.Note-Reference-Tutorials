---
date: 2025-11-30
description: Jednoduše převádějte OneNote na obrázek pomocí Aspose.Note pro Javu.
  Postupujte podle tohoto krok‑za‑krokem tutoriálu a uložte OneNote jako obrázek s
  výchozími nastaveními.
language: cs
linktitle: Convert OneNote to Image using Default Options - Java
second_title: Aspose.Note Java API
title: Převést OneNote na obrázek pomocí výchozích možností – Java
url: /java/onenote-document-loading/convert-to-image-default-options/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod OneNote na obrázek pomocí výchozích možností – Java

## Úvod

V moderních aplikacích je převod souborů OneNote do statických formátů obrázků běžnou potřebou — ať už potřebujete náhledy pro galerii, vložit stránky do PDF, nebo jednoduše archivovat obsah jako soubory PNG/JPEG. Tento tutoriál vám ukáže **jak převést OneNote na obrázek** pomocí Aspose.Note pro Java s výchozími možnostmi knihovny. Na konci průvodce budete schopni **uložit OneNote jako obrázek** pomocí jen několika řádků kódu.

## Rychlé odpovědi
- **Jaká knihovna zpracovává převod OneNote v Javě?** Aspose.Note for Java.  
- **Mohu převést OneNote na PNG bez dalších nastavení?** Ano — výchozí možnosti automaticky vytvářejí PNG, GIF, JPEG atd.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence.  
- **Jaká verze Javy je požadována?** Java 8 nebo vyšší.  
- **Je převod dostatečně rychlý pro dávkové zpracování?** Ano — Aspose.Note zpracovává dokumenty v paměti, což umožňuje efektivní hromadné převody.

## Co znamená „převod OneNote na obrázek“?
Převod OneNote na obrázek znamená převzít bohatý, vícevrstvý obsah souboru `.one` a vykreslit každou stránku jako rastrový grafický soubor (např. PNG, GIF, JPEG). Tato transformace je užitečná pro generování náhledů, archivaci obsahu a integraci se systémy, které přijímají pouze obrázkové vstupy.

## Proč použít Aspose.Note pro Java?
- **Žádná závislost na Microsoft Office** — funguje na jakékoli platformě, která podporuje Javu.  
- **Vysoká věrnost** — zachovává písma, barvy a rozvržení přesně tak, jak se zobrazují v OneNote.  
- **Jednoduché API** — několik volání metod provede celý převod.  
- **Podporuje více formátů obrázků** — GIF, PNG, JPEG, BMP a další.

## Požadavky

Před zahájením se ujistěte, že jsou následující komponenty nainstalovány a nakonfigurovány:

### Java Development Kit (JDK)
1. **Stáhněte** nejnovější JDK z webu Oracle (nebo použijte OpenJDK).  
2. **Nainstalujte** jej podle instrukcí pro konkrétní platformu. Ověřte pomocí `java -version`.

### Aspose.Note pro Java
1. **Stáhněte** knihovnu ze [stránky ke stažení Aspose.Note pro Java](https://releases.aspose.com/note/java/).  
2. **Přidejte** `aspose-note-xx.jar` (a všechny závislosti) do classpath vašeho projektu.

## Import balíčků
Prvním krokem je importovat třídy potřebné pro načtení souboru OneNote a jeho uložení jako obrázek.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Postupný návod

### Krok 1: Načtení dokumentu OneNote
Načtěte zdrojový soubor `.one` do objektu `Aspose.Note` `Document`. Konstruktor `LoadOptions` bez parametrů říká knihovně, aby použila výchozí chování načítání.

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

> **Tip:** Nechte `dataDir` ukazovat na absolutní cestu nebo použijte `Paths.get(...)` pro lepší kompatibilitu napříč platformami.

### Krok 2: Uložení dokumentu jako obrázek
Zavolejte metodu `save`, zadejte požadovaný název výstupního souboru a vyberte formát obrázku pomocí `SaveFormat`. Níže uvedený příklad uloží první stránku jako GIF, ale můžete nahradit `SaveFormat.Gif` za `SaveFormat.Png`, `SaveFormat.Jpeg` atd., abyste **převáděli OneNote na PNG** nebo jiné formáty.

```java
// Save the document as Gif.
oneFile.save(dataDir + "ConvertToImageUsingDefaultOptions_out.gif", SaveFormat.Gif);
```

**Co se děje pod kapotou?**  
Aspose.Note vykreslí každou stránku do bitmapy a poté ji zakóduje pomocí vybraného kodeku obrázku. Protože spoleháme na výchozí možnosti, knihovna automaticky určuje velikost stránky, DPI a barevnou hloubku.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| **Prázdný výstup obrázku** | Nesprávná cesta k souboru nebo chybějící oprávnění ke čtení | Ověřte `dataDir` a ujistěte se, že soubor `.one` existuje. |
| **Nedostatek paměti při velkých sešitech** | Načítání velmi velkých sešitů do paměti | Zpracovávejte stránky jednotlivě pomocí `Document.getPages()` a uložte každou stránku samostatně. |
| **Nesprávné vykreslení písma** | Písmo není nainstalováno na serveru | Nainstalujte požadovaná písma nebo je vložte do souboru OneNote před převodem. |

## Často kladené otázky

**Q: Mohu převést více‑stránkový sešit OneNote na samostatné obrázky?**  
A: Ano. Procházejte `oneFile.getPages()` a pro každou stránku zavolejte `save`, přičemž zadáte jedinečný název souboru.

**Q: Jak změním rozlišení obrázku?**  
A: Použijte `ImageSaveOptions` pro nastavení DPI před uložením: `ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png); options.setResolution(300); oneFile.save("out.png", options);`

**Q: Je možné převést OneNote přímo na PDF místo obrázku?**  
A: Ano. Nahraďte `SaveFormat.Gif` za `SaveFormat.Pdf` a vytvoříte PDF dokument.

**Q: Přidává bezplatná zkušební verze vodoznaky na výstupní obrázky?**  
A: Ne. Zkušební verze vytváří obrázky v plné kvalitě bez vodoznaků; licence je vyžadována pouze pro komerční nasazení.

**Q: Který formát obrázku poskytuje nejmenší velikost souboru?**  
A: GIF a JPEG obvykle vytvářejí menší soubory než PNG, ale výběr závisí na požadavcích na kvalitu — PNG je bezztrátový, zatímco JPEG je ztrátový.

## Závěr
Po provedení těchto stručných kroků nyní víte **jak převést OneNote na obrázek** pomocí Aspose.Note pro Java s výchozími nastaveními. Tato funkce vám umožní integrovat obsah OneNote do webových galerií, generovat náhledy nebo archivovat stránky jako statické obrázky — vše bez nutnosti instalace Microsoft Office.

## Často kladené otázky

### Q1: Může Aspose.Note pro Java zpracovat složité dokumenty OneNote?
A1: Ano, Aspose.Note pro Java dokáže efektivně zpracovat složité dokumenty OneNote a zajistit přesný převod do různých formátů.

### Q2: Je k dispozici bezplatná zkušební verze Aspose.Note pro Java?
A2: Ano, můžete získat bezplatnou zkušební verzi Aspose.Note pro Java na [webových stránkách](https://releases.aspose.com/).

### Q3: Kde najdu komplexní dokumentaci k Aspose.Note pro Java?
A3: Podrobnou dokumentaci najdete na [Aspose.Note for Java Documentation](https://reference.aspose.com/note/java/).

### Q4: Jak mohu získat dočasnou licenci pro Aspose.Note pro Java?
A4: Dočasnou licenci můžete získat na [stránce dočasné licence](https://purchase.aspose.com/temporary-license/) na webu Aspose.

### Q5: Existuje komunitní fórum, kde mohu získat podporu pro Aspose.Note pro Java?
A5: Ano, můžete se připojit ke komunitnímu fóru na [Aspose.Note for Java Support](https://forum.aspose.com/c/note/28), kde můžete požádat o pomoc a komunikovat s ostatními uživateli.

---

**Poslední aktualizace:** 2025-11-30  
**Testováno s:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
