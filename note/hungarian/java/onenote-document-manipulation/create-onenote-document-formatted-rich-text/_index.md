---
date: 2026-02-18
description: Ismerje meg, hogyan hozhat létre OneNote dokumentumot, formázhat gazdag
  szöveget, és menthet PDF‑ként Java‑ban az Aspose.Note használatával. Lépésről‑lépésre
  útmutató a zökkenőmentes automatizáláshoz.
linktitle: Create OneNote document and save as PDF in Java
second_title: Aspose.Note Java API
title: OneNote dokumentum létrehozása és PDF‑ként mentése Java‑ban
url: /hu/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote dokumentum létrehozása és PDF-ként mentése Java-ban

## Bevezetés

Ha **OneNote dokumentumot** kell **létrehoznod** és **OneNote-ot PDF‑ként mentened**, miközben megőrzöd a gazdag szövegformázást, jó helyen jársz. Ebben az útmutatóban végigvezetünk a OneNote dokumentum létrehozásán, egyéni stílusok alkalmazásán, és a közvetlen PDF‑exporton az Aspose.Note for Java segítségével. A végére egy újrahasználható kódrészletet kapsz, amelyet bármely Java projektbe beilleszthetsz a kifinomult OneNote‑PDF konverziók automatizálásához.

## Gyors válaszok
- **Ez az útmutató mit tanít?** Hogyan kell OneNote dokumentumot létrehozni stílusos szöveggel, és PDF‑ként menteni.  
- **Melyik könyvtár szükséges?** Aspose.Note for Java (letölthető a hivatalos oldalról).  
- **Szükségem van licencre?** Ideiglenes licenc teszteléshez elegendő; teljes licenc szükséges a termeléshez.  
- **Milyen IDE-t használhatok?** Bármely Java IDE—IntelliJ IDEA, Eclipse vagy NetBeans.  
- **Megváltoztathatom a kimeneti formátumot?** Igen, az Aspose.Note támogatja a PDF, HTML, PNG és további formátumokat.

## Mi az a „OneNote PDF‑ként mentése”?
A OneNote PDF‑ként mentése azt jelenti, hogy a OneNote oldal struktúráját – beleértve a szöveget, képeket és formázást – egy statikus PDF fájlba konvertáljuk, amely bármely platformon megtekinthető anélkül, hogy a OneNote-ra szükség lenne.

## Miért formázzuk a gazdag szöveget Java-ban?
A **gazdag szöveg formázásának** közvetlen alkalmazása Java-ban lehetővé teszi, hogy professzionális megjelenésű dokumentumokat generálj, amelyek megfelelnek a márka irányelveinek, manuális szerkesztés nélkül.

## Előfeltételek

1. **Java Development Kit (JDK)** – bármely friss verzió (8 vagy újabb).  
2. **Aspose.Note for Java JAR** – töltsd le a [letöltési hivatkozás](https://releases.aspose.com/note/java/) segítségével.  
3. **IDE** – IntelliJ IDEA, Eclipse vagy bármely kedvelt szerkesztő.  

## Csomagok importálása

Mielőtt elkezdenénk, importáld a szükséges osztályokat a Java fájlodba:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## OneNote dokumentum létrehozása – Lépésről‑lépésre útmutató

### 1. lépés: Dokumentum és oldal beállítása

Inicializáld a `Document` és `Page` objektumokat, amelyek a teljes tartalmat tárolják:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### 2. lépés: Cím létrehozása formázással

Adj hozzá egy cím elemet, és alkalmazz **set paragraph style**‑t a megjelenés szabályozásához:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

### 3. lépés: Gazdag szöveg létrehozása formázással

Itt gazdag‑szöveges tartalmat építünk több `TextStyle` objektummal, hogy bemutassuk a **gazdag szöveg formázását**:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

### 4. lépés: Elemek hozzáadása az oldalhoz és a dokumentumhoz

Kombináld a címet és a gazdag szöveget az oldal hierarchiájába:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### 5. lépés: Dokumentum mentése – OneNote PDF exportálása

Végül exportáld a OneNote dokumentumot PDF fájlként:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Gyakori problémák és megoldások

| Probléma | Megoldás |
|----------|----------|
| **Fájl nem található** | Ellenőrizd, hogy a `dataDir` egy létező mappára mutat, és van írási jogosultságod. |
| **Hiányzó betűkészletek** | Győződj meg arról, hogy a hivatkozott betűk (pl. *Calibri*) telepítve vannak a gépen. |
| **Licenc nincs alkalmazva** | Töltsd be az Aspose licencet a `Document` létrehozása előtt, hogy elkerüld a kiértékelési vízjeleket. |

## Gyakran ismételt kérdések

**K: Testreszabhatom a betűstílusokat tovább?**  
V: Igen, a `TextStyle` és `ParagraphStyle` osztályok segítségével további tulajdonságokat, például aláhúzást, áthúzást és szövegigazítást is beállíthatsz.

**K: Az Aspose.Note for Java kompatibilis minden Java IDE-vel?**  
V: Teljesen. Amennyiben az IDE támogatja a standard Java fejlesztést, hozzáadhatod az Aspose.Note JAR‑t a projekt classpath‑jához.

**K: Integrálhatom ezt a funkciót webalkalmazásokba?**  
V: Igen, ugyanaz a kód működik servlet‑alapú vagy Spring Boot alkalmazásokban is, lehetővé téve a dinamikus OneNote‑PDF generálást a szerver oldalon.

**K: Vannak licencelési követelmények az Aspose.Note for Java használatához?**  
V: Kereskedelmi licenc szükséges a termeléshez. Ideiglenes licenc elérhető értékeléshez és teszteléshez.

**K: Támogatja az Aspose.Note for Java más dokumentumformátumokat is a OneNote-on kívül?**  
V: Igen, támogatja a PDF, HTML, PNG, JPEG és több exportformátumot, így rugalmasan konvertálhatod a OneNote oldalakat a szükséges formátumba.

## Következtetés

Ebben az útmutatóban bemutattuk, hogyan **hozz létre OneNote dokumentumot**, alkalmazz **gazdag szövegformázást**, és **mentsd OneNote‑ot PDF‑ként** az Aspose.Note for Java segítségével. A lépésről‑lépésre leírtak követésével automatizálhatod a kifinomult OneNote dokumentumok létrehozását és PDF‑re konvertálását bármely Java‑alapú megoldásban.

---

**Utolsó frissítés:** 2026-02-18  
**Tesztelve:** Aspose.Note for Java 24.11 (a legújabb a kiadás időpontjában)  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}