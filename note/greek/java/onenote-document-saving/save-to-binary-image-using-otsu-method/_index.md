---
date: 2026-09-19
description: Μάθετε binary image conversion των αρχείων OneNote με τη μέθοδο Otsu
  σε Java χρησιμοποιώντας το Aspose.Note. Μετατρέψτε το OneNote σε PNG, εφαρμόστε
  image thresholding Otsu και λάβετε black‑white images για OCR.
keywords:
- binary image conversion
- image thresholding otsu
- save onenote png
- black white image java
lastmod: 2026-09-19
linktitle: Binary image conversion του OneNote χρησιμοποιώντας τη μέθοδο Otsu σε Java
og_description: Μάθετε binary image conversion των αρχείων OneNote με τη μέθοδο Otsu
  σε Java χρησιμοποιώντας το Aspose.Note. Μετατρέψτε το OneNote σε PNG, εφαρμόστε
  image thresholding Otsu και λάβετε black‑white images για OCR.
og_image_alt: Developer guide showing OneNote to binary PNG conversion using Aspose.Note
  Java API
og_title: Binary image conversion του OneNote χρησιμοποιώντας τη μέθοδο Otsu σε Java
schemas:
- author: Aspose
  dateModified: '2026-09-19'
  description: Learn binary image conversion of OneNote files with the Otsu method
    in Java using Aspose.Note. Convert OneNote to PNG, apply image thresholding Otsu,
    and get black‑white images for OCR.
  headline: Binary image conversion of OneNote using Otsu method in Java
  type: TechArticle
- questions:
  - answer: Yes, the API provides methods such as `document.getPages().get(i).getText()`
      to retrieve plain‑text content programmatically.
    question: Can I use Aspose.Note for Java to extract text from OneNote documents?
  - answer: Absolutely. It supports the legacy `.one` format as well as the newer
      `.onetoc2` and `.onepkg` containers used by recent Office releases.
    question: Is Aspose.Note for Java compatible with different versions of OneNote
      files?
  - answer: Yes, you can switch to other algorithms (e.g., `BinarizationMethod.Niblack`)
      or adjust parameters like `windowSize` and `kFactor` to fine‑tune the thresholding
      behavior.
    question: Can I customize the binarization options for saving documents as binary
      images?
  - answer: While the library focuses on OneNote‑to‑image conversion, you can combine
      OCR output with the `Document` API to reconstruct pages, effectively converting
      images back into a OneNote notebook.
    question: Does Aspose.Note for Java support converting binary images back to OneNote
      documents?
  - answer: Visit the Aspose.Note community forum, consult the official API reference,
      or open a support ticket through the Aspose customer portal.
    question: Where can I get support if I encounter issues while using Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- binary image conversion
- Aspose.Note
- Java image processing
- OneNote PNG export
title: Binary image conversion του OneNote χρησιμοποιώντας τη μέθοδο Otsu σε Java
url: /el/java/onenote-document-saving/save-to-binary-image-using-otsu-method/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δυαδική μετατροπή εικόνας OneNote με τη μέθοδο Otsu σε Java

Σε αυτό το μάθημα θα μάθετε **binary image conversion** εγγράφων OneNote εφαρμόζοντας την τεχνική κατωφλίου Otsu με το Aspose.Note for Java. Η μετατροπή μιας σελίδας OneNote σε ασπρόμαυρο PNG είναι χρήσιμη για προεπεξεργασία OCR, μείωση του μεγέθους αποθήκευσης ή τροφοδότηση εικόνων σε επόμενες διεργασίες υπολογιστικής όρασης. Τα παρακάτω βήματα σας καθοδηγούν στη φόρτωση ενός αρχείου `.one`, στη ρύθμιση της δυαδικοποίησης και στην αποθήκευση του αποτελέσματος ως ελαφριά δυαδική εικόνα.

## Σύντομες απαντήσεις
- **Τι κάνει η μέθοδος Otsu;** Επιλέγει αυτόματα το βέλτιστο κατώφλι γκρι κλίμακας που διαχωρίζει το προσκήνιο από το φόντο, παράγοντας μια καθαρή ασπρόμαυρη εικόνα.  
- **Ποια μορφή χρησιμοποιείται για το αποτέλεσμα;** PNG, επειδή προσφέρει συμπίεση χωρίς απώλειες και ευρεία υποστήριξη πλατφόρμας.  
- **Χρειάζομαι άδεια για την εκτέλεση του κώδικα;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγικές εγκαταστάσεις.  
- **Μπορώ να αλλάξω το αποτέλεσμα σε άλλη μορφή;** Ναι – αντικαταστήστε `SaveFormat.Png` με οποιαδήποτε μορφή αναφέρεται στις επιλογές αποθήκευσης εικόνας του Aspose.Note.  
- **Είναι κατάλληλο για OCR;** Απόλυτα – τα δυαδικά PNG βελτιώνουν δραματικά την ακρίβεια του OCR εξαλείφοντας τον γκρι θόρυβο.

## Τι είναι η μέθοδος Otsu;

Η μέθοδος Otsu καθορίζει αυτόματα το βέλτιστο κατώφλι που μετατρέπει μια εικόνα γκρι κλίμακας σε δυαδική (ασπρόμαυρη) εικόνα ελαχιστοποιώντας την ενδο‑τάξη διακύμανση. Αυτός ο αλγόριθμος μονού περάσματος είναι γρήγορος, λειτουργεί σε οποιοδήποτε μέγεθος εικόνας και είναι ιδανικός για προεπεξεργασία σελίδων OneNote πριν από OCR ή εργασίες αναγνώρισης προτύπων.

## Γιατί να αποθηκεύσετε το OneNote ως PNG;

Η αποθήκευση σελίδων OneNote ως PNG παρέχει μια καθολικά αναγνώσιμη, χωρίς απώλειες, αναπαράσταση που μπορεί να καταναλωθεί από προγράμματα περιήγησης, κινητές εφαρμογές και μηχανές OCR. Το PNG υποστηρίζει επίσης διαφάνεια, χρήσιμη όταν συνθέτετε εικόνες αργότερα. Επειδή το PNG είναι μορφή raster, το μέγεθος του αρχείου παραμένει μέτριο—το Aspose.Note μπορεί να επεξεργαστεί σημειωματάρια με **up to 500 pages** χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, καθιστώντας τη μετατροπή κλιμακώσιμη για μεγάλα αρχεία.

## Προαπαιτούμενα
- Java Development Kit (JDK) 8 ή νεότερο εγκατεστημένο.  
- Maven ή Gradle για διαχείριση εξαρτήσεων, ή το JAR του Aspose.Note προστεθειμένο χειροκίνητα στο classpath.  
- Έγκυρη άδεια Aspose.Note for Java για παραγωγική χρήση (η δωρεάν δοκιμή λειτουργεί για δοκιμές).  

## Εισαγωγή πακέτων

Οι κλάσεις `Document`, `ImageBinarizationOptions` και `ImageSaveOptions` αποτελούν μέρος του API του Aspose.Note.  

`Document` είναι το αντικείμενο υψηλότερου επιπέδου που αντιπροσωπεύει ένα αρχείο OneNote στη μνήμη.  
`ImageBinarizationOptions` περιέχει ρυθμίσεις για τον αλγόριθμο δυαδικοποίησης, συμπεριλαμβανομένης της επιλογής Otsu.  
`ImageSaveOptions` ορίζει τη μορφή εξόδου, την ανάλυση και τη χρωματική λειτουργία για την αποθηκευμένη εικόνα.

## Βήμα 1: φόρτωση του εγγράφου OneNote

Καθορίστε το φάκελο που περιέχει το αρχείο `.one` και δημιουργήστε ένα αντικείμενο `Document`. Η κλάση `Document` διαβάζει τη δομή του αρχείου OneNote και κάνει κάθε σελίδα διαθέσιμη για περαιτέρω επεξεργασία.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Βήμα 2: ρύθμιση της δυαδικοποίησης με Otsu

Δημιουργήστε ένα αντικείμενο `ImageBinarizationOptions` και ορίστε την ιδιότητα `method` σε `BinarizationMethod.Otsu`. Αυτό λέει στο Aspose.Note να εφαρμόσει τον αλγόριθμο Otsu κατά την απόδοση της εικόνας.

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Βήμα 3: ορισμός επιλογών αποθήκευσης εικόνας (PNG, ασπρόμαυρο)

Δημιουργήστε ένα αντικείμενο `ImageSaveOptions`, καθορίστε `SaveFormat.Png` και εξαναγκάστε τη χρωματική λειτουργία σε ασπρόμαυρο. Συνδέστε το προηγούμενο `ImageBinarizationOptions` ώστε η κατωφλίωση Otsu να εκτελείται κατά την αποθήκευση.

```java
dataDir = dataDir + "SaveToBinaryImageUsingOtsuMethod_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.Otsu);
```

## Βήμα 4: αποθήκευση του εγγράφου ως δυαδική εικόνα

Καλέστε τη μέθοδο `save` στο αντικείμενο `Document`, περνώντας τη διαδρομή του αρχείου προορισμού και τις ρυθμισμένες `ImageSaveOptions`. Το αποτέλεσμα είναι ένα δυαδικό PNG όπου κάθε pixel είναι είτε καθαρό μαύρο είτε καθαρό λευκό.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## Συχνά προβλήματα & συμβουλές
- **File not found:** Βεβαιωθείτε ότι το `dataDir` τελειώνει με το κατάλληλο διαχωριστικό διαδρομής (`/` σε Unix, `\\` σε Windows) πριν προσθέσετε το όνομα αρχείου.  
- **Blank output:** Η πηγή σελίδας OneNote πρέπει να περιέχει ορατό περιεχόμενο· κενές σελίδες παράγουν κενό PNG.  
- **Performance:** Για σημειωματάρια μεγαλύτερα από 200 σελίδες, επεξεργαστείτε τις σελίδες σε βρόχο και απελευθερώστε κάθε αντικείμενο `Document` μετά την αποθήκευση για να διατηρήσετε τη χρήση μνήμης χαμηλή.  
- **Resolution control:** Χρησιμοποιήστε `options.setResolution(300)` για αύξηση DPI ώστε να έχετε υψηλότερης ποιότητας είσοδο OCR.  

## Συχνές ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω το Aspose.Note for Java για εξαγωγή κειμένου από έγγραφα OneNote;**  
Α: Ναι, το API παρέχει μεθόδους όπως `document.getPages().get(i).getText()` για την ανάκτηση του απλού κειμένου προγραμματιστικά.

**Ε: Είναι το Aspose.Note for Java συμβατό με διαφορετικές εκδόσεις αρχείων OneNote;**  
Α: Απόλυτα. Υποστηρίζει τη παλαιότερη μορφή `.one` καθώς και τα νεότερα containers `.onetoc2` και `.onepkg` που χρησιμοποιούνται στις πρόσφατες εκδόσεις του Office.

**Ε: Μπορώ να προσαρμόσω τις επιλογές δυαδικοποίησης για αποθήκευση εγγράφων ως δυαδικές εικόνες;**  
Α: Ναι, μπορείτε να μεταβείτε σε άλλους αλγόριθμους (π.χ., `BinarizationMethod.Niblack`) ή να ρυθμίσετε παραμέτρους όπως `windowSize` και `kFactor` για λεπτομερή ρύθμιση της συμπεριφοράς του κατωφλίου.

**Ε: Υποστηρίζει το Aspose.Note for Java τη μετατροπή δυαδικών εικόνων πίσω σε έγγραφα OneNote;**  
Α: Ενώ η βιβλιοθήκη εστιάζει στη μετατροπή OneNote‑σε‑εικόνα, μπορείτε να συνδυάσετε την έξοδο OCR με το API `Document` για την ανακατασκευή σελίδων, μετατρέποντας ουσιαστικά τις εικόνες ξανά σε σημειωματάριο OneNote.

**Ε: Πού μπορώ να λάβω υποστήριξη εάν αντιμετωπίσω προβλήματα κατά τη χρήση του Aspose.Note for Java;**  
Α: Επισκεφθείτε το φόρουμ κοινότητας του Aspose.Note, συμβουλευτείτε την επίσημη τεκμηρίωση API ή ανοίξτε ένα ticket υποστήριξης μέσω του πελατειακού portal του Aspose.

**Ε: Πώς αλλάζω τη μορφή εξόδου από PNG σε JPEG;**  
Α: Αντικαταστήστε το `SaveFormat.Png` με `SaveFormat.Jpeg` στον κατασκευαστή `ImageSaveOptions` και, προαιρετικά, προσαρμόστε το επίπεδο συμπίεσης με `options.setJpegQuality(85)`.

**Ε: Υπάρχει τρόπος να ορίσω προσαρμοσμένο DPI για την εξαγόμενη εικόνα;**  
Α: Ναι, καλέστε `options.setResolution(300)` (ή οποιαδήποτε τιμή DPI) πριν από το `document.save(...)` για να ελέγξετε την ανάλυση εξόδου.

**Ε: Μπορώ να επεξεργαστώ πολλές σελίδες OneNote σε βρόχο;**  
Α: Σίγουρα—περιηγηθείτε στο `document.getPages()` και εφαρμόστε την ίδια λογική δυαδικοποίησης και αποθήκευσης σε κάθε σελίδα, αποθηκεύοντας τα αποτελέσματα με διαφορετικά ονόματα αρχείων.

---

**Τελευταία ενημέρωση:** 2026-09-19  
**Δοκιμάστηκε με:** Aspose.Note for Java 26.4  
**Συγγραφέας:** Aspose  

```java
// Save the document.
oneFile.save(dataDir, options);
```

## Σχετικά Μαθήματα

- [Χρησιμοποιήστε το Aspose.Note for Java για αποθήκευση OneNote ως PNG με επιλογές – Μετατροπή σημειωματάριου σε εικόνα](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [Εξαγωγή OneNote σε εικόνα BMP χρησιμοποιώντας τις επιλογές αποθήκευσης εικόνας του Aspose.Note for Java](/note/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/)
- [Μάθετε πώς να αυξήσετε το DPI του JPEG – Ορίστε την ανάλυση εξόδου εικόνας στο OneNote με το Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}