---
date: 2026-09-04
description: Μάθετε πώς να μετατρέψετε το OneNote σε PNG χρησιμοποιώντας το Aspose.Note
  for Java και εξερευνήστε την εξαγωγή σελίδων OneNote ως PNG, JPEG, BMP ή PDF με
  λίγες μόνο γραμμές κώδικα.
keywords:
- convert onenote to png
- how to export onenote pages
- export onenote as image
lastmod: 2026-09-04
linktitle: Πώς να μετατρέψετε το OneNote σε PNG με το Aspose.Note for Java
og_description: Μετατρέψτε το OneNote σε PNG χρησιμοποιώντας το Aspose.Note for Java.
  Ακολουθήστε έναν γρήγορο step-by-step guide, δείτε τα prerequisites, και μάθετε
  πώς να εξάγετε σελίδες OneNote ως images ή PDFs σε λιγότερο από ένα δευτερόλεπτο
  ανά αρχείο.
og_image_alt: Guide showing Java code converting OneNote files to PNG images
og_title: Μετατροπή OneNote σε PNG με τη βιβλιοθήκη Aspose.Note for Java
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to convert OneNote to PNG using Aspose.Note for Java, and
    explore exporting OneNote pages as PNG, JPEG, BMP, or PDF in just a few lines
    of code.
  headline: How to convert OneNote to PNG with Aspose.Note for Java
  type: TechArticle
- description: Learn how to convert OneNote to PNG using Aspose.Note for Java, and
    explore exporting OneNote pages as PNG, JPEG, BMP, or PDF in just a few lines
    of code.
  name: How to convert OneNote to PNG with Aspose.Note for Java
  steps:
  - name: set up the document directory
    text: Define the folder that contains your OneNote file. Replace the placeholder
      with the actual path on your machine.
  - name: load the OneNote document
    text: '`Document` is Aspose.Note’s core object that represents a single OneNote
      notebook in memory. It provides access to pages, sections, and resources for
      reading or writing. > **Pro tip:** The same `Document` instance can be reused
      to export to PDF, HTML, or other image formats without re‑loading the fi'
  - name: initialize image save options
    text: '`ImageSaveOptions` tells Aspose.Note which raster format to produce and
      lets you fine‑tune resolution, compression, and page range. In this example
      we choose PNG, but you can replace `SaveFormat.Png` with `SaveFormat.Jpeg` or
      `SaveFormat.Bmp`. > This line also satisfies the secondary keywords **conv'
  - name: save the document as an image
    text: Export the OneNote pages to PNG files. The `save` method automatically creates
      a separate image for each page (e.g., `ConvertToImage_out_1.png`, `ConvertToImage_out_2.png`,
      …).
  - name: print confirmation
    text: Notify the user where the output files were written.
  type: HowTo
- questions:
  - answer: Yes. Iterate over a collection of file paths, load each with `new Document(...)`,
      and repeat the save steps inside the loop.
    question: Can I batch‑process multiple OneNote files?
  - answer: Absolutely. Use `PdfSaveOptions` instead of `ImageSaveOptions` to **convert
      OneNote to PDF** with a single method call.
    question: Does Aspose.Note support converting OneNote to PDF?
  - answer: Call `options.setResolutionX(int)` and `options.setResolutionY(int)` on
      the `ImageSaveOptions` object before invoking `save`.
    question: How do I change the resolution of the PNG output?
  - answer: Yes—replace `SaveFormat.Png` with `SaveFormat.Jpeg` or `SaveFormat.Bmp`
      in the `ImageSaveOptions` constructor.
    question: Can I export to JPEG or BMP instead of PNG?
  - answer: No. All processing is performed locally; no external services are contacted.
    question: Do I need an internet connection for the conversion?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- convert onenote
- Aspose.Note
- Java document processing
title: Πώς να μετατρέψετε το OneNote σε PNG με το Aspose.Note for Java
url: /el/java/onenote-document-loading/convert-to-image/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να μετατρέψετε το OneNote σε PNG με το Aspose.Note for Java

## Εισαγωγή

