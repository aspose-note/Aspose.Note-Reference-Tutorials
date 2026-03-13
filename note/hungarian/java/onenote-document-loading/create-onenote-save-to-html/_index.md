---
date: 2026-02-07
description: Ismerje meg, hogyan exportálhat betűtípusokat, miközben az OneNote-ot
  HTML-ként menti az Aspose.Note for Java használatával. Ez az útmutató bemutatja,
  hogyan hozhat létre OneNote-fájlt programozottan, és hogyan ágyazhat be betűtípusokat,
  CSS-t és képeket.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Hogyan exportáljunk betűtípusokat a OneNote HTML-be mentéskor – Java
url: /hu/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan exportáljunk betűtípusokat a OneNote HTML‑ként mentésekor – Java

## Bevezetés

Ebben az útmutatóban megtanulja, **hogyan exportálhat betűtípusokat**, amikor a **OneNote‑ot HTML‑ként menti** az Aspose.Note for Java segítségével. Lépésről‑lépésre bemutatjuk, hogyan hozhatunk létre egy OneNote‑dokumentumot programozottan, hogyan állíthatjuk be a HTML‑mentési opciókat, és hogyan ágyazhatjuk be a szükséges betűtípus‑fájlokat, hogy a kapott HTML pontosan úgy nézzen ki, mint az eredeti OneNote‑oldalak. Ez a megközelítés tökéletes, ha a OneNote‑tartalom vizuális hűségét web‑barát formátumban szeretné megőrizni.

## Gyors válaszok
- **Melyik könyvtár kezeli az exportot?** Aspose.Note for Java  
- **Be lehet ágyazni a betűtípusokat a HTML‑be?** Igen – állítsa be az `ExportFonts` értékét `ExportEmbedded`‑re  
- **Szükség van licencre a termeléshez?** Érvényes Aspose.Note licenc szükséges kereskedelmi használathoz  
- **Melyik Java verzió támogatott?** Java 8 vagy újabb  
- **Lehetséges a források külön fájlokba mentése?** Természetesen – állítsa be a `ResourceExportType`‑ot ennek megfelelően  

## Mi az a „betűtípusok exportálása” a OneNote HTML konverziójában?

Amikor egy OneNote‑jegyzetfüzetet HTML‑re konvertál, a vizuális megjelenés a CSS‑ből, képekből és különösen az eredeti oldalakban használt betűtípusokból áll. A **betűtípusok exportálása** azt jelenti, hogy a betűtípus‑fájlokat (pl. TTF) közvetlenül a HTML‑csomagba ágyazzuk, így a böngészők pontosan úgy tudják megjeleníteni a szöveget, ahogy az OneNote‑ban látható, még akkor is, ha a végfelhasználó gépén nincsenek telepítve ezek a betűtípusok.

## Miért hozunk létre OneNote‑t programozottan és mentjük HTML‑ként?

- **Automatizálás:** Jelentések, dokumentáció vagy tudásbázis‑cikkek generálása OneNote‑ból manuális másolás‑beillesztés nélkül.  
- **Következetesség:** Elrendezés, stílus és egyedi betűtípusok megőrzése különböző eszközökön.  
- **Átvitel:** A HTML univerzálisan megtekinthető – nincs szükség a OneNote kliensre.  

## Előfeltételek

