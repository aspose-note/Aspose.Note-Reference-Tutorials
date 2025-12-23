---
date: 2025-12-23
description: Ismerje meg, hogyan adhat hozzá alternatív szöveget a OneNote dokumentumok
  képeihez Java és az Aspose.Note segítségével. Ez az útmutató bemutatja, hogyan adjon
  alternatív szöveget a képekhez a jobb hozzáférhetőség érdekében.
linktitle: How to Add Alt Text to Image in OneNote using Java
second_title: Aspose.Note Java API
title: Hogyan adjunk alternatív szöveget a képhez a OneNote-ban Java használatával
url: /hu/java/onenote-image-alternative-text/add-alternative-text-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan adjunk alt szöveget a képekhez a OneNote-ban Java használatával

## Bevezetés

Ebben az útmutatóban megtanulja, **hogyan adjon hozzá alt** szöveget a képekhez a OneNote dokumentumokban Java és az Aspose.Note API használatával. Az alternatív szöveg (alt text) hozzáadása javítja a képernyőolvasó felhasználók hozzáférhetőségét és növeli a tartalom általános inkluzivitását. A útmutató végére képes lesz Java-ban beállítani a kép alt szövegét, így a OneNote fájljai jobban megfelelnek a hozzáférhetőségi szabványoknak.

## Gyors válaszok
- **Melyik könyvtár szükséges?** Aspose.Note for Java  
- **Melyik elsődleges kulcsszóra céloz ez az útmutató?** how to add alt  
- **Szükségem van licencre a termeléshez?** Igen, kereskedelmi licenc szükséges (ingyenes próba elérhető).  
- **Hozzáadhatok alt szöveget több képhez?** Természetesen – csak ismételje meg a lépéseket minden egyes képnél.  
- **Melyik Java verzió támogatott?** Java 8 vagy újabb.

## Mi a “how to add alt” a OneNote kontextusában?

Az alt szöveg hozzáadása azt jelenti, hogy egy szöveges leírást biztosítunk a képhez, amelyet a segítő technológiák olvashatnak. Ez a leírás segíti a képet nem látható felhasználókat a kép céljának megértésében.

## Miért adjunk alt szöveget a képekhez a OneNote-ban?

- **Hozzáférhetőség:** Megfelel a WCAG irányelveknek és javítja a látássérült felhasználók élményét.  
- **Kereshetőség:** A keresőmotorok indexelhetik a leírást, így a tartalma könnyebben megtalálható.  
- **Professzionalizmus:** Mutatja az inkluzív tervezés iránti elkötelezettséget.

## Előfeltételek

Mielőtt belemerülne az útmutatóba, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

1. Java Development Kit (JDK) – 8 vagy újabb verzió.  
2. Aspose.Note for Java könyvtár – töltse le innen: [here](https://releases.aspose.com/note/java/).  
3. Egy IDE, például IntelliJ IDEA vagy Eclipse.  
4. Alapvető Java programozási ismeretek.

## Csomagok importálása

Először importálja a szükséges csomagokat a Java projektjébe az Aspose.Note funkciók használatához.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;
```

Most bontsuk le a **alternatív szöveg kép** hozzáadásának folyamatát egy OneNote dokumentumhoz Java és Aspose.Note használatával lépésről lépésre.

## Hogyan adjunk alt szöveget a képekhez a OneNote-ban Java használatával

### 1. lépés: Dokumentum könyvtár beállítása

```java
String dataDir = "Your Document Directory";
```

Cserélje le a `"Your Document Directory"` értéket a mappára, amely tartalmazza a forrásképet, és ahová a kimeneti fájlt menteni szeretné.

### 2. lépés: Dokumentum objektum létrehozása

```java
Document document = new Document();
```

Ez létrehoz egy új, üres OneNote dokumentumot.

### 3. lépés: Oldal objektum létrehozása

```java
Page page = new Page();
```

Az oldal fogja tartalmazni a hozzáadni kívánt képet.

### 4. lépés: Kép hozzáadása az oldalhoz

```java
Image image = new Image(null, dataDir + "image.jpg");
```

Az `Image` konstruktor betölti a képfájlt a megadott útvonalról.

### 5. lépés: Alternatív szöveg címének beállítása

```java
image.setAlternativeTextTitle("ImageAlternativeText Title");
```

Itt **alt szöveget adunk hozzá**, amely a kép rövid címeként szolgál.

### 6. lépés: Alternatív szöveg leírásának beállítása

```java
image.setAlternativeTextDescription("ImageAlternativeText Description");
```

Ez a leírás részletesebb magyarázatot ad – tökéletes a képernyőolvasók számára.

### 7. lépés: Kép hozzáfűzése az oldalhoz

```java
page.appendChildLast(image);
```

A kép (most alt szöveggel gazdagítva) hozzáadódik az oldalhoz.

### 8. lépés: Oldal hozzáfűzése a dokumentumhoz

```java
document.appendChildLast(page);
```

Csatolja az oldalt a OneNote dokumentumhoz.

### 9. lépés: Dokumentum mentése

```java
document.save(dataDir + "AlternativeText_out.one");
```

A dokumentum mentésre kerül, az alternatív szöveg a képen beágyazva.

## Gyakori problémák és megoldások

- **FileNotFoundException:** Ellenőrizze, hogy a `dataDir` a megfelelő mappára mutat, és hogy a `image.jpg` létezik.  
- **NullPointerException a képnél:** Győződjön meg arról, hogy a kép útvonala érvényes, és a fájl nem sérült.  
- **Licenc hibák:** Használjon érvényes Aspose.Note licencfájlt, vagy futtassa próbaverzióban az értékeléshez.

## Gyakran ismételt kérdések

**Q: Hozzáadhatok alt szöveget több képhez egyetlen dokumentumban?**  
A: Igen, egyszerűen ismételje meg a 4‑6. lépéseket minden egyes annotálni kívánt képhez.

**Q: Mely képformátumok támogatottak az alt szöveg hozzáadásához?**  
A: Az Aspose.Note támogatja a JPEG, PNG, GIF, BMP és több más gyakori formátumot.

**Q: Lehet módosítani vagy eltávolítani az alt szöveget, miután be lett állítva?**  
A: Természetesen. Hívja a `setAlternativeTextTitle("")` vagy `setAlternativeTextDescription("")` metódust az értékek törléséhez, vagy adjon meg új karakterláncokat a frissítéshez.

**Q: Az Aspose.Note kínál API-kat más nyelvekhez is a Java mellett?**  
A: Igen, a könyvtár elérhető .NET, C++ és Python számára is.

**Q: Hol tölthetem le az Aspose.Note próba verzióját?**  
A: Ingyenes próbaverziót szerezhet itt: [here](https://releases.aspose.com/).

## Összegzés

A lépésről‑lépésre útmutató követésével most már tudja, **hogyan adjon alt** szöveget a képekhez a OneNote-ban Java használatával. Az `add alternative text image` megvalósítása nem csak a dokumentumait hozzáférhetőbbé teszi, hanem javítja azok kereshetőségét és általános minőségét is. Nyugodtan kísérletezzen különböző címekkel és leírásokkal, hogy a legjobban közvetítse minden kép jelentését.

---

**Utolsó frissítés:** 2025-12-23  
**Tesztelve:** Aspose.Note for Java 24.11  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}