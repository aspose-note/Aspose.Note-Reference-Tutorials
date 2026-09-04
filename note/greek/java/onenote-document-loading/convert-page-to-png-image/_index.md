---
date: 2026-09-04
description: Μάθετε πώς να εξάγετε τη σελίδα OneNote σε εικόνα PNG σε Java χρησιμοποιώντας
  το Aspose.Note. Αυτός ο οδηγός δείχνει τη μετατροπή .one σε png, τον καθορισμό του
  page index και την αποθήκευση ως εικόνα.
keywords:
- how to export onenote
- convert onenote to png
- save onenote as image
- convert .one to png
lastmod: 2026-09-04
linktitle: Εξαγωγή σελίδας OneNote σε εικόνα PNG σε Java
og_description: Πώς να εξάγετε τη σελίδα OneNote σε PNG σε Java με το Aspose.Note.
  Αυτός ο οδηγός σας καθοδηγεί στη φόρτωση ενός αρχείου .one, την επιλογή μιας σελίδας
  και την αποθήκευση μιας high‑quality PNG εικόνας.
og_image_alt: 'Tutorial: Export OneNote page to PNG image using Aspose.Note for Java'
og_title: Πώς να εξάγετε τη σελίδα OneNote σε PNG σε Java με το Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to export OneNote page to PNG image in Java using Aspose.Note.
    This guide shows converting .one to png, setting the page index, and saving as
    an image.
  headline: How to export OneNote page to PNG in Java with Aspose.Note
  type: TechArticle
- description: Learn how to export OneNote page to PNG image in Java using Aspose.Note.
    This guide shows converting .one to png, setting the page index, and saving as
    an image.
  name: How to export OneNote page to PNG in Java with Aspose.Note
  steps:
  - name: Load the OneNote document
    text: The `Document` class represents a OneNote file in memory. Loading the file
      is the foundation for **convert .one to png**.
  - name: Initialise image‑save options
    text: '`ImageSaveOptions` tells Aspose.Note that the output should be **PNG**.
      You can also adjust DPI, color depth, and compression here.'
  - name: Set the page index (how to convert OneNote page)
    text: The `setPageIndex` method selects which page to export. Page numbering starts
      at **0**, so `0` refers to the first page. Adjust this value to export a different
      page or loop through pages for bulk conversion.
  - name: Save the document as PNG (save OneNote as PNG)
    text: Calling `save` writes the selected page to a PNG file on disk. The file
      name `ConvertSpecificPageToPngImage_out.png` is just an example—you can name
      it whatever you like. This final step **exports onenote page image** ready for
      use in reports, web pages, or further processing.
  type: HowTo
- questions:
  - answer: Aspose.Note for Java.
    question: What library is needed?
  - answer: Yes—use `setPageIndex` to target the exact page.
    question: Can I export a single page?
  - answer: PNG, JPEG, GIF, BMP, TIFF (PNG shown here).
    question: Supported image formats?
  - answer: A free trial is available; a license is required for production.
    question: Do I need a license?
  - answer: Typically under 10 minutes for a basic conversion.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote conversion
- Aspose.Note
- java image export
title: Πώς να εξάγετε τη σελίδα OneNote σε PNG σε Java με το Aspose.Note
url: /el/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να εξάγετε μια σελίδα OneNote σε PNG με Java και Aspose.Note

Σε αυτό το tutorial θα μάθετε **πώς να εξάγετε μια σελίδα OneNote** σε εικόνα PNG χρησιμοποιώντας τη βιβλιοθήκη Aspose.Note for Java. Η εξαγωγή σελίδων OneNote είναι συχνή απαίτηση όταν χρειάζεται να μοιραστείτε σημειώσεις εκτός του οικοσυστήματος OneNote, να τις ενσωματώσετε σε αναφορές ή να εκτελέσετε αλγόριθμους επεξεργασίας εικόνας. Θα καλύψουμε τη ρύθμιση του περιβάλλοντος, τη φόρτωση ενός αρχείου .one, την επιλογή μιας συγκεκριμένης σελίδας, τη διαμόρφωση των επιλογών εικόνας και, τέλος, την αποθήκευση ενός αρχείου PNG υψηλής ανάλυσης.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη χρειάζεται;** Aspose.Note for Java.  
- **Μπορώ να εξάγω μια μόνο σελίδα;** Ναι—χρησιμοποιήστε `setPageIndex` για να στοχεύσετε τη συγκεκριμένη σελίδα.  
- **Υποστηριζόμενες μορφές εικόνας;** PNG, JPEG, GIF, BMP, TIFF (εδώ εμφανίζεται PNG).  
- **Χρειάζομαι άδεια;** Διατίθεται δωρεάν δοκιμή· απαιτείται άδεια για παραγωγή.  
- **Πόσο διαρκεί η υλοποίηση;** Συνήθως λιγότερο από 10 λεπτά για μια βασική μετατροπή.  
- **Πώς να μετατρέψετε .one σε png;** Φορτώστε το αρχείο `.one` με `Document`, ορίστε το index της σελίδας και αποθηκεύστε με `ImageSaveOptions`.  

