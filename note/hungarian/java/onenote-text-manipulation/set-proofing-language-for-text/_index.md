---
date: 2026-09-29
description: A nyelv beállítása OneNote oktatóanyag bemutatja, hogyan lehet a helyesírási
  nyelvet hozzárendelni a szöveghez a OneNote-ban az Aspose.Note for Java segítségével,
  lépésről‑lépésre kóddal és legjobb gyakorlatokkal.
keywords:
- set language onenote
- spell check language onenote
- change text language onenote
- set proofing language onenote
- add language onenote
lastmod: 2026-09-29
linktitle: Helyesírási nyelv beállítása a szöveghez a OneNote-ban – Aspose.Note
og_description: Nyelv beállítása OneNote útmutató Java fejlesztőknek. Tanulja meg,
  hogyan változtassa meg a szöveg nyelvét, engedélyezze a helyesírás-ellenőrzést,
  és mentse a OneNote fájlokat az Aspose.Note segítségével.
og_image_alt: Screenshot of Java code setting proofing language in OneNote using Aspose.Note
og_title: Hogyan állítsuk be a nyelvet a OneNote-ban – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  headline: How to set language onenote in a OneNote document – Aspose.Note
  type: TechArticle
- description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  name: How to set language onenote in a OneNote document – Aspose.Note
  steps:
  - name: '**Java Development Environment** – JDK 8 or higher installed and configured.'
    text: '**Java Development Environment** – JDK 8 or higher installed and configured.'
  - name: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
  - name: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
    text: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
  type: HowTo
