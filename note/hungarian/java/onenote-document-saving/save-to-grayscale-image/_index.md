---
date: 2026-06-30
description: Ismerje meg, hogyan exportálhatja a OneNote-ot egy dokumentum szürkeárnyalatos
  PNG képként való mentésével az Aspose.Note for Java segítségével. Tartalmazza a
  OneNote dokumentum betöltésének és a szürkeárnyalatos kép létrehozásának lépéseit.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Hogyan exportáljuk a OneNote-ot szürkeárnyalatos képként – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: Hogyan exportáljuk a OneNote-ot szürkeárnyalatos képként – Aspose.Note
url: /hu/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mentés szürkeárnyalatos képként a OneNote-ban – Aspose.Note

## Bevezetés

Ezen az útmutatón keresztül megtudja, **hogyan exportálja a onenote-ot**, egy OneNote `.one` fájl magas minőségű szürkeárnyalatos PNG képpé konvertálásával az Aspose.Note for Java segítségével. A szürkeárnyalatos konverzióra a Java fejlesztők gyakran szükségük van nyomtatáshoz, archiváláshoz, vagy a **OneNote méretének csökkentéséhez** anélkül, hogy a lényeges tartalom elveszne. Lépésről lépésre végigvezetjük a OneNote dokumentum betöltésén, a mentési beállítások konfigurálásán – beleértve a **kép felbontásának beállítását** – és végül a dokumentum PNG formátumban történő mentésén.

## Gyors válaszok
- **Mi jelent a “how to export onenote”?** Ez a OneNote fájl programozott módon történő átalakítását jelenti egy másik formátumba, például képpé, kód használatával.  
- **Melyik formátum a legjobb a szürkeárnyalatos kimenethez?** A PNG jól működik, mivel megőrzi a veszteségmentes minőséget, és támogatja a dedikált szürkeárnyalatos színmódot.  
- **Szükségem van licencre?** Érvényes Aspose.Note licenc szükséges a termelési használathoz; ideiglenes próbaverzió licenc elérhető teszteléshez.  
- **Milyen Java verzió szükséges?** Java 8 vagy újabb ajánlott.  
- **Módosíthatom a kép méretét?** Igen, a `ImageSaveOptions` tulajdonságait, például a `Resolution` vagy `PageSize` értékét a mentés előtt módosíthatja.  

## Mi az a “how to export onenote”?

A OneNote exportálása azt jelenti, hogy programozott módon egy OneNote `.one` fájlt egy másik ábrázolásba konvertálunk – például PDF, HTML vagy kép formátumba. Ebben az útmutatóban a **szürkeárnyalatos PNG** képek létrehozására összpontosítunk, ami gyakori igény a dokumentáció vagy a nyomtatásra kész munkafolyamatok esetén. Az Aspose.Note használatával a konverzió teljesen memóriában történik, így a Microsoft OneNote telepítése a szerveren soha nem szükséges.

## Miért exportáljuk a OneNote-ot szürkeárnyalatos képként?

A szürkeárnyalatos PNG-k általában **30‑40 %-kal kisebbek**, mint a teljes színű változatok, ami felgyorsítja a webes kiszolgálást és csökkenti a tárolási költségeket. Emellett **élesebb kontrasztot** biztosítanak a lézernyomtatókon, így a jelentések könnyebben olvashatók. Mivel a PNG univerzálisan támogatott, a keletkezett fájlok böngészőkön, mobil eszközökön és asztali szerkesztőkön is működnek további kodekek nélkül.

## Előfeltételek

