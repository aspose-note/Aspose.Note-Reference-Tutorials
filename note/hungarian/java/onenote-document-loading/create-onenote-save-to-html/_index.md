---
date: 2025-12-02
description: Tanulja meg, hogyan exportálhat betűtípusokat, miközben a OneNote-ot
  HTML-ként menti az Aspose.Note for Java segítségével. Ez az útmutató bemutatja,
  hogyan hozhat létre OneNote-fájlokat programozottan, és hogyan ágyazhat be betűtípusokat,
  CSS-t és képeket.
language: hu
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Hogyan exportáljuk a betűtípusokat a OneNote HTML-be mentésekor – Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan exportáljunk betűtípusokat a OneNote HTML‑ként mentésekor – Java

## Bevezetés

Ebben az útmutatóban megismerheti, **hogyan exportáljon betűtípusokat**, amikor **OneNote‑t ment HTML‑ként** az Aspose.Note for Java használatával. Végigvezetjük a OneNote dokumentum programozott létrehozását, a HTML mentési beállítások konfigurálását, és a szükséges betűtípusfájlok beágyazását, hogy a kapott HTML pontosan úgy nézzen ki, mint az eredeti OneNote oldalak. Ez a megközelítés tökéletes, ha a OneNote tartalom vizuális hűségét web‑barát formátumban kell megőrizni.

## Gyors válaszok
- **Melyik könyvtár kezeli az exportálást?** Aspose.Note for Java  
- **Beágyazhatók a betűtípusok a HTML‑be?** Igen – állítsa be az `ExportFonts` értékét `ExportEmbedded`‑re  
- **Szükség van licencre a termeléshez?** Érvényes Aspose.Note licenc szükséges kereskedelmi használathoz  
- **Melyik Java verzió támogatott?** Java 8 vagy újabb  
- **Lehetséges a forrásokat külön fájlokba menteni?** Természetesen – állítsa be ennek megfelelően a `ResourceExportType`‑t  

## Mi a “betűtípusok exportálása” a OneNote HTML konverzió kontextusában?

Amikor egy OneNote jegyzetfüzetet HTML‑re konvertál, a vizuális megjelenés a CSS‑től, a képektől és különösen az eredeti oldalakon használt betűtípusoktól függ. A **betűtípusok exportálása** azt jelenti, hogy a betűtípusfájlokat (pl. TTF) közvetlenül a HTML csomagba ágyazzuk be, így a böngészők pontosan úgy jelenítik meg a szöveget, ahogy az OneNote‑ban látható, még akkor is, ha a végfelhasználó gépén nincsenek telepítve ezek a betűtípusok.

## Miért hozunk létre OneNote‑t programozottan, és mentjük HTML‑ként?

- **Automatizálás:** Jelentések, dokumentáció vagy tudásbázis cikkek generálása OneNote‑ból manuális másolás‑beillesztés nélkül.  
- **Következetesség:** Az elrendezés, a stílus és az egyedi betűtípusok megőrzése különböző eszközökön.  
- **Hordozhatóság:** A HTML univerzálisan megtekinthető – nincs szükség OneNote kliensre.  

## Előfeltételek

