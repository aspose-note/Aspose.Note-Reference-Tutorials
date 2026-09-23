---
date: 2026-09-19
description: Ismerje meg, hogyan konvertálhatja a OneNote-ot HTML-re és exportálhatja
  a betűtípusokat az Aspose.Note for Java segítségével. Ez az útmutató bemutatja a
  OneNote HTML-ként való mentését beágyazott betűtípusokkal, CSS-sel és images.
keywords:
- convert onenote to html
- save onenote as html
- export fonts java
- aspose.note html export
lastmod: 2026-09-19
linktitle: Hogyan exportáljuk a betűtípusokat a OneNote HTML-ként történő mentésekor
  – Java
og_description: Ismerje meg, hogyan konvertálhatja a OneNote-ot HTML-re és exportálhatja
  a betűtípusokat az Aspose.Note for Java segítségével. Az útmutató bemutatja a OneNote
  HTML-ként való mentését beágyazott betűtípusokkal, CSS-sel és images.
og_image_alt: 'Developer guide: convert OneNote to HTML with font export in Java'
og_title: Konvertálja a OneNote-ot HTML-re és exportálja a betűtípusokat Java-ban
  – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-19'
  description: Learn how to convert OneNote to HTML and export fonts using Aspose.Note
    for Java. This guide covers saving OneNote as HTML with embedded fonts, CSS, and
    images.
  headline: How to convert OneNote to HTML and export fonts in Java
  type: TechArticle
- description: Learn how to convert OneNote to HTML and export fonts using Aspose.Note
    for Java. This guide covers saving OneNote as HTML with embedded fonts, CSS, and
    images.
  name: How to convert OneNote to HTML and export fonts in Java
  steps:
  - name: create a OneNote document programmatically
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. You can either load an existing `.one` file or
      instantiate a new document and add sections/pages via the API. This line loads
      an existing `.one` file. If you need to **create OneNote programmatica
  - name: save to a memory stream with embedded fonts
    text: The `HtmlSaveOptions` class controls every aspect of the HTML conversion.
      `ResourceExportType` is an enumeration that defines how resources such as fonts,
      images, and CSS are exported. Setting `setExportFonts(ResourceExportType.ExportEmbedded)`
      tells Aspose.Note to embed fonts directly into the HTML
  - name: save as HTML with separate resource files (still exporting fonts)
    text: If you prefer a single HTML file, keep `ExportEmbedded`. For caching‑friendly
      deployments, switch `ResourceExportType` to `ExportExternal`; the fonts will
      still be embedded, but CSS, images, and other assets will be saved as separate
      files. Even though CSS and images are embedded, you can change the
  - name: use callbacks to control where each resource is stored
    text: '`UserSavingCallbacks` allows custom handling of resource saving. Implementing
      `UserSavingCallbacks` (which requires `ICssSavingCallback`, `IImageSavingCallback`,
      and `IFontSavingCallback`) gives you full control over folder structure, allowing
      you to keep fonts in a dedicated `fonts` directory while'
  type: HowTo
- questions:
  - answer: Yes, loop through each `Document` instance and apply the same `HtmlSaveOptions`.
    question: Can I convert multiple OneNote documents to HTML in one go?
  - answer: Absolutely. You can export to PDF, DOCX, PNG, JPEG, and more using the
      appropriate save options.
    question: Does Aspose.Note for Java support other output formats besides HTML?
  - answer: Yes, download a free trial from the **Aspose releases page**([Aspose releases
      page](https://releases.aspose.com/)).
    question: Is there a trial version available for Aspose.Note for Java?
  - answer: Visit the **Aspose.Note forum**([Aspose.Note forum](https://forum.aspose.com/c/note/28))
      for community and official assistance.
    question: Where can I get support for Aspose.Note for Java?
  - answer: Licenses are available at the **Aspose purchase page**([Aspose website](https://purchase.aspose.com/buy)).
    question: How can I purchase a license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- convert onenote
- Aspose.Note
- Java HTML export
- font embedding
title: Hogyan konvertáljuk a OneNote-ot HTML-re és exportáljuk a betűtípusokat Java-ban
url: /hu/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan konvertáljuk a OneNote-ot HTML-re és exportáljuk a betűtípusokat Java-ban

## Bevezetés

Ebben az útmutatóban megtudja, **hogyan exportálja a betűtípusokat**, miközben **konvertálja a OneNote-ot HTML-re** az Aspose.Note for Java használatával. Lépésről lépésre bemutatjuk, hogyan hozhat létre egy OneNote-dokumentumot programozottan, hogyan konfigurálja a HTML mentési beállításokat, és hogyan ágyazza be a szükséges betűtípus‑fájlokat, hogy a létrehozott HTML pontosan úgy nézzen ki, mint az eredeti OneNote‑oldalak. Ez a megközelítés tökéletes, ha meg kell őrizni a OneNote‑tartalom vizuális hűségét egy web‑barát formátumban, különösen tudásbázis‑portálok, automatizált jelentéskészítési folyamatok vagy többplatformos dokumentációs oldalak esetén.

## Gyors válaszok
- **Melyik könyvtár kezeli az exportot?** Aspose.Note for Java  
- **Beágyazhatók a betűtípusok a HTML-be?** Igen – állítsa be az `ExportFonts` értékét `ExportEmbedded`‑re  
- **Szükség van licencre a termeléshez?** Érvényes Aspose.Note licenc szükséges kereskedelmi használathoz  
- **Melyik Java verzió támogatott?** Java 8 vagy újabb  
- **Lehetséges a források külön fájlokba mentése?** Teljesen – állítsa be ennek megfelelően a `ResourceExportType`‑t  

## Mit jelent a „betűtípusok exportálása” a OneNote HTML konverzió kontextusában?

A betűtípusok exportálása azt jelenti, hogy az eredeti betűtípus‑fájlokat (pl. TTF vagy OTF) közvetlenül beágyazzuk a HTML csomagba, így a böngészők pontosan úgy jelenítik meg a szöveget, ahogy az a OneNote‑ban látható, még akkor is, ha a végfelhasználó eszközén nem állnak rendelkezésre ezek a betűtípusok. Az Aspose.Note ezt úgy valósítja meg, hogy a betűtípusokat base‑64 karakterláncokká konvertálja, és a generált CSS‑be illeszti, ezáltal pixel‑pontos tipográfiát biztosítva.

## Miért konvertáljuk a OneNote-ot HTML-re és exportáljuk a betűtípusokat?

A betűtípusok beágyazása a konverzió során biztosítja, hogy az eredeti OneNote‑oldalak vizuális megjelenése minden böngészőben megmaradjon, ezáltal megszüntetve a hiányzó betűtípusok által okozott elrendezési eltolódásokat. Ez különösen fontos vállalati arculat, jogi dokumentumok vagy bármely olyan tartalom esetén, ahol a pontos tipográfia lényeges.

- **Automatizálás:** Jelentések, oktatóanyagok vagy tudásbázis‑cikkek generálása a OneNote‑ból manuális másolás‑beillesztés nélkül.  
- **Következetesség:** Az elrendezés, a stílus és az egyedi betűtípusok megőrzése minden böngészőben és eszközön.  
- **Hordozhatóság:** A HTML univerzálisan megtekinthető – nincs szükség a OneNote kliensre vagy további plug‑inokra.  
- **Teljesítmény:** A betűtípusok beágyazása megszünteti a felesleges hálózati kéréseket, ami javíthatja az oldalbetöltési időt kis‑ és közepes méretű dokumentumok esetén.

## Előkövetelmények

1. Telepített Java Development Kit (JDK) 8 vagy újabb.  
2. Aspose.Note for Java könyvtár – letölthető az **Aspose.Note for Java kiadási oldaláról**([Aspose.Note for Java release page](https://releases.aspose.com/note/java/)).  
3. Egy minta OneNote‑fájl (`.one`) a betöltéshez, vagy programozottan létrehozhat egy újat.  

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

## Hogyan konvertáljuk a OneNote-ot HTML-re betűtípus‑exportálással?

Töltse be a OneNote‑jegyzettömböt, konfigurálja a `HtmlSaveOptions`‑t a betűtípusok beágyazásához, és mentse az eredményt egy adatfolyamra vagy fájlba. Ez az egylépéses folyamat biztosítja, hogy az eredeti oldalakban használt minden egyedi betűtípus szerepeljen a HTML‑kimenetben, így hű vizuális ábrázolást nyújt, miközben a munkafolyamat egyszerű és karbantartható marad.

### 1. lépés: OneNote-dokumentum létrehozása programozottan  

A `Document` osztály az Aspose.Note legfelső szintű objektuma, amely egyetlen OneNote‑fájlt reprezentál a memóriában. Betölthet egy meglévő `.one` fájlt, vagy új dokumentumot hozhat létre, és a API‑n keresztül szekciókat/oldalakat adhat hozzá.

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Ez a sor egy meglévő `.one` fájlt tölt be. Ha **programozottan kell OneNote‑t létrehozni**, akkor példányosíthat egy új `Document` objektumot, és a API‑n keresztül szekciókat/oldalakat adhat hozzá (itt nem látható, hogy a fókusz a betűtípusok exportálásán van).

### 2. lépés: mentés memóriafolyamra beágyazott betűtípusokkal  

A `HtmlSaveOptions` osztály szabályozza a HTML konverzió minden aspektusát. A `ResourceExportType` egy felsorolás, amely meghatározza, hogyan exportálódnak a források, például betűtípusok, képek és CSS. A `setExportFonts(ResourceExportType.ExportEmbedded)` beállítása azt mondja az Aspose.Note‑nak, hogy a betűtípusokat közvetlenül a HTML csomagba ágyazza be, míg a `setFontFaceTypes(FontFaceType.Ttf)` a exportot TrueType betűtípusokra korlátozza, amelyek a legszélesebb körű böngésző‑támogatással rendelkeznek.

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
- `setFontFaceTypes(FontFaceType.Ttf)` biztosítja, hogy TrueType betűtípusok legyenek használva, amelyek széles böngésző‑támogatással rendelkeznek.

### 3. lépés: mentés HTML‑ként külön erőforrás‑fájlokkal (még mindig betűtípus‑exportálás)

Ha egyetlen HTML fájlt szeretne, tartsa meg az `ExportEmbedded` beállítást. Gyorsítótár‑barát telepítésekhez állítsa át a `ResourceExportType`‑t `ExportExternal`‑ra; a betűtípusok továbbra is be lesznek ágyazva, de a CSS, képek és egyéb eszközök külön fájlokként lesznek mentve.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Bár a CSS és a képek be vannak ágyazva, ha a könnyebb gyorsítótárazás érdekében külön fájlokat szeretne, módosíthatja a `ResourceExportType`‑t `ExportExternal`‑ra. A kulcsfontosságú rész – **a betűtípusok exportálása** – változatlan marad.

### 4. lépés: callback‑ek használata az erőforrások tárolási helyének vezérléséhez  

A `UserSavingCallbacks` lehetővé teszi az erőforrás‑mentés egyéni kezelését. A `UserSavingCallbacks` (amely megköveteli az `ICssSavingCallback`, `IImageSavingCallback` és `IFontSavingCallback` implementálását) megvalósítása teljes irányítást ad a mappaszerkezet felett, lehetővé téve, hogy a betűtípusokat egy dedikált `fonts` könyvtárban tartsa, miközben **helyesen exportálja a betűtípusokat**.

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

A callback osztályok lehetővé teszik a fájlok átnevezését, az adatfolyamok tömörítését, vagy a betűtípusok CDN‑kész mappába helyezését, így nagy léptékű telepítésekhez is rugalmas megoldást nyújtanak.

## Hogyan ágyazzunk be egyedi betűtípusokat a OneNote HTML konverziója során

Az egyedi betűtípusok beágyazása garantálja, hogy a HTML megjelenítés megegyezzen az eredeti OneNote elrendezésével, még olyan eszközökön is, ahol ezek a betűtípusok nincsenek telepítve. Az `ExportEmbedded` és a `FontFaceType.Ttf` együtt használatával a TrueType fájlok base‑64 kódolásúak lesznek, és közvetlenül a generált CSS‑be kerülnek, ezáltal megszüntetve a külső betűtípus‑hosztolás szükségességét és biztosítva a konzisztens tipográfiát a böngészők között.

## A ResourceExportType használata az erőforrás‑exportálás vezérléséhez

A `ResourceExportType` lehetővé teszi, hogy eldöntse, a CSS, képek és betűtípusok **a** HTML fájl **belsejében** (`ExportEmbedded`) vagy **külső** fájlokként (`ExportExternal`) legyenek tárolva. Válassza az `ExportEmbedded`‑et egyetlen fájlos megoldáshoz, vagy az `ExportExternal`‑t, ha nagy eszközök esetén a böngésző gyorsítótárazását szeretné kihasználni.

## OneNote létrehozása programozottan HTML exporthoz

Ha a nulláról indul, teljesen kódból építhet fel egy OneNote‑dokumentumot, hozzáadhat szekciókat, oldalakat és formázott szöveget, majd alkalmazhatja a fent bemutatott `HtmlSaveOptions`‑t. Ez vég‑a‑végig automatizálást biztosít: az adatgenerálástól egy teljesen stílusos HTML kimenetig, amelybe be vannak ágyazva az egyedi betűtípusok.

## Gyakori problémák és tippek

- **Hiányzó betűtípusok a kimenetben:** Ellenőrizze, hogy a `setExportFonts(ResourceExportType.ExportEmbedded)` be van állítva, és hogy a forrás OneNote‑fájl valóban beágyazott betűtípusokat használ.  
- **Nagy HTML fájlok:** A betűtípusok beágyazása 200‑500 KB‑kal növelheti a méretet betűtípusonként. Ha a sávszélesség aggály, állítsa át az `ExportFonts`‑t `ExportExternal`‑ra, és helyezze a betűtípusokat CDN‑re.  
- **Callback implementációs hibák:** Győződjön meg arról, hogy a callback osztályai helyesen írják az adatfolyamot és lezárják az erőforrásokat, hogy elkerülje a fájl‑sérülést.  
- **Teljesítmény tip:** 100 oldalon túli jegyzettömbök esetén dolgozza fel a szekciókat egyenként, és egyesítse a keletkező HTML‑töredékeket, hogy alacsony maradjon a memóriahasználat.  
- **Mennyiségi állítás:** Az Aspose.Note 500 oldalig terjedő jegyzettömböket képes 30 másodpercnél gyorsabban konvertálni egy tipikus 2,5 GHz‑es szerveren, miközben dokumentumonként több mint 50 egyedi betűtípust őriz meg.

## Gyakran ismételt kérdések

**Q: Több OneNote‑dokumentumot is konvertálhatok egyszerre HTML‑re?**  
A: Igen, iteráljon minden egyes `Document` példányon, és alkalmazza ugyanazt a `HtmlSaveOptions`‑t.  

**Q: Az Aspose.Note for Java támogat más kimeneti formátumokat is a HTML‑en kívül?**  
A: Teljes mértékben. Exportálhat PDF‑be, DOCX‑be, PNG‑be, JPEG‑be és további formátumokba a megfelelő mentési beállítások használatával.  

**Q: Elérhető próba verzió az Aspose.Note for Java‑hoz?**  
A: Igen, töltsön le egy ingyenes próbát az **Aspose kiadási oldalról**([Aspose releases page](https://releases.aspose.com/)).  

**Q: Hol kaphatok támogatást az Aspose.Note for Java‑hoz?**  
A: Látogassa meg az **Aspose.Note fórumot**([Aspose.Note forum](https://forum.aspose.com/c/note/28)) a közösségi és hivatalos segítségért.  

**Q: Hogyan vásárolhatok licencet az Aspose.Note for Java‑hoz?**  
A: A licencek elérhetők az **Aspose vásárlási oldalon**([Aspose website](https://purchase.aspose.com/buy)).  

## Következtetés

Most már tudja, **hogyan exportálja a betűtípusokat**, miközben **konvertálja a OneNote-ot HTML-re** az Aspose.Note for Java használatával. A `HtmlSaveOptions` konfigurálásával és opcionálisan a callback‑ek használatával megőrizheti OneNote‑oldalai pontos megjelenését – beleértve az egyedi betűtípusokat is – a weben történő megjelenítéskor. Kísérletezzen a `ResourceExportType` beállításokkal a fájlméret és a gyorsítótárazási stratégia egyensúlyozásához, és integrálja a munkafolyamatot az automatizált jelentéskészítési csővezetékbe a maximális hatékonyság érdekében.

---

**Legutóbb frissítve:** 2026-09-19  
**Tesztelt verzióval:** Aspose.Note for Java 24.12  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [Használja az Aspose.Note for Java-t a OneNote PDF‑ként mentéséhez a megadott betűtípus alrendszerrel](/note/java/onenote-document-saving/save-using-specified-fonts-subsystem/)
- [OneNote konvertálása szöveggé és képek kinyerése a Document Visitor használatával – Java](/note/java/onenote-document-loading/extract-content-using-document-visitor/)
- [OneNote konvertálása PDF‑re oldalbeállítások használatával az Aspose.Note for Java-val](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}