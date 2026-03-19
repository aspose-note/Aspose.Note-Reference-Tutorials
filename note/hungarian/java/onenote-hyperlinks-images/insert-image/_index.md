---
date: 2026-03-19
description: Tanulja meg, hogyan adhat hozzá képet a OneNote-hoz Java-val az Aspose.Note
  for Java segítségével, beleértve, hogyan állíthatja be a kép méreteit Java-ban,
  és hogyan mentheti a OneNote-ot PDF formátumban.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Kép hozzáadása a OneNote-hoz Java-val
url: /hu/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kép beszúrása OneNote dokumentumba Java-val

## Bevezetés

Ebben az útmutatóban megtanulja, **hogyan adjunk hozzá képet a OneNote-hoz** programozott módon Java és az Aspose.Note for Java könyvtár segítségével. Képek beágyazása a OneNote oldalakba hasznos, ha értekezési jegyzőkönyveket, automatizált jelentéseket vagy olyan dokumentációt kell létrehozni, amely szöveget kombinál vizuális adatokkal. A leírás végére képes lesz meglévő OneNote fájlt betölteni, képet beszúrni, opcionálisan méretét és pozícióját beállítani, és akár **OneNote mentése PDF‑ként** – mindezt a OneNote felhasználói felületének megnyitása nélkül.

## Gyors válaszok
- **Mi a legegyszerűbb módja a kép hozzáadásának a OneNote-hoz Java-val?**  
  Használja az Aspose.Note for Java `Image` osztályát, és fűzze hozzá egy oldalhoz.
- **Szükségem van licencre a termelésben való használathoz?**  
  Igen, kereskedelmi licenc szükséges a termelési környezetben való telepítéshez.
- **Beállíthatok egyedi méreteket a képre?**  
  Természetesen – hívja meg a `setWidth()` és `setHeight()` metódusokat az `Image` objektumon.
- **Lehetséges a OneNote fájl mentése PDF‑ként a kép hozzáadása után?**  
  Igen, hívja meg a `save(..., SaveFormat.Pdf)` metódust a **OneNote mentéséhez PDF‑ként**.
- **Melyik Java verzió támogatott?**  
  Az Aspose.Note for Java a JDK 8‑as és újabb verziókkal működik.

## Miért adjunk képet a OneNote-hoz?

A vizuális elemek hozzáadása érthetőbbé és vonzóbbá teszi a jegyzeteket. A képek ábrákat, képernyőképeket vagy adatgrafikonokat illusztrálhatnak, amelyek egyébként hosszú szöveges leírásokat igényelnének. Ennek a lépésnek az automatizálása időt takarít meg, különösen nagy mennyiségű jegyzet adatforrásokból történő generálásakor.

## Előkövetelmények

Mielőtt elkezdenénk, győződjön meg róla, hogy az alábbiak rendelkezésre állnak:

### 1. Java fejlesztői csomag (JDK)
Telepítse a JDK 8‑at vagy újabbat. Letöltheti az Oracle weboldaláról, vagy használhat egy OpenJDK disztribúciót.

