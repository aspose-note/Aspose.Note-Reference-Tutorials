---
date: 2025-12-17
description: Ismerje meg, hogyan exportálhatja a OneNote-ot úgy, hogy egy dokumentumot
  szürkeárnyalatos PNG képként ment el az Aspose.Note for Java segítségével. Tartalmazza
  a OneNote dokumentum betöltésének és a szürkeárnyalatos kép létrehozásának lépéseit.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: Hogyan exportáljuk a OneNote-ot szürkeárnyalatos képként – Aspose.Note
url: /hu/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mentés szürkeárnyalatos képként a OneNote-ban - Aspose.Note

## Bevezetés

Ebben az útmutatóban megmutatjuk, hogyan **exportáljuk a onenote-ot** úgy, hogy egy dokumentumot szürkeárnyalatos képként mentünk az Aspose.Note for Java segítségével. A szürkeárnyalatos képek monokróm képek, amelyek csak szürke árnyalatokat tartalmaznak, ami nyomtatás, archiválás vagy a fájlméret csökkentése esetén hasznos lehet. Lépésről lépésre bemutatjuk a OneNote dokumentum betöltését, a mentési beállítások konfigurálását a **szürkeárnyalatos kép létrehozásához**, és végül a **dokumentum PNG-ként mentését**.

## Gyors válaszok
- **Mi jelentése a “how to export onenote” kifejezésnek?** Ez azt jelenti, hogy egy OneNote fájlt programozott módon egy másik formátumba, például képre konvertálunk.  
- **Melyik formátum a legjobb a szürkeárnyalatos kimenethez?** A PNG jól működik, mivel veszteségmentes minőséget megőriz és támogatja a szürkeárnyalatos színmódot.  
- **Szükségem van licencre?** Érvényes Aspose.Note licenc szükséges a termelési használathoz; teszteléshez ideiglenes próbaverzió licenc elérhető.  
- **Milyen Java verzió szükséges?** Java 8 vagy újabb ajánlott.  
- **Módosíthatom a kép méretét?** Igen, a mentés előtt módosíthatja az `ImageSaveOptions` tulajdonságait, például a `Resolution` vagy `PageSize` értékét.

## Mi a “how to export onenote”?
A OneNote exportálása azt jelenti, hogy programozott módon egy OneNote `.one` fájlt egy másik ábrázolásba konvertálunk – például PDF, HTML vagy kép formátumba. Ebben az útmutatóban a **szürkeárnyalatos PNG** képre való exportálásra összpontosítunk, ami gyakori igény a dokumentációs vagy nyomtatási munkafolyamatokban.

## Miért exportáljuk a OneNote-ot szürkeárnyalatos képként?
- **Csökkentett fájlméret** – A szürkeárnyalatos PNG-k általában kisebbek, mint a teljes színű képek.  
- **Jobb olvashatóság** – Nyomtatott jelentések esetén a szürkeárnyalat gyakran tisztább kontrasztot biztosít.  
- **Kompatibilitás** – A PNG széles körben támogatott böngészőkben, szerkesztőkben és mobil eszközökön.  

## Előfeltételek

Mielőtt elkezdenénk, győződjön meg, hogy a következőkkel rendelkezik:

1. Java Development Kit (JDK) telepítve van a rendszerén.  
2. Aspose.Note for Java könyvtár. Letöltheti [innen](https://releases.aspose.com/note/java/).  
3. Alapvető Java programozási ismeretek.  

## Csomagok importálása

A kezdéshez importálja a szükséges csomagokat:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 1. lépés: OneNote dokumentum betöltése

Először **töltse be a onenote dokumentumot** az Aspose.Note-ba. Cserélje le a `"Your Document Directory"`-t a helyi mappája elérési útjára, és a `"Aspose.one"`-t a OneNote fájl nevére.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 2. lépés: Kimeneti útvonal és beállítások megadása

Adja meg a szürkeárnyalatos kép kimeneti útvonalát, és állítsa be a mentési opciókat. A `ColorMode`-t `GrayScale`-re állítjuk, és a **save document as png** formátumot használjuk.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## 3. lépés: Dokumentum mentése

Végül mentse a dokumentumot szürkeárnyalatos PNG képként a konfigurált opciók segítségével.

```java
oneFile.save(dataDir, options);
```

## Gyakori problémák és megoldások
- **FileNotFoundException** – Ellenőrizze, hogy a `dataDir` a megfelelő mappára mutat-e, és hogy a `.one` fájl létezik-e.  
- **LicenseException** – Győződjön meg róla, hogy a `save` hívása előtt érvényes Aspose.Note licencet alkalmazott.  
- **Alacsony felbontású kimenet** – Szükség esetén állítsa be a `options.setResolution(300)`-t a DPI növeléséhez.  

## Gyakran Ismételt Kérdések

**Q1: Menthetem a szürkeárnyalatos képet más formátumban?**  
A1: Igen, egyszerűen módosítsa a `SaveFormat` paramétert az `ImageSaveOptions` konstruktorában `Jpeg`, `Bmp` stb. értékre.

**Q2: Az Aspose.Note kompatibilis minden OneNote dokumentumverzióval?**  
A2: Az Aspose.Note támogatja a Microsoft OneNote 2010 és újabb verzióit.

**Q3: Az Aspose.Note használatához szükséges licenc?**  
A3: Érvényes licenc szükséges a termelési használathoz, de értékeléshez ideiglenes próbaverzió licenc is beszerezhető.

**Q4: Módosíthatok más dokumentumrészeket a kép mentése előtt?**  
A4: Természetesen! Az Aspose.Note átfogó API-t biztosít a szakaszok, oldalak és tartalom szerkesztéséhez exportálás előtt.

**Q5: Hol találok támogatást, ha problémáim vannak?**  
A5: Támogatást az Aspose.Note fórumon talál [itt](https://forum.aspose.com/c/note/28).

## Összegzés

Most már megtanulta, hogyan **exportálja a onenote-ot** egy OneNote fájl betöltésével, a mentési beállítások konfigurálásával a **szürkeárnyalatos kép létrehozásához**, és a **dokumentum PNG-ként mentésével**. Ez a technika hasznos könnyű, nyomtatásra kész vizuális anyagok előállításához a OneNote jegyzetfüzetekből. Nyugodtan kísérletezzen más `ColorMode` beállításokkal vagy képformátumokkal, hogy megfeleljenek projektje igényeinek.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Utolsó frissítés:** 2025-12-17  
**Tesztelve:** Aspose.Note 24.12 for Java  
**Szerző:** Aspose