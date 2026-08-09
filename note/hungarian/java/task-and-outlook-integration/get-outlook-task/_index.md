---
date: 2026-04-01
description: Tanulja meg, hogyan lehet feladatokat kinyerni az Outlookból a OneNote-ban
  az Aspose.Note for Java segítségével. Kövesse ezt a lépésről‑lépésre útmutatót,
  hogy gyorsan lekérje a feladat részleteit.
keywords:
- how to extract tasks
- Aspose.Note Java
- Outlook task extraction
linktitle: Outlook feladat lekérése a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
title: Outlook feladatok kinyerése a OneNote-ba az Aspose.Note segítségével
url: /hu/java/task-and-outlook-integration/get-outlook-task/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Outlook feladat lekérése a OneNote-ban - Aspose.Note

## Bevezetés
Welcome to our comprehensive guide on **how to extract tasks** from Outlook in a OneNote notebook using Aspose.Note for Java. Whether you’re building a migration tool, generating reports, or simply need to sync task data, this tutorial walks you through every step— from loading the OneNote file to reading each Outlook task’s properties. By the end, you’ll have a ready‑to‑use code snippet that you can adapt to your own projects.

## Gyors válaszok
- **Mit fed le ez a bemutató?** Extracting Outlook task details from a OneNote document with Aspose.Note for Java.  
- **Melyik API-t használja?** Aspose.Note Java library.  
- **Szükségem van licencre?** A free trial works for development; a commercial license is required for production.  
- **Mennyi időt vesz igénybe a megvalósítás?** About 10‑15 minutes once the environment is set up.  
- **Feldolgozhatok több jegyzetfüzetet?** Yes—just loop over files and reuse the same logic.

## Mi a feladatkinyerés?
Task extraction refers to reading structured task information (such as due dates, status, and icons) that Outlook stores inside OneNote pages as `NoteTask` tags. This enables programmatic access to task metadata without manual copying.

## Miért használjuk az Aspose.Note-ot Java-hoz?
- **No Microsoft Office required** – works on any platform with a Java runtime.  
- **Full fidelity** – preserves all OneNote elements while giving you direct access to tags.  
- **High performance** – optimized for large notebooks and batch processing.  

## Előfeltételek
Before we dive in, make sure you have the following ready:

- **Java fejlesztői környezet** – JDK 8 vagy újabb telepítve és konfigurálva.  
- **Aspose.Note könyvtár** – Download the latest Java package from the official site [here](https://releases.aspose.com/note/java/).  
- **Minta OneNote fájl** – The tutorial uses `Sample1.one`; you can replace it with any notebook that contains Outlook tasks.

## Csomagok importálása
Add the required imports to your Java class. These classes give you access to the document model and the Outlook‑specific `NoteTask` tag.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```

## Lépésről‑lépésre útmutató

### 1. lépés: Dokumentum könyvtár beállítása
Define the folder that holds your OneNote file. Using an absolute or relative path works, but keep the path string tidy for readability.

```java
String dataDir = "Your Document Directory";
```

### 2. lépés: OneNote dokumentum betöltése
Create a `Document` instance by pointing to the `.one` file. Aspose.Note parses the file into a DOM‑like structure you can traverse.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### 3. lépés: Az összes RichText csomópont lekérése
Outlook tasks are stored inside `RichText` elements. Retrieve every `RichText` node so you can inspect its tags.

```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```

### 4. lépés: Minden csomópont bejárása
Loop through each `RichText` node, examine its tags, and act when you encounter a `NoteTask`. The code below prints the most useful properties for each task.

```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Retrieve properties
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```

**Pro tipp:** If you only need a subset of properties, you can skip the others to improve performance when processing large notebooks.

### Gyakori problémák és megoldások
- **Nincsenek feladatok:** Ensure the OneNote page actually contains Outlook tasks. They appear as check‑boxes with a small Outlook icon.  
- **Null értékek:** Some task fields (e.g., `CompletedTime`) may be `null` if the task hasn’t been completed. Guard against `NullPointerException` by checking for `null` before printing.  
- **Fájl nem található:** Verify that `dataDir` ends with the appropriate path separator (`/` or `\\`) for your OS.

## Következtetés
Congratulations! You’ve learned **how to extract tasks** from Outlook in OneNote using the Aspose.Note Java API. This approach gives you full programmatic control over task data, enabling integration with custom reporting tools, databases, or other business workflows.

## Gyakran ismételt kérdések

**K:** Az Aspose.Note kompatibilis az összes OneNote verzióval?  
**V:** Aspose.Note supports Microsoft OneNote 2010 and later versions.

**K:** Használhatom az Aspose.Note-ot személyes és kereskedelmi projektekhez is?  
**V:** Yes, Aspose.Note can be used for both personal and commercial projects. Visit [here](https://purchase.aspose.com/buy) to explore licensing options.

**K:** Van ingyenes próba a Aspose.Note-hoz?  
**V:** Yes, you can access the free trial [here](https://releases.aspose.com/).

**K:** Hogyan kaphatok támogatást az Aspose.Note-hoz?  
**V:** Visit the [Aspose.Note Forum](https://forum.aspose.com/c/note/28) for community support. For additional assistance, consider purchasing a [temporary license](https://purchase.aspose.com/temporary-license/).

**K:** Van elérhető minta OneNote dokumentum teszteléshez?  
**V:** You can find sample documents in the Aspose.Note documentation [here](https://reference.aspose.com/note/java/).

---

**Utolsó frissítés:** 2026-04-01  
**Tesztelve:** Aspose.Note for Java 24.12 (latest at time of writing)  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}