---
date: 2025-12-13
description: Tanulja meg, hogyan állíthatja be a küszöbértéket a OneNote PNG formátumba
  konvertálásához az Aspose.Note Java segítségével, fekete‑fehér OneNote képek létrehozásához
  képbinarizációval Java‑ban.
linktitle: Save to Binary Image Using Fixed Threshold in OneNote
second_title: Aspose.Note Java API
title: Hogyan állítsuk be a küszöböt a OneNote bináris képként mentésekor
url: /hu/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan állítsuk be a küszöböt a OneNote bináris képként mentésekor

## Bevezetés

Ebben az útmutatóban megtanulja, **hogyan állítsa be a küszöböt** a Microsoft OneNote oldal exportálásához magas kontrasztú, fekete‑fehér PNG képként. A rögzített küszöbérték finomhangolásával pontos irányítást kap a konverzió felett, ami ideálissá teszi például OCR előfeldolgozáshoz vagy dokumentumarchiváláshoz. Lépésről lépésre végigvezetjük a folyamatot az Aspose.Note Java API használatával, így gyorsan **konvertálhat OneNote‑t PNG‑re** megbízható **image binarization Java** technikákkal.

## Gyors válaszok
- **Mit jelent a „küszöb beállítása”?** A pixelek intenzitásának határértékét állítja be, amikor egy színes képet fekete‑fehérre konvertál.
- **Milyen formátum jön létre?** Egy PNG fájl, amelyet bármely képnéző képes megnyitni.
- **Módosíthatom a küszöb Igen – változtassa meg a `setBinarizationThreshold()` hívást.
- **Szükség van licencre?** Fejlesztéshez egy ingyenes próbaverzió is működik; termeléshez kereskedelmi licenc szükséges.
- **Kompatibilis-e minden OneNote verzióval?** Az Aspose.Note támogatja a OneNote 2010, 2013, 2016 és újabb verzióit.

## Előfeltételek

Mielőtt elkezdené, győződjön meg róla, hogy rendelkezik:

1. Telepített Java Development Kit (JDK) környezettel.
2. Az Aspose.Note for Java könyvtárral, letöltve innen: [here](https://releases.aspose.com/note/java/).
3. Alapvető Java szintaxis ismeretekkel.

## Csomagok importálása

Először importálja a szükséges osztályokat a Java forrásfájlba.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## 1. lépés: Dokumentum betöltése

Töltse be azt a OneNote fájlt, amelyet feldolgozni szeretne.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 2. lépés: Binárizálási beállítások megadása

Határozza meg a **image binarization Java** beállításokat, és adja meg a kívánt rögzített küszöböt.

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

> **Pro tipp:** Kísérletezzen 0‑255 közötti küszöbértékekkel, hogy megtalálja a legjobb beállítást az adott dokumentumhoz. Az alacsonyabb értékek világosabb képet eredményeznek, a magasabbak sötétebb kimenetet adnak.

## 3. lépés: Kép mentési beállítások megadása

Állítsa be a kép formátumát, színmódját, és csatolja a binárizálási beállításokat.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

A `ColorMode.BlackAndWhite` beállítás biztosítja, hogy a végleges fájl egy **black and white OneNote** kép legyen.

## 4. lépés: Dokumentum mentése

Hajtsa végre a mentési műveletet a korábban definiált beállításokkal.

```java
oneFile.save(dataDir, options);
```

A kód futtatása után egy `SaveToBinaryImageUsingFixedThreshold_out.png` nevű PNG fájlt talál a kimeneti mappában, amely készen áll a további feldolgozásra vagy archiválásra.

## Összegzés

Bemutattuk, **hogyan állítsuk be a küszöböt**, hogy tiszta, magas kontrasztú PNG képet kapjunk egy OneNote fájlból az Aspose.Note for Java segítségével. A **image binarization Java** opciók elsajátításával megbízhatóan **konvertálhat OneNote‑t PNG‑re**, és **black and white OneNote** anyagokat hozhat létre OCR‑hez, nyomtatáshoz vagy digitális megőrzéshez.

## GYIK

### Q1: Módosíthatom a binárizálás küszöbértékét?

A1: Igen, a `setBinarizationThreshold()` metódus paraméterének módosításával a saját igényei szerint állíthatja be a küszöböt.

### Q2: Az Aspose.Note for Java kompatibilis-e a Microsoft OneNote minden verziójával?

A2: Az Aspose.Note for Java támogatja a Microsoft OneNote különböző verzióit, beleértve a 2010, 2013 és 2016 kiadásokat.

### Q3: Van korlátozás a feldolgozható dokumentumok méretére vonatkozóan?

A3: Az Aspose.Note for Java nem korlátozza a feldolgozható dokumentumok méretét, így nagy fájlokkal is hatékonyan dolgozhat.

### Q4: Több OneNote dokumentumot is konvertálhatok egyszerre?

A4: Igen, több OneNote dokumentumot is batch‑feldolgozhat úgy, hogy végigiterál minden fájlon és alkalmazza a szükséges műveleteket.

### Q5: Elérhető technikai támogatás az Aspose.Note for Java‑hoz?

A5: Igen, technikai támogatás érhető el a [Aspose.Note fórumon](https://forum.aspose.com/c/note/28), ahol kérdéseket tehet fel és segítséget kaphat a szakértőktől.

## Gyakran Ismételt Kérdések

**K: Mi történik, ha túl alacsonyra állítom a küszöböt?**  
V: A kép kifakultnak tűnhet, sok szürke árnyalat marad meg a tiszta fekete‑fehér kontraszt helyett.

**K: Használhatok más binárizálási módszert?**  
V: Igen, az Aspose.Note támogatja az adaptív küszöbölést is; egyszerűen cserélje le a `BinarizationMethod.FixedThreshold` értéket `BinarizationMethod.Adaptive`‑ra.

**K: Lehet közvetlenül más formátumba exportálni, például JPEG‑be?**  
V: Természetesen – a `ImageSaveOptions` konstruktorában cserélje a `SaveFormat.Png`‑t `SaveFormat.Jpeg`‑re.

**K: Hogyan kezeljem a jelszóval védett OneNote fájlokat?**  
V: Töltse be a dokumentumot a megfelelő overloaddal, amely elfogad egy jelszó‑stringet, mielőtt a binárizálási lépéseket alkalmazná.

**K: Működik ez a megoldás Linuxon/macOS‑en is?**  
V: Az Aspose.Note Java könyvtár platform‑független, így ugyanaz a kód bármely, kompatibilis JDK‑val rendelkező operációs rendszeren fut.

---

**Last Updated:** 2025-12-13  
**Tested With:** Aspose.Note for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}