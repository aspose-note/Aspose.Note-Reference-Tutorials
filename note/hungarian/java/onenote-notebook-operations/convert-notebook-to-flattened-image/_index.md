---
date: 2026-03-21
description: Ismerje meg, hogyan laposíthatja a jegyzetfüzetet az OneNote PNG formátumba
  konvertálásával az Aspose.Note for Java segítségével. Ez az útmutató bemutatja a
  képfelbontás beállítását, az OneNote képként mentését, valamint a jegyzetfüzetek
  hatékony laposítását.
linktitle: How to Flatten Notebook – Convert OneNote to PNG
second_title: Aspose.Note Java API
title: Hogyan laposítsuk a jegyzetfüzetet – OneNote konvertálása PNG-re
url: /hu/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan laposítsuk a jegyzetfüzetet – OneNote átalakítása PNG formátumba

## Bevezetés

Ebben az útmutatóban megtudja, **hogyan laposítsa a jegyzetfüzet** tartalmát úgy, hogy egy OneNote jegyzetfüzetet magas minőségű PNG képpé konvertál az Aspose.Note for Java segítségével. Akár egy jegyzetfüzet pillanatképét szeretné beágyazni egy jelentésbe, megosztani egy csak‑olvasásra szánt nézetet kollégáival, vagy egy megfelelőségi képet archiválni, ez a lépésről‑lépésre útmutató pontosan megmutatja, hogyan mentse a OneNote‑ot képként a felbontás szabályozásával.

## Gyors válaszok
- **Mit jelent a „laposítás” (flatten notebook)?** Összevonja az összes oldal elemet egy raszteres képpé.  
- **Melyik formátumot használja?** Alapértelmezett a PNG, amely veszteségmentes minőséget biztosít.  
- **Módosíthatom a DPI‑t?** Igen, használja a `setResolution` metódust az `ImageSaveOptions`‑on.  
- **Szükség van licencre?** Egy ingyenes próba verzió elegendő értékeléshez; a kereskedelmi licenc szükséges a termeléshez.  
- **Minden operációs rendszeren támogatott?** A Java API bárhol fut, ahol a Java elérhető.

## Mi az a OneNote átalakítása PNG‑re?

A OneNote‑t PNG‑re konvertálni azt jelenti, hogy a jegyzetfüzet minden oldaláról egy bitmap ábrát hozunk létre, amely megőrzi a szöveget, a rajzokat és a beágyazott objektumokat egyetlen képfájlban. Ez különösen hasznos dokumentációhoz, prezentációkhoz vagy megfelelőségi archiváláshoz.

## Miért konvertáljuk a OneNote‑ot PNG‑re az Aspose.Note‑tal?

- **Teljes hűség** – Minden vizuális elem megmarad.  
- **Egyetlen fájl kimenet** – Nem kell több oldal fájlt kezelni.  
- **Testreszabható felbontás** – Állítsa be a DPI‑t a minőségi követelményeknek megfelelően.  
- **Nincs Office telepítés szükséges** – Teljesen független a Microsoft OneNote‑tól.

## Előfeltételek

Mielőtt elkezdenénk, győződjön meg róla, hogy a következők rendelkezésre állnak:

1. Java Development Kit (JDK) telepítve van a rendszerén.  
2. Aspose.Note for Java könyvtár letöltve és beállítva a Java projektjében. A könyvtárat letöltheti [innen](https://releases.aspose.com/note/java/).  
3. Alapvető Java programozási ismeretek.

## Csomagok importálása

A kezdéshez importálja a szükséges csomagokat az Aspose.Note for Java‑ból:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Lépés‑ről‑lépésre útmutató

### 1. lépés: Dokumentum könyvtár beállítása

Először határozza meg azt a könyvtárat, ahol a jegyzetfüzet fájlja található:

```java
String dataDir = "Your Document Directory";
```

Cserélje le a `"Your Document Directory"`‑t a jegyzetfüzet fájl elérési útjára.

### 2. lépés: Jegyzetfüzet betöltése

Ezután töltse be a jegyzetfüzet fájlt a `Notebook` osztály segítségével:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Cserélje le a `"test.onetoc2"`‑t a saját jegyzetfüzet fájl nevére.

### 3. lépés: Kép mentési beállítások (set image resolution java)

Most állítsa be a jegyzetfüzet képként való mentésének opcióit. A mentési formátumot PNG‑re állítjuk, és a felbontást 400 DPI‑re:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

A felbontást igényei szerint módosíthatja. Itt **állítja be a kép felbontását**, hogy szabályozza a kimeneti minőséget.

### 4. lépés: Jegyzetfüzet laposítása (how to flatten notebook)

Annak biztosítására, hogy minden elem egyetlen képpé laposodik, állítsa a `flatten` opciót `true`‑ra:

```java
saveOptions.setFlatten(true);
```

A `flatten` `true`‑ra állítása garantálja, hogy a létrehozott PNG pontosan a jegyzetfüzet elrendezését tükrözi.

### 5. lépés: Kép mentése (save onenote as image)

Végül mentse a jegyzetfüzetet egy laposított képként:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Cserélje le a `"ExportImageasFlattenedNotebook_out.png"`‑t a kívánt kimeneti fájlnévre. Ez a lépés **menti a OneNote‑ot képként**, amelyet bárhol megoszthat vagy beágyazhat.

## Gyakori felhasználási esetek

- **Dokumentáció:** A jegyzetfüzet képet beágyazhatja műszaki kézikönyvekbe vagy felhasználói útmutatókba.  
- **Prezentációk:** Használjon magas felbontású PNG diát a PowerPoint‑ban anélkül, hogy a betűtípus vagy az objektumok kompatibilitásától aggódna.  
- **Archiválás:** Tároljon egy csak‑olvasásra szánt pillanatképet a jegyzetfüzetről megfelelőségi auditokhoz.

## Hibaelhárítási tippek

- **Fájl nem található:** Ellenőrizze a `dataDir` útvonalat, és győződjön meg róla, hogy a `.onetoc2` fájl létezik.  
- **Alacsony minőségű kép:** Növelje a DPI‑t a `documentSaveOptions.setResolution(600);` módosításával.  
- **Hiányzó elemek:** Győződjön meg róla, hogy a `saveOptions.setFlatten(true);` engedélyezve van; ellenkező esetben egyes rétegek külön maradhatnak.

## Gyakran ismételt kérdések

**Q1: Módosíthatom a kimeneti kép felbontását?**  
A1: Igen, a `setResolution` metódus paraméterének módosításával a saját igényei szerint állíthatja be a felbontást.

**Q2: Az Aspose.Note támogat más képformátumokat az exportáláshoz?**  
A2: Igen, az Aspose.Note különféle képformátumokat támogat, például PNG, JPEG, BMP stb., a jegyzetfüzetek exportálásához.

**Q3: További testreszabásra van lehetőség a kimeneti képnél?**  
A3: Igen, az Aspose.Note kiterjedt lehetőségeket kínál a kimeneti kép testreszabására, beleértve az oldalméretet, orientációt és minőségi beállításokat.

**Q4: Elérhető próba verzió az Aspose.Note for Java‑hoz?**  
A4: Igen, ingyenes próba verziót szerezhet [innen](https://releases.aspose.com/).

**Q5: Hol találok támogatást az Aspose.Note for Java‑hoz?**  
A5: Támogatást és erőforrásokat az Aspose.Note fórumon talál [itt](https://forum.aspose.com/c/note/28).

---

**Utoljára frissítve:** 2026-03-21  
**Tesztelt verzió:** Aspose.Note for Java 24.12  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}