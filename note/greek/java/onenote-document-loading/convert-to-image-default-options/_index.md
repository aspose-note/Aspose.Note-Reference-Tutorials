---
date: 2026-08-23
description: Μάθετε πώς να μετατρέψετε το OneNote σε PNG χρησιμοποιώντας το Aspose.Note
  for Java με default settings. Αυτός ο step‑by‑step guide δείχνει τη μετατροπή σε
  image, PDF, και τη ρύθμιση της image resolution.
keywords:
- convert onenote to png
- convert onenote to pdf
- set image resolution java
- Aspose.Note Java
- OneNote image conversion
lastmod: 2026-08-23
linktitle: Πώς να μετατρέψετε το OneNote σε PNG χρησιμοποιώντας default options σε
  Java
og_description: Μετατρέψτε το OneNote σε PNG με το Aspose.Note for Java. Ακολουθήστε
  αυτό το concise tutorial για να μετατρέψετε αρχεία .one σε high‑quality images,
  PDFs, και να ελέγξετε τη resolution.
og_image_alt: Guide showing Java code converting OneNote to PNG with Aspose.Note
og_title: Μετατρέψτε το OneNote σε PNG χρησιμοποιώντας default options σε Java
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to convert OneNote to PNG using Aspose.Note for Java with
    default settings. This step‑by‑step guide shows conversion to image, PDF, and
    setting image resolution.
  headline: How to convert OneNote to PNG using default options in Java
  type: TechArticle