1. Telepített Java Development Kit (JDK) 8 vagy újabb.  
2. Aspose.Note for Java könyvtár – letölthető [innen](https://releases.aspose.com/note/java/).  
3. Egy minta OneNote fájl (`.one`) a betöltéshez, vagy létrehozhat egy újat programozottan.  

## Csomagok importálása

Először importálja a szükséges osztályokat a Java projektjébe:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Hogyan exportáljunk betűtípusokat a OneNote HTML‑ként mentésekor?

Az alábbi lépésről‑lépésre útmutató megmutatja, **hogyan exportálhat betűtípusokat** és egyéb erőforrásokat.

### 1. lépés: OneNote‑dokumentum létrehozása programozottan  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Ez a sor betölti a meglévő `.one` fájlt. Ha **programozottan szeretne OneNote‑t létrehozni**, egyszerűen példányosíthat egy új `Document` objektumot, és a API‑val szekciókat/oldalakat adhat hozzá (ez itt nincs bemutatva, hogy a betűtípus‑exportálásra koncentráljunk).

### 2. lépés: Mentés memóriastreambe beágyazott betűtípusokkal  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- A `setExportFonts(ResourceExportType.ExportEmbedded)` azt mondja az Aspose.Note‑nak, hogy **exportálja a betűtípusokat** közvetlenül a HTML‑csomagba.  
- A `setFontFaceTypes(FontFaceType.Ttf)` biztosítja, hogy a TrueType betűtípusok legyenek használva, amelyek széles böngésző‑támogatással rendelkeznek.

### 3. lépés: Mentés HTML‑ként külön erőforrás‑fájlokkal (még mindig betűtípus‑exportálással)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Bár a CSS és a képek be vannak ágyazva, a `ResourceExportType`‑ot átállíthatja `ExportExternal`‑ra, ha külön fájlokat szeretne a könnyebb gyorsítótárazás érdekében. A kulcsfontosságú rész – **a betűtípusok exportálása** – változatlan marad.

### 4. lépés: Visszahívások használata az erőforrások tárolási helyének szabályozásához  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

A `UserSavingCallbacks` osztály (amelyben meg kell valósítania az `ICssSavingCallback`, `IImageSavingCallback` és `IFontSavingCallback` interfészeket) teljes kontrollt ad a mappaszerkezet felett, lehetővé téve, hogy a betűtípusokat egy dedikált `fonts` könyvtárba helyezze, miközben **helyesen exportálja a betűtípusokat**.

## Egyedi betűtípusok beágyazása OneNote‑ból HTML‑re konvertáláskor

Az egyedi betűtípusok beágyazása garantálja, hogy a HTML megjelenése megegyezzen az eredeti OneNote‑elrendezéssel, még olyan eszközökön is, ahol ezek a betűtípusok nincsenek telepítve. Az `ExportEmbedded` és a `FontFaceType.Ttf` használatával a TrueType fájlok base‑64 kódolva kerülnek a generált CSS‑be, így nincs szükség külső betűtípus‑hosztingra.

## A ResourceExportType használata az erőforrás‑exportálás szabályozásához

A `ResourceExportType` lehetővé teszi, hogy a CSS, képek és betűtípusok **a HTML fájlon belül** (`ExportEmbedded`) vagy **külső** fájlokként (`ExportExternal`) legyenek tárolva. Válassza az `ExportEmbedded`‑et egyetlen fájlos megoldáshoz, vagy az `ExportExternal`‑t, ha nagyobb eszközök gyorsítótárazását szeretné kihasználni.

## OneNote‑dokumentum programozott létrehozása HTML exporthoz

Ha a nulláról indul, teljesen kódból felépíthet egy OneNote‑dokumentumot, szekciókat, oldalakat és gazdag szöveget adhat hozzá, majd alkalmazhatja a fenti `HtmlSaveOptions` beállításokat. Így teljes automatizálást ér el: az adatgenerálástól a teljesen stílusos HTML‑kimenetig, beágyazott egyedi betűtípusokkal.

## Gyakori problémák és tippek

- **Hiányzó betűtípusok a kimenetben:** Ellenőrizze, hogy a `setExportFonts(ResourceExportType.ExportEmbedded)` be van állítva, és hogy a forrás OneNote‑fájl valóban beágyazott betűtípusokat használ.  
- **Nagy HTML‑fájlok:** A betűtípusok beágyazása növelheti a méretet. Ha a sávszélesség aggály, állítsa az `ExportFonts`‑t `ExportExternal`‑ra, és helyezze a betűtípusokat CDN‑re.  
- **Visszahívás‑implementációs hibák:** Győződjön meg róla, hogy a visszahívás‑osztályok helyesen írják a streamet és lezárják az erőforrásokat, hogy elkerülje a fájl‑sérülést.  

## Gyakran ismételt kérdések

**K: Konvertálhatok több OneNote‑dokumentumot egyszerre HTML‑re?**  
V: Igen, egyszerűen iteráljon minden `Document` példányon, és alkalmazza ugyanazt a `HtmlSaveOptions`‑t.  

**K: Támogatja az Aspose.Note for Java más kimeneti formátumokat is a HTML‑en kívül?**  
V: Természetesen. Exportálhat PDF‑be, DOCX‑be, PNG‑be, JPEG‑be és még sok más formátumba a megfelelő mentési opciók használatával.  

**K: Van-e elérhető próbaverzió az Aspose.Note for Java‑hoz?**  
V: Igen, töltsön le egy ingyenes próbát [innen](https://releases.aspose.com/).  

**K: Hol kaphatok támogatást az Aspose.Note for Java‑hoz?**  
V: Látogassa meg az [Aspose.Note fórumot](https://forum.aspose.com/c/note/28) a közösségi és hivatalos segítségért.  

**K: Hogyan vásárolhatok licencet az Aspose.Note for Java‑hoz?**  
V: A licencek a [Aspose weboldalán](https://purchase.aspose.com/buy) érhetők el.  

## Összegzés

Most már tudja, **hogyan exportálhat betűtípusokat**, miközben **HTML‑ként menti a OneNote‑ot** az Aspose.Note for Java segítségével. A `HtmlSaveOptions` megfelelő beállításával és opcionálisan a visszahívások használatával megőrizheti a OneNote‑oldalak pontos megjelenését – beleértve az egyedi betűtípusokat is – a weben történő közzététel során. Kísérletezzen különböző `ResourceExportType` beállításokkal, hogy megtalálja a projektje teljesítmény‑ és tárolási igényeinek legmegfelelőbb megoldást.

---

**Utolsó frissítés:** 2026-02-07  
**Tesztelt verzió:** Aspose.Note for Java 24.12  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}