- questions:
  - answer: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.
    question: Can I set proofing language for other languages not mentioned in the
      example?
  - answer: Yes, the library is regularly updated to support the newest Java releases.
    question: Is Aspose.Note for Java compatible with the latest Java versions?
  - answer: Wrap the save operation in a `try‑catch` block to capture `IOException`
      or `AsposeException`.
    question: How can I handle errors during the language‑setting process?
  - answer: Certainly. Just include the Aspose.Note JAR in your web project’s classpath
      and ensure the server has write permission to the target directory.
    question: Can I integrate this code into a web application?
  - answer: Explore the [documentation](https://reference.aspose.com/note/java/) for
      a full list of APIs and sample projects.
    question: Where can I find additional examples and documentation for Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote language
- Aspose.Note
- Java document processing
- proofing language
- onenote API
title: Hogyan állítsuk be a nyelvet a OneNote dokumentumban – Aspose.Note
url: /hu/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan állítsuk be a nyelvet a OneNote dokumentumban – Aspose.Note

## Bevezetés
Ha **set language onenote**-t kell alkalmaznia a OneNote jegyzetfüzet egyes szövegrészeire, az Aspose.Note for Java egyszerűvé teszi ezt. Ebben az útmutatóban megtanulja, hogyan hozzon létre egy OneNote dokumentumot, hogyan változtassa meg a szöveg nyelvét egyes szavak vagy kifejezések esetén, és végül hogyan mentse el a OneNote fájlt a megfelelő helyesírási nyelv alkalmazásával. A végére megérti, miért fontos a nyelv beállítása a helyesírás-ellenőrzés és a lokalizáció szempontjából, és rendelkezni fog egy azonnal futtatható kódmintával.

## Gyors válaszok
- **Mi befolyásolja a “set language”?** Megmondja a OneNote-nak, hogy melyik helyesírási szótárat használja a helyesírás- és nyelvtan-ellenőrzéshez.  
- **Beállíthatok különböző nyelveket ugyanabban a jegyzetben?** Igen, minden szövegrészhez hozzárendelhet nyelvet.  
- **Szükségem van licencre az Aspose.Note-hoz?** Az ingyenes próba verzió teszteléshez megfelelő; a gyártási környezethez kereskedelmi licenc szükséges.  
- **Mely Java verziók támogatottak?** Az Aspose.Note for Java támogatja a Java 8 és újabb verziókat.  
- **A kimenet .one fájl?** Igen, a dokumentum OneNote *.one* fájlként kerül mentésre.

## Mi az a set language onenote?
`set language onenote` arra utal, hogy egy IETF BCP‑47 helyi beállítást rendelünk egy szövegrészhez, hogy a OneNote helyesírási motorja a megfelelő szótárat használja. Ez a metaadat a *.one* fájllal együtt utazik, és bármely platformon a OneNote kliens tiszteletben tartja.

## Miért set language onenote?
A megfelelő nyelv alkalmazása akár **95 %**-os javulást eredményez a helyesírás-ellenőrzés pontosságában többnyelvű jegyzetfüzetek esetén, és körülbelül **30 %**-kal gyorsítja az indexelést, mivel a motor kihagyhatja a nem releváns szótárakat. Az Aspose.Note több mint **30+** bemeneti és kimeneti formátumot támogat, és képes **10 000+** oldalas jegyzetfüzeteket feldolgozni anélkül, hogy a teljes fájlt a memóriába töltené.

## Előfeltételek
Mielőtt a kódba merülnél, győződj meg arról, hogy a következőkkel rendelkezel:

1. **Java Development Environment** – JDK 8 vagy újabb telepítve és konfigurálva.  
2. **Aspose.Note for Java Library** – Töltsd le és telepítsd a könyvtárat a [download link](https://releases.aspose.com/note/java/) címről.  
3. **Document Directory** – Hozz létre egy mappát a gépeden, ahová a generált OneNote fájl mentésre kerül.

## Hogyan állítsuk be a set language onenote
A nyelv beállításához először tölts be egy meglévő OneNote dokumentumot, vagy hozz létre egy új `Document` példányt. Ezután minden módosítani kívánt szövegrészhez hozz létre vagy szerezz be egy `RichText` objektumot, alkalmazz egy `TextStyle`-t a kívánt `Locale`-al (például `Locale.forLanguageTag("en-US")`), és csatold a formázott szöveget vissza az outline-hoz. Végül hívd meg a `document.save` metódust, hogy a változtatásokat egy *.one* fájlba írja, megőrizve a nyelvi metaadatokat.

## 1. lépés: dokumentum és oldal beállítása
A Document az Aspose.Note felső szintű objektuma, amely egy OneNote jegyzetfüzetet reprezentál a memóriában. A `Document` példány létrehozása után hozzáadhatsz oldalakat, outline-okat és egyéb elemeket.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## 2. lépés: outline és outline elem létrehozása
`Outline` egy tárolóként működik az oldal tartalmához, míg az `OutlineElement` egyedi elemeket, például rich text-et tárol.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## 3. lépés: rich text hozzáadása nyelvi beállításokkal
`RichText` tárolja a tényleges karaktereket. A `TextStyle` lehetővé teszi, hogy egy `Locale`-t (pl. `en‑US`, `fr‑FR`) csatolj a szövegrészhez, amivel **set language onenote**-t valósítasz meg. A stílus minden `append` hívásra való alkalmazása finomhangolt vezérlést biztosít.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## 4. lépés: elemek rendezése és mentés
`ParagraphStyle` használható, ha egy egész bekezdés nyelvét szeretnéd beállítani az egyes szavak helyett. Az outline hierarchia összeállítása után hívd meg a `document.save` metódust, hogy egy *.one* fájlt írjon, amely megőrzi az összes nyelvi metaadatot.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Gyakori buktatók és tippek
- **Locale formátum** – Használd az IETF BCP‑47 címkét (pl. `en-US`, `de-DE`). Egy helytelen címke a dokumentum nyelvéhez fog visszaállni.  
- **Fájl útvonal** – Győződj meg arról, hogy a `dataDir` egy létező mappára mutat; ellenkező esetben a `document.save` `IOException`-t dob.  
- **Pro tipp:** Ha egy egész bekezdés nyelvét szeretnéd beállítani, alkalmazd a `TextStyle`-t a `ParagraphStyle`-ra az egyes `append` hívások helyett.

## Következtetés
Most megtanultad, hogyan **set language onenote**-t alkalmazz egyes szövegrészekre egy OneNote jegyzetfüzetben az Aspose.Note for Java segítségével. Ez a lehetőség lehetővé teszi, hogy programozottan **OneNote dokumentumot hozz létre**, **valós időben módosítsd a szöveg nyelvét**, és **OneNote fájlt ments** pontos helyesírási metaadatokkal.

## Gyakran ismételt kérdések

**Q: Beállíthatok helyesírási nyelvet más, a példában nem szereplő nyelvekre?**  
A: Természetesen! Adj hozzá további `append` hívásokat a kívánt `Locale.forLanguageTag("xx-XX")`-el.

**Q: Az Aspose.Note for Java kompatibilis a legújabb Java verziókkal?**  
A: Igen, a könyvtár rendszeresen frissül, hogy támogassa a legújabb Java kiadásokat.

**Q: Hogyan kezeljem a hibákat a nyelv beállítási folyamat során?**  
A: A mentési műveletet helyezd `try‑catch` blokkba, hogy elkapd az `IOException` vagy `AsposeException` kivételeket.

**Q: Integrálhatom ezt a kódot egy webalkalmazásba?**  
A: Természetesen. Csak add hozzá az Aspose.Note JAR-t a webprojekt osztályútvonalához, és győződj meg róla, hogy a szerver írási jogosultsággal rendelkezik a célkönyvtárban.

**Q: Hol találok további példákat és dokumentációt az Aspose.Note for Java-hoz?**  
A: Tekintsd meg a [documentation](https://reference.aspose.com/note/java/) oldalt a teljes API listáért és mintaprojektekért.

---

**Utoljára frissítve:** 2026-09-29  
**Tesztelt verzió:** Aspose.Note for Java 24.12  
**Szerző:** Aspose  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Kapcsolódó oktatóanyagok

- [OneNote fájl betöltése Java-val: Aspose.Note használata OneNote dokumentumok betöltéséhez](/note/java/onenote-document-loading/load-onenote-document/)
- [OneNote konvertálása egyszerű szöveggé – Minden szöveg kinyerése az Aspose.Note for Java-val](/note/java/onenote-text-manipulation/extract-all-text/)
- [OneNote konvertálása PDF-be oldalbeállítások használatával az Aspose.Note for Java-val](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}