## Τι είναι η «εξαγωγή σελίδας OneNote»;
Η εξαγωγή μιας σελίδας OneNote σημαίνει τη μετατροπή μιας συγκεκριμένης σελίδας μέσα σε ένα έγγραφο `.one` σε ένα ανεξάρτητο αρχείο εικόνας (PNG σε αυτήν την περίπτωση). Αυτό είναι χρήσιμο όταν χρειάζεται να **εξαγάγετε εικόνα σελίδας OneNote** για κοινή χρήση, ενσωμάτωση ή περαιτέρω ανάλυση εικόνας. Η διαδικασία ξεκινά με τη φόρτωση του αρχείου OneNote, την επιλογή της επιθυμητής σελίδας και, στη συνέχεια, την απόδοση αυτής της σελίδας ως εικόνα raster.

## Γιατί να χρησιμοποιήσετε Aspose.Note for Java για τη μετατροπή OneNote σε PNG;
Το Aspose.Note υποστηρίζει **50+ input and output formats** και μπορεί να αποδώσει τετράδια με εκατοντάδες σελίδες χωρίς να απαιτεί Microsoft Office. Παρέχει λεπτομερή έλεγχο της επιλογής σελίδας, DPI και βάθους χρώματος, παραδίδοντας αρχεία PNG που διατηρούν τα διανυσματικά γραφικά και την καθαρότητα του κειμένου. Η βιβλιοθήκη λειτουργεί σε οποιαδήποτε πλατφόρμα που υποστηρίζει Java 8+, καθιστώντας την ιδανική για διακομιστές παρτίδας μετατροπών.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