### 2. Aspose.Note for Java könyvtár
Töltse le a legújabb Aspose.Note for Java könyvtárat, és adja hozzá a projekt osztályútvonalához. A részletes beállítási útmutató elérhető a hivatalos [documentation](https://reference.aspose.com/note/java/) oldalon.

## Importálás csomagok

Kezdje a szükséges osztályok importálásával. Ezek az importok hozzáférést biztosítanak az Aspose.Note alapfunkcióihoz, valamint az alapvető Java segédprogramokhoz.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Lépésről‑lépésre útmutató

Az alábbiakban egy tömör, számozott áttekintést talál. Minden lépés rövid magyarázatot tartalmaz, majd a pontos kódot, amelyet másolnia kell.

### 1. lépés: OneNote dokumentum betöltése

Létrehozunk egy `LoadOptions` példányt (hasznos a későbbi testreszabásokhoz), és megnyitjuk a meglévő `.one` fájlt.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

### 2. lépés: Céloldal lekérése

Egyszerűség kedvéért az első oldallal dolgozunk a dokumentumban, de bármelyik szükséges oldalra navigálhat.

```java
Page page = oneFile.getFirstChild();
```

### 3. lépés: A beágyazni kívánt kép betöltése

Példányosítunk egy `Image` objektumot a dokumentum hivatkozásával és a kép fájl elérési útjával.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

### 4. lépés: Kép méretek beállítása Java (opcionális)

Ha a képet egy meghatározott területhez szeretné igazítani, állítsa be a szélességet, magasságot és az eltolásokat. Itt jön képbe a másodlagos kulcsszó **set image dimensions java**.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

### 5. lépés: Kép hozzáfűzése az oldalhoz

Az `appendChildLast` metódus a képet az adott oldal utolsó elemként adja hozzá.

```java
page.appendChildLast(image);
```

### 6. lépés: Dokumentum mentése – mentheted a OneNote-ot PDF‑ként is

Végül mentse el a módosításokat. A példa bemutatja, hogyan mentse a fájlt PDF‑ként, ezzel teljesítve a másodlagos kulcsszót **save onenote as pdf**.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Általános problémák és megoldások

| Tünet | Valószínű ok | Megoldás |
|---------|--------------|-----|
| `FileNotFoundException` a kép betöltésekor | Helytelen képútvonal | Ellenőrizze, hogy a `dataDir` és a kép fájlneve helyes-e. |
| A kép torzul | Szélesség/magasság helytelen beállítása | Használja az eredeti kép méreteit, vagy számoljon ki megfelelő képarányt a `setWidth`/`setHeight` hívása előtt. |
| PDF kimenet üres | Hiányzó licenc az Aspose.Note-hoz | Alkalmazzon érvényes licencet a `save` hívása előtt. |

## Gyakran Ismételt Kérdések

### Q1: Beszúrhatok több képet egyetlen OneNote dokumentumba ezzel a módszerrel?

**A:** Igen. Egyszerűen ismételje meg a 3‑5‑ös lépéseket minden egyes képhez, amelyet hozzá szeretne adni, akár ugyanarra, akár különböző oldalakra.

### Q2: Az Aspose.Note for Java kompatibilis-e az összes OneNote verzióval?

**A:** Az Aspose.Note for Java támogatja a Microsoft OneNote 2010‑el és újabb verziókkal létrehozott OneNote fájlokat.

### Q3: Beszúrhatok különböző formátumú képeket, például PNG‑t vagy GIF‑et egy OneNote dokumentumba?

**A:** Természetesen. A könyvtár támogatja a PNG, JPEG, GIF, BMP és több más elterjedt formátumot.

### Q4: Van elérhető próba verziója az Aspose.Note for Java‑nak tesztelési célokra?

**A:** Igen, letölthet egy ingyenes próbaverziót az Aspose weboldaláról, hogy kipróbálja az API‑t a vásárlás előtt.

### Q5: Hogyan kaphatok technikai támogatást az Aspose.Note for Java‑hoz?

**A:** Segítséget kaphat a [forum](https://forum.aspose.com/c/note/28) oldalán, amely az Aspose.Note termékeknek van dedikálva.

## Összegzés

Most már rendelkezik egy teljes, termelés‑kész példával, amely megmutatja, **hogyan adjunk hozzá képet a OneNote-hoz** Java használatával, testre szabhatja a megjelenését, és opcionálisan **OneNote mentése PDF‑ként**. Nyugodtan alakítsa át a kódot saját munkafolyamataihoz – legyen szó jelentéskészítő motorról, automatizált dokumentációs rendszerről vagy egyedi jegyzetkészítő alkalmazásról.

---

**Utolsó frissítés:** 2026-03-19  
**Tesztelve:** Aspose.Note for Java 24.10  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}