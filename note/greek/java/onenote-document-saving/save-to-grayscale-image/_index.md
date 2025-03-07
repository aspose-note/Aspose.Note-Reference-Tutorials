---
title: Αποθήκευση στην εικόνα σε κλίμακα του γκρι στο OneNote - Aspose.Note
linktitle: Αποθήκευση στην εικόνα σε κλίμακα του γκρι στο OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Μάθετε πώς να αποθηκεύετε ένα έγγραφο ως εικόνα σε κλίμακα του γκρι στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Χειριστείτε εύκολα τα έγγραφα του Microsoft OneNote μέσω προγραμματισμού.
weight: 17
url: /el/java/onenote-document-saving/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση στην εικόνα σε κλίμακα του γκρι στο OneNote - Aspose.Note

## Εισαγωγή

Σε αυτό το σεμινάριο, θα διερευνήσουμε πώς να αποθηκεύσετε ένα έγγραφο ως εικόνα σε κλίμακα του γκρι στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Οι εικόνες σε κλίμακα του γκρι είναι μονόχρωμες εικόνες όπου οι πληροφορίες χρώματος αντιπροσωπεύονται μόνο με αποχρώσεις του γκρι. Το Aspose.Note είναι ένα ισχυρό Java API που επιτρέπει τον χειρισμό των εγγράφων του Microsoft OneNote μέσω προγραμματισμού.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

1. Το Java Development Kit (JDK) είναι εγκατεστημένο στο σύστημά σας.
2.  Aspose.Note για τη βιβλιοθήκη Java. Μπορείτε να το κατεβάσετε από[εδώ](https://releases.aspose.com/note/java/).
3. Βασική κατανόηση προγραμματισμού Java.

## Εισαγωγή πακέτων

Για να ξεκινήσετε, εισαγάγετε τα απαραίτητα πακέτα:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Βήμα 1: Φορτώστε το έγγραφο

 Αρχικά, φορτώστε το έγγραφο στο Aspose.Note. Αντικαθιστώ`"Your Document Directory"` με τη διαδρομή προς τον κατάλογο εγγράφων σας και`"Aspose.one"` με το όνομα του εγγράφου σας στο OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Βήμα 2: Ορίστε τη διαδρομή εξόδου και τις επιλογές

Καθορίστε τη διαδρομή εξόδου για την εικόνα σε κλίμακα του γκρι και καθορίστε τις επιλογές αποθήκευσης. Θα ρυθμίσουμε τη λειτουργία χρώματος σε κλίμακα του γκρι.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Βήμα 3: Αποθηκεύστε το έγγραφο

Τέλος, αποθηκεύστε το έγγραφο ως εικόνα σε κλίμακα του γκρι χρησιμοποιώντας τις καθορισμένες επιλογές.

```java
oneFile.save(dataDir, options);
```

## συμπέρασμα

Συγχαρητήρια! Μάθατε με επιτυχία πώς να αποθηκεύετε ένα έγγραφο ως εικόνα σε κλίμακα του γκρι στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Αυτό μπορεί να είναι απίστευτα χρήσιμο για διάφορες εφαρμογές όπου απαιτούνται εικόνες σε κλίμακα του γκρι.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να αποθηκεύσω την εικόνα σε κλίμακα του γκρι σε διαφορετική μορφή;

 Α1: Ναι, μπορείς. Απλώς αλλάξτε το`SaveFormat` παράμετρος στο`ImageSaveOptions` κατασκευαστή στην επιθυμητή μορφή.

### Ε2: Είναι το Aspose.Note συμβατό με όλες τις εκδόσεις των εγγράφων OneNote;

A2: Το Aspose.Note υποστηρίζει Microsoft OneNote 2010 και νεότερη έκδοση.

### Ε3: Απαιτεί το Aspose.Note άδεια χρήσης;

A3: Ναι, χρειάζεστε έγκυρη άδεια χρήσης για να χρησιμοποιήσετε το Aspose.Note σε περιβάλλοντα παραγωγής. Ωστόσο, μπορείτε να αποκτήσετε μια προσωρινή άδεια για σκοπούς δοκιμής.

### Ε4: Μπορώ να χειριστώ άλλες πτυχές του εγγράφου πριν το αποθηκεύσω ως εικόνα;

Α4: Απολύτως! Το Aspose.Note παρέχει ένα ευρύ φάσμα δυνατοτήτων για την επεξεργασία εγγράφων OneNote μέσω προγραμματισμού.

### Ε5: Πού μπορώ να βρω υποστήριξη εάν αντιμετωπίσω προβλήματα;

A5: Μπορείτε να βρείτε υποστήριξη στο φόρουμ Aspose.Note[εδώ](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