1. **Java Development Kit (JDK)** – έκδοση 8 ή νεότερη.  
2. **Aspose.Note for Java** – κατεβάστε το πιο πρόσφατο JAR από το [Aspose website](https://releases.aspose.com/note/java/).  
3. **Ένα έγγραφο OneNote** (`.one`) που περιέχει τη σελίδα που θέλετε να εξάγετε.

## Εισαγωγή πακέτων

Πρώτα, εισάγετε τις απαραίτητες κλάσεις Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Οδηγός βήμα‑βήμα

### Βήμα 1: Φόρτωση του εγγράφου OneNote

Η κλάση `Document` αντιπροσωπεύει ένα αρχείο OneNote στη μνήμη. Η φόρτωση του αρχείου είναι η βάση για **convert .one to png**.

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

### Βήμα 2: Αρχικοποίηση επιλογών αποθήκευσης εικόνας

`ImageSaveOptions` ενημερώνει το Aspose.Note ότι η έξοδος πρέπει να είναι **PNG**. Μπορείτε επίσης να ρυθμίσετε DPI, βάθος χρώματος και συμπίεση εδώ.

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

### Βήμα 3: Ορισμός του δείκτη σελίδας (πώς να μετατρέψετε σελίδα OneNote)

Η μέθοδος `setPageIndex` επιλέγει ποια σελίδα θα εξαχθεί. Η αρίθμηση των σελίδων ξεκινά από **0**, έτσι το `0` αναφέρεται στην πρώτη σελίδα. Προσαρμόστε αυτήν την τιμή για να εξάγετε διαφορετική σελίδα ή να κάνετε βρόχο στις σελίδες για μαζική μετατροπή.

```java
// set page index
opts.setPageIndex(0);
```

### Βήμα 4: Αποθήκευση του εγγράφου ως PNG (αποθήκευση OneNote ως PNG)

Καλώντας το `save` γράφει την επιλεγμένη σελίδα σε αρχείο PNG στο δίσκο. Το όνομα αρχείου `ConvertSpecificPageToPngImage_out.png` είναι μόνο ένα παράδειγμα—μπορείτε να το ονομάσετε όπως θέλετε. Αυτό το τελικό βήμα **exports onenote page image** έτοιμο για χρήση σε αναφορές, ιστοσελίδες ή περαιτέρω επεξεργασία.

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

## Συχνά προβλήματα & συμβουλές

- **Λανθασμένος δείκτης σελίδας** – Θυμηθείτε ότι η αρίθμηση ξεκινά από 0. Αν λάβετε μια κενή εικόνα, ελέγξτε την τιμή του δείκτη.  
- **Λείπει το Aspose.Note JAR** – Βεβαιωθείτε ότι το JAR βρίσκεται στο classpath· διαφορετικά θα δείτε `ClassNotFoundException`.  
- **Μεγάλες σελίδες** – Για πολύ μεγάλες σελίδες, σκεφτείτε να αυξήσετε το μέγεθος της μνήμης heap της JVM (`-Xmx`) για να αποφύγετε `OutOfMemoryError`.  
- **Έλεγχος ανάλυσης** – Χρησιμοποιήστε `opts.setResolution(300)` (ή οποιοδήποτε DPI χρειάζεστε) πριν καλέσετε `save` για να βελτιώσετε την καθαρότητα της εικόνας.  

## Συχνές ερωτήσεις

**Q1: Μπορώ να μετατρέψω πολλές σελίδες σε εικόνες PNG με μία ενέργεια χρησιμοποιώντας Aspose.Note for Java;**  
A1: Ναι, μπορείτε να επαναλάβετε τις σελίδες του εγγράφου, να ενημερώσετε `opts.setPageIndex(i)`, και να καλέσετε `save` για κάθε επανάληψη.

**Q2: Υποστηρίζει το Aspose.Note for Java άλλες μορφές εικόνας εκτός του PNG;**  
A2: Απόλυτα. Ορίστε `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp`, ή `SaveFormat.Tiff` στο `ImageSaveOptions` για να δημιουργήσετε αυτές τις μορφές.

**Q3: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.Note for Java;**  
A3: Ναι, μπορείτε να κατεβάσετε μια δωρεάν δοκιμή από τη [Aspose Note download page](https://releases.aspose.com/).

**Q4: Πού μπορώ να λάβω τεχνική βοήθεια αν αντιμετωπίσω προβλήματα;**  
A5: Μπορείτε να ζητήσετε υποστήριξη από το φόρουμ της κοινότητας Aspose [Aspose community forum](https://forum.aspose.com/c/note/28).

**Q5: Πώς μπορώ να αγοράσω άδεια για το Aspose.Note for Java;**  
A5: Μπορείτε να αγοράσετε άδεια από τη [purchase page](https://purchase.aspose.com/buy).

**Q6: Πώς αντιμετωπίζονται οι ενσωματωμένες εικόνες κατά την εξαγωγή;**  
A6: Οι ενσωματωμένες εικόνες αποδίδονται αυτόματα στην έξοδο PNG· δεν απαιτείται επιπλέον κώδικας.

**Q7: Μπορώ να ορίσω το DPI ή την ανάλυση της εικόνας;**  
A7: Ναι, χρησιμοποιήστε `opts.setResolution(int dpi)` πριν καλέσετε `save` για να ελέγξετε την ποιότητα εξόδου.

---

**Τελευταία ενημέρωση:** 2026-09-04  
**Δοκιμάστηκε με:** Aspose.Note for Java 24.11 (latest)  
**Συγγραφέας:** Aspose

## Σχετικά μαθήματα

- [Εξαγωγή OneNote σε εικόνα BMP χρησιμοποιώντας τις επιλογές αποθήκευσης εικόνας του Aspose.Note for Java](/note/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/)
- [Εξαγωγή σελίδων OneNote – Μετατροπή συγκεκριμένου εύρους σελίδων σε PDF με Java](/note/java/onenote-document-loading/convert-page-range-to-pdf/)
- [Μάθετε πώς να αυξήσετε το DPI του JPEG – Ορίστε την ανάλυση εξόδου εικόνας στο OneNote με Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}