---
title: Μετατροπή σημειωματάριου σε επίπεδη εικόνα στο OneNote - Aspose.Note
linktitle: Μετατροπή σημειωματάριου σε επίπεδη εικόνα στο OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Μάθετε πώς να μετατρέπετε ένα σημειωματάριο σε μια επίπεδη εικόνα στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Διατηρήστε όλα τα στοιχεία σε ένα μόνο αρχείο εικόνας χωρίς κόπο.
weight: 13
url: /el/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή σημειωματάριου σε επίπεδη εικόνα στο OneNote - Aspose.Note

## Εισαγωγή

Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία μετατροπής ενός σημειωματάριου σε μια επίπεδη εικόνα στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Αυτό σας επιτρέπει να αποθηκεύσετε το σημειωματάριό σας ως αρχείο εικόνας, διασφαλίζοντας ότι όλα τα στοιχεία διατηρούνται σε μια ενιαία μορφή εικόνας.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

1. Το Java Development Kit (JDK) είναι εγκατεστημένο στο σύστημά σας.
2.  Λήψη και ρύθμιση της βιβλιοθήκης Aspose.Note για Java στο έργο σας Java. Μπορείτε να κατεβάσετε τη βιβλιοθήκη από[εδώ](https://releases.aspose.com/note/java/).
3. Βασικές γνώσεις προγραμματισμού Java.

## Εισαγωγή πακέτων

Για να ξεκινήσετε, πρέπει να εισαγάγετε τα απαραίτητα πακέτα από το Aspose.Note για Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Βήμα 1: Ρύθμιση καταλόγου εγγράφων

Αρχικά, ορίστε τον κατάλογο όπου βρίσκεται το αρχείο του σημειωματάριου σας:

```java
String dataDir = "Your Document Directory";
```

 Αντικαθιστώ`"Your Document Directory"` με τη διαδρομή προς το αρχείο του σημειωματάριου σας.

## Βήμα 2: Φόρτωση σημειωματάριου

 Στη συνέχεια, φορτώστε το αρχείο του σημειωματάριου χρησιμοποιώντας το`Notebook` τάξη:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Φροντίστε να αντικαταστήσετε`"test.onetoc2"` με το όνομα του αρχείου του σημειωματάριου σας.

## Βήμα 3: Ορίστε τις επιλογές αποθήκευσης εικόνας

Τώρα, ρυθμίστε τις επιλογές για την αποθήκευση του σημειωματάριου ως εικόνα. Θα καθορίσουμε τη μορφή αποθήκευσης ως PNG και θα ορίσουμε την ανάλυση στα 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Μπορείτε να προσαρμόσετε την ανάλυση σύμφωνα με τις απαιτήσεις σας.

## Βήμα 4: Ισιώνετε το σημειωματάριο

Για να διασφαλίσετε ότι όλα τα στοιχεία ισοπεδώνονται σε μια ενιαία εικόνα, ρυθμίστε το`flatten` επιλογή να`true`:

```java
saveOptions.setFlatten(true);
```

Αυτό διασφαλίζει ότι η εικόνα που προκύπτει διατηρεί τη διάταξη του σημειωματάριου σας.

## Βήμα 5: Αποθήκευση εικόνας

Τέλος, αποθηκεύστε το σημειωματάριο ως επίπεδη εικόνα:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Αντικαθιστώ`"ExportImageasFlattenedNotebook_out.png"` με το επιθυμητό όνομα αρχείου εξόδου.

## συμπέρασμα

Συμπερασματικά, χρησιμοποιώντας το Aspose.Note για Java, μπορείτε εύκολα να μετατρέψετε το σημειωματάριό σας σε μια επίπεδη εικόνα στο OneNote. Αυτή η διαδικασία διασφαλίζει ότι όλα τα στοιχεία διατηρούνται σε μια ενιαία μορφή εικόνας, διευκολύνοντας την εύκολη κοινή χρήση και προβολή.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να προσαρμόσω την ανάλυση της εικόνας εξόδου;

 A1: Ναι, μπορείτε να προσαρμόσετε την ανάλυση σύμφωνα με τις απαιτήσεις σας τροποποιώντας το`setResolution` παράμετρος μεθόδου.

### Ε2: Το Aspose.Note υποστηρίζει άλλες μορφές εικόνας για εξαγωγή;

A2: Ναι, το Aspose.Note υποστηρίζει διάφορες μορφές εικόνας, όπως PNG, JPEG, BMP, κ.λπ., για εξαγωγή φορητών υπολογιστών.

### Ε3: Μπορώ να προσαρμόσω περαιτέρω την εικόνα εξόδου;

A3: Ναι, το Aspose.Note παρέχει εκτενείς επιλογές για την προσαρμογή της εικόνας εξόδου, συμπεριλαμβανομένων των ρυθμίσεων μεγέθους σελίδας, προσανατολισμού και ποιότητας.

### Ε4: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Note για Java;

 A4: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμαστική έκδοση από[εδώ](https://releases.aspose.com/).

### Ε5: Πού μπορώ να βρω υποστήριξη για το Aspose.Note για Java;

 A5: Μπορείτε να βρείτε υποστήριξη και πόρους στο φόρουμ Aspose.Note[εδώ](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
