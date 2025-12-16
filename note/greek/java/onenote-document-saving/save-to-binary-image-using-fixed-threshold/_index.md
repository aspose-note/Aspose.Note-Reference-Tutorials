---
date: 2025-12-13
description: Μάθετε πώς να ρυθμίσετε το κατώφλι για να μετατρέψετε το OneNote σε PNG
  με το Aspose.Note Java, δημιουργώντας ασπρόμαυρες εικόνες OneNote χρησιμοποιώντας
  τη δυαδικοποίηση εικόνας σε Java.
linktitle: Save to Binary Image Using Fixed Threshold in OneNote
second_title: Aspose.Note Java API
title: Πώς να ρυθμίσετε το όριο κατά την αποθήκευση του OneNote σε δυαδική εικόνα
url: /el/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Ρυθμίσετε το Κατώφλι Κατά την Αποθήκευση του OneNote σε Δυαδική Εικόνα

## Εισαγωγή

Σε αυτό το tutorial θα ανακαλύψετε **πώς να ρυθμίσετε το threshold** για να εξάγετε μια σελίδα του Microsoft OneNote ως εικόνα PNG υψηλής αντίθεσης, ασπρόμαυρη. Με την προσαρμογή της σταθερής τιμής του threshold αποκτάτε ακριβή έλεγχο της μετατροπής, καθιστώντας το ιδανικό για σενάρια όπως η προεπεξεργασία OCR ή η αρχειοθέτηση εγγράφων. Θα περάσουμε από κάθε βήμα χρησιμοποιώντας το Aspose.Note Java API, ώστε να μπορείτε γρήγορα **convert OneNote to PNG** με αξιόπιστες τεχνικές **image binarization Java**.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει το “adjust threshold”;** Ορίζει το όριο έντασης pixel που χρησιμοποιείται κατά τη μετατροπή μιας έγχρωμης εικόνας σε ασπρόμαυρη.
- **Ποια μορφή παράγεται;** Ένα αρχείο PNG που μπορεί να ανοιχθεί από οποιονδήποτε προβολέα εικόνων.
- **Μπορώ να αλλάξω την τιμή του threshold;** Ναι – τροποποιήστε την κλήση `setBinarizationThreshold()`.
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.
- **Είναι συμβατό με όλες τις εκδόσεις του OneNote;** Το Aspose.Note υποστηρίζει OneNote 2010, 2013, 2016 και μεταγενέστερες.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

1. Εγκατεστημένο Java Development Kit (JDK).
2. Τη βιβλιοθήκη Aspose.Note for Java που έχετε κατεβάσει από [εδώ](https://releases.aspose.com/note/java/).
3. Βασική εξοικείωση με τη σύνταξη της Java.

## Εισαγωγή Πακέτων

Πρώτα, εισάγετε τις απαιτούμενες κλάσεις στο αρχείο πηγαίου κώδικα Java.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Βήμα 1: Φόρτωση του Εγγράφου

Φορτώστε το αρχείο OneNote που θέλετε να επεξεργαστείτε.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Βήμα 2: Ορισμός Επιλογών Δυαδικοποίησης

Ορίστε τις ρυθμίσεις **image binarization Java** και καθορίστε το σταθερό threshold που θέλετε να χρησιμοποιήσετε.

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

> **Pro tip:** Πειραματιστείτε με τιμές threshold μεταξύ 0‑255 για να βρείτε το ιδανικό σημείο για το συγκεκριμένο σας έγγραφο. Οι χαμηλότερες τιμές παράγουν πιο ανοιχτές εικόνες, ενώ οι υψηλότερες δίνουν πιο σκοτεινό αποτέλεσμα.

## Βήμα 3: Ορισμός Επιλογών Αποθήκευσης Εικόνας

Διαμορφώστε τη μορφή εικόνας, τη λειτουργία χρώματος και συνδέστε τις επιλογές δυαδικοποίησης.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

Η ρύθμιση `ColorMode.BlackAndWhite` εξασφαλίζει ότι το τελικό αρχείο είναι μια **black and white OneNote** εικόνα.

## Βήμα 4: Αποθήκευση του Εγγράφου

Εκτελέστε την ενέργεια αποθήκευσης με τις προηγουμένως ορισμένες επιλογές.

```java
oneFile.save(dataDir, options);
```

Μετά την εκτέλεση του κώδικα, θα βρείτε ένα αρχείο PNG με όνομα `SaveToBinaryImageUsingFixedThreshold_out.png` στον φάκελο εξόδου, έτοιμο για περαιτέρω επεξεργασία ή αρχειοθέτηση.

## Συμπέρασμα

Σας δείξαμε **πώς να ρυθμίσετε το threshold** για να δημιουργήσετε μια καθαρή, υψηλής αντίθεσης PNG από ένα αρχείο OneNote χρησιμοποιώντας το Aspose.Note for Java. Με την εξοικείωση στις επιλογές **image binarization Java**, μπορείτε αξιόπιστα **convert OneNote to PNG** και να δημιουργήσετε **black and white OneNote** πόρους για OCR, εκτύπωση ή ψηφιακή διατήρηση.

## Συχνές Ερωτήσεις

**Ε: Τι συμβαίνει αν θέσω το threshold πολύ χαμηλό;**  
Α: Η παραγόμενη εικόνα μπορεί να φαίνεται ξεθωριασμένη, με πολλούς γκρι τόνους αντί για καθαρό ασπρόμαυρο αντίθεση.

**Ε: Μπορώ να χρησιμοποιήσω διαφορετική μέθοδο δυαδικοποίησης;**  
Α: Ναι, το Aspose.Note υποστηρίζει επίσης προσαρμοστικό thresholding· απλώς αντικαταστήστε το `BinarizationMethod.FixedThreshold` με `BinarizationMethod.Adaptive`.

**Ε: Είναι δυνατόν να εξάγω απευθείας σε άλλες μορφές όπως JPEG;**  
Α: Απόλυτα—αλλάξτε το `SaveFormat.Png` σε `SaveFormat.Jpeg` στον κατασκευαστή `ImageSaveOptions`.

**Ε: Πώς διαχειρίζομαι αρχεία OneNote που προστατεύονται με κωδικό πρόσβασης;**  
Α: Φορτώστε το έγγραφο με την κατάλληλη υπερφόρτωση που δέχεται μια συμβολοσειρά κωδικού πριν εφαρμόσετε τα βήματα δυαδικοποίησης.

**Ε: Λειτουργεί αυτή η προσέγγιση σε Linux/macOS;**  
Α: Η βιβλιοθήκη Aspose.Note Java είναι ανεξάρτητη από πλατφόρμα, επομένως ο ίδιος κώδικας εκτελείται σε οποιοδήποτε λειτουργικό σύστημα με συμβατό JDK.

---

**Τελευταία ενημέρωση:** 2025-12-13  
**Δοκιμή με:** Aspose.Note for Java 24.12 (τελευταία έκδοση)  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}