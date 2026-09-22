---
date: 2026-08-24
description: Μάθετε πώς να μετατρέψετε το OneNote σε PNG χρησιμοποιώντας το Aspose.Note
  for Java με default options. Ο οδηγός βήμα‑βήμα καλύπτει τη μετατροπή PDF, την image
  resolution και το batch processing.
keywords:
- convert onenote to png
- how to convert onenote
- set image resolution java
lastmod: 2026-08-24
linktitle: Μετατροπή OneNote σε Image χρησιμοποιώντας Default Options - Java
og_description: Μετατρέψτε το OneNote σε PNG χρησιμοποιώντας το Aspose.Note for Java
  με default settings. Ακολουθήστε το σύντομο tutorial μας για γρήγορη, υψηλής πιστότητας
  image conversion.
og_image_alt: Screenshot of Java code converting OneNote to PNG with Aspose.Note
og_title: Μετατροπή OneNote σε PNG σε Java – Γρήγορος οδηγός Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-24'
  description: Learn how to convert OneNote to PNG using Aspose.Note for Java with
    default options. Step‑by‑step guide covers PDF conversion, image resolution, and
    batch processing.
  headline: How to convert OneNote to PNG using default options in Java
  type: TechArticle
- questions:
  - answer: Yes. Iterate over `oneFile.getPages()` and call `save` for each page,
      providing a unique file name.
    question: Can I convert a multi‑page OneNote notebook to separate images?
  - answer: 'Use `ImageSaveOptions` to set DPI before saving: `ImageSaveOptions options
      = new ImageSaveOptions(SaveFormat.Png); options.setResolution(300); oneFile.save("out.png",
      options);` This is the recommended way to **set image resolution java**.'
    question: How do I change the image resolution?
  - answer: Absolutely. Replace `SaveFormat.Png` with `SaveFormat.Pdf` to generate
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
- Java image conversion
title: Πώς να μετατρέψετε το OneNote σε PNG χρησιμοποιώντας τις default options σε
  Java
url: /el/java/onenote-document-loading/convert-to-image-default-options/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή OneNote σε PNG χρησιμοποιώντας τις προεπιλεγμένες επιλογές σε Java

## Εισαγωγή

Σ στις σύγχρονες εφαρμογές, η **μετατροπή OneNote σε PNG** είναι συχνή ανάγκη—είτε δημιουργείτε μικρογραφίες για μια διαδικτυακή γκαλερί, ενσωματώνετε σελίδες σε PDF, είτε αρχειοθετείτε περιεχόμενο ως στατικές εικόνες. Αυτό το μάθημα σας οδηγεί βήμα-βήμα στη **μετατροπή OneNote σε PNG** με το Aspose.Note για Java χρησιμοποιώντας τις προεπιλεγμένες επιλογές της βιβλιοθήκης. Στο τέλος, θα μπορείτε να αποθηκεύετε σελίδες OneNote ως εικόνες PNG με λίγες γραμμές κώδικα και να κατανοήσετε πώς να επεκτείνετε τη διαδικασία για μετατροπή σε PDF και έλεγχο ανάλυσης εικόνας.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται τη μετατροπή OneNote σε Java;** Aspose.Note for Java.  
- **Μπορώ να μετατρέψω OneNote σε PNG χωρίς επιπλέον ρυθμίσεις;** Ναι—οι προεπιλεγμένες επιλογές εξάγουν αυτόματα PNG, GIF, JPEG κ.λπ.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποια έκδοση Java απαιτείται;** Java 8 ή νεότερη.  
- **Είναι η μετατροπή αρκετά γρήγορη για μαζική επεξεργασία;** Ναι—το Aspose.Note επεξεργάζεται τα έγγραφα στη μνήμη, καθιστώντας τις μαζικές μετατροπές αποδοτικές.

## Τι είναι η «μετατροπή OneNote σε εικόνα»;
Η μετατροπή OneNote σε εικόνα σημαίνει ότι παίρνουμε το πλούσιο, πολυεπίπεδο περιεχόμενο ενός αρχείου `.one` και αποδίδουμε κάθε σελίδα ως ραστερ γραφικό, όπως PNG, GIF ή JPEG. Αυτή η μετατροπή είναι χρήσιμη για δημιουργία προεπισκοπήσεων, αρχειοθέτηση περιεχομένου και ενσωμάτωση με συστήματα που δέχονται μόνο εικόνες.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για Java;
Το Aspose.Note για Java προσφέρει μια πλήρως διαχειριζόμενη, χωρίς Microsoft‑Office λύση που αποδίδει τις σελίδες OneNote με τέλεια πιστότητα pixel. Υποστηρίζει **6 μορφές εικόνας** (PNG, JPEG, GIF, BMP, TIFF και SVG) και μπορεί να επεξεργαστεί σημειωματάρια με **έως 500 σελίδες** χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, προσφέροντας χρόνους μετατροπής κάτω των 2 δευτερολέπτων ανά σελίδα σε τυπικό εξοπλισμό διακομιστή.

## Προαπαιτήσεις

Πριν ξεκινήσετε, βεβαιωθείτε ότι τα παρακάτω είναι εγκατεστημένα και ρυθμισμένα:

### Java Development Kit (JDK)
1. **Λήψη** του τελευταίου JDK από την ιστοσελίδα της Oracle (ή Adopt OpenJDK).  
2. **Εγκατάσταση** ακολουθώντας τις οδηγίες για την πλατφόρμα σας. Επαληθεύστε με `java -version`.

### Aspose.Note για Java
1. **Λήψη** της βιβλιοθήκης από τη [σελίδα λήψης Aspose.Note for Java](https://releases.aspose.com/note/java/).  
2. **Προσθήκη** του `aspose-note-xx.jar` (και τυχόν εξαρτήσεων) στο classpath του έργου σας.  
3. Μπορείτε επίσης να περιηγηθείτε στον πλήρη κατάλογο προϊόντων στην [ιστοσελίδα Aspose](https://releases.aspose.com/).

## Εισαγωγή πακέτων
Το πρώτο βήμα είναι η εισαγωγή των κλάσεων που απαιτούνται για τη φόρτωση ενός αρχείου OneNote και την αποθήκευσή του ως εικόνα.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Οδηγός βήμα‑βήμα

### Βήμα 1: Φόρτωση του εγγράφου OneNote
Η κλάση `Document` αντιπροσωπεύει ένα σημειωματάριο OneNote στη μνήμη, εκθέτοντας σελίδες, ενότητες και πόρους. Φορτώστε το πηγαίο αρχείο `.one` σε ένα αντικείμενο `Aspose.Note` `Document`. Ο κατασκευαστής `LoadOptions` χωρίς παραμέτρους λέει στη βιβλιοθήκη να χρησιμοποιήσει τη προεπιλεγμένη συμπεριφορά φόρτωσης.

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

> **Συμβουλή:** Κρατήστε το `dataDir` να δείχνει σε απόλυτη διαδρομή ή χρησιμοποιήστε `Paths.get(...)` για καλύτερη διαλειτουργικότητα.

### Βήμα 2: Αποθήκευση του εγγράφου ως εικόνα
Η απαρίθμηση `SaveFormat` ορίζει τον τύπο εξόδου εικόνας (PNG, JPEG, GIF κ.λπ.). Καλέστε τη μέθοδο `save`, καθορίστε το επιθυμητό όνομα αρχείου εξόδου και επιλέξτε μορφή εικόνας μέσω `SaveFormat`. Το παρακάτω παράδειγμα αποθηκεύει την πρώτη σελίδα ως PNG, αλλά μπορείτε να αντικαταστήσετε το `SaveFormat.Png` με οποιαδήποτε υποστηριζόμενη μορφή για **μετατροπή OneNote σε PNG** ή άλλους τύπους εικόνας.

```java
// Save the document as Gif.
oneFile.save(dataDir + "ConvertToImageUsingDefaultOptions_out.gif", SaveFormat.Gif);
```

**Τι συμβαίνει στο παρασκήνιο;**  
Το Aspose.Note αποδίδει κάθε σελίδα σε bitmap, έπειτα την κωδικοποιεί χρησιμοποιώντας τον επιλεγμένο κωδικοποιητή εικόνας. Επειδή βασιζόμαστε στις προεπιλεγμένες επιλογές, η βιβλιοθήκη καθορίζει αυτόματα το μέγεθος σελίδας, DPI και βάθος χρώματος.

## Συχνά προβλήματα & λύσεις
| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Κενή εικόνα εξόδου** | Λανθασμένη διαδρομή αρχείου ή έλλειψη δικαιωμάτων ανάγνωσης | Επαληθεύστε το `dataDir` και βεβαιωθείτε ότι το αρχείο `.one` υπάρχει. |
| **Out‑of‑memory για μεγάλα σημειωματάρια** | Φόρτωση πολύ μεγάλων σημειωματάριων στη μνήμη | Επεξεργαστείτε τις σελίδες ξεχωριστά χρησιμοποιώντας `Document.getPages()` και αποθηκεύστε κάθε σελίδα ξεχωριστά. |
| **Μη υποστηριζόμενη απόδοση γραμματοσειράς** | Η γραμματοσειρά δεν είναι εγκατεστημένη στον διακομιστή | Εγκαταστήστε τις απαιτούμενες γραμματοσειρές ή ενσωματώστε τις στο αρχείο OneNote πριν από τη μετατροπή. |

## Συχνές ερωτήσεις

**Q: Μπορώ να μετατρέψω ένα πολύπλευρο σημειωματάριο OneNote σε ξεχωριστές εικόνες;**  
A: Ναι. Επανάληψη μέσω `oneFile.getPages()` και κλήση `save` για κάθε σελίδα, παρέχοντας μοναδικό όνομα αρχείου.

**Q: Πώς αλλάζω την ανάλυση της εικόνας;**  
A: Χρησιμοποιήστε `ImageSaveOptions` για να ορίσετε DPI πριν από την αποθήκευση: `ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png); options.setResolution(300); oneFile.save("out.png", options);` Αυτός είναι ο προτεινόμενος τρόπος για **ορισμό ανάλυσης εικόνας java**.

**Q: Είναι δυνατόν να μετατρέψω το OneNote απευθείας σε PDF αντί για εικόνα;**  
A: Απόλυτα. Αντικαταστήστε το `SaveFormat.Png` με `SaveFormat.Pdf` για δημιουργία εγγράφου PDF.

**Q: Η δωρεάν δοκιμή προσθέτει υδατογράμματα στις εικόνες εξόδου;**  
A: Όχι. Η δοκιμαστική έκδοση παράγει εικόνες πλήρους ποιότητας χωρίς υδατογραφήματα· άδεια απαιτείται μόνο για εμπορική ανάπτυξη.

**Q: Ποια μορφή εικόνας δίνει το μικρότερο μέγεθος αρχείου;**  
A: Τα GIF και JPEG συνήθως παράγουν μικρότερα αρχεία από το PNG, αλλά η επιλογή εξαρτάται από τις ανάγκες ποιότητας—το PNG είναι χωρίς απώλειες, ενώ το JPEG είναι με απώλειες.

## Πρόσθετες συχνές ερωτήσεις

**Q: Μπορεί το Aspose.Note για Java να διαχειριστεί σύνθετα έγγραφα OneNote;**  
A: Ναι, το Aspose.Note για Java μπορεί να επεξεργαστεί αποδοτικά σύνθετα έγγραφα OneNote, εξασφαλίζοντας ακριβή μετατροπή σε διάφορες μορφές.

**Q: Υπάρχει δωρεάν δοκιμή για το Aspose.Note για Java;**  
A: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμή του Aspose.Note για Java από την [ιστοσελίδα](https://releases.aspose.com/).

**Q: Πού μπορώ να βρω ολοκληρωμένη τεκμηρίωση για το Aspose.Note για Java;**  
A: Μπορείτε να ανατρέξετε στην αναλυτική τεκμηρίωση που διατίθεται στο [Aspose.Note for Java Documentation](https://reference.aspose.com/note/java/).

**Q: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.Note για Java;**  
A: Μπορείτε να αποκτήσετε προσωρινή άδεια από τη [σελίδα προσωρινής άδειας](https://purchase.aspose.com/temporary-license/) στην ιστοσελίδα Aspose.

**Q: Υπάρχει κοινότητα όπου μπορώ να ζητήσω υποστήριξη για το Aspose.Note για Java;**  
A: Ναι, μπορείτε να συμμετάσχετε στο φόρουμ κοινότητας στο [Aspose.Note for Java Support](https://forum.aspose.com/c/note/28) για βοήθεια και αλληλεπίδραση με άλλους χρήστες.

## Συμπέρασμα
Ακολουθώντας αυτά τα σύντομα βήματα, γνωρίζετε πλέον **πώς να μετατρέψετε OneNote σε PNG** χρησιμοποιώντας το Aspose.Note για Java με τις προεπιλεγμένες ρυθμίσεις. Αυτή η δυνατότητα σας επιτρέπει να ενσωματώσετε περιεχόμενο OneNote σε διαδικτυακές γκαλερί, να δημιουργήσετε μικρογραφίες ή να αρχειοθετήσετε σελίδες ως στατικές εικόνες—όλα χωρίς την ανάγκη εγκατάστασης του Microsoft Office. Μπορείτε επίσης να επεκτείνετε τη ροή εργασίας για μετατροπή σε PDF ή έλεγχο ανάλυσης εικόνας, προσφέροντάς σας πλήρη ευελιξία για τα έργα Java.

---

**Τελευταία ενημέρωση:** 2026-08-24  
**Δοκιμή με:** Aspose.Note for Java 26.4  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Πώς να εξάγετε τη σελίδα OneNote σε εικόνα PNG σε Java χρησιμοποιώντας το Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [Ορισμός ανάλυσης εικόνας κατά την αποθήκευση OneNote με το Aspose.Note](/note/java/onenote-document-saving/)
- [Μετατροπή σημειωματάριου σε εικόνα με επιλογές στο OneNote - Aspose.Note](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}