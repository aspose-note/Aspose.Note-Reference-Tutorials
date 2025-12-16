---
date: 2025-12-13
description: Naučte se, jak nastavit práh pro převod OneNote na PNG pomocí Aspose.Note
  Java, a vytvářet černobílé obrázky OneNote pomocí binarizace obrazu v Javě.
linktitle: Save to Binary Image Using Fixed Threshold in OneNote
second_title: Aspose.Note Java API
title: Jak upravit práh při ukládání OneNote do binárního obrazu
url: /cs/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak upravit práh při ukládání OneNote do binárního obrazu

## Úvod

V tomto tutoriálu se dozvíte **jak upravit práh** pro export stránky Microsoft OneNote jako vysokokontrastního černobílého PNG obrazu. Úpravou pevné hodnoty prahu získáte přesnou kontrolu nad konverzí, což je ideální pro scénáře jako předzpracování OCR nebo archivace dokumentů. Provedeme vás každým krokem pomocí Aspose.Note Java API, abyste mohli rychle **převést OneNote na PNG** s spolehlivými technikami **image binarization Java**.

## Rychlé odpovědi
- **Co znamená „adjust threshold“?** Nastavuje ořez pixelové intenzity používaný při převodu barevného obrazu na černobílý.
- **Jaký formát je vytvořen?** PNG soubor, který lze otevřít v libovolném prohlížeči obrázků.
- **Mohu změnit hodnotu prahu?** Ano – upravte volání `setBinarizationThreshold()`.
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.
- **Je to kompatibilní se všemi verzemi OneNote?** Aspose.Note podporuje OneNote 2010, 2013, 2016 a novější.

## Předpoklady

 ujistěte se, že máte:

1. Nainstalovaný Java Development Kit (JDK).
2. Aspose.Note pro Java knihovnu staženou z [zde](https://releases.aspose.com/note/java/).
3. Základní znalost syntaxe Java.

## Import balíčků

Nejprve importujte požadované třídy do vašeho Java zdrojového souboru.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Krok 1: Načtení dokumentu

Načtěte OneNote soubor, který chcete zpracovat.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Krok 2: Nastavení možností binarizace

Definujte nastavení **image binarization Java** a specifikujte pevný práh, který chcete použít.

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

> **Tip:** Experimentujte s hodnotami prahu mezi 0‑255, abyste našli optimální nastavení pro váš konkrétní dokument. Nižší hodnoty produkují světlejší obrázky, vyšší hodnoty dávají tmavější výstup.

## Krok 3: Nastavení možností uložení obrazu

Nakonfigurujte formát obrazu, režim barev a připojte možnosti binarizace.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

Nastavení `ColorMode.BlackAndWhite` zajišťuje, že výsledný soubor je **černobílý OneNote** obrázek.

## Krok 4: Uložení dokumentu

Proveďte operaci uložení s dříve definovanými možnostmi.

```java
oneFile.save(dataDir, options);
```

Po spuštění kódu najdete PNG soubor pojmenovaný `SaveToBinaryImageUsingFixedThreshold_out.png` ve vašem výstupním adresáři, připravený k dalšímu zpracování nebo archivaci.

## Závěr

Ukázali jsme **jak upravit práh**, abyste z OneNote souboru pomocí Aspose.Note pro Java vytvořili čistý, vysokokontrastní PNG. Ovládnutím možností **image binarization Java** můžete spolehlivě **převést OneNote na PNG** a vytvořit **černobílé OneNote** prostředky pro OCR, tisk nebo digitální archivaci.

## Často kladené otázky

**Q: Co se stane, když nastavím práh příliš nízko?**  
A: Výsledný obrázek může vypadat vybledle, s mnoha šedými tóny místo ostrého černobílého kontrastu.

**Q: Mohu použít jinou metodu binarizace?**  
A: Ano, Aspose.Note také podporuje adaptivní prahování; stačí nahradit `BinarizationMethod.FixedThreshold` za `BinarizationMethod.Adaptive`.

**Q: Je možné exportovat přímo do jiných formátů, jako je JPEG?**  
A: Rozhodně—změňte `SaveFormat.Png` na `SaveFormat.Jpeg` v konstruktoru `ImageSaveOptions`.

**Q: Jak zacházet s OneNote soubory chráněnými heslem?**  
A: Načtěte dokument pomocí odpovídající přetížené metody, která přijímá řetězec hesla, před aplikací kroků binarizace.

**Q: Funguje tento přístup na Linux/macOS?**  
A: Knihovna Aspose.Note Java je platformně nezávislá, takže stejný kód běží na jakémkoli OS s kompatibilním JDK.

**Poslední aktualizace:** 2025-12-13  
**Testováno s:** Aspose.Note for Java 24.12 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}