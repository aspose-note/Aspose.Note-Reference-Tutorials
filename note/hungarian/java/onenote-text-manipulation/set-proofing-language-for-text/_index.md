---
date: 2026-03-29
description: Tanulja meg, hogyan állíthatja be a szöveg nyelvét a OneNote-ban az Aspose.Note
  for Java használatával. Ez a lépésről‑lépésre útmutató megmutatja, hogyan hozhat
  létre OneNote‑dokumentumot, változtathatja meg a szöveg nyelvét, és mentheti hatékonyan
  a OneNote‑fájlt.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Hogyan állítsuk be a szöveg nyelvét a OneNote-ban – Aspose.Note
url: /hu/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan állítsuk be a nyelvet a szöveghez a OneNote-ban – Aspose.Note

## Bevezetés
Ha **hogyan állítsuk be a nyelvet** szeretne beállítani a OneNote jegyzetfüzetben lévő szövegrészekhez, az Aspose.Note for Java egyszerűvé teszi ezt. Ebben az útmutatóban megtanulja, hogyan hozzon létre egy OneNote dokumentumot, hogyan változtassa meg a szöveg nyelvét egyes szavak vagy kifejezések esetén, és végül hogyan mentse el a OneNote fájlt a megfelelő helyesírási nyelv alkalmazásával. A végére megérti, miért fontos a nyelv beállítása a helyesírás-ellenőrzés és a lokalizáció szempontjából, és egy azonnal futtatható kódmintát kap.

## Gyors válaszok
- **Mi befolyásol a “set language” beállítás?** A OneNote számára megadja, hogy melyik helyesírási szótárat használja a helyesírás- és nyelvtani ellenőrzéshez.  
- **Beállíthatok különböző nyelveket ugyanabban a jegyzetben?** Igen, minden szövegrészhez hozzárendelhet nyelvet.  
- **Szükségem van licencre az Aspose.Note-hoz?** Egy ingyenes próba a teszteléshez működik; a termeléshez kereskedelmi licenc szükséges.  
- **Mely Java verziók támogatottak?** Az Aspose.Note for Java a Java 8 és újabb verziókat támogatja.  
- **A kimenet .one fájl?** Igen, a dokumentum OneNote *.one* fájlként kerül mentésre.

## Előfeltételek
Az kódba merülés előtt győződjön meg róla, hogy a következőkkel rendelkezik:

1. **Java fejlesztői környezet** – JDK 8 vagy újabb telepítve és konfigurálva.  
2. **Aspose.Note for Java könyvtár** – Töltse le és telepítse a könyvtárat a [letöltési hivatkozás](https://releases.aspose.com/note/java/).  
3. **Dokumentum könyvtár** – Hozzon létre egy mappát a gépén, ahová a generált OneNote fájl mentésre kerül.

## Miért állítsuk be a nyelvet a szöveghez a OneNote-ban?
Az ellenőrző nyelv beállítása biztosítja, hogy a helyesírás-ellenőrzés, a nyelvtani javaslatok és a keresési indexelés helyesen működjön a többnyelvű tartalom esetén. Ez különösen hasznos a következő esetekben:

- **Globális csapatok**, amelyek egyetlen jegyzetfüzeten dolgoznak együtt.  
- **Lokalizált dokumentáció**, ahol minden szakasz más nyelven lehet.  
- **Adat‑vezérelt alkalmazások**, amelyek programozottan generálnak jegyzeteket a felhasználók világszerte.

## Csomagok importálása
Kezdje a szükséges Aspose.Note osztályok és Java segédeszközök importálásával.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## 1. lépés: Dokumentum és oldal beállítása
Hozzon létre egy új OneNote dokumentumot és egy oldalt, amely a tartalmát fogja tartalmazni. Ez a lépés bemutatja a **create OneNote document** funkciót.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## 2. lépés: Vázlat és vázlat elem létrehozása
A vázlat a jegyzetfüzet tartalmának tárolója. Itt építjük fel azt a struktúrát, amely később a nyelvspecifikus szöveget fogja tartalmazni.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## 3. lépés: Rich Text hozzáadása nyelvi beállításokkal
Most **change text language** módon egy `TextStyle`-t egy adott `Locale`-lel csatolunk minden szövegrészhez. Ez bemutatja a **set language for text** funkciót.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## 4. lépés: Elemek szervezése és mentés
Állítsa össze a vázlat hierarchiáját, csatolja az oldalhoz, és végül **save OneNote file** a nyelvi beállításokkal.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Gyakori hibák és tippek
- **Locale formátum** – Használja az IETF BCP‑47 címkét (pl. `en-US`, `de-DE`). Egy helytelen címke a dokumentum nyelvéhez fog visszaállni.  
- **Fájl útvonal** – Győződjön meg róla, hogy a `dataDir` egy létező mappára mutat; ellenkező esetben a `document.save` `IOException`-t dob.  
- **Pro tipp:** Ha egy egész bekezdés nyelvét szeretné beállítani, alkalmazza a `TextStyle`-t a `ParagraphStyle`-ra az egyes `append` hívások helyett.

## Következtetés
Most megtanulta, hogyan **how to set language** egyes szövegrészekhez egy OneNote jegyzetfüzetben az Aspose.Note for Java használatával. Ez a lehetőség lehetővé teszi, hogy programozottan **create OneNote document**, **change text language** valós időben, és **save OneNote file** pontos helyesírási metaadatokkal.

## Gyakran ismételt kérdések

**Q: Beállíthatok helyesírási nyelvet más nyelvekre, amelyek nincsenek a példában?**  
A: Természetesen! Adjunk hozzá további `append` hívásokat a kívánt `Locale.forLanguageTag("xx-XX")` használatával.

**Q: Az Aspose.Note for Java kompatibilis a legújabb Java verziókkal?**  
A: Igen, a könyvtár rendszeresen frissül, hogy támogassa a legújabb Java kiadásokat.

**Q: Hogyan kezeljem a hibákat a nyelv‑beállítási folyamat során?**  
A: A mentési műveletet helyezze `try‑catch` blokkba, hogy elkapja az `IOException` vagy `AsposeException` kivételeket.

**Q: Integrálhatom ezt a kódot egy webalkalmazásba?**  
A: Természetesen. Csak helyezze az Aspose.Note JAR-t a webprojekt osztályútvonalába, és győződjön meg róla, hogy a szervernek írási joga van a célkönyvtárhoz.

**Q: Hol találok további példákat és dokumentációt az Aspose.Note for Java-hoz?**  
A: Tekintse meg a [dokumentációt](https://reference.aspose.com/note/java/) a teljes API és minta projektek listájáért.

---

**Legutóbb frissítve:** 2026-03-29  
**Tesztelve:** Aspose.Note for Java 24.12  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}