---
title: Αποθήκευση με χρήση του υποσυστήματος καθορισμένων γραμματοσειρών στο OneNote
linktitle: Αποθήκευση με χρήση του υποσυστήματος καθορισμένων γραμματοσειρών στο OneNote
second_title: Aspose.Note Java API
description: Μάθετε πώς να αποθηκεύετε έγγραφα του OneNote χρησιμοποιώντας καθορισμένο υποσύστημα γραμματοσειρών σε Java με το Aspose.Note. Εξασφαλίστε συνεπή αναπαράσταση γραμματοσειρών σε όλες τις πλατφόρμες χωρίς κόπο.
weight: 22
url: /el/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση με χρήση του υποσυστήματος καθορισμένων γραμματοσειρών στο OneNote

## Εισαγωγή

Το Aspose.Note για Java παρέχει ισχυρές δυνατότητες για εργασία με έγγραφα OneNote. Μια κοινή απαίτηση όταν εργάζεστε με τέτοια έγγραφα είναι να διασφαλίζετε ότι οι γραμματοσειρές διατηρούνται σωστά, ειδικά εάν το έγγραφο πρόκειται να εξαχθεί ή να αποθηκευτεί σε διαφορετικές μορφές όπως το PDF. Αυτό το σεμινάριο θα σας καθοδηγήσει στη διαδικασία αποθήκευσης εγγράφων του OneNote καθορίζοντας παράλληλα το υποσύστημα γραμματοσειρών, διασφαλίζοντας συνεπή και ακριβή αναπαράσταση του κειμένου σε διάφορες πλατφόρμες.

## Προαπαιτούμενα

Πριν ξεκινήσουμε το σεμινάριο, βεβαιωθείτε ότι έχετε ρυθμίσει τις ακόλουθες προϋποθέσεις:

### 1. Java Development Kit (JDK)

 Βεβαιωθείτε ότι έχετε εγκατεστημένο το Java Development Kit (JDK) στο σύστημά σας. Μπορείτε να το κατεβάσετε από[εδώ](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) αν δεν το έχεις κάνει ήδη.