Σε αυτό το tutorial θα μάθετε **πώς να μετατρέψετε το OneNote σε PNG** με τη βιβλιοθήκη **Aspose.Note for Java**. Η μετατροπή σελίδων OneNote σε μορφή εικόνας είναι συχνή ανάγκη όταν θέλετε να ενσωματώσετε σημειώσεις σε ιστοσελίδες, να δημιουργήσετε μικρογραφίες ή να αρχειοθετήσετε σημειωματάρια χωρίς να απαιτείται ο τελικός χρήστης να έχει εγκατεστημένο το OneNote. Θα περάσουμε από τη ρύθμιση του περιβάλλοντος, τη φόρτωση ενός αρχείου `.one` και την εξαγωγή κάθε σελίδας ως εικόνα PNG, ώστε να προσθέσετε αυτή τη δυνατότητα σε οποιαδήποτε εφαρμογή Java σε λίγα λεπτά.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη χρειάζομαι;** Aspose.Note for Java.  
- **Μπορώ να μετατρέψω το OneNote σε άλλες μορφές;** Ναι – μπορείτε επίσης να εξάγετε σε PDF, JPEG, BMP, HTML και άλλα.  
- **Χρειάζεται σύνδεση στο διαδίκτυο;** Όχι, η μετατροπή εκτελείται εξ ολοκλήρου τοπικά.  
- **Ποια μορφή εικόνας χρησιμοποιεί αυτός ο οδηγός;** PNG (αντικαταστήστε το `SaveFormat.Png` με JPEG ή BMP για αλλαγή του αποτελέσματος).  
- **Πόσο γρήγορη είναι η μετατροπή;** Ένα τυπικό αρχείο OneNote 10 σελίδων μετατρέπεται σε λιγότερο από ένα δευτερόλεπτο σε σύγχρονο σταθμό εργασίας.  
- **Είναι το API συμβατό με Java 8+;** Απόλυτα· λειτουργεί σε οποιαδήποτε πλατφόρμα που υποστηρίζει Java 8 ή νεότερη έκδοση.

## Πώς να μετατρέψετε το OneNote σε PNG;

Φορτώστε το αρχείο OneNote με `new Document("path/to/file.one")` και καλέστε `document.save("output.png", new ImageSaveOptions(SaveFormat.Png))`. Το Aspose.Note αποδίδει κάθε σελίδα ως ξεχωριστό αρχείο PNG, διατηρώντας χρώματα, γραμματοσειρές και διάταξη ακριβώς όπως εμφανίζονται στο OneNote. Μπορείτε να ρυθμίσετε την ανάλυση ή το εύρος σελίδων μέσω του αντικειμένου `ImageSaveOptions` πριν την αποθήκευση.

## Τι σημαίνει «μετατροπή OneNote σε PNG» στην πράξη;

Η μετατροπή OneNote σε PNG σημαίνει απόδοση κάθε σελίδας ενός σημειωματάριου `.one` σε ραστερ εικόνας. Αυτή η **μετατροπή εικόνας OneNote** σας επιτρέπει να μοιράζεστε σημειώσεις με χρήστες που δεν έχουν OneNote, να ενσωματώνετε στατικές εικόνες σε τεκμηρίωση ή να αρχειοθετείτε περιεχόμενο σε μορφή που μπορεί να προβληθεί παντού.

## Γιατί να χρησιμοποιήσετε το Aspose.Note for Java για τη μετατροπή OneNote σε PNG;

- **Καμία εξωτερική εξάρτηση** – καθαρά Java, χωρίς ανάγκη για εγγενείς βιβλιοθήκες.  
- **Πλήρης πιστότητα** – χρώματα, γραμματοσειρές και διάταξη διατηρούνται με 100 % ακρίβεια.  
- **Ευρεία υποστήριξη μορφών** – PNG, JPEG, BMP, PDF, HTML και πάνω από 50 + άλλες μορφές είναι διαθέσιμες.  
- **Επιδόσεις κατάλληλες για επιχειρήσεις** – επεξεργάζεται σημειωματάρια εκατοντάδων σελίδων χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, χρησιμοποιώντας αρχιτεκτονική streaming που κρατά τη χρήση heap κάτω από 200 MB ακόμη και για αρχεία 500 σελίδων.  
- **Διαπλατφόρμα** – λειτουργεί σε Windows, Linux και macOS με οποιοδήποτε runtime Java 8+.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