1. Java Development Kit (JDK) 8 vagy újabb telepítve.  
2. Aspose.Note for Java könyvtár – töltse le a legújabb kiadást [innen](https://releases.aspose.com/note/java/).  
3. Alapvető Java szintaxis ismeret és Maven/Gradle projekt beállítás.  

## Csomagok importálása

A `ImageSaveOptions` osztály szabályozza, hogyan renderelődik a dokumentum képpé.  
A `ColorMode` egy felsorolt típus, amely lehetővé teszi a teljes szín és a szürkeárnyalatos kimenet közötti váltást.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 1. lépés: OneNote dokumentum betöltése

A `Document` egy OneNote jegyzetfüzetet képvisel, és módszereket biztosít a tartalom betöltésére, szerkesztésére és mentésére. Először **töltse be a OneNote dokumentumot** az Aspose.Note-ba. Cserélje le a `"Your Document Directory"`-t a helyi mappája elérési útjára, és a `"Aspose.one"`-t a OneNote fájl nevére.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 2. lépés: Kimeneti útvonal és beállítások megadása

A `ImageSaveOptions` beállítja, hogyan renderelődik egy OneNote dokumentum képfájlba. A `ColorMode` felsorolás választja ki a színrenderelési módot, például szürkeárnyalatos vagy teljes szín. Adja meg a szürkeárnyalatos kép kimeneti útvonalát, és határozza meg a mentési beállításokat. A `ColorMode`-ot `GrayScale`-re állítjuk, és a **dokumentum PNG formátumban történő mentését** használjuk. Emellett **beállíthatja a kép felbontását** 300 DPI-re a magas minőségű nyomtatáshoz.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## 3. lépés: Dokumentum mentése

Végül mentse a dokumentumot szürkeárnyalatos PNG képként a beállított opciók használatával. A `save` metódus a fájlt lemezre írja, köztes ideiglenes fájlok nélkül.

```java
oneFile.save(dataDir, options);
```

## Gyakori problémák és megoldások
- **FileNotFoundException** – Ellenőrizze, hogy a `dataDir` a megfelelő mappára mutat, és hogy a `.one` fájl létezik.  
- **LicenseException** – Győződjön meg róla, hogy a `save` hívása előtt érvényes Aspose.Note licencet alkalmazott.  
- **Alacsony felbontású kimenet** – Állítsa be a `options.setResolution(300)`-at a DPI növeléséhez; a magasabb DPI élesebb nyomatot eredményez, de nagyobb fájlméretet.  

## Gyakran feltett kérdések

**Q1: Menthetem a szürkeárnyalatos képet más formátumban?**  
A1: Igen, egyszerűen módosítsa a `SaveFormat` paramétert az `ImageSaveOptions` konstruktorában `Jpeg`, `Bmp` vagy a 20+ támogatott képformátum egyikére.

**Q2: Az Aspose.Note kompatibilis az összes OneNote dokumentumverzióval?**  
A2: Az Aspose.Note a Microsoft OneNote 2010 és újabb verzióit támogatja, ami a ma aktívan használt jegyzetfüzetek több mint 95 %-át lefedi.

**Q3: Az Aspose.Note használatához szükséges licenc?**  
A3: Érvényes licenc szükséges a termelési használathoz, de ideiglenes próbaverzió licenc szerezhető ingyenes értékeléshez.

**Q4: Módosíthatok más dokumentumrészeket a kép mentése előtt?**  
A4: Természetesen! Az Aspose.Note API-kat biztosít a szakaszok, oldalak és egyedi elemek, például szöveg, táblázatok és képek szerkesztéséhez exportálás előtt.

**Q5: Hol találok támogatást, ha problémáim vannak?**  
A5: Támogatást találhat az Aspose.Note fórumon [itt](https://forum.aspose.com/c/note/28).

## Összegzés

Most már megtanulta, **hogyan exportálja a onenote-ot** egy OneNote fájl betöltésével, a mentési beállítások **szürkeárnyalatos kép létrehozására** való konfigurálásával, és a **dokumentum PNG formátumban történő mentésével**. Ez a megközelítés ideális könnyű, nyomtatásra kész vizuálok előállításához OneNote jegyzetfüzetekből. Nyugodtan kísérletezzen más `ColorMode` beállításokkal, magasabb DPI értékekkel vagy alternatív képformátumokkal, hogy megfeleljen a projekt követelményeinek.

---

**Utolsó frissítés:** 2026-06-30  
**Tesztelt verzió:** Aspose.Note 27.0 for Java  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó útmutatók

- [OneNote oldal exportálása PNG képre Java-ban az Aspose.Note használatával](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote jpeg felbontás beállítása – Kimeneti kép felbontás beállítása OneNote-ban - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Hogyan mentse a OneNote-ot PDF-be az Aspose.Note for Java használatával](/note/java/onenote-document-loading/load-save-format/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}