### 2. Aspose.Note για Java Library

 Πραγματοποιήστε λήψη και ρύθμιση της βιβλιοθήκης Aspose.Note για Java. Μπορείτε να το κατεβάσετε από το[δικτυακός τόπος](https://releases.aspose.com/note/java/).

## Εισαγωγή πακέτων

Φροντίστε να εισαγάγετε τα απαραίτητα πακέτα στο έργο σας Java:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Τώρα ας αναλύσουμε κάθε παράδειγμα σε πολλά βήματα για να κατανοήσουμε καλύτερα τη διαδικασία.

## Βήμα 1: Αποθήκευση χρησιμοποιώντας το υποσύστημα γραμματοσειρών εγγράφων με το προεπιλεγμένο όνομα γραμματοσειράς

Αυτό το βήμα δείχνει πώς να αποθηκεύσετε ένα έγγραφο σε μορφή PDF χρησιμοποιώντας ένα καθορισμένο προεπιλεγμένο όνομα γραμματοσειράς.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Φορτώστε το έγγραφο στο Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Καθορίστε την προεπιλεγμένη γραμματοσειρά.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Αποθηκεύστε το έγγραφο ως PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Σε αυτό το βήμα:
- Το έγγραφο OneNote φορτώνεται χρησιμοποιώντας το Aspose.Note.
- Η προεπιλεγμένη γραμματοσειρά ορίζεται ως "Times New Roman".
- Το έγγραφο αποθηκεύεται σε μορφή PDF με την καθορισμένη γραμματοσειρά.

## Βήμα 2: Αποθήκευση χρησιμοποιώντας το υποσύστημα γραμματοσειρών εγγράφων με προεπιλεγμένη γραμματοσειρά από το αρχείο

Αυτό το βήμα δείχνει πώς να αποθηκεύσετε ένα έγγραφο σε μορφή PDF χρησιμοποιώντας μια προεπιλεγμένη γραμματοσειρά που έχει φορτωθεί από ένα αρχείο.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Φορτώστε το έγγραφο στο Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Καθορίστε τη διαδρομή προς το αρχείο γραμματοσειράς.
    String fontFile = "geo_1.ttf";

    // Καθορίστε την προεπιλεγμένη γραμματοσειρά από το αρχείο.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Αποθηκεύστε το έγγραφο ως PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Σε αυτό το βήμα:
- Το αρχείο γραμματοσειράς "geo_1.ttf" έχει φορτωθεί.
- Η προεπιλεγμένη γραμματοσειρά καθορίζεται από το φορτωμένο αρχείο γραμματοσειράς.
- Το έγγραφο αποθηκεύεται σε μορφή PDF με την καθορισμένη γραμματοσειρά.

## Βήμα 3: Αποθήκευση χρησιμοποιώντας το υποσύστημα γραμματοσειρών εγγράφων με προεπιλεγμένη γραμματοσειρά από τη ροή

Αυτό το βήμα δείχνει πώς να αποθηκεύσετε ένα έγγραφο σε μορφή PDF χρησιμοποιώντας μια προεπιλεγμένη γραμματοσειρά που έχει φορτωθεί από μια ροή.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Φορτώστε το έγγραφο στο Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Καθορίστε τη διαδρομή προς το αρχείο γραμματοσειράς.
    String fontFile = "geo_1.ttf";

    // Φορτώστε το αρχείο γραμματοσειράς ως ροή.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Καθορίστε την προεπιλεγμένη γραμματοσειρά από τη ροή.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Αποθηκεύστε το έγγραφο ως PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Σε αυτό το βήμα:
- Το αρχείο γραμματοσειράς "geo_1.ttf" φορτώνεται ως ροή.
- Η προεπιλεγμένη γραμματοσειρά καθορίζεται από τη φορτωμένη ροή.
- Το έγγραφο αποθηκεύεται σε μορφή PDF με την καθορισμένη γραμματοσειρά.

## συμπέρασμα

Σε αυτό το σεμινάριο, μάθαμε πώς να αποθηκεύουμε έγγραφα του OneNote χρησιμοποιώντας καθορισμένο υποσύστημα γραμματοσειρών σε Java χρησιμοποιώντας το Aspose.Note. Ακολουθώντας αυτά τα βήματα, μπορείτε να εξασφαλίσετε συνεπή αναπαράσταση γραμματοσειρών σε διάφορες πλατφόρμες κατά την εξαγωγή ή την αποθήκευση των εγγράφων σας.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να καθορίσω διαφορετικές γραμματοσειρές για διαφορετικά μέρη του εγγράφου;

A1: Ναι, μπορείτε να καθορίσετε διαφορετικές γραμματοσειρές για διαφορετικά μέρη του εγγράφου χρησιμοποιώντας το Aspose.Note για Java.

### Ε2: Είναι το Aspose.Note συμβατό με όλες τις εκδόσεις του OneNote;

A2: Το Aspose.Note υποστηρίζει διάφορες εκδόσεις του OneNote, διασφαλίζοντας τη συμβατότητα σε διαφορετικά περιβάλλοντα.

### Ε3: Πώς μπορώ να χειριστώ τις γραμματοσειρές που λείπουν κατά την αποθήκευση εγγράφων;

A3: Το Aspose.Note παρέχει επιλογές για τον καθορισμό προεπιλεγμένων γραμματοσειρών για τον αποτελεσματικό χειρισμό γραμματοσειρών που λείπουν κατά την αποθήκευση εγγράφων.

### Ε4: Μπορώ να προσαρμόσω τις ιδιότητες της γραμματοσειράς, όπως το μέγεθος και το στυλ;

A4: Ναι, μπορείτε να προσαρμόσετε τις ιδιότητες γραμματοσειράς όπως το μέγεθος, το στυλ και το χρώμα χρησιμοποιώντας το Aspose.Note για Java.

### Ε5: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Note για Java;

A5: Ναι, μπορείτε να λάβετε μια δωρεάν δοκιμή του Aspose.Note για Java από τον ιστότοπο.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
