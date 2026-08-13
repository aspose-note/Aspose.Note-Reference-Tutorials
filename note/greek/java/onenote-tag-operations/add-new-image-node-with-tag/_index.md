---
date: 2026-08-13
description: Μάθετε πώς να εισάγετε εικόνα στο OneNote, να προσθέσετε ετικέτα στην
  εικόνα και να αποθηκεύσετε το OneNote ως PDF χρησιμοποιώντας το Aspose.Note για
  Java.
keywords:
- insert image into onenote
- save onenote as pdf
- java add tag to image
lastmod: 2026-08-13
linktitle: Προσθήκη ετικέτας σε εικόνα στο OneNote – Aspose.Note
og_description: Εισαγάγετε εικόνα στο OneNote, προσθέστε μια κίτρινη-αστέρι ετικέτα
  στην εικόνα και εξάγετε το σημειωματάριο ως PDF χρησιμοποιώντας το Aspose.Note για
  Java. Ακολουθήστε τον οδηγό βήμα-βήμα για γρήγορη υλοποίηση.
og_image_alt: Guide showing how to insert an image and tag it in OneNote using Aspose.Note
  for Java
og_title: Εισαγωγή εικόνας στο OneNote και προσθήκη ετικέτας – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to insert image into OneNote, add a tag to the image, and
    save OneNote as PDF using Aspose.Note for Java.
  headline: Insert image into OneNote and add tag with Aspose.Note – Java
  type: TechArticle
- description: Learn how to insert image into OneNote, add a tag to the image, and
    save OneNote as PDF using Aspose.Note for Java.
  name: Insert image into OneNote and add tag with Aspose.Note – Java
  steps:
  - name: create document object
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      OneNote notebook in memory. After instantiation, all subsequent operations flow
      through this object.
  - name: initialize page class object
    text: The `Page` class defines a single page inside the notebook. You can set
      page properties such as title and size before adding content.
  - name: initialize outline class object
    text: The `Outline` class groups related content blocks on a page. Outlines are
      containers for `OutlineElement` objects.
  - name: initialize outline element class object
    text: The `OutlineElement` class represents an individual block inside an outline,
      such as a paragraph, image, or table.
  - name: load and insert image
    text: '*(This step demonstrates **insert image into OneNote**)* The `Image` class
      encapsulates image data to be placed on a OneNote page.'
  - name: add note tag to image
    text: '*(Here we answer **how to add image tag**)* The `NoteTag` class defines
      a visual tag that can be attached to page elements.'
  - name: add outline element node
    text: Attach the image (now tagged) to the outline element so it appears in the
      correct order on the page.
  - name: add outline node
    text: Insert the outline into the page’s collection of outlines.
  - name: add page node
    text: Add the fully built page to the document’s page collection.
  type: HowTo
