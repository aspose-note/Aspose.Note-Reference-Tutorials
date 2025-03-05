---
title: Szöveg lektorálási nyelvének beállítása a OneNote-ban – Aspose.Note
linktitle: Szöveg lektorálási nyelvének beállítása a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Használja ki az Aspose.Note for Java-ban rejlő lehetőségeket! Lépésről lépésre szóló útmutatónkból megtudhatja, hogyan állíthat be zökkenőmentesen a szöveghez a OneNote-ban a korrektúra nyelvét.
type: docs
weight: 22
url: /hu/java/onenote-text-manipulation/set-proofing-language-for-text/
---
## Bevezetés
A szoftverfejlesztés dinamikus világában az Aspose.Note for Java a OneNote-dokumentumok programozott kezelésének és kezelésének hatékony eszközeként tűnik ki. Ha Java-alkalmazásait a OneNote-ban szöveglektorálási nyelv beállításával szeretné továbbfejleszteni, akkor jó helyen jár. Ez az oktatóanyag lépésről lépésre végigvezeti Önt a folyamaton, biztosítva, hogy világosan megértse az egyes fogalmakat.
## Előfeltételek
Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételeket teljesítette:
1. Java fejlesztői környezet: Győződjön meg arról, hogy be van állítva Java fejlesztői környezet a gépén.
2.  Aspose.Note for Java Library: Töltse le és telepítse az Aspose.Note for Java könyvtárat a[letöltési link](https://releases.aspose.com/note/java/).
3. Dokumentumkönyvtár: Hozzon létre egy könyvtárat a dokumentumok számára a kimeneti fájl tárolására.
## Csomagok importálása
Kezdje a szükséges csomagok importálásával a fejlesztési folyamat elindításához. Íme egy kódrészlet, amely segít az indulásban:
```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```
## 1. lépés: Állítsa be a dokumentumot és az oldalt
Hozzon létre egy új dokumentumot és oldalt a munkához. Ez szolgál majd a OneNote-manipuláció alapjául.
```java
// A dokumentumok könyvtárának elérési útja.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```
## 2. lépés: Hozzon létre Vázlat és Vázlat elemet
Készítsen vázlatot és vázlatelemet az oldalszerkezeten belül. Ez az a hely, ahol a lektorálási nyelvi beállításokkal rendelkező szöveg található.
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```
## 3. lépés: Rich Text hozzáadása a nyelvi beállításokkal
Integráljon formázott szöveget a vázlatelembe, és adja meg a lektorálási nyelvet minden szövegszegmenshez.
```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```
## 4. lépés: Az elemek rendszerezése és mentése
Állítsa össze a létrehozott elemeket, és mentse a dokumentumot a megadott könyvtárba.
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```
## Következtetés
Gratulálunk! Sikeresen beállította a szövegellenőrzési nyelvet a OneNote-ban az Aspose.Note for Java használatával. Ez az oktatóanyag olyan ismeretekkel és kódrészletekkel látta el, amelyekkel zökkenőmentesen javíthatja Java-alkalmazásait.
## GYIK
### K: Beállíthatok ellenőrző nyelvet más, a példában nem említett nyelvekhez?
 V: Abszolút! Módosítsa a kódot a kívánt nyelvi címkék hozzáadásával a`setLanguage` módszer.
### K: Az Aspose.Note for Java kompatibilis a legújabb Java-verziókkal?
V: Igen, az Aspose.Note for Java rendszeresen frissül, hogy biztosítsa a kompatibilitást a legújabb Java-kiadásokkal.
### K: Hogyan kezelhetem a hibákat a lektorálási nyelv beállítási folyamata során?
V: Valósítson meg hibakezelési mechanizmusokat try-catch blokkokkal az esetleges problémák megoldására.
### K: Integrálhatom ezt a kódot webes alkalmazásokba?
V: Természetesen! Győződjön meg arról, hogy az Aspose.Note for Java könyvtár megfelelően van konfigurálva a webprojektben.
### K: Hol találhatok további példákat és dokumentációt az Aspose.Note for Java-hoz?
 V: Fedezze fel a[dokumentáció](https://reference.aspose.com/note/java/) átfogó forrásokért.