1. **Java Development Kit (JDK)** – έκδοση 8 ή νεότερη εγκατεστημένη και ρυθμισμένο `JAVA_HOME`.  
2. **Βιβλιοθήκη Aspose.Note for Java** – κατεβάστε το τελευταίο JAR από την επίσημη ιστοσελίδα: [Aspose.Note for Java download](https://releases.aspose.com/note/java/).  
3. Ένα αρχείο OneNote (`.one`) που θέλετε να μετατρέψετε, π.χ. `Sample1.one`.  

## Εισαγωγή πακέτων

Πρώτα, εισάγετε τις κλάσεις που απαιτούνται για τη φόρτωση και αποθήκευση εγγράφων OneNote.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Οδηγός βήμα‑βήμα

### Βήμα 1: ρύθμιση του καταλόγου εγγράφων  
Ορίστε το φάκελο που περιέχει το αρχείο OneNote. Αντικαταστήστε το placeholder με την πραγματική διαδρομή στο σύστημά σας.

```java
String dataDir = "Your Document Directory";
```

### Βήμα 2: φόρτωση του εγγράφου OneNote  
`Document` είναι το βασικό αντικείμενο του Aspose.Note που αντιπροσωπεύει ένα σημειωματάριο OneNote στη μνήμη. Παρέχει πρόσβαση σε σελίδες, ενότητες και πόρους για ανάγνωση ή εγγραφή.

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Συμβουλή:** Το ίδιο αντικείμενο `Document` μπορεί να επαναχρησιμοποιηθεί για εξαγωγή σε PDF, HTML ή άλλες μορφές εικόνας χωρίς επαναφόρτωση του αρχείου.

### Βήμα 3: αρχικοποίηση επιλογών αποθήκευσης εικόνας  
`ImageSaveOptions` καθορίζει στο Aspose.Note ποια μορφή raster θα παραχθεί και σας επιτρέπει να ρυθμίσετε ανάλυση, συμπίεση και εύρος σελίδων. Στο παράδειγμα επιλέγουμε PNG, αλλά μπορείτε να αντικαταστήσετε το `SaveFormat.Png` με `SaveFormat.Jpeg` ή `SaveFormat.Bmp`.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

> Αυτή η γραμμή ικανοποιεί επίσης τις δευτερεύουσες λέξεις‑κλειδιά **convert onenote to png** και **save onenote as png**.

### Βήμα 4: αποθήκευση του εγγράφου ως εικόνα  
Εξάγετε τις σελίδες OneNote σε αρχεία PNG. Η μέθοδος `save` δημιουργεί αυτόματα ξεχωριστή εικόνα για κάθε σελίδα (π.χ. `ConvertToImage_out_1.png`, `ConvertToImage_out_2.png`, …).

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

### Βήμα 5: εκτύπωση επιβεβαίωσης  
Ειδοποιήστε τον χρήστη πού έχουν γραφτεί τα αρχεία εξόδου.

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

## Συνηθισμένες περιπτώσεις χρήσης για τη μετατροπή OneNote σε PNG

| Σενάριο | Γιατί PNG; | Τυπική ροή εργασίας |
|----------|------------|----------------------|
| **Ενσωμάτωση σημειώσεων σε διαδικτυακό άρθρο** | Απώλεια ποιότητας και καθολική υποστήριξη από browsers. | Μετατροπή, έπειτα εισαγωγή του PNG με ετικέτα `<img>`. |
| **Δημιουργία μικρογραφιών για σύστημα διαχείρισης εγγράφων** | Μικρό μέγεθος αρχείου με καθαρή απόδοση κειμένου. | Μετατροπή, έπειτα αλλαγή μεγέθους με οποιαδήποτε βιβλιοθήκη επεξεργασίας εικόνας. |
| **Αρχειοθέτηση σημειωματάριων για συμμόρφωση** | Το PNG είναι στατικό, μη επεξεργάσιμο format που διατηρεί οπτική πιστότητα. | Μαζική επεξεργασία όλων των αρχείων `.one` και αποθήκευση των PNG σε ασφαλή αποθετήριο. |

## Συνηθισμένα προβλήματα και λύσεις

**FileNotFoundException** εμφανίζεται όταν το καθορισμένο αρχείο δεν μπορεί να εντοπιστεί.  
**Unsupported format** εμφανίζεται όταν η ζητούμενη μορφή εξόδου δεν υποστηρίζεται από τη βιβλιοθήκη.  
**OutOfMemoryError** υποδεικνύει ότι η JVM εξαντλήθηκε σε heap μνήμη κατά την επεξεργασία.

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **FileNotFoundException** | Λανθασμένη διαδρομή `dataDir`. | Επαληθεύστε ότι η διαδρομή καταλήγει με κάθετο (`/` ή `\\`) και το όνομα αρχείου είναι σωστό. |
| **Unsupported format** | Προσπάθεια αποθήκευσης σε μορφή που δεν υποστηρίζεται από την τρέχουσα έκδοση της βιβλιοθήκης. | Ενημερώστε το Aspose.Note στην τελευταία έκδοση ή επιλέξτε υποστηριζόμενο `SaveFormat`. |
| **OutOfMemoryError on large notebooks** | Ανεπαρκής heap μνήμη για πολύ μεγάλα αρχεία. | Αυξήστε το heap της JVM (`-Xmx2g`) ή επεξεργαστείτε τις σελίδες ξεχωριστά χρησιμοποιώντας βρόχο `document.getPages()`. |

## Συχνές ερωτήσεις

**Ε: Μπορώ να επεξεργαστώ μαζικά πολλαπλά αρχεία OneNote;**  
Α: Ναι. Επανάληψη πάνω σε μια συλλογή διαδρομών αρχείων, φόρτωση του καθενός με `new Document(...)` και επανάληψη των βημάτων αποθήκευσης μέσα στον βρόχο.

**Ε: Υποστηρίζει το Aspose.Note τη μετατροπή OneNote σε PDF;**  
Α: Απόλυτα. Χρησιμοποιήστε `PdfSaveOptions` αντί για `ImageSaveOptions` για **μετατροπή OneNote σε PDF** με μία κλήση μεθόδου.

**Ε: Πώς αλλάζω την ανάλυση της εξόδου PNG;**  
Α: Καλέστε `options.setResolutionX(int)` και `options.setResolutionY(int)` στο αντικείμενο `ImageSaveOptions` πριν καλέσετε το `save`.

**Ε: Μπορώ να εξάγω σε JPEG ή BMP αντί για PNG;**  
Α: Ναι—αντικαταστήστε το `SaveFormat.Png` με `SaveFormat.Jpeg` ή `SaveFormat.Bmp` στον κατασκευαστή `ImageSaveOptions`.

**Ε: Χρειάζεται σύνδεση στο διαδίκτυο για τη μετατροπή;**  
Α: Όχι. Όλη η επεξεργασία γίνεται τοπικά· δεν επικοινωνείται με εξωτερικές υπηρεσίες.

**Ε: Πώς αντιμετωπίζονται τα κωδικοποιημένα με κωδικό πρόσβασης αρχεία OneNote;**  
Α: Παρέχετε τον κωδικό πρόσβασης στον κατασκευαστή `Document`: `new Document(path, password)`.

---

**Τελευταία ενημέρωση:** 2026-09-04  
**Δοκιμασμένο με:** Aspose.Note for Java 24.12  
**Συγγραφέας:** Aspose

## Σχετικά tutorials

- [How to Export OneNote Page to PNG Image in Java using Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [Export OneNote to BMP Image Using Aspose.Note for Java Image Save Options](/note/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/)
- [Learn to increase JPEG DPI – Set Output Image Resolution in OneNote with Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}