- questions:
  - answer: You can find the documentation at the **[Aspose.Note Java API reference](https://reference.aspose.com/note/java/)**.
    question: Where can I find Aspose.Note documentation?
  - answer: You can download it from the releases page **[Aspose.Note Java release
      page](https://releases.aspose.com/note/java/)**.
    question: How do I download Aspose.Note for Java?
  - answer: Yes, you can access the free trial at the **[Aspose free trial page](https://releases.aspose.com/)**.
    question: Is there a free trial available?
  - answer: Visit the community forum **[Aspose.Note community forum](https://forum.aspose.com/c/note/28)**
      for support.
    question: Where can I get support for Aspose.Note?
  - answer: If required, you can obtain a temporary license from the **[temporary
      license request page](https://purchase.aspose.com/temporary-license/)**.
    question: Do I need a temporary license?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote automation
- aspose.note java
- insert image into onenote
- add tag to image
- export onenote pdf
title: Εισαγωγή εικόνας στο OneNote και προσθήκη ετικέτας με το Aspose.Note – Java
url: /el/java/onenote-tag-operations/add-new-image-node-with-tag/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εισαγωγή εικόνας στο OneNote και προσθήκη ετικέτας με Aspose.Note – Java

## Εισαγωγή
Αν χρειάζεστε **εισαγωγή εικόνας στο OneNote** ενώ εργάζεστε με Java, το Aspose.Note κάνει όλη τη διαδικασία απλή. Σε αυτό το tutorial θα περάσουμε από την εισαγωγή μιας εικόνας σε μια σελίδα OneNote, την εφαρμογή μιας ετικέτας κίτρινου αστεριού στην εικόνα, και τελικά **αποθήκευση OneNote ως PDF**. Στο τέλος θα δείτε ακριβώς πώς να προσθέσετε ετικέτα σε εικόνα, να εισάγετε εικόνα στο OneNote και να μετατρέψετε το OneNote σε PDF—όλα με λίγες γραμμές κώδικα.

## Γρήγορες απαντήσεις
- **Τι σημαίνει “προσθήκη ετικέτας σε εικόνα”;** Καρφώνει μια οπτική ετικέτα σημειώματος (π.χ., ένα κίτρινο αστέρι) σε έναν κόμβο εικόνας σε μια σελίδα OneNote.  
- **Ποια βιβλιοθήκη το διαχειρίζεται;** Aspose.Note for Java.  
- **Χρειάζομαι άδεια για δοκιμή;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.  
- **Μπορώ να εξάγω το αποτέλεσμα ως PDF;** Ναι – χρησιμοποιήστε `doc.save(..., SaveFormat.Pdf)` για **αποθήκευση OneNote ως PDF**.  
- **Πόσο χρόνο διαρκεί η υλοποίηση;** Συνήθως λιγότερο από 10 λεπτά για ένα βασικό σενάριο.

## Τι είναι η “προσθήκη ετικέτας σε εικόνα” στο OneNote;
Το στοιχείο `NoteTag` είναι ένα αντικείμενο μεταδεδομένων που επισημαίνει οπτικά μια εικόνα με ένα εικονίδιο όπως αστέρι ή σημαία. Εμφανίζεται στη διεπαφή του OneNote και μπορεί να αναζητηθεί ή να φιλτραριστεί, επιτρέποντας στους χρήστες να εντοπίζουν γρήγορα τις επισημασμένες εικόνες σε μεγάλα σημειωματάρια.

## Γιατί να προσθέσετε ετικέτα σε εικόνα στο OneNote;
Η επισήμανση εικόνων παρέχει έναν ελαφρύ τρόπο προσθήκης πλαισίου χωρίς να τροποποιείται η ίδια η εικόνα. Οι ετικέτες αποθηκεύονται ως μέρος της δομής της σελίδας, επιτρέποντας γρήγορες αναζητήσεις, οπτικές ενδείξεις και κατηγοριοποίηση, κάτι που είναι ιδιαίτερα χρήσιμο στην έρευνα, την παρακολούθηση έργων ή τα εκπαιδευτικά σημειωματάρια.

- Οργανώστε το οπτικό περιεχόμενο χωρίς να τροποποιήσετε την εικόνα.  
- Εντοπίστε γρήγορα σημαντικά γραφικά χρησιμοποιώντας την αναζήτηση ετικετών του OneNote.  
- Παρέχετε πλαίσιο (π.χ., “επιθεώρηση αργότερα”, “σημαντική αναφορά”) απευθείας στη σελίδα.  

## Προαπαιτούμενα
Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

1. Aspose.Note for Java: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.Note. Αν όχι, μπορείτε να τη κατεβάσετε από τη **[Aspose.Note for Java download page](https://releases.aspose.com/note/java/)**.  
2. Περιβάλλον ανάπτυξης Java: Ένα λειτουργικό JDK (8 ή νεότερο) και ένα IDE ή εργαλείο κατασκευής της επιλογής σας.  

Τώρα που έχουμε τα προαπαιτούμενα, ας προχωρήσουμε στα επόμενα βήματα.

## Εισαγωγή πακέτων
Στο έργο Java, ξεκινήστε εισάγοντας τα απαραίτητα πακέτα:

Η κλάση `Document` αντιπροσωπεύει ένα σημειωματάριο OneNote στη μνήμη.  
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```

## Πώς να εισάγετε εικόνα στο OneNote;

Φορτώστε το αρχείο εικόνας-στόχο, δημιουργήστε έναν κόμβο `Image` και προσθέστε τον στο περίγραμμα της σελίδας. Η εισαγωγή απαιτεί μόνο τρεις κλήσεις API και διατηρεί την αρχική ανάλυση της εικόνας. Αυτή η προσέγγιση λειτουργεί για μορφές PNG, JPEG, BMP και GIF χωρίς πρόσθετη μετατροπή.

### Βήμα 1: δημιουργία αντικειμένου εγγράφου
Η κλάση `Document` είναι το κορυφαίο αντικείμενο του Aspose.Note που αντιπροσωπεύει ένα σημειωματάριο OneNote στη μνήμη. Μετά τη δημιουργία, όλες οι επόμενες λειτουργίες περνούν μέσω αυτού του αντικειμένου.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
```

### Βήμα 2: αρχικοποίηση αντικειμένου κλάσης σελίδας
Η κλάση `Page` ορίζει μια μοναδική σελίδα μέσα στο σημειωματάριο. Μπορείτε να ορίσετε ιδιότητες σελίδας όπως τίτλο και μέγεθος πριν προσθέσετε περιεχόμενο.

```java
// initialize Page class object
Page page = new Page();
```

### Βήμα 3: αρχικοποίηση αντικειμένου κλάσης outline
Η κλάση `Outline` ομαδοποιεί σχετιζόμενα μπλοκ περιεχομένου σε μια σελίδα. Τα outlines είναι δοχεία για αντικείμενα `OutlineElement`.

```java
// initialize Outline class object
Outline outline = new Outline();
```

### Βήμα 4: αρχικοποίηση αντικειμένου κλάσης outline element
Η κλάση `OutlineElement` αντιπροσωπεύει ένα μεμονωμένο μπλοκ μέσα σε ένα outline, όπως παράγραφο, εικόνα ή πίνακα.

```java
// initialize OutlineElement class object
OutlineElement outlineElem = new OutlineElement();
```

## Πώς να προσθέσετε ετικέτα σε εικόνα στο OneNote;

Δημιουργήστε ένα αντικείμενο `NoteTag`, ρυθμίστε τον τύπο του (π.χ., κίτρινο αστέρι) και συνδέστε το με τον προηγουμένως δημιουργημένο κόμβο `Image`. Η ετικέτα γίνεται μέρος των μεταδεδομένων της εικόνας και αποδίδεται αυτόματα από το OneNote.

Για να συνδέσετε μια ετικέτα, δημιουργήστε ένα αντικείμενο `NoteTag`, ορίστε το `TagIcon` στο επιθυμητό σύμβολο (για παράδειγμα, `TagIcon.YellowStar`) και συνδέστε το με τον κόμβο `Image` χρησιμοποιώντας τη μέθοδο `addTag`. Η ετικέτα γίνεται μέρος των μεταδεδομένων της εικόνας και αποδίδεται αυτόματα από το OneNote.

### Βήμα 5: φόρτωση και εισαγωγή εικόνας  
*(Αυτό το βήμα δείχνει **εισαγωγή εικόνας στο OneNote**)*  
Η κλάση `Image` περιλαμβάνει τα δεδομένα εικόνας που θα τοποθετηθούν σε μια σελίδα OneNote.  
```java
// load an image
Image image = new Image(dataDir + "Input.jpg");
// insert image in the document node
outlineElem.appendChildLast(image);
```

### Βήμα 6: προσθήκη note tag σε εικόνα  
*(Εδώ απαντάμε **πώς να προσθέσετε ετικέτα εικόνας**)*  
Η κλάση `NoteTag` ορίζει μια οπτική ετικέτα που μπορεί να συνδεθεί με στοιχεία της σελίδας.  
```java
// add a yellow star note tag to the image
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```

### Βήμα 7: προσθήκη κόμβου στοιχείου outline
Συνδέστε την εικόνα (τώρα με ετικέτα) στο στοιχείο outline ώστε να εμφανίζεται με τη σωστή σειρά στη σελίδα.

```java
// add outline element node
outline.appendChildLast(outlineElem);
```

### Βήμα 8: προσθήκη κόμβου outline
Εισάγετε το outline στη συλλογή outlines της σελίδας.

```java
// add outline node
page.appendChildLast(outline);
```

### Βήμα 9: προσθήκη κόμβου σελίδας
Προσθέστε τη πλήρως κατασκευασμένη σελίδα στη συλλογή σελίδων του εγγράφου.

```java
// add page node
doc.appendChildLast(page);
```

## Πώς να αποθηκεύσετε το OneNote ως PDF;

Καλέστε τη μέθοδο `save` στο αντικείμενο `Document`, καθορίζοντας `SaveFormat.Pdf`. Το Aspose.Note μετατρέπει όλα τα στοιχεία της σελίδας—συμπεριλαμβανομένων εικόνων, ετικετών και outlines—σε μια ακριβή αναπαράσταση PDF χωρίς να απαιτείται η εγκατάσταση του Microsoft OneNote.

Η απαρίθμηση `SaveFormat` καθορίζει τη μορφή εξόδου για την αποθήκευση ενός εγγράφου.  
```java
// save OneNote document as a PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```

Συγχαρητήρια! Έχετε προσθέσει επιτυχώς **ετικέτα σε εικόνα**, εισάγει μια εικόνα στο OneNote και εξάγει το σημειωματάριο σε PDF χρησιμοποιώντας το Aspose.Note for Java.

## Κοινά προβλήματα και λύσεις
| Πρόβλημα | Λύση |
|----------|------|
| **Η εικόνα δεν εμφανίζεται** | Επαληθεύστε ότι η διαδρομή στο `dataDir + "Input.jpg"` είναι σωστή και το αρχείο είναι προσβάσιμο. |
| **Η ετικέτα δεν είναι ορατή** | Βεβαιωθείτε ότι χρησιμοποιείτε μια έκδοση του OneNote που υποστηρίζει ετικέτες σημειώματος (οι πιο πρόσφατες εκδόσεις το κάνουν). |
| **Η έξοδος PDF είναι κενή** | Ελέγξτε ότι το έγγραφο περιέχει τουλάχιστον μία σελίδα/outline πριν καλέσετε το `save`. |

## Συχνές ερωτήσεις

**Q: Πού μπορώ να βρω την τεκμηρίωση του Aspose.Note;**  
A: Μπορείτε να βρείτε την τεκμηρίωση στη **[Aspose.Note Java API reference](https://reference.aspose.com/note/java/)**.

**Q: Πώς να κατεβάσω το Aspose.Note for Java;**  
A: Μπορείτε να το κατεβάσετε από τη σελίδα κυκλοφορίας **[Aspose.Note Java release page](https://releases.aspose.com/note/java/)**.

**Q: Υπάρχει διαθέσιμη δωρεάν δοκιμή;**  
A: Ναι, μπορείτε να αποκτήσετε πρόσβαση στη δωρεάν δοκιμή στη **[Aspose free trial page](https://releases.aspose.com/)**.

**Q: Πού μπορώ να λάβω υποστήριξη για το Aspose.Note;**  
A: Επισκεφθείτε το φόρουμ κοινότητας **[Aspose.Note community forum](https://forum.aspose.com/c/note/28)** για υποστήριξη.

**Q: Χρειάζομαι προσωρινή άδεια;**  
A: Εάν απαιτείται, μπορείτε να αποκτήσετε προσωρινή άδεια από τη **[temporary license request page](https://purchase.aspose.com/temporary-license/)**.

## Συμπέρασμα
Η εξοικείωση με το Aspose.Note for Java ανοίγει συναρπαστικές δυνατότητες στη διαχείριση εγγράφων OneNote. Ακολουθώντας αυτό το tutorial, έχετε μάθει **πώς να προσθέσετε ετικέτα σε εικόνα**, **να εισάγετε εικόνα στο OneNote**, και **να αποθηκεύσετε το OneNote ως PDF**—δεξιότητες που μπορείτε να εφαρμόσετε σε μια ευρεία γκάμα έργων αυτοματοποίησης. Συνεχίστε να εξερευνάτε την τεκμηρίωση του Aspose.Note στη **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)** για πιο προχωρημένα χαρακτηριστικά και δυνατότητες.

---

**Τελευταία ενημέρωση:** 2026-08-13  
**Δοκιμή με:** Aspose.Note 24.11 for Java  
**Συγγραφέας:** Aspose

## Σχετικά μαθήματα

- [Πώς να προσθέσετε εικόνα στο OneNote χρησιμοποιώντας Java – Δημιουργία εγγράφου και εισαγωγή εικόνας](/note/java/onenote-hyperlinks-images/build-doc-insert-image/)
- [Πώς να αποθηκεύσετε το OneNote ως PDF με Aspose.Note for Java](/note/java/onenote-document-loading/load-save-format/)
- [Εισαγωγή γραμμής πίνακα Java - Προσθήκη κόμβου πίνακα με ετικέτα στο OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}