---
date: 2025-12-20
description: Lär dig hur du lägger till bild i OneNote med Aspose.Note för Java. Steg‑för‑steg‑guide
  för att skapa OneNote‑dokument och infoga bilder programatiskt.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Hur man lägger till bild i OneNote med Java – Skapa dokument och infoga bild
url: /sv/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man lägger till bild i OneNote med Java – Skapa dokument och infoga bild

## Introduktion

I den här handledningen lär du dig **hur man lägger till bild i OneNote** med hjälp av Aspose.Note Java‑API. Vi går igenom hur du skapar ett OneNote‑dokument från grunden, infogar en bild och sparar resultatet som PDF. Oavsett om du bygger ett rapportverktyg, automatiserar anteckningsföring eller bara behöver bädda in grafik programatiskt, ger den här guiden dig en tydlig, praktisk väg.

## Snabba svar
- **Vilket bibliotek behövs?** Aspose.Note för Java.  
- **Kan jag infoga vilket bildformat som helst?** JPEG, PNG, BMP, GIF och fler stöds.  
- **Vilka utdataformat finns tillgängliga?** Du kan spara som OneNote, PDF, XPS, HTML osv.  
- **Behöver jag en licens för produktion?** Ja, en kommersiell licens krävs för icke‑testanvändning.  
- **Är koden plattformsoberoende?** Absolut – Java körs på Windows, Linux och macOS.  

## Vad betyder “add picture to OneNote”?
Att lägga till en bild i OneNote innebär att programatiskt bädda in en bildfil i en OneNote‑sida så att den visas tillsammans med text, konturer eller andra element. Aspose.Note‑API:t abstraherar OneNote‑filformatet, så att du kan fokusera på innehållet istället för den underliggande XML‑strukturen.

## Varför lägga till bild i OneNote med Java?
- **Automatisering:** Generera mötesprotokoll med skärmdumpar automatiskt.  
- **Konsistens:** Säkerställ att varje sida följer samma layout och varumärkesprofil.  
- **Integration:** Kombinera data från andra system (t.ex. diagram) direkt i OneNote‑anteckningsböcker.  
- **Plattformsoberoende:** Java låter dig köra samma kod på vilken server‑ eller skrivbordsmiljö som helst.  

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. **Java Development Kit (JDK)** – någon aktuell version (8 eller senare).  
2. **Aspose.Note för Java‑bibliotek** – ladda ner det från [webbplatsen](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse eller någon annan Java‑kompatibel editor du föredrar.  

## Importera paket

Börja med att importera de nödvändiga klasserna i din Java‑källfil:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Steg‑för‑steg‑guide

### Steg 1: Skapa dokumentet

Skapa ett nytt OneNote‑dokument och en sidbehållare där innehållet ska ligga.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Steg 2: Initiera konturen

En *outline* fungerar som en behållare för element såsom text och bilder. Vi sätter dess offset till noll så att innehållet börjar i det övre‑vänstra hörnet.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Steg 3: Ladda och justera bilden

Ladda bilden du vill bädda in och justera den till högra sidan av sidan. Här lägger vi faktiskt **till bild i OneNote**.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Steg 4: Fäst bilden i ett Outline‑element

Bunta in bilden i ett `OutlineElement`. Detta steg länkar det visuella objektet till dokumentets outline‑hierarki.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Steg 5: Bygg upp dokumentstrukturen

Lägg till outline‑elementet i outline‑en, fäst sedan outline‑en på sidan och slutligen lägg till sidan i dokumentet.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Steg 6: Spara OneNote‑dokumentet

Spara dokumentet på disk. I detta exempel exporterar vi till PDF, men du kan också spara som en inbyggd OneNote‑fil (`.one`) genom att ändra `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Vanliga problem och lösningar

| Problem | Varför det händer | Lösning |
|---------|-------------------|---------|
| **Bild visas inte** | Fel filväg eller format som inte stöds. | Kontrollera att `dataDir` pekar på rätt mapp och använd ett stödformat (JPEG, PNG osv.). |
| **Dokument sparas som tom PDF** | Outline‑offset har satts felaktigt. | Se till att `setVerticalOffset(0)` och `setHorizontalOffset(0)` anropas, eller justera offset så att innehållet ligger inom sidans gränser. |
| **IOException vid sparning** | Målmappen finns inte eller saknar skrivbehörighet. | Skapa mappen i förväg eller kör programmet med rätt behörigheter. |

## Vanliga frågor

**Q1: Var kan jag hitta dokumentationen för Aspose.Note för Java?**  
A1: Du kan komma åt dokumentationen [här](https://reference.aspose.com/note/java/).

**Q2: Hur laddar jag ner Aspose.Note för Java?**  
A2: Du kan ladda ner Aspose.Note för Java från [nedladdningssidan](https://releases.aspose.com/note/java/).

**Q3: Finns det en gratis provversion av Aspose.Note för Java?**  
A3: Ja, du kan få en gratis provversion från [webbplatsen](https://releases.aspose.com/).

**Q4: Vart kan jag få support för Aspose.Note för Java?**  
A4: För support, besök [Aspose.Note‑forumet](https://forum.aspose.com/c/note/28).

**Q5: Kan jag få en tillfällig licens för Aspose.Note för Java?**  
A5: Ja, du kan begära en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

---

**Senast uppdaterad:** 2025-12-20  
**Testad med:** Aspose.Note för Java 24.12 (senaste)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}