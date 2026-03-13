---
date: 2026-02-07
description: Naučte se, jak exportovat písma při ukládání OneNote jako HTML pomocí
  Aspose.Note pro Javu. Tento průvodce vám ukáže, jak programově vytvořit OneNote
  a vložit písma, CSS a obrázky.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Jak exportovat písma při ukládání OneNote do HTML – Java
url: /cs/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak exportovat písma při ukládání OneNote jako HTML – Java

## Úvod

V tomto tutoriálu se dozvíte **jak exportovat písma**, když **uložíte OneNote jako HTML** pomocí Aspose.Note pro Java. Provedeme vás vytvořením OneNote dokumentu programově, nastavením možností uložení HTML a vložením požadovaných souborů písem, aby výsledné HTML vypadalo přesně jako původní stránky OneNote. Tento přístup je ideální, když potřebujete zachovat vizuální věrnost obsahu OneNote ve webově přátelském formátu.

## Rychlé odpovědi
- **Jaká knihovna provádí export?** Aspose.Note for Java  
- **Lze písma vložit do HTML?** Ano – nastavte `ExportFonts` na `ExportEmbedded`  
- **Potřebuji licenci pro produkci?** Platná licence Aspose.Note je vyžadována pro komerční použití  
- **Která verze Javy je podporována?** Java 8 nebo vyšší  
- **Je možné uložit zdroje do samostatných souborů?** Rozhodně – nakonfigurujte `ResourceExportType` podle toho  

## Co znamená „jak exportovat písma“ v kontextu konverze OneNote do HTML?

Když převádíte poznámkový blok OneNote do HTML, vizuální vzhled závisí na CSS, obrázcích a zejména na písmech použitých v původních stránkách. **Exportování písem** znamená vložení souborů písem (např. TTF) přímo do HTML balíčku, aby prohlížeče mohly vykreslit text přesně tak, jak se zobrazuje v OneNote, i když uživatel nemá tato písma nainstalována lokálně.

## Proč vytvářet OneNote programově a ukládat jej jako HTML?

- **Automatizace:** Generovat zprávy, dokumentaci nebo články znalostní báze z OneNote bez ručního kopírování a vkládání.  
- **Konzistence:** Zachovat rozvržení, stylování a vlastní písma napříč zařízeními.  
- **Přenositelnost:** HTML je univerzálně zobrazitelné – není potřeba klient OneNote.  

## Požadavky