1. Java Development Kit (JDK) 8 vagy újabb telepítve.  
2. Aspose.Note for Java könyvtár – letölthető [innen](https://releases.aspose.com/note/java/).  
3. Egy minta OneNote fájl (`.one`) a betöltéshez, vagy programozottan létrehozhat egy újat.  

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

Az alábbi lépésről‑lépésre útmutató bemutatja, hogyan **exportálhat betűtípusokat** és egyéb erőforrásokat.

### 1. lépés: OneNote dokumentum létrehozása programozottan  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Ez a sor betölt egy meglévő `.one` fájlt. Ha **programozottan szeretne OneNote‑t létrehozni**, példányosíthat egy új `Document` objektumot, és a API‑val hozzáadhat szekciókat/oldalakat (ez itt nincs bemutatva, hogy a betűtípusok exportálására koncentráljunk).

### 2. lépés: Mentés memóriafolyamra beágyazott betűtípusokkal  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` azt mondja az Aspose.Note‑nak, hogy **exportálja a betűtípusokat** közvetlenül a HTML csomagba.  
- `setFontFaceTypes(FontFaceType.Ttf)` biztosítja, hogy TrueType betűtípusok legyenek használva, amelyek széles körű böngésző támogatással rendelkeznek.

### 3. lépés: Mentés HTML‑ként külön erőforrásfájlokkal (a betűtípusok továbbra is exportálva vannak)

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Még ha a CSS és a képek be vannak ágyazva, a `ResourceExportType`‑t `ExportExternal`‑ra is állíthatja, ha külön fájlokat szeretne a könnyebb gyorsítótárazás érdekében. A kulcsfontosságú rész – **a betűtípusok exportálása** – változatlan marad.

### 4. lépés: Callback‑ek használata az erőforrások tárolási helyének vezérléséhez  

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

A `UserSavingCallbacks` osztály (implementálnia kell az `ICssSavingCallback`, `IImageSavingCallback` és `IFontSavingCallback` interfészeket) teljes irányítást biztosít a mappaszerkezet felett, lehetővé téve, hogy a betűtípusokat egy dedikált `fonts` könyvtárban tartsa, miközben a **betűtípusok exportálása** helyesen történik.

## Gyakori problémák és tippek

- **Hiányzó betűtípusok a kimenetben:** Ellenőrizze, hogy a `setExportFonts(ResourceExportType.ExportEmbedded)` be van állítva, és hogy a forrás OneNote fájl valóban beágyazott betűtípusokat használ.  
- **Nagy HTML fájlok:** A betűtípusok beágyazása növelheti a méretet. Ha a sávszélesség aggály, állítsa át az `ExportFonts`‑t `ExportExternal`‑ra, és helyezze a betűtípusokat CDN‑re.  
- **Callback implementációs hibák:** Győződjön meg arról, hogy a callback osztályok helyesen írják a streamet és lezárják az erőforrásokat, hogy elkerüljék a fájlok sérülését.  

## Gyakran feltett kérdések

**Q: Több OneNote dokumentumot konvertálhatok egyszerre HTML‑re?**  
A: Igen, iteráljon minden `Document` példányon, és alkalmazza ugyanazt a `HtmlSaveOptions`‑t.  

**Q: Az Aspose.Note for Java támogat más kimeneti formátumokat is a HTML‑en kívül?**  
A: Természetesen. Exportálhat PDF‑be, DOCX‑be, PNG‑be, JPEG‑be és további formátumokba a megfelelő mentési beállítások használatával.  

**Q: Elérhető próba verzió az Aspose.Note for Java‑hoz?**  
A: Igen, töltsön le egy ingyenes próbaverziót [innen](https://releases.aspose.com/).  

**Q: Hol kaphatok támogatást az Aspose.Note for Java‑hoz?**  
A: Látogassa meg az [Aspose.Note fórumot](https://forum.aspose.com/c/note/28) a közösségi és hivatalos segítségért.  

**Q: Hogyan vásárolhatok licencet az Aspose.Note for Java‑hoz?**  
A: Licencelés elérhető az [Aspose weboldalon](https://purchase.aspose.com/buy).  

## Összegzés

Most már tudja, **hogyan exportáljon betűtípusokat**, miközben **OneNote‑t HTML‑ként ment** az Aspose.Note for Java használatával. A `HtmlSaveOptions` konfigurálásával és opcionálisan a callback‑ek használatával megőrizheti OneNote oldalai pontos megjelenését – beleértve az egyedi betűtípusokat is – amikor a weben teszi közzé. Nyugodtan kísérletezzen a különböző `ResourceExportType` beállításokkal, hogy a projekt teljesítmény‑ és tárolási igényeinek megfeleljen.

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