- questions:
  - answer: Yes. Iterate over `Document.getPages()` and call `save` for each page,
      providing a unique file name.
    question: Can I convert a multi‑page OneNote notebook to separate images?
  - answer: 'Use `ImageSaveOptions` to set DPI before saving: `ImageSaveOptions options
      = new ImageSaveOptions(SaveFormat.Png); options.setResolution(300); document.save("out.png",
      options);` This is the recommended way to **set image resolution java**.'
    question: How do I change the image resolution?
  - answer: Absolutely. Replace `SaveFormat.Gif` with `SaveFormat.Pdf` to generate
      a PDF document.
    question: Is it possible to convert OneNote directly to PDF instead of an image?
  - answer: No. The trial version produces full‑quality images without watermarks;
      a license is only required for commercial deployment.
    question: Does the free trial impose watermarks on the output images?
  - answer: GIF and JPEG typically produce smaller files than PNG, but choose based
      on quality needs—PNG is lossless, while JPEG is lossy.
    question: Which image format gives the smallest file size?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- convert onenote
- Aspose.Note
- Java document processing
title: Πώς να μετατρέψετε το OneNote σε PNG χρησιμοποιώντας default options σε Java
url: /el/java/onenote-document-loading/convert-to-image-default-options/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να μετατρέψετε το OneNote σε PNG χρησιμοποιώντας τις προεπιλεγμένες επιλογές σε Java

## Εισαγωγή

Η μετατροπή του OneNote σε PNG είναι μια συχνή απαίτηση όταν χρειάζεστε στατικές προεπισκοπήσεις, μικρογραφίες ή αρχειακές εικόνες των σελίδων του σημειωματάριου. Σε αυτό το tutorial θα μάθετε πώς να **convert OneNote to PNG** χρησιμοποιώντας το Aspose.Note for Java με τις προεπιλεγμένες ρυθμίσεις της βιβλιοθήκης. Στο τέλος θα μπορείτε να δημιουργήσετε αρχεία PNG με λίγες γραμμές κώδικα, να καταλάβετε πώς να μεταβείτε σε PDF και να μάθετε πώς να ορίσετε την ανάλυση της εικόνας όταν χρειάζεται—όλα χωρίς την εγκατάσταση του Microsoft Office.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται τη μετατροπή OneNote σε Java;** Aspose.Note for Java.  
- **Μπορώ να μετατρέψω το OneNote σε PNG χωρίς επιπλέον ρυθμίσεις;** Ναι—οι προεπιλεγμένες επιλογές εξάγουν αυτόματα PNG, GIF, JPEG, κ.λπ.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποια έκδοση Java απαιτείται;** Java 8 ή νεότερη.  
- **Είναι η μετατροπή αρκετά γρήγορη για επεξεργασία παρτίδας;** Ναι—η Aspose.Note επεξεργάζεται τα έγγραφα στη μνήμη, κάνοντας τις μαζικές μετατροπές αποδοτικές.

## Τι είναι η “μετατροπή OneNote σε εικόνα”;

Η μετατροπή OneNote σε εικόνα σημαίνει την απόδοση κάθε σελίδας ενός αρχείου `.one` ως raster γραφικό, όπως PNG, GIF ή JPEG. Αυτή η μετατροπή δημιουργεί ένα στιγμιότυπο pixel‑perfect της αρχικής σελίδας, διατηρώντας τις γραμματοσειρές, τα χρώματα και τη διάταξη ώστε να μπορείτε να ενσωματώσετε το αποτέλεσμα σε γκαλερί ιστού, συνημμένα email ή αρχειακά συστήματα. Επειδή η έξοδος είναι μια τυπική μορφή εικόνας, τα επόμενα εργαλεία μπορούν να την εμφανίσουν χωρίς την ανάγκη εγκατάστασης του OneNote.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για Java;

Το Aspose.Note αποδίδει τις σελίδες OneNote απευθείας σε Java, εξαλείφοντας την ανάγκη για Microsoft Office ή Windows. Υποστηρίζει σημειωματάρια έως **500 σελίδες** και μπορεί να επεξεργαστεί αρχεία μεγαλύτερα από **200 MB** διατηρώντας **100 % ακρίβεια διάταξης**. Το API προσφέρει **έξι μορφές εικόνας** (PNG, JPEG, GIF, BMP, TIFF και WebP) και παρέχει ενσωματωμένη διαχείριση DPI, ώστε να λαμβάνετε υψηλής ανάλυσης αποτελέσματα χωρίς επιπλέον ρυθμίσεις. Αυτό το καθιστά την πιο αξιόπιστη, πλατφόρμα‑ανεξάρτητη λύση για επιχειρησιακή μετατροπή εικόνων OneNote.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι τα παρακάτω στοιχεία είναι εγκατεστημένα και σωστά ρυθμισμένα:

1. **Java Development Kit (JDK) 8 ή νεότερο** – κατεβάστε από την Oracle ή χρησιμοποιήστε το OpenJDK και επιβεβαιώστε με `java -version`.  
2. **Aspose.Note for Java** – αποκτήστε το τελευταίο JAR από τη [Aspose.Note for Java download page](https://releases.aspose.com/note/java/). Προσθέστε το `aspose-note-xx.jar` και τα εξαρτημένα JARs στο classpath του έργου σας.  
3. **Ένα IDE ανάπτυξης** (IntelliJ IDEA, Eclipse ή VS Code) – οποιοδήποτε περιβάλλον που μπορεί να μεταγλωττίσει και να εκτελέσει εφαρμογές Java.  

> **Pro tip:** Χρησιμοποιήστε απόλυτες διαδρομές ή `java.nio.file.Paths.get(...)` όταν ορίζετε τη θέση του πηγαίου σημειωματάριου· αυτό αποφεύγει προβλήματα διαδρομών ανά πλατφόρμα.  
Μπορείτε επίσης να επισκεφθείτε την [Aspose website](https://releases.aspose.com/) για περισσότερες πληροφορίες.

## Εισαγωγή πακέτων

Το πρώτο βήμα είναι η εισαγωγή των κλάσεων που απαιτούνται για τη φόρτωση ενός αρχείου OneNote και την αποθήκευσή του ως εικόνα.  

Η κλάση `Document` αντιπροσωπεύει ένα σημειωματάριο OneNote στη μνήμη, παρέχοντάς σας πρόσβαση σε σελίδες, ενότητες και μεταδεδομένα.  

Η `LoadOptions` παρέχει παραμέτρους για τη φόρτωση ενός αρχείου OneNote· ένας κενός κατασκευαστής χρησιμοποιεί τη προεπιλεγμένη συμπεριφορά φόρτωσης της βιβλιοθήκης.  

Η `SaveFormat` απαριθμεί τις υποστηριζόμενες μορφές εξόδου όπως PNG, JPEG, GIF και PDF.  

Η `ImageSaveOptions` σας επιτρέπει να ρυθμίσετε λεπτομερώς τις ρυθμίσεις εικόνας όπως DPI, βάθος χρώματος και επίπεδο συμπίεσης.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Οδηγός βήμα‑βήμα

### Πώς να μετατρέψετε το OneNote σε PNG χρησιμοποιώντας τις προεπιλεγμένες επιλογές;

Φορτώστε το πηγαίο αρχείο `.one`, καλέστε τη μέθοδο `save` και ορίστε το `SaveFormat.Png`. Το Aspose.Note θα καθορίσει αυτόματα το μέγεθος της σελίδας, το DPI και το βάθος χρώματος, και θα δημιουργήσει ένα αρχείο PNG για κάθε σελίδα. Η ολόκληρη διαδικασία ολοκληρώνεται συνήθως σε λιγότερο από ένα δευτερόλεπτο για ένα 10‑σελίδων σημειωματάριο σε τυπικό μηχάνημα ανάπτυξης.

#### Βήμα 1: φόρτωση του εγγράφου OneNote

Η κλάση `Document` είναι το κορυφαίο αντικείμενο του Aspose.Note που αντιπροσωπεύει ένα μόνο αρχείο OneNote στη μνήμη. Χρησιμοποιήστε τον κατασκευαστή που δέχεται διαδρομή αρχείου μαζί με `LoadOptions` για να διαβάσετε το σημειωματάριο με τις προεπιλεγμένες ρυθμίσεις.

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

> **Pro tip:** Κρατήστε το `dataDir` να δείχνει σε απόλυτη διαδρομή ή χρησιμοποιήστε `Paths.get(...)` για καλύτερη διαλειτουργικότητα.

#### Βήμα 2: αποθήκευση του εγγράφου ως εικόνα

Καλέστε τη μέθοδο `save`, ορίστε το επιθυμητό όνομα αρχείου εξόδου και επιλέξτε μορφή εικόνας μέσω `SaveFormat`. Το παρακάτω παράδειγμα αποθηκεύει την πρώτη σελίδα ως GIF, αλλά μπορείτε να αντικαταστήσετε το `SaveFormat.Gif` με `SaveFormat.Png`, `SaveFormat.Jpeg`, κ.λπ., για **convert OneNote to PNG** ή άλλες μορφές.

```java
// Save the document as Gif.
oneFile.save(dataDir + "ConvertToImageUsingDefaultOptions_out.gif", SaveFormat.Gif);
```

**Τι συμβαίνει στο παρασκήνιο;**  
Το Aspose.Note αποδίδει κάθε σελίδα σε bitmap, στη συνέχεια την κωδικοποιεί χρησιμοποιώντας τον επιλεγμένο κωδικοποιητή εικόνας. Επειδή βασιζόμαστε στις προεπιλεγμένες επιλογές, η βιβλιοθήκη καθορίζει αυτόματα το μέγεθος της σελίδας, το DPI και το βάθος χρώματος.

## Συχνά προβλήματα & λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Κενή εικόνα εξόδου** | Λανθασμένη διαδρομή αρχείου ή έλλειψη δικαιωμάτων ανάγνωσης | Επαληθεύστε το `dataDir` και βεβαιωθείτε ότι το αρχείο `.one` υπάρχει. |
| **Έλλειψη μνήμης για μεγάλα σημειωματάρια** | Φόρτωση πολύ μεγάλων σημειωματάριων στη μνήμη | Επεξεργαστείτε τις σελίδες ξεχωριστά χρησιμοποιώντας `Document.getPages()` και αποθηκεύστε κάθε σελίδα ξεχωριστά. |
| **Μη υποστηριζόμενη απόδοση γραμματοσειράς** | Η γραμματοσειρά δεν είναι εγκατεστημένη στον διακομιστή | Εγκαταστήστε τις απαιτούμενες γραμματοσειρές ή ενσωματώστε τις στο αρχείο OneNote πριν από τη μετατροπή. |

## Συχνές ερωτήσεις

**Q: Μπορώ να μετατρέψω ένα πολύπλοκο OneNote σημειωματάριο σε ξεχωριστές εικόνες;**  
A: Ναι. Επανάληψη μέσω `Document.getPages()` και κλήση του `save` για κάθε σελίδα, παρέχοντας μοναδικό όνομα αρχείου.

**Q: Πώς αλλάζω την ανάλυση της εικόνας;**  
A: Χρησιμοποιήστε το `ImageSaveOptions` για να ορίσετε DPI πριν την αποθήκευση: `ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png); options.setResolution(300); document.save("out.png", options);` Αυτός είναι ο προτεινόμενος τρόπος για **set image resolution java**.

**Q: Είναι δυνατόν να μετατρέψω το OneNote απευθείας σε PDF αντί για εικόνα;**  
A: Απόλυτα. Αντικαταστήστε το `SaveFormat.Gif` με `SaveFormat.Pdf` για να δημιουργήσετε ένα έγγραφο PDF.

**Q: Η δωρεάν δοκιμή προσθέτει υδατογράμματα στις εικόνες εξόδου;**  
A: Όχι. Η δοκιμαστική έκδοση παράγει εικόνες πλήρους ποιότητας χωρίς υδατογράμματα· άδεια απαιτείται μόνο για εμπορική χρήση.

**Q: Ποια μορφή εικόνας δίνει το μικρότερο μέγεθος αρχείου;**  
A: Τα GIF και JPEG συνήθως παράγουν μικρότερα αρχεία από το PNG, αλλά η επιλογή εξαρτάται από τις ανάγκες ποιότητας—το PNG είναι lossless, ενώ το JPEG είναι lossy.

## Συχνές Ερωτήσεις

### Q1: Μπορεί το Aspose.Note για Java να διαχειριστεί σύνθετα έγγραφα OneNote;
A1: Ναι, το Aspose.Note για Java μπορεί να διαχειριστεί αποτελεσματικά σύνθετα έγγραφα OneNote, εξασφαλίζοντας ακριβή μετατροπή σε διάφορες μορφές.

### Q2: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.Note για Java;
A2: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμή του Aspose.Note για Java από την [website](https://releases.aspose.com/).

### Q3: Πού μπορώ να βρω πλήρη τεκμηρίωση για το Aspose.Note για Java;
A3: Μπορείτε να ανατρέξετε στην αναλυτική τεκμηρίωση στο [Aspose.Note for Java Documentation](https://reference.aspose.com/note/java/).

### Q4: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.Note για Java;
A4: Μπορείτε να αποκτήσετε προσωρινή άδεια από τη [temporary license page](https://purchase.aspose.com/temporary-license/) στην ιστοσελίδα Aspose.

### Q5: Υπάρχει κοινότητα φόρουμ όπου μπορώ να ζητήσω υποστήριξη για το Aspose.Note για Java;
A5: Ναι, μπορείτε να συμμετάσχετε στο φόρουμ κοινότητας στο [Aspose.Note for Java Support](https://forum.aspose.com/c/note/28) για βοήθεια και αλληλεπίδραση με άλλους χρήστες.

## Πρόσθετες συχνές ερωτήσεις

**Q: Μπορώ να μετατρέψω το OneNote σε PDF στην ίδια ροή εργασίας;**  
A: Ναι—απλώς αλλάξτε το `SaveFormat` σε `SaveFormat.Pdf` και η βιβλιοθήκη θα δημιουργήσει μια έκδοση PDF του σημειωματάριου.

**Q: Πώς ορίζω την ανάλυση εικόνας Java όταν αποθηκεύω πολλές σελίδες;**  
A: Δημιουργήστε μια παρουσία `ImageSaveOptions`, ορίστε το επιθυμητό DPI και περάστε το στη μέθοδο `save` για κάθε σελίδα. Αυτό σας επιτρέπει να **set image resolution java** σταθερά σε όλα τα αρχεία εξόδου.

**Q: Υπάρχουν συμβουλές απόδοσης για μαζική μετατροπή πολλών σημειωματάριων;**  
A: Επεξεργαστείτε τα σημειωματάρια διαδοχικά, επαναχρησιμοποιήστε ένα αντικείμενο `ImageSaveOptions` και απελευθερώστε κάθε `Document` μετά την αποθήκευση για εξοικονόμηση μνήμης.

## Συμπέρασμα

Ακολουθώντας αυτά τα σύντομα βήματα, τώρα γνωρίζετε **πώς να μετατρέψετε το OneNote σε PNG** χρησιμοποιώντας το Aspose.Note for Java με τις προεπιλεγμένες ρυθμίσεις. Αυτή η δυνατότητα σας επιτρέπει να ενσωματώσετε το περιεχόμενο OneNote σε γκαλερί ιστού, να δημιουργήσετε μικρογραφίες ή να αρχειοθετήσετε σελίδες ως στατικές εικόνες—όλα χωρίς την ανάγκη εγκατάστασης του Microsoft Office. Μπορείτε επίσης να επεκτείνετε τη ροή εργασίας για μετατροπή σε PDF ή έλεγχο της ανάλυσης εικόνας, προσφέροντας πλήρη ευελιξία στα Java projects σας.

---

**Last Updated:** 2026-08-23  
**Tested With:** Aspose.Note for Java 26.5  
**Author:** Aspose

## Σχετικά Μαθήματα

- [Πώς να εξάγετε τη σελίδα OneNote σε εικόνα PNG σε Java χρησιμοποιώντας το Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [Πώς να μετατρέψετε το OneNote σε PNG – Επίπεδη εικόνα σημειωματάριου με Aspose.Note](/note/java/onenote-notebook-operations/convert-notebook-to-flattened-image/)
- [aspnote set jpeg resolution – Ορισμός ανάλυσης εξόδου εικόνας στο OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}