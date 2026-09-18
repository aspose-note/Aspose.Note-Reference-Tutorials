---
date: 2026-03-29
description: Naučte se, jak nastavit jazyk textu v OneNote pomocí Aspose.Note pro
  Javu. Tento krok‑za‑krokem průvodce vám ukáže, jak vytvořit dokument OneNote, změnit
  jazyk textu a efektivně uložit soubor OneNote.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Jak nastavit jazyk pro text v OneNote – Aspose.Note
url: /cs/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nastavit jazyk pro text v OneNote – Aspose.Note

## Úvod
Pokud potřebujete **jak nastavit jazyk** pro konkrétní části textu v poznámkovém bloku OneNote, Aspose.Note pro Java to usnadňuje. V tomto tutoriálu se naučíte, jak vytvořit dokument OneNote, změnit jazyk textu pro jednotlivá slova nebo fráze a nakonec uložit soubor OneNote s aplikovaným správným jazykem korektury. Na konci pochopíte, proč nastavení jazyka má význam pro kontrolu pravopisu a lokalizaci, a budete mít připravený spustitelný ukázkový kód.

## Rychlé odpovědi
- **Co ovlivňuje „nastavení jazyka“?** Říká OneNote, který slovník pro kontrolu pravopisu a gramatiku použít.  
- **Mohu nastavit různé jazyky ve stejné poznámce?** Ano, můžete přiřadit jazyk každému úseku textu.  
- **Potřebuji licenci pro Aspose.Note?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence.  
- **Které verze Javy jsou podporovány?** Aspose.Note pro Java podporuje Javu 8 a novější.  
- **Je výstup .one soubor?** Ano, dokument je uložen jako soubor OneNote *.one*.

## Předpoklady
Než se pustíte do kódu, ujistěte se, že máte následující:

1. **Java Development Environment** – Nainstalovaný a nakonfigurovaný JDK 8 nebo vyšší.  
2. **Aspose.Note for Java Library** – Stáhněte a nainstalujte knihovnu z [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Vytvořte složku na svém počítači, kam bude uložen generovaný soubor OneNote.

## Proč nastavit jazyk pro text v OneNote?
Nastavení jazyka pro korekturu zajišťuje, že kontrola pravopisu, návrhy gramatiky a indexování vyhledávání fungují správně pro vícejazyčný obsah. To je zvláště užitečné pro:

- **Globální týmy** spolupracující na jednom poznámkovém bloku.  
- **Lokalizovaná dokumentace**, kde může být každá sekce v jiném jazyce.  
- **Datově řízené aplikace**, které programově generují poznámky pro uživatele po celém světě.

## Import balíčků
Začněte importováním potřebných tříd Aspose.Note a Java utilit.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Krok 1: Nastavení dokumentu a stránky
Vytvořte nový dokument OneNote a stránku, která bude obsahovat váš obsah. Tento krok také demonstruje **create OneNote document**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Krok 2: Vytvoření obrysu a elementu obrysu
Obrys je kontejner pro obsah poznámkového bloku. Zde vytváříme strukturu, která později bude obsahovat jazykově specifický text.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Krok 3: Přidání formátovaného textu s nastavením jazyka
Nyní **change text language** připojením `TextStyle` s konkrétním `Locale` ke každému textovému segmentu. Toto demonstruje **set language for text**.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Krok 4: Organizace elementů a uložení
Sestavte hierarchii obrysu, připojte ji ke stránce a nakonec **save OneNote file** s aplikovaným nastavením jazyka.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Časté úskalí a tipy
- **Locale format** – Použijte značku IETF BCP‑47 (např. `en-US`, `de-DE`). Nesprávná značka se vrátí na jazyk dokumentu.  
- **File path** – Ujistěte se, že `dataDir` ukazuje na existující složku; jinak `document.save` vyhodí `IOException`.  
- **Pro tip:** Pokud potřebujete nastavit jazyk pro celý odstavec, použijte `TextStyle` na `ParagraphStyle` místo každého volání `append`.

## Závěr
Právě jste se naučili **how to set language** pro jednotlivé úryvky textu v poznámkovém bloku OneNote pomocí Aspose.Note pro Java. Tato schopnost vám umožní **create OneNote document** programově, **change text language** za běhu a **save OneNote file** s přesnými metadaty korektury.

## Často kladené otázky

**Q: Mohu nastavit jazyk korektury pro jiné jazyky, které nejsou v příkladu uvedeny?**  
A: Ano! Přidejte další volání `append` s požadovaným `Locale.forLanguageTag("xx-XX")`.

**Q: Je Aspose.Note pro Java kompatibilní s nejnovějšími verzemi Javy?**  
A: Ano, knihovna je pravidelně aktualizována, aby podporovala nejnovější vydání Javy.

**Q: Jak mohu ošetřit chyby během procesu nastavení jazyka?**  
A: Zabalte operaci uložení do bloku `try‑catch`, abyste zachytili `IOException` nebo `AsposeException`.

**Q: Mohu tento kód integrovat do webové aplikace?**  
A: Samozřejmě. Stačí zahrnout Aspose.Note JAR do classpath vašeho webového projektu a zajistit, aby server měl oprávnění k zápisu do cílového adresáře.

**Q: Kde najdu další příklady a dokumentaci pro Aspose.Note pro Java?**  
A: Prozkoumejte [documentation](https://reference.aspose.com/note/java/) pro úplný seznam API a ukázkových projektů.

---

**Poslední aktualizace:** 2026-03-29  
**Testováno s:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}