1. Nainstalovaný Java Development Kit (JDK) 8 nebo novější.  
2. Knihovna Aspose.Note pro Java – stáhněte ji z [here](https://releases.aspose.com/note/java/).  
3. Vzorek souboru OneNote (`.one`) k načtení, nebo můžete vytvořit nový programově.  

## Import balíčků

Nejprve importujte požadované třídy do svého Java projektu:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Jak exportovat písma při ukládání OneNote jako HTML?

Níže je krok‑za‑krokem průvodce, který vám ukáže **jak exportovat písma** a další zdroje.

### Krok 1: Vytvořit OneNote dokument programově  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Tento řádek načte existující soubor `.one`. Pokud potřebujete **vytvořit OneNote programově**, můžete vytvořit novou instanci objektu `Document` a přidat sekce/stránky pomocí API (není zde ukázáno, aby byl zachován fokus na exportování písem).

### Krok 2: Uložit do paměťového proudu s vloženými písmy  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` říká Aspose.Note, aby **exportovalo písma** přímo do HTML balíčku.  
- `setFontFaceTypes(FontFaceType.Ttf)` zajišťuje použití TrueType písem, která mají širokou podporu v prohlížečích.

### Krok 3: Uložit jako HTML s oddělenými soubory zdrojů (stále exportuje písma)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

I když jsou CSS a obrázky vloženy, můžete změnit `ResourceExportType` na `ExportExternal`, pokud dáváte přednost samostatným souborům pro snadnější cachování. Klíčová část – **exportování písem** – zůstává beze změny.

### Krok 4: Použít zpětné volání pro kontrolu, kam se každý zdroj uloží  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Třída `UserSavingCallbacks` (budete muset implementovat `ICssSavingCallback`, `IImageSavingCallback` a `IFontSavingCallback`) vám poskytuje plnou kontrolu nad strukturou složek, což vám umožní uchovávat písma v samostatném adresáři `fonts`, zatímco **exportujete písma** správně.

## Jak vložit vlastní písma při konverzi OneNote do HTML

Vložení vlastních písem zaručuje, že vykreslení HTML odpovídá původnímu rozvržení OneNote, i na zařízeních, která tato písma nemají nainstalována. Použitím `ExportEmbedded` spolu s `FontFaceType.Ttf` jsou soubory TrueType kódovány base‑64 a vloženy přímo do generovaného CSS, čímž se eliminuje potřeba externího hostování písem.

## Použití ResourceExportType pro řízení exportu zdrojů

`ResourceExportType` vám umožňuje rozhodnout, zda jsou CSS, obrázky a písma uloženy **uvnitř** HTML souboru (`ExportEmbedded`) nebo jako **externí** soubory (`ExportExternal`). Zvolte `ExportEmbedded` pro řešení v jednom souboru, nebo `ExportExternal`, pokud chcete využít cachování prohlížeče pro velké assety.

## Vytvoření OneNote programově pro export do HTML

Pokud začínáte od nuly, můžete vytvořit OneNote dokument kompletně v kódu, přidat sekce, stránky a bohatý text a poté použít stejné `HtmlSaveOptions`, jak jsou uvedeny výše. To vám poskytne kompletní automatizaci: od generování dat po plně stylovaný HTML výstup s vloženými vlastními písmy.

## Časté problémy a tipy

- **Chybějící písma ve výstupu:** Ověřte, že je nastaveno `setExportFonts(ResourceExportType.ExportEmbedded)` a že zdrojový soubor OneNote skutečně používá vložená písma.  
- **Velké HTML soubory:** Vkládání písem může zvýšit velikost. Pokud je šířka pásma problém, přepněte `ExportFonts` na `ExportExternal` a hostujte písma na CDN.  
- **Chyby při implementaci zpětných volání:** Ujistěte se, že vaše třídy zpětných volání správně zapisují stream a uzavírají zdroje, aby nedošlo k poškození souboru.  

## Často kladené otázky

**Q: Mohu převést více OneNote dokumentů do HTML najednou?**  
A: Ano, projděte každou instanci `Document` a použijte stejné `HtmlSaveOptions`.  

**Q: Podporuje Aspose.Note pro Java další výstupní formáty kromě HTML?**  
A: Rozhodně. Můžete exportovat do PDF, DOCX, PNG, JPEG a dalších pomocí příslušných možností uložení.  

**Q: Je k dispozici zkušební verze Aspose.Note pro Java?**  
A: Ano, stáhněte si bezplatnou zkušební verzi z [here](https://releases.aspose.com/).  

**Q: Kde mohu získat podporu pro Aspose.Note pro Java?**  
A: Navštivte [Aspose.Note forum](https://forum.aspose.com/c/note/28) pro komunitní a oficiální pomoc.  

**Q: Jak mohu zakoupit licenci pro Aspose.Note pro Java?**  
A: Licence jsou k dispozici na [Aspose website](https://purchase.aspose.com/buy).  

## Závěr

Nyní víte **jak exportovat písma**, když **ukládáte OneNote jako HTML** pomocí Aspose.Note pro Java. Konfigurací `HtmlSaveOptions` a volitelným použitím zpětných volání můžete zachovat přesný vzhled vašich OneNote stránek – včetně vlastních písem – při jejich publikaci na webu. Neváhejte experimentovat s různými nastaveními `ResourceExportType`, aby vyhovovaly požadavkům vašeho projektu na výkon a úložiště.

---

**Poslední aktualizace:** 2026-02-07  
**Testováno s:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}