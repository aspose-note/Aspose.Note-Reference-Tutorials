---
date: 2026-06-30
description: Μάθετε πώς να εξάγετε το OneNote αποθηκεύοντας ένα έγγραφο ως εικόνα
  PNG σε grayscale χρησιμοποιώντας το Aspose.Note για Java. Περιλαμβάνει βήματα για
  τη φόρτωση του εγγράφου OneNote και τη δημιουργία εικόνας σε grayscale.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Πώς να εξάγετε το OneNote ως εικόνα σε grayscale – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: Πώς να εξάγετε το OneNote ως εικόνα σε grayscale – Aspose.Note
url: /el/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση σε Ασπρόμαυρη Εικόνα στο OneNote - Aspose.Note

## Εισαγωγή

Σε αυτό το μάθημα θα ανακαλύψετε **πώς να εξάγετε το onenote** μετατρέποντας ένα αρχείο OneNote `.one` σε μια υψηλής ποιότητας ασπρόμαυρη εικόνα PNG χρησιμοποιώντας το Aspose.Note για Java. Η μετατροπή σε ασπρόμαυρο συχνά απαιτείται από προγραμματιστές Java για εκτύπωση, αρχειοθέτηση ή για **μείωση του μεγέθους του OneNote** χωρίς να χάσετε το απαραίτητο περιεχόμενο. Θα περάσουμε από τη φόρτωση ενός εγγράφου OneNote, τη διαμόρφωση των επιλογών αποθήκευσης—συμπεριλαμβανομένης της **ρύθμισης της ανάλυσης της εικόνας**—και τέλος την αποθήκευση του εγγράφου ως PNG.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει «πώς να εξάγετε το onenote»;** Αναφέρεται στη προγραμματιστική μετατροπή ενός αρχείου OneNote σε άλλη μορφή, όπως μια εικόνα, χρησιμοποιώντας κώδικα.  
- **Ποια μορφή είναι η καλύτερη για ασπρόμαυρη έξοδο;** Το PNG λειτουργεί καλά επειδή διατηρεί την απώλεια‑μη‑ποιότητας και υποστηρίζει μια ειδική ασπρόμαυρη χρωματική λειτουργία.  
- **Χρειάζομαι άδεια;** Απαιτείται έγκυρη άδεια Aspose.Note για παραγωγική χρήση· μια προσωρινή δοκιμαστική άδεια είναι διαθέσιμη για δοκιμές.  
- **Ποια έκδοση της Java απαιτείται;** Συνιστάται Java 8 ή νεότερη.  
- **Μπορώ να αλλάξω το μέγεθος της εικόνας;** Ναι, μπορείτε να ρυθμίσετε τις ιδιότητες του `ImageSaveOptions` όπως `Resolution` ή `PageSize` πριν από την αποθήκευση.  

## Τι είναι «πώς να εξάγετε το onenote»;

Η εξαγωγή του OneNote σημαίνει προγραμματιστική μετατροπή ενός αρχείου OneNote `.one` σε άλλη αναπαράσταση—όπως PDF, HTML ή εικόνα. Σε αυτόν τον οδηγό εστιάζουμε στη **δημιουργία ασπρόμαυρων PNG** εικόνων, μια συχνή απαίτηση για τεκμηρίωση ή ροές εργασίας έτοιμες για εκτύπωση. Χρησιμοποιώντας το Aspose.Note, η μετατροπή γίνεται εξ ολοκλήρου στη μνήμη, έτσι δεν χρειάζεται ποτέ να έχετε εγκατεστημένο το Microsoft OneNote στον διακομιστή.

## Γιατί να εξάγετε το OneNote ως ασπρόμαυρη εικόνα;

Τα ασπρόμαυρα PNG είναι συνήθως **30‑40 % μικρότερα** από τα πλήρους χρώματος αντίστοιχα, κάτι που επιταχύνει την παράδοση στο web και μειώνει το κόστος αποθήκευσης. Παρέχουν επίσης **καλύτερη αντίθεση** σε εκτυπωτές λέιζερ, κάνοντας τις αναφορές πιο ευανάγνωστες. Επειδή το PNG υποστηρίζεται καθολικά, τα παραγόμενα αρχεία λειτουργούν σε προγράμματα περιήγησης, κινητές συσκευές και επιτραπέζιους επεξεργαστές χωρίς πρόσθετους κωδικοποιητές.

## Προαπαιτούμενα

1. Java Development Kit (JDK) 8 ή νεότερο εγκατεστημένο.  
2. Βιβλιοθήκη Aspose.Note για Java – κατεβάστε την τελευταία έκδοση από [εδώ](https://releases.aspose.com/note/java/).  
3. Βασική κατανόηση της σύνταξης Java και της ρύθμισης έργου Maven/Gradle.  

## Εισαγωγή Πακέτων

Η κλάση `ImageSaveOptions` ελέγχει πώς το έγγραφο αποδίδεται σε εικόνα.  
`ColorMode` είναι μια απαρίθμηση που σας επιτρέπει να εναλλάσσετε μεταξύ πλήρους χρώματος και ασπρόμαυρης εξόδου.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Βήμα 1: Φόρτωση του Εγγράφου OneNote

`Document` αντιπροσωπεύει ένα σημειωματάριο OneNote και παρέχει μεθόδους για φόρτωση, επεξεργασία και αποθήκευση του περιεχομένου του. Πρώτα, **φορτώστε το έγγραφο OneNote** στο Aspose.Note. Αντικαταστήστε το `"Your Document Directory"` με τη διαδρομή προς το τοπικό σας φάκελο και το `"Aspose.one"` με το όνομα του αρχείου OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Βήμα 2: Ορισμός Διαδρομής Εξόδου και Επιλογών

`ImageSaveOptions` διαμορφώνει πώς ένα έγγραφο OneNote αποδίδεται σε αρχείο εικόνας. Η απαρίθμηση `ColorMode` επιλέγει τη λειτουργία απόδοσης χρώματος, όπως ασπρόμαυρο ή πλήρες χρώμα. Ορίστε τη διαδρομή εξόδου για την ασπρόμαυρη εικόνα και καθορίστε τις επιλογές αποθήκευσης. Θα ορίσουμε το `ColorMode` σε `GrayScale` και θα χρησιμοποιήσουμε τη μορφή **αποθήκευσης εγγράφου ως PNG**. Μπορείτε επίσης να **ρυθμίσετε την ανάλυση της εικόνας** στα 300 DPI για εκτυπώσεις υψηλής ποιότητας.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Βήμα 3: Αποθήκευση του Εγγράφου

Τέλος, αποθηκεύστε το έγγραφο ως ασπρόμαυρη εικόνα PNG χρησιμοποιώντας τις ρυθμισμένες επιλογές. Η μέθοδος `save` γράφει το αρχείο στον δίσκο χωρίς να απαιτούνται ενδιάμεσα προσωρινά αρχεία.

```java
oneFile.save(dataDir, options);
```

## Συνηθισμένα Προβλήματα και Λύσεις
- **FileNotFoundException** – Επαληθεύστε ότι το `dataDir` δείχνει στον σωστό φάκελο και ότι το αρχείο `.one` υπάρχει.  
- **LicenseException** – Βεβαιωθείτε ότι έχετε εφαρμόσει μια έγκυρη άδεια Aspose.Note πριν καλέσετε το `save`.  
- **Low‑resolution output** – Ρυθμίστε το `options.setResolution(300)` για αύξηση DPI· υψηλότερο DPI δίνει πιο καθαρές εκτυπώσεις αλλά μεγαλύτερα αρχεία.  

## Συχνές Ερωτήσεις

**Q1: Μπορώ να αποθηκεύσω την ασπρόμαυρη εικόνα σε διαφορετική μορφή;**  
A1: Ναι, απλώς αλλάξτε την παράμετρο `SaveFormat` στον κατασκευαστή `ImageSaveOptions` σε `Jpeg`, `Bmp` ή οποιαδήποτε από τις 20+ υποστηριζόμενες μορφές εικόνας.

**Q2: Είναι το Aspose.Note συμβατό με όλες τις εκδόσεις εγγράφων OneNote;**  
A2: Το Aspose.Note υποστηρίζει το Microsoft OneNote 2010 και μεταγενέστερες εκδόσεις, καλύπτοντας πάνω από 95 % των σημειωματάριων που χρησιμοποιούνται ενεργά σήμερα.

**Q3: Απαιτεί το Aspose.Note άδεια για χρήση;**  
A3: Απαιτείται έγκυρη άδεια για παραγωγική χρήση, αλλά μπορεί να ληφθεί προσωρινή δοκιμαστική άδεια για αξιολόγηση χωρίς κόστος.

**Q4: Μπορώ να επεξεργαστώ άλλα στοιχεία του εγγράφου πριν το αποθηκεύσω ως εικόνα;**  
A4: Απολύτως! Το Aspose.Note παρέχει API για επεξεργασία ενοτήτων, σελίδων και μεμονωμένων στοιχείων όπως κείμενο, πίνακες και εικόνες πριν από την εξαγωγή.

**Q5: Πού μπορώ να βρω υποστήριξη αν αντιμετωπίσω προβλήματα;**  
A5: Μπορείτε να βρείτε υποστήριξη στο φόρουμ Aspose.Note [εδώ](https://forum.aspose.com/c/note/28).

## Συμπέρασμα

Τώρα έχετε μάθει **πώς να εξάγετε το onenote** φορτώνοντας ένα αρχείο OneNote, διαμορφώνοντας τις επιλογές αποθήκευσης για **δημιουργία ασπρόμαυρης εικόνας**, και **αποθηκεύοντας το έγγραφο ως PNG**. Αυτή η προσέγγιση είναι ιδανική για τη δημιουργία ελαφριών, έτοιμων για εκτύπωση οπτικών από σημειωματάρια OneNote. Μη διστάσετε να πειραματιστείτε με άλλες ρυθμίσεις `ColorMode`, υψηλότερες τιμές DPI ή εναλλακτικές μορφές εικόνας ώστε να ταιριάζουν στις απαιτήσεις του έργου σας.

---

**Τελευταία Ενημέρωση:** 2026-06-30  
**Δοκιμή Με:** Aspose.Note 27.0 for Java  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Εξαγωγή Σελίδας OneNote σε Εικόνα PNG σε Java χρησιμοποιώντας Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote ορισμός ανάλυσης jpeg – Ορισμός Ανάλυσης Εικόνας Εξόδου στο OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Πώς να Αποθηκεύσετε το OneNote ως PDF με Aspose.Note για Java](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}