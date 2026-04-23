---
date: 2026-02-10
description: Tanulja meg, hogyan konvertálja a OneNote-ot szöveggé, és hogyan nyerjen
  ki képeket az Aspose.Note for Java segítségével. Az útmutató bemutatja, hogyan olvassuk
  be a .one fájlt Java-ban, és hogyan hajtsuk végre a OneNote szövegkinyerést.
linktitle: Convert OneNote to Text and Extract Images using Document Visitor - Java
second_title: Aspose.Note Java API
title: OneNote konvertálása szöveggé és képek kinyerése a Document Visitor használatával
  – Java
url: /hu/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote konvertálása szöveggé és képek kinyerése Document Visitor segítségével – Java

## Bevezetés

Az Aspose.Note for Java megkönnyíti a **OneNote szöveggé konvertálását**, miközben **képeket nyer ki a OneNote jegyzetfüzetekből**. Ebben az útmutatóban egy komplett, gyakorlati példán keresztül mutatjuk be, hogyan töltsünk be egy OneNote fájlt, járjuk be a szerkezetét egy egyedi `DocumentVisitor` segítségével, és nyerjük ki a képeket valamint az egyszerű szöveget. A végére már tudni fogja, hogyan **olvassa be a .one fájlt Java‑ban**, és miért ideális ez a megközelítés automatizált tartalom-migrációhoz vagy jelentéskészítéshez.

## Gyors válaszok
- **Melyik könyvtárra van szükségem?** Aspose.Note for Java (letöltési link alább).  
- **Kizárólag képeket tudok kinyerni?** Igen – valósítsa meg a `VisitImageStart` metódust egy `DocumentVisitor`‑ben.  
- **Hogyan olvassak be egy .one fájlt Java‑ban?** Használja a `new Document(path, new LoadOptions())` kifejezést.  
- **Szükség van licencre a termeléshez?** Kereskedelmi licenc szükséges a nem‑próba használathoz.  
- **Melyik Java verzió támogatott?** JDK 8 vagy újabb.

## Mi az a OneNote konvertálása szöveggé?

A OneNote szöveggé konvertálása azt jelenti, hogy a `.one` jegyzetfüzet nyers szöveges tartalmát kinyerjük, és egyszerű Unicode szövegként mentjük el. Ez akkor hasznos, ha kereshető archívumokra, könnyű adatfolyamokra vagy egyszerű összefoglalókra van szükség az eredeti OneNote formázás nélkül.

## Miért használjuk az Aspose.Note Document Visitor‑t a OneNote szövegkinyeréshez?

- **Finomhangolt vezérlés:** A visitor minta lehetővé teszi, hogy pontosan meghatározza, mely csomópontokat (oldalak, vázlatok, képek, gazdag szöveg) szeretné feldolgozni.  
- **Teljesítmény:** Elkerüli a teljes dokumentum egyetlen blobként való betöltését a memóriába; minden csomópontot igény szerint látogat meg.  
- **Sokoldalúság:** Ugyanaz a visitor kiterjeszthető képek, táblázatok vagy egyedi metaadatok kinyerésére, így egyetlen megoldást nyújt mind a **OneNote szöveggé konvertálásához**, mind a **képek kinyeréséhez**.

## Előfeltételek

Mielőtt elkezdené, győződjön meg róla, hogy rendelkezik:

1. Java Development Kit (JDK) 8 vagy újabb verzióval.  
2. Aspose.Note for Java könyvtárral. Letöltheti **[itt](https://releases.aspose.com/note/java/)**.  
3. Egy OneNote dokumentummal (`.one` fájl), amelyből képeket szeretne kinyerni vagy szöveget konvertálni.

## Csomagok importálása

Először importálja a szükséges osztályokat az Aspose.Note API‑ból.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## 1. lépés: Egyedi Document Visitor létrehozása

Hozzon létre egy osztályt, amely kiterjeszti a `DocumentVisitor`‑t. Ez az osztály minden egyes csomópontnál meghívásra kerül a OneNote dokumentumban, lehetővé téve a **OneNote képek kinyerését** és opcionálisan a szöveg gyűjtését.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## 2. lépés: Visitor metódusok megvalósítása

Adjon felülírást azokhoz a csomóponttípusokhoz, amelyek érdeklik. Az alábbiakban a gazdag szöveget, képeket, címeket, oldalakat, vázlatokat és vázlategységeket kezeljük. A `VisitImageStart` metódusban történik a képek kinyerése.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### Miért kell ezeket a metódusokat megvalósítani?

- **Képek kinyerése a OneNote‑ból:** A `VisitImageStart` közvetlen hozzáférést biztosít a nyers képbyte-okhoz.  
- **OneNote szöveggé konvertálása:** A `VisitRichTextStart` összegyűjti a szöveges tartalmat, lehetővé téve egy egyszerű **OneNote szöveggé konvertálás** műveletet.  
- **.one fájl Java‑ban olvasása:** A visitor minta elrejti a `.one` fájl alacsony szintű szerkezetét, így nem kell magát a bináris formátumot értelmezni.

## 3. lépés: Visitor futtatása a fő metódusból

Töltse be a `.one` fájlt, példányosítsa a visitor‑t, és indítsa el a bejárást.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Gyakori felhasználási esetek

- **Automatizált jelentéskészítés:** Képek és szöveg kinyerése egy OneNote megbeszélés jegyzetfüzetéből PDF vagy HTML összefoglaló generálásához.  
- **Tartalom migráció:** Régi OneNote archívumok konvertálása egyszerű szövegfájlokká indexelés vagy keresőmotorok számára.  
- **Digitális eszközök kinyerése:** Beágyazott képernyőképek, diagramok vagy fényképek gyűjtése további alkalmazásokban való újrafelhasználásra.  

## Hibaelhárítás és tippek

- **Nagy jegyzetfüzetek:** Ha memóriaproblémákba ütközik, dolgozzon oldalanként, ellenőrizve a `VisitPageStart`‑ot, és csak szükség esetén töltse be az oldal‑szintű erőforrásokat.  
- **Képformátumok:** Az `Image` objektum nyers byte‑okat ad vissza; a mentés előtt meg kell határozni a formátumot (PNG, JPEG).  
- **Licenchibák:** Győződjön meg róla, hogy a termelésben beállította az Aspose licencet (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) a dokumentum betöltése előtt.  
- **Képek hatékony kinyerése:** Szűrje a csomópontokat a `VisitImageStart`‑ben méret vagy formátum alapján, ha csak bizonyos típusú képekre van szükség.  

## Gyakran ismételt kérdések

**K: Képes vagyok-e specifikus típusú tartalmat kinyerni a OneNote dokumentumból?**  
V: Igen – csak azokat a visitor metódusokat kell felülírni, amelyekre szüksége van (pl. `VisitImageStart` a képekhez, `VisitRichTextStart` a szöveghez).

**K: Az Aspose.Note for Java kompatibilis-e a különböző OneNote dokumentumverziókkal?**  
V: Teljes mértékben. A könyvtár támogatja az összes fő OneNote fájlverziót, így biztonságosan **olvashat .one fájl Java** projekteket a forrás OneNote verziójától függetlenül.

**K: Integrálhatom-e ezt a kinyerési folyamatot a Java alkalmazásomba?**  
V: Igen. A visitor minta zökkenőmentesen működik bármely Java kódbázisban; csak adja hozzá a könyvtár JAR‑ját, és hívja meg a fenti példát.

**K: Az Aspose.Note for Java támogatja-e a komplex OneNote dokumentumok kezelését?**  
V: Igen. A beágyazott vázlatok, médiák és egyedi adatok mind elérhetők a visitor API‑n keresztül.

**K: Van-e korlátozás a feldolgozható OneNote dokumentum méretére?**  
V: Nincs szigorú határ, de rendkívül nagy jegyzetfüzetek több heap memóriát igényelhetnek; érdemes oldalanként feldolgozni őket.

**K: Hogyan konvertáljam a kinyert szöveget egyszerű szövegfájlba?**  
V: Miután a `myConverter.GetText()` egy `String`‑et ad vissza, írja ki egy fájlba a szokásos Java I/O‑val (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---

**Utolsó frissítés:** 2026-02-10  
**Tesztelt verzió:** Aspose.Note for Java 24.10  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}