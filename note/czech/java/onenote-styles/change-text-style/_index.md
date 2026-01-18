---
date: 2026-01-18
description: Naučte se, jak nastavit barvu písma v Java v OneNote pomocí Aspose.Note,
  zvýraznit text, upravit velikost písma a uložit OneNote jako PDF. Průvodce krok
  za krokem s kódem.
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Nastavit barvu písma v OneNote pomocí Java – Aspose.Note
url: /cs/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavit barvu písma Java v OneNote – Aspose.Note

## Úvod

V tomto tutoriálu se dozvíte, jak **nastavit barvu písma Java** pro text uvnitř dokumentu OneNote pomocí API Aspose.Note pro Java. Provedeme vás načtením souboru `.one`, přístupem k jeho uzlům RichText, aplikací změn barvy, zvýraznění a velikosti písma a nakonec **uložením OneNote jako PDF**. Ať už potřebujete **zvýraznit text v OneNote**, **upravit velikost písma v OneNote**, nebo jen změnit celkový styl textu, níže uvedené kroky vám poskytnou kompletní, připravené řešení pro produkci.

## Rychlé odpovědi
- **Mohu změnit barvu písma konkrétních slov?** Ano – iterujte přes objekty `TextRun` a nastavte `setFontColor`.
- **Umožňuje mi Aspose.Note uložit OneNote jako PDF?** Ano; použijte `document.save("output.pdf")`.
- **Jaká verze Javy je vyžadována?** Java 8 nebo vyšší.
- **Je podporováno zvýraznění?** Použijte `setHighlight(Color)` na `TextStyle`.
- **Mohu převést OneNote do PDF jedním řádkem?** Ne přímo, ale metoda `save` provádí konverzi.

## Co je „set font color java“?

Tento výraz označuje programové přiřazení nové barvy písma textovým prvkům v souboru OneNote pomocí kódu v Javě. S Aspose.Note získáte plnou kontrolu nad atributy stylu, jako je barva písma, zvýraznění a velikost, aniž byste museli otevírat uživatelské rozhraní OneNote.

## Proč měnit styl textu v OneNote?

- **Zlepšená čitelnost** – barevný nebo zvýrazněný text přitahuje pozornost k důležitým bodům.
- **Konzistence značky** – vynucení firemních barev napříč zápisy ze schůzek.
- **Kvalita exportu** – stylizované poznámky vypadají profesionálně, když je **převádíte OneNote do PDF** pro sdílení.

## Požadavky

Než se pustíme dál, ujistěte se, že máte:

1. Základní znalosti programování v Javě.  
2. Nainstalovaný JDK 8 nebo novější.  
3. Knihovnu Aspose.Note pro Java přidanou do vašeho projektu (Maven/Gradle nebo ruční JAR).  
4. Ukázkový soubor OneNote (`Sample1.one`) pro experimentování.  

## Import balíčků

Nejprve importujte třídy, které budeme potřebovat:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## Průvodce krok za krokem

### Krok 1: Načtení dokumentu

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

Načteme soubor OneNote (`Sample1.one`), aby Aspose.Note mohl pracovat s jeho vnitřní strukturou.

### Krok 2: Přístup k uzlům RichText

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

Objekty `RichText` obsahují skutečné odstavce. Získáním prvního uzlu získáme odkaz na text, který chceme stylovat.

### Krok 3: Změna stylu textu (set font color java)

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

Uvnitř smyčky **nastavíme barvu písma Java** na žlutou, použijeme modré zvýraznění (ukazuje **zvýraznění textu v OneNote**), a zvýšíme velikost na 20 bodů, což ilustruje **úpravu velikosti písma v OneNote**.

### Krok 4: Uložení dokumentu (uložit OneNote jako PDF)

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

Voláním `save` s příponou `.pdf` automaticky **převádí OneNote do PDF**, čímž získáte soubor připravený ke sdílení.

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|---------|-------|--------|
| Žádná změna barvy není vidět | Dokument byl otevřen v OneNote před uložením | Zavřete OneNote nebo znovu načtěte soubor po dokončení Java procesu |
| Zvýraznění nebylo použito | Použití barvy, která se shoduje s pozadím | Zvolte kontrastní `Color` (např. `Color.yellow`) |
| `document.save` vyvolá `IOException` | Neplatná výstupní cesta | Ujistěte se, že adresář existuje a máte oprávnění k zápisu |

## Často kladené otázky

**Q: Mohu tyto změny stylu aplikovat jen na určité sekce mého souboru OneNote?**  
A: Ano – před iterací přes `TextRun`y filtrujte uzly `RichText` podle jejich nadřazeného `Section` nebo `Page`.

**Q: Kromě barvy, zvýraznění a velikosti, jaké další formátování Aspose.Note podporuje?**  
A: Můžete měnit rodinu písma, tučné/kurzívu/podtržení, zarovnání a dokonce i mezery mezi odstavci.

**Q: Je možné hromadně zpracovávat více souborů OneNote?**  
A: Ano. Zabalte načítací a stylovací logiku do smyčky, která zpracuje každý soubor `.one` ve složce.

**Q: Podporuje knihovna přímé ukládání do jiných formátů, jako je DOCX?**  
A: Ano – Aspose.Note může exportovat do PDF, DOCX, HTML a několika formátů obrázků.

**Q: Kde mohu najít více příkladů a referenci API?**  
A: Navštivte oficiální dokumentační stránku Aspose.Note, prozkoumejte referenci API a stáhněte si bezplatnou zkušební verzi pro praktické testování.

## Závěr

Nyní máte kompletní příklad od začátku do konce, jak **nastavit barvu písma Java**, zvýraznit text, upravit velikost písma a **uložit OneNote jako PDF** pomocí Aspose.Note. Klidně upravte kód tak, aby cílil na konkrétní stránky, aplikoval podmíněné stylování nebo jej integroval do větších pipeline pro zpracování dokumentů.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-01-18  
**Testováno s:** Aspose.Note 24.11 for Java  
**Autor:** Aspose