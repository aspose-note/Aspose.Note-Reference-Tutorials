---
date: 2026-10-15
description: Ismerje meg, hogyan állíthatja be az oldal címét egy OneNote dokumentumban
  az Aspose.Note .NET számára. Kövesse lépésről‑lépésre útmutatónkat a címzett oldalak
  létrehozásához és az alapértelmezett szövegstílus alkalmazásához.
keywords:
- how to set page title
- set default text style
- create titled page
- document with page title
lastmod: 2026-10-15
linktitle: Dokumentum létrehozása oldal címmel az Aspose.Note-ban
og_description: Ismerje meg, hogyan állíthatja be az oldal címét egy OneNote dokumentumban
  az Aspose.Note .NET számára. Ez a lépésről‑lépésre útmutató megmutatja, hogyan hozhat
  létre címzett oldalt, alkalmazza az alapértelmezett szövegstílust, és mentse a fájlt.
og_image_alt: 'Aspose.Note tutorial: setting page title in OneNote document with .NET'
og_title: Hogyan állítsuk be az oldal címét egy OneNote dokumentumban az Aspose.Note
  használatával
schemas:
- author: Aspose
  dateModified: '2026-10-15'
  description: Learn how to set page title in a OneNote document using Aspose.Note
    for .NET. Follow our step‑by‑step guide for creating titled pages and applying
    default text style.
  headline: How to set page title in OneNote document using Aspose.Note
  type: TechArticle
- description: Learn how to set page title in a OneNote document using Aspose.Note
    for .NET. Follow our step‑by‑step guide for creating titled pages and applying
    default text style.
  name: How to set page title in OneNote document using Aspose.Note
  steps:
  - name: Download Visual Studio from the Microsoft website.
    text: Download Visual Studio from the Microsoft website.
  - name: Select the “.NET desktop development” workload during installation.
    text: Select the “.NET desktop development” workload during installation.
  - name: Create a new console‑application project (or any .NET project type you prefer).
    text: Create a new console‑application project (or any .NET project type you prefer).
  - name: 'Get Aspose.Note: Download the library from the [website](https://releases.aspose.com/note/net/).'
    text: 'Get Aspose.Note: Download the library from the [website](https://releases.aspose.com/note/net/).'
  - name: 'Install via NuGet Package Manager: search for **Aspose.Note** and install
      the latest version.'
    text: 'Install via NuGet Package Manager: search for **Aspose.Note** and install
      the latest version.'
  type: HowTo
- questions:
  - answer: Yes, you can change the font name, size, and color through the `DefaultTextStyle`
      object before assigning the title.
    question: Can I customize the title text style?
  - answer: Absolutely. The library supports .NET Core, .NET 5+, and .NET 6+, enabling
      cross‑platform development.
    question: Is Aspose.Note compatible with .NET Core?
  - answer: Yes. Use the `Image` and `Attachment` classes to embed multimedia content
      alongside your titled page.
    question: Can I add images and attachments to the document?
  - answer: It does. You can load a `.one` file, modify its pages (including titles),
      and save it back.
    question: Does Aspose.Note support reading existing OneNote files?
  - answer: You can find support and assistance on the [Aspose.Note forum](https://forum.aspose.com/c/note/28),
      where experts and community members help with queries.
    question: Where can I find support if I encounter any issues?
  type: FAQPage
second_title: Aspose.Note .NET API
tags:
- Aspose.Note
- OneNote API
- page title
- .NET
- document creation
title: Hogyan állítsuk be az oldal címét egy OneNote dokumentumban az Aspose.Note
  használatával
url: /hu/net/loading-and-saving-operations/create-doc-with-page-title/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan állítsuk be az oldal címét egy OneNote dokumentumban az Aspose.Note használatával

## Bevezetés

Ebben az oktatóanyagról megtanulja **hogyan állítsuk be az oldal címét** egy OneNote dokumentum létrehozásakor az Aspose.Note for .NET használatával. Az oldal címének beállítása javítja a navigációt, a kereshetőséget és a OneNote jegyzetfüzetek általános olvashatóságát. Lépésről lépésre végigvezetjük a projekt beállításától a végleges fájl mentéséig, és megmutatjuk, hogyan alkalmazzon alapértelmezett szövegstílust a címre.

## Gyors válaszok
- **Mi a “page title” jelentése?** A OneNote oldal tetején megjelenő szöveg, amely a címsorát képezi.  
- **Melyik API osztály hozza létre a címet?** A `Page` osztály `PageTitle` tulajdonsága.  
- **Szükségem van licencre a minta futtatásához?** Egy ingyenes próba a fejlesztéshez elegendő; a termeléshez kereskedelmi licenc szükséges.  
- **Támogatott a .NET Core?** Igen – az Aspose.Note fut .NET Core-on, .NET 5+-on és .NET 6+-on.  
- **Testreszabhatom a cím betűtípusát?** Természetesen – a betűtípus nevét, méretét és színét a `DefaultTextStyle` objektummal állíthatja be.

## Mi a „hogyan állítsuk be az oldal címét”?
**hogyan állítsuk be az oldal címét** a folyamat, amely során egy címsor karakterláncot rendelünk egy OneNote oldal `Title` eleméhez az Aspose.Note API-ján keresztül. Ez a művelet az oldal dokumentumhierarchiához való hozzáadása előtt történik, és biztosítja, hogy a cím helyesen jelenjen meg a OneNote felhasználói felületén, valamint keresésre és az oldalak jegyzetfüzetben való rendezésére is használható legyen.

## Miért használjuk az Aspose.Note-ot az oldal címének beállításához?
Az Aspose.Note **30+ bemeneti és kimeneti formátumot** támogat, és képes **akár 10 000 oldal** tartalmú jegyzetfüzeteket kezelni anélkül, hogy a teljes fájlt memóriába töltené. A könyvtár automatikusan kezeli a Unicode karaktereket, jobbról balra író írásrendszereket és a komplex formázásokat, ami megkíméli Önt az alacsony szintű OneNote XML kód írásától.

## Előfeltételek

Mielőtt elkezdenénk, győződjön meg arról, hogy a következő előfeltételek telepítve és beállítva vannak:

### Visual Studio telepítése

1. Töltse le a Visual Studio-t a Microsoft weboldaláról.  
2. A telepítés során válassza ki a “.NET desktop development” munkaterhet.  
3. Hozzon létre egy új konzol‑alkalmazás projektet (vagy bármilyen .NET projekt típust, amelyet preferál).

### Aspose.Note telepítése

1. Szerezze be az Aspose.Note-ot: töltse le a könyvtárat a [weboldalról](https://releases.aspose.com/note/net/).  
2. Telepítse a NuGet Package Manager segítségével: keressen rá a **Aspose.Note** csomagra, és telepítse a legújabb verziót.

## Névtér importálása

A következő névterek biztosítják a hozzáférést az Aspose.Note alapvető osztályaihoz:

```text
using Aspose.Note;
using Aspose.Note.Drawing;
using Aspose.Note.Rendering;
```

Most bontsuk le a dokumentum oldal címmel való létrehozásának folyamatát több lépésre:

## Hogyan állítsuk be az oldal címét egy OneNote dokumentumban

Töltsön be egy új `Document` objektumot, hozzon létre egy `Page`-et, állítsa be a cím szövegét, alkalmazzon alapértelmezett stílust, és végül mentse a fájlt. Ez a teljes munkafolyamat csak néhány kódsort igényel, és nem szükséges kézi XML kezelés.

## 1. lépés: dokumentum objektum létrehozása

A `Document` osztály egy memóriában lévő OneNote jegyzetfüzetet képvisel, amely több oldalt és szekciót is tartalmazhat.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

## 2. lépés: oldal osztály objektum inicializálása

`Page` objektumok egyes oldalak modelljei egy OneNote jegyzetfüzetben, és tartalmazzák a tartalmakat, mint például a cím, a vázlatok és a képek.

```csharp
// Create an object of the Document class
Document doc = new Aspose.Note.Document();
```

## 3. lépés: alapértelmezett szövegstílus beállítása

`DefaultTextStyle` határozza meg az alapértelmezett betűcsaládot, méretet és színt, amely a szövegelemekre kerül alkalmazásra, amikor azok létrejönnek.

```csharp
// Initialize Page class object
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 4. lépés: oldal címének tulajdonságainak beállítása

A `Page` `Title` tulajdonsága tartalmazza a címsor információkat, beleértve a szöveget, a dátumot és az időt.

```csharp
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## 5. lépés: oldal csomópont hozzáadása a dokumentumhoz

`Document.Pages.Add` beilleszti az újonnan létrehozott `Page`-et a jegyzetfüzet oldalgyűjteményébe, meghatározva annak pozícióját.

```csharp
// Set page title properties
page.Title = new Title()
{
    TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
};
```

## 6. lépés: OneNote dokumentum mentése

`Document.Save` a jegyzetfüzetet egy fájlba írja a megadott formátumban, például `.one` formátumban a OneNote-hoz.

```csharp
// Append Page node in the document
doc.AppendChildLast(page);
```

## Gyakori problémák és megoldások

- **A cím nem jelenik meg** – Győződjön meg arról, hogy a `Title` tulajdonságot *mielőtt* az oldalt a dokumentumhoz hozzáadná, beállította.  
- **Helytelen betűtípus megjelenítés** – Ellenőrizze, hogy a megadott betűtípus telepítve van-e a célgépen; ellenkező esetben az Aspose.Note egy alapértelmezett betűtípust használ.  
- **Nagy jegyzetfüzetek memória nyomást okoznak** – Használja a `Document.Load`-ot a `LoadOptions`-szel, amely engedélyezi a lusta betöltést nagyon nagy fájlok esetén.

## Gyakran ismételt kérdések

**K: Testreszabhatom a cím szövegstílusát?**  
V: Igen, a `DefaultTextStyle` objektumon keresztül megváltoztathatja a betűtípus nevét, méretét és színét, mielőtt a címet hozzárendeli.

**K: Az Aspose.Note kompatibilis a .NET Core-rel?**  
V: Teljesen. A könyvtár támogatja a .NET Core-t, a .NET 5+-ot és a .NET 6+-ot, lehetővé téve a többplatformos fejlesztést.

**K: Hozzáadhatok képeket és mellékleteket a dokumentumhoz?**  
V: Igen. Használja az `Image` és `Attachment` osztályokat a multimédiás tartalom beágyazásához a címmel ellátott oldal mellett.

**K: Az Aspose.Note támogatja meglévő OneNote fájlok olvasását?**  
V: Igen. Betölthet egy `.one` fájlt, módosíthatja annak oldalait (beleértve a címeket), és vissza is mentheti.

**K: Hol találok támogatást, ha problémáim vannak?**  
V: Támogatást és segítséget a [Aspose.Note fórumon](https://forum.aspose.com/c/note/28) talál, ahol szakértők és közösségi tagok segítenek a kérdésekben.

---

**Utoljára frissítve:** 2026-10-15  
**Tesztelve:** Aspose.Note 24.11 for .NET  
**Szerző:** Aspose  

```csharp
// Save OneNote document
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## Kapcsolódó oktatóanyagok

- [Oldal cím stílusának módosítása az Aspose.Note-ban](/note/net/text-manipulation/change-page-title-style/)
- [Cím létrehozása MS stílussal az Aspose.Note-ban](/note/net/text-manipulation/create-title-ms-style/)
- [Alapértelmezett bekezdésstílus beállítása az Aspose.Note-ban](/note/net/text-manipulation/set-default-paragraph-style/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}