---
title: Αποθήκευση σε PDF χρησιμοποιώντας τις Ρυθμίσεις σελίδας στο OneNote - Aspose.Note
linktitle: Αποθήκευση σε PDF χρησιμοποιώντας τις Ρυθμίσεις σελίδας στο OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Μάθετε πώς να αποθηκεύετε έγγραφα OneNote σε PDF σε Java χρησιμοποιώντας τη βιβλιοθήκη Aspose.Note. Οδηγός βήμα προς βήμα με παραδείγματα κώδικα για διαφορετικές ρυθμίσεις σελίδας.
weight: 19
url: /el/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση σε PDF χρησιμοποιώντας τις Ρυθμίσεις σελίδας στο OneNote - Aspose.Note

## Εισαγωγή

Σε αυτό το σεμινάριο, θα μάθουμε πώς να αποθηκεύουμε έγγραφα του OneNote σε μορφή PDF χρησιμοποιώντας διαφορετικές ρυθμίσεις σελίδας με το Aspose.Note για Java. Θα καλύψουμε δύο μεθόδους: αποθήκευση με ρυθμίσεις σελίδας Letter και αποθήκευση με ρυθμίσεις σελίδας A4 χωρίς όριο ύψους.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

1. Το Java Development Kit (JDK) είναι εγκατεστημένο στο σύστημά σας.
2. Το Aspose.Note για τη βιβλιοθήκη Java κατεβάστηκε και συμπεριλήφθηκε στο έργο σας Java.
3. Βασική κατανόηση της γλώσσας προγραμματισμού Java.

## Εισαγωγή πακέτων

Βεβαιωθείτε ότι έχετε εισαγάγει τα απαραίτητα πακέτα για τη χρήση του Aspose.Note για Java στο έργο σας. Ακολουθεί η δήλωση εισαγωγής:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Αποθήκευση σε PDF χρησιμοποιώντας τις Ρυθμίσεις σελίδας Letter

### Βήμα 1: Φορτώστε το έγγραφο

Αρχικά, φορτώστε το έγγραφο του OneNote στο Aspose.Σημείωση:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Βήμα 2: Καθορίστε τη διαδρομή προορισμού

Καθορίστε τη διαδρομή προορισμού για το αρχείο PDF:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Βήμα 3: Αποθηκεύστε το έγγραφο

Αποθηκεύστε το έγγραφο με τις ρυθμίσεις σελίδας Letter:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Αποθήκευση σε PDF χρησιμοποιώντας Ρυθμίσεις σελίδας A4 χωρίς όριο ύψους

### Βήμα 1: Φορτώστε το έγγραφο

Ομοίως, φορτώστε το έγγραφο του OneNote στο Aspose.Σημείωση:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Βήμα 2: Καθορίστε τη διαδρομή προορισμού

Καθορίστε τη διαδρομή προορισμού για το αρχείο PDF:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Βήμα 3: Αποθηκεύστε το έγγραφο

Αποθηκεύστε το έγγραφο με ρυθμίσεις σελίδας Α4 χωρίς όριο ύψους:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Αφού ακολουθήσετε αυτά τα βήματα, θα έχετε αποθηκεύσει με επιτυχία το έγγραφο OneNote σε PDF χρησιμοποιώντας διαφορετικές ρυθμίσεις σελίδας.

## συμπέρασμα

Σε αυτό το σεμινάριο, έχουμε εξερευνήσει τον τρόπο αποθήκευσης εγγράφων του OneNote σε μορφή PDF χρησιμοποιώντας το Aspose.Note για τη βιβλιοθήκη Java. Ακολουθώντας τον οδηγό βήμα προς βήμα, μπορείτε εύκολα να ενσωματώσετε αυτή τη λειτουργία στις εφαρμογές σας Java.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να προσαρμόσω περαιτέρω τις ρυθμίσεις της σελίδας;

A1: Ναι, μπορείτε να προσαρμόσετε τις ρυθμίσεις σελίδας σύμφωνα με τις απαιτήσεις σας χρησιμοποιώντας το Aspose.Note για Java.

### Ε2: Το Aspose.Note υποστηρίζει άλλες μορφές εξόδου εκτός από το PDF;

A2: Ναι, το Aspose.Note υποστηρίζει διάφορες μορφές εξόδου, συμπεριλαμβανομένων εικόνων και HTML.

### Ε3: Είναι το Aspose.Note συμβατό με διαφορετικές εκδόσεις αρχείων OneNote;

A3: Ναι, το Aspose.Note υποστηρίζει αρχεία OneNote από διαφορετικές εκδόσεις, συμπεριλαμβανομένων των .one και .onetoc2.

### Ε4: Μπορώ να μετατρέψω πολλά αρχεία OneNote σε PDF σε μία μόνο εκτέλεση;

A4: Ναι, μπορείτε να επεξεργαστείτε ομαδικά πολλά αρχεία OneNote χρησιμοποιώντας το Aspose.Note για Java.

### Ε5: Υπάρχει κάποια δοκιμαστική έκδοση διαθέσιμη για δοκιμαστικούς σκοπούς;

A5: Ναι, μπορείτε να λάβετε μια δωρεάν δοκιμή του Aspose.Note για Java από τον ιστότοπο.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
