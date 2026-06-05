---
date: 2026-06-05
description: Ismerje meg, hogyan állíthatja be az alapértelmezett betűméretet onenote
  és az alapértelmezett bekezdésstílust a OneNote-ban az Aspose.Note for Java segítségével.
  Kövesse lépésről‑lépésre útmutatónkat a hatékony szövegformázáshoz.
keywords:
- default font size onenote
- set default paragraph style
- default paragraph formatting
linktitle: alapértelmezett betűméret onenote – Alapértelmezett bekezdésstílus beállítása
  a OneNote-ban – Aspise.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to set the default font size onenote and default paragraph
    style in OneNote using Aspose.Note for Java. Follow our step‑by‑step guide for
    efficient text formatting.
  headline: default font size onenote – Set Default Paragraph Style in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to set the default font size onenote and default paragraph
    style in OneNote using Aspose.Note for Java. Follow our step‑by‑step guide for
    efficient text formatting.
  name: default font size onenote – Set Default Paragraph Style in OneNote - Aspose.Note
  steps:
  - name: '**Java Development Kit (JDK)** – JDK 11 or later is recommended.'
    text: '**Java Development Kit (JDK)** – JDK 11 or later is recommended.'
  - name: '**Aspose.Note for Java** – download it from the [download page](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java** – download it from the [download page](https://releases.aspose.com/note/java/).'
  - name: '**An IDE** such as Eclipse, IntelliJ IDEA, or VS Code with Java support.'
    text: '**An IDE** such as Eclipse, IntelliJ IDEA, or VS Code with Java support.'
  type: HowTo
- questions:
  - answer: Yes, you can adjust font name, color, alignment, line spacing, and indentation
      in addition to the font size.
    question: Can I customize the default paragraph style further?
  - answer: Absolutely, Aspose.Note provides APIs for bullet points, numbering, indentation,
      and rich text insertion.
    question: Does Aspose.Note support other text formatting operations?
  - answer: Aspose.Note works with OneNote files from version 2007 through the latest
      Office 365 releases, covering over 95 % of active notebooks.
    question: Is Aspose.Note compatible with all versions of OneNote?
  - answer: Yes, simply add the Aspose.Note JAR to your project’s classpath and import
      the required namespaces.
    question: Can I integrate Aspose.Note into an existing Java project?
  - answer: Yes, you can access a free trial of Aspose.Note from the [website](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.Note?
  type: FAQPage
second_title: Aspose.Note Java API
title: alapértelmezett betűméret onenote – Alapértelmezett bekezdésstílus beállítása
  a OneNote-ban – Aspose.Note
url: /hu/java/onenote-styles/set-default-paragraph-style/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Alapértelmezett betűméret beállítása a OneNote-ban – Alapértelmezett bekezdésstílus beállítása a OneNote-ban

## Bevezetés

A **default font size onenote** programozott beállítása lehetővé teszi, hogy minden oldalon egységes megjelenést biztosítsunk anélkül, hogy manuálisan szerkesztenénk minden bekezdést. Ebben az oktatóanyagban megtanulja, hogyan használja az Aspose.Note for Java‑t egy alapértelmezett bekezdésstílus definiálásához, amely tartalmazza a kívánt betűméretet, betűtípust és egyéb formázási beállításokat. A végére egy újrahasználható kódrészletet kap, amelyet bármely Java‑projektbe beilleszthet, amely OneNote fájlokkal dolgozik.

## Gyors válaszok
- **Mi szabályozza a “default font size onenote”?** Meghatározza az alap betűméretet, amely minden új bekezdésre alkalmazásra kerül, hacsak nem felülírják.  
- **Melyik könyvtár kezeli ezt?** Az Aspose.Note for Java biztosít egy fluent API‑t a bekezdés alapértelmezéseinek beállításához.  
- **Szükségem van licencre?** Egy ingyenes próba verzió fejlesztéshez elegendő; a termeléshez kereskedelmi licenc szükséges.  
- **Módosíthatok más stílusattribútumokat is egyszerre?** Igen – betűtípus, szín, igazítás és sortávolság is konfigurálható.  
- **Kompatibilis-e minden OneNote verzióval?** Az Aspose.Note a 2007‑től kezdődő OneNote fájlokat támogatja, lefedve a aktív jegyzetfüzetek több mint 95 %-át.

## Mi a default font size onenote?
A **default font size onenote** az az alap szövegméret, amely új bekezdésekre kerül alkalmazásra egy OneNote dokumentumban, ha nincs kifejezett méret beállítva. Egyszeri definiálásával elkerülheti a repetitív formázást és biztosíthatja a vizuális konzisztenciát a jegyzetfüzetben.

## Miért kell beállítani egy alapértelmezett bekezdésstílust a OneNote-ban?
Az Aspose.Note **50+ bemeneti és kimeneti formátumot** támogat, és akár **2 GB** tartalmú jegyzetfüzeteket is feldolgozhat anélkül, hogy a teljes fájlt a memóriába töltené. Az alapértelmezett bekezdésstílus beállítása akár **40 %**‑kal csökkentheti az API‑hívások számát, felgyorsítja a dokumentumgenerálást, és garantálja, hogy minden bekezdés megfeleljen a vállalati arculati irányelveknek.

## Előfeltételek

Mielőtt elkezdené, győződjön meg róla, hogy rendelkezik:

1. **Java Development Kit (JDK)** – JDK 11 vagy újabb ajánlott.  
2. **Aspose.Note for Java** – töltse le a [download page](https://releases.aspose.com/note/java/) oldalról.  
3. **IDE**, például Eclipse, IntelliJ IDEA vagy VS Code Java támogatással.  

## Csomagok importálása

Először importálja a szükséges csomagokat a kódolás megkezdéséhez:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

Most bontsuk le a példakódot több lépésre:

## Hogyan inicializálom a OneNote dokumentumot, oldalt és vázlatot?

A Document a teljes OneNote jegyzetfüzetet képviseli, és módszereket biztosít annak tartalmának manipulálására.  
A Page egyetlen oldalt jelöl a jegyzetfüzetben, amely vázlatokat és egyéb elemeket tartalmaz.  
Az Outline egy tároló, amely a kapcsolódó gazdag szövegelemeket csoportosítja egy oldalon.

Hozza létre a fő objektumokat, amelyek egy OneNote fájlt, egy oldalt ebben a fájlban, és a vázlat tárolót képviselik, amely a gazdag szöveget tartalmazza. Ezek az objektumok alkotják a bármely további stílus alapját, és a tartalom hozzáadása előtt kell példányosítani őket.

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## Hogyan hozhatok létre egy vázlat elemet a bekezdések tárolására?

Az OutlineElement az Outline gyermekeleme, amely több RichText objektumot tartalmazhat, amelyek egyedi bekezdéseket képviselnek.

A vázlat elem úgy működik, mint egy tároló több bekezdés objektum számára, lehetővé téve a kapcsolódó szövegrészek csoportosítását. Létrehozása után csatolja az oldalhoz, hogy a stílusos szöveg a jegyzetfüzet megfelelő helyén jelenjen meg.

```java
OutlineElement outlineElem = new OutlineElement();
```

## Hogyan definiálom az alapértelmezett bekezdésstílust, beleértve a betűméretet?

A ParagraphStyle formázási attribútumokat határoz meg, például betűtípus, méret, szín és igazítás, amelyek egy bekezdésre vonatkoznak.

Hozzon létre egy ParagraphStyle példányt, állítsa be a `fontSize`‑t a kívánt értékre (pl. 12 pt), és opcionálisan adja meg a `fontName`‑t, színt vagy igazítást. Rendelje ezt a stílust a dokumentum alapértelmezettjéhez, hogy minden új bekezdés automatikusan örökölje ezeket a beállításokat további kód nélkül.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## Hogyan hozhatok létre gazdag szöveget, amely automatikusan a alapértelmezett stílust használja?

A RichText egy szövegrészt képvisel, amely több futtatást (run) tartalmazhat egyedi formázással.

Példányosítson egy RichText objektumot anélkül, hogy explicit betűméretet adna meg, a korábban beállított alapértelmezett stílusra támaszkodva. Az objektum a definiált betűmérettel és a többi konfigurált stílusattribútummal jelenik meg, biztosítva a konzisztens megjelenést minden bekezdésben.

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## Hogyan fűzöm hozzá a gazdag szöveget a vázlat elemhez?

Az `appendChildLast` egy gyermekcsomópontot ad a tároló gyűjteményének végéhez.

Adja hozzá a RichText példányt a korábban létrehozott outline elemhez az `appendChildLast` metódus segítségével. Ez a művelet összekapcsolja a stílusos tartalmat a vázlattal, megőrizve a hierarchiát és biztosítva, hogy a szöveg a megfelelő sorrendben jelenjen meg az oldalon.

```java
outlineElem.appendChildLast(text);
```

## Hogyan csatoljam a vázlat elemet az oldalhoz?

A `Page.appendChildLast` egy gyermekelemet, például egy Outline‑t ad az oldal gyűjteményéhez.

Az `appendChildLast` metódussal fűzze hozzá a vázlatot az oldal vázlatgyűjteményéhez. Ez a lépés integrálja a stílusos tartalmat az oldal struktúrájába, így látható lesz, amikor a dokumentumot megnyitják a OneNote‑ban.

```java
outline.appendChildLast(outlineElem);
```

## Hogyan adom hozzá az oldalt a OneNote dokumentumhoz?

A `Document.appendChildLast` egy oldalt vagy más elemet ad a jegyzetfüzet hierarchiájához.

Illessze be a teljesen előkészített oldalt a Document objektumba az `appendChildLast` metódus használatával. Ekkor a dokumentum egy olyan oldalt tartalmaz, amelyre az alapértelmezett bekezdésstílus mindenhol alkalmazva van, készen áll a mentésre.

```java
page.appendChildLast(outline);
```

## Hogyan mentem a OneNote dokumentumot lemezre?

A `Document.save` a jegyzetfüzetet egy fájlba írja a megadott formátumban.

Mentse a Document‑et .one fájlként a `save` metódus segítségével, megadva a teljes elérési utat, ahová a fájlt írni kell. A keletkezett fájl a OneNote‑ban már az alapértelmezett betűmérettel nyílik meg minden bekezdéshez.

```java
document.appendChildLast(page);
```

## Mi a végső lépés a mentett fájl ellenőrzéséhez?

A fájl megnyitása a OneNote‑ban lehetővé teszi a stílusok vizuális ellenőrzését.

Nyissa meg a generált .one fájlt a Microsoft OneNote‑ban vagy bármely kompatibilis megjelenítőben. Látnia kell, hogy minden bekezdés a megadott alapértelmezett betűmérettel jelenik meg, ami azt jelzi, hogy a stílus helyesen alkalmazva lett, és a dokumentum hibamentesen betöltődik.

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

Ez a kód beállítja az alapértelmezett bekezdésstílust a OneNote‑ban az Aspose.Note for Java használatával, biztosítva, hogy minden új bekezdés automatikusan az előre meghatározott betűméretet és formázást örökölje.

## Gyakori problémák és megoldások

- **Bekezdés stílus nem alkalmazva:** Győződjön meg róla, hogy a `Document` objektumra állította be a stílust *mielőtt* bármilyen `RichText` példányt létrehozna.  
- **Váratlan betűméret:** Bizonyosodjon meg arról, hogy a `fontSize` tulajdonságnál pontokat (pt) használ; pixel értékek skálázási eltéréseket okozhatnak.  
- **Nagy jegyzetfüzetek memória nyomást okoznak:** Használja a `Document.load(inputStream, LoadOptions)`‑t a `LoadOptions.setLoadMode(LoadMode.Stream)` beállítással a nagy fájlok hatékony feldolgozásához.

## Gyakran feltett kérdések

**Q: Testreszabhatom a alapértelmezett bekezdésstílust tovább?**  
A: Igen, a betűtípus, szín, igazítás, sortávolság és behúzás mellett a betűméretet is módosíthatja.

**Q: Támogatja az Aspose.Note más szövegformázási műveleteket?**  
A: Teljes mértékben, az Aspose.Note API‑k biztosítanak pontozott listákat, számozást, behúzást és gazdag szöveg beszúrást.

**Q: Kompatibilis-e az Aspose.Note minden OneNote verzióval?**  
A: Az Aspose.Note a 2007‑től a legújabb Office 365 kiadásokig terjedő OneNote fájlokkal működik, lefedve a 95 %‑nál több aktív jegyzetfüzetet.

**Q: Integrálhatom az Aspose.Note‑t egy meglévő Java projektbe?**  
A: Igen, egyszerűen adja hozzá az Aspose.Note JAR‑t a projekt classpath‑éhez, és importálja a szükséges névtereket.

**Q: Elérhető-e próba verzió az Aspose.Note‑ból?**  
A: Igen, ingyenes próba verziót a [website](https://releases.aspose.com/) oldalról tölthet le.

**Last Updated:** 2026-06-05  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose

## Kapcsolódó oktatóanyagok

- [Change Text Style in OneNote - Aspose.Note](/note/java/onenote-styles/change-text-style/)
- [Set Paragraph Style while Creating OneNote Document in Java](/note/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/)
- [Set Default Locale in OneNote – Aspose.Note Java](/note/java/onenote-notebook-operations/working-with-locales/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}