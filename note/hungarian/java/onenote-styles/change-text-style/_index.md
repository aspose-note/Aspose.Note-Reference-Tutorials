---
date: 2026-01-18
description: Ismerje meg, hogyan állíthatja be a betűszínt Java-ban a OneNote-ban
  az Aspose.Note használatával, emelje ki a szöveget, módosítsa a betűméretet, és
  mentse a OneNote-ot PDF formátumban. Lépésről‑lépésre útmutató kóddal.
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Betűszín beállítása Java-val a OneNote-ban – Aspose.Note
url: /hu/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Betűszín beállítása Java-ban a OneNote-ban – Aspose.Note

## Bevezetés

Ebben az útmutatóban megtudja, hogyan **állíthatja be a betűszínt Java-ban** a OneNote-dokumentum szövegéhez az Aspose.Note for Java API segítségével. Végigvezetjük a `.one` fájl betöltésén, a RichText csomópontok elérésén, a szín, kiemelés és betűméret módosításán, és végül a **OneNote PDF-ként mentésén**. Akár **szöveget szeretne kiemelni a OneNote-ban**, **betűméretet módosítani a OneNote-ban**, vagy egyszerűen csak az általános szövegstílust változtatni akarja, az alábbi lépések egy teljes, termelésre kész megoldást nyújtanak.

## Gyors válaszok
- **Módosíthatom egyes szavak betűszínét?** Igen – iteráljon a `TextRun` objektumokon, és állítsa be a `setFontColor`.
- **Az Aspose.Note lehetővé teszi, hogy a OneNote-ot PDF-ként mentsem?** Természetesen; használja a `document.save("output.pdf")`-t.
- **Milyen Java verzió szükséges?** Java 8 vagy újabb.
- **Támogatott a kiemelés?** Használja a `setHighlight(Color)`-t a `TextStyle`-on.
- **Átalakíthatom a OneNote-ot PDF-re egyetlen sorban?** Nem közvetlenül, de a `save` metódus elvégzi a konverziót.

## Mi az a „set font color java”?

Ez a kifejezés arra utal, hogy programozott módon új betűszínt rendelünk szövegelemekhez egy OneNote-fájlban Java kód használatával. Az Aspose.Note segítségével teljes irányítást kap a stílusattribútumok, például betűszín, kiemelés és méret felett anélkül, hogy megnyitná a OneNote felhasználói felületét.

## Miért változtassuk meg a szövegstílust a OneNote-ban?

- **Javított olvashatóság** – a színes vagy kiemelt szöveg felhívja a figyelmet a kulcsfontosságú pontokra.
- **Márka konzisztencia** – a vállalati színek érvényesítése a megbeszélési jegyzetekben.
- **Export minőség** – a formázott jegyzetek kifinomultnak tűnnek, amikor **konvertálja a OneNote-ot PDF-re** a megosztáshoz.

## Előfeltételek

Az elmélyülés előtt győződjön meg róla, hogy rendelkezik:

1. Alapvető Java programozási ismeretek.  
2. Telepített JDK 8 vagy újabb.  
3. Az Aspose.Note for Java könyvtár hozzáadva a projekthez (Maven/Gradle vagy manuális JAR).  
4. Egy minta OneNote fájl (`Sample1.one`) a kísérletezéshez.

## Csomagok importálása

First, import the classes we’ll need:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## Lépésről‑lépésre útmutató

### 1. lépés: Dokumentum betöltése

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

Betöltjük a OneNote fájlt (`Sample1.one`), hogy az Aspose.Note hozzáférhessen a belső struktúrájához.

### 2. lépés: RichText csomópontok elérése

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

A `RichText` objektumok tartalmazzák a tényleges bekezdéseket. Az első csomópont lekérésével hozzáférést kapunk a formázni kívánt szöveghez.

### 3. lépés: Szövegstílus módosítása (set font color java)

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

A cikluson belül **beállítjuk a betűszínt Java-ban** sárgára, kék kiemelést alkalmazunk (bemutatva a **highlight text onenote** funkciót), és a méretet 20 pontra növeljük, ami a **modify font size onenote** példát mutatja.

### 4. lépés: Dokumentum mentése (save onenote as pdf)

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

`save` meghívása `.pdf` kiterjesztéssel automatikusan **konvertálja a OneNote-ot PDF-re**, így egy megosztható fájlt kap.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| Nincs színváltozás látható | A dokumentum a mentés előtt meg volt nyitva a OneNote-ban | Zárja be a OneNote-ot vagy töltse újra a fájlt a Java folyamat befejezése után |
| Kiemelés nem alkalmazódik | Olyan szín használata, amely megegyezik a háttérrel | Válasszon kontrasztos `Color`-t (pl. `Color.yellow`) |
| `document.save` `IOException`-t dob | Érvénytelen kimeneti útvonal | Győződjön meg róla, hogy a könyvtár létezik, és van írási jogosultsága |

## Gyakran ismételt kérdések

**K: Alkalmazhatom ezeket a stílusváltoztatásokat csak a OneNote-fájl bizonyos szakaszaira?**  
V: Igen – szűrje a `RichText` csomópontokat a szülő `Section` vagy `Page` alapján, mielőtt iterálna a `TextRun`-okon.

**K: A szín, kiemelés és méret mellett milyen egyéb formázásokat kezel az Aspose.Note?**  
V: Megváltoztathatja a betűcsaládot, félkövér/dőlt/aláhúzott, igazítást, sőt a bekezdés távolságát is.

**K: Lehetséges több OneNote-fájl kötegelt feldolgozása?**  
V: Teljesen. A betöltési és stíluslogikát egy ciklusba helyezve feldolgozhatja a mappában lévő minden `.one` fájlt.

**K: Támogatja a könyvtár a közvetlen mentést más formátumokba, például DOCX-be?**  
V: Igen – az Aspose.Note exportálhat PDF, DOCX, HTML és több képformátumba.

**K: Hol találok további példákat és API-referenciát?**  
V: Látogassa meg a hivatalos Aspose.Note dokumentációs oldalt, böngéssze az API-referenciát, és töltse le az ingyenes próbaverziót a gyakorlati teszteléshez.

## Következtetés

Most már rendelkezik egy teljes, vég‑től‑végig példával arra, hogyan **állítsa be a betűszínt Java-ban**, kiemelje a szöveget, módosítsa a betűméretet, és **mentse a OneNote-ot PDF-ként** az Aspose.Note használatával. Nyugodtan módosítsa a kódot, hogy konkrét oldalakat célozzon, feltételes formázást alkalmazzon, vagy integrálja nagyobb dokumentum‑feldolgozó csővezetékekbe.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Utolsó frissítés:** 2026-01-18  
**Tesztelve:** Aspose.Note 24.11 for Java  
**Szerző:** Aspose