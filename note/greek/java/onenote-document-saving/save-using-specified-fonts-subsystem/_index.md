---
date: 2025-12-18
description: Μάθετε πώς να **αποθηκεύσετε το OneNote ως PDF** χρησιμοποιώντας το υποσύστημα
  καθορισμένων γραμματοσειρών σε Java με το Aspose.Note. Αυτός ο οδηγός δείχνει επίσης
  πώς να μετατρέψετε το OneNote σε PDF, να φορτώσετε προσαρμοσμένα αρχεία γραμματοσειρών
  και να καθορίσετε προεπιλεγμένες γραμματοσειρές.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: Αποθήκευση του OneNote ως PDF με χρήση του υποσυστήματος καθορισμένων γραμματοσειρών
url: /el/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση OneNote ως PDF χρησιμοποιώντας το υποσύστημα καθορισμένων γραμματοσειρών

## Εισαγωγή

Σε πολλές επιχειρηματικές περιπτώσεις χρειάζεται να **αποθηκεύσετε το OneNote ως PDF** διατηρώντας την ακριβή εμφάνιση των αρχικών σελίδων. Το Aspose.Note for Java το καθιστά εύκολο, επιτρέποντάς σας να ελέγχετε το υποσύστημα γραμματοσειρών κατά τη μετατροπή. Σε αυτό το tutorial θα δούμε τρεις πρακτικούς τρόπους για **μετατροπή OneNote σε PDF**, καλύπτοντας πώς να **φορτώσετε προσαρμοσμένα αρχεία γραμματοσειρών**, **καθορίσετε προεπιλεγμένη γραμματοσειρά**, και ακόμη **χρησιμοποιήσετε ροή γραμματοσειράς** όταν η γραμματοσειρά δεν είναι διαθέσιμη στο μηχάνημα-στόχο.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “save OneNote as PDF”;** Μετατρέπει ένα αρχείο .one σε PDF διατηρώντας τη διάταξη και το στυλ αμετάβλητα.  
- **Ποιο API διαχειρίζεται τις γραμματοσειρές;** Το `DocumentFontsSubsystem` σας επιτρέπει να ορίσετε προεπιλεγμένη γραμματοσειρά ή να φορτώσετε προσαρμοσμένο αρχείο/ροή γραμματοσειράς.  
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Ναι, απαιτείται εμπορική άδεια Aspose.Note για χρήση εκτός δοκιμής.  
- **Μπορώ να μετατρέψω πολλά αρχεία σε batch;** Απόλυτα – απλώς κάντε βρόχο πάνω στη λογική φόρτωσης και αποθήκευσης του `Document`.  
- **Ποια έκδοση Java απαιτείται;** Java 15 ή νεότερη (το παράδειγμα χρησιμοποιεί JDK 15).

## Τι είναι η “save OneNote as PDF” με υποσύστημα γραμματοσειρών;

Η αποθήκευση OneNote ως PDF με υποσύστημα γραμματοσειρών σημαίνει ότι κατά τη διαδικασία μετατροπής το Aspose.Note αντικαθιστά τυχόν ελλιπείς χαρακτήρες με τη γραμματοσειρά που παρέχετε. Αυτό εγγυάται ότι το PDF φαίνεται ταυτόσημο σε οποιαδήποτε συσκευή, ακόμη και όταν η αρχική γραμματοσειρά δεν είναι εγκατεστημένη.

## Γιατί να ελέγχετε το υποσύστημα γραμματοσειρών όταν **μετατρέπετε OneNote σε PDF**;

- **Συνεπής branding** – τα εταιρικά έγγραφα διατηρούν την ακριβή γραμματοσειρά.  
- **Αξιοπιστία跨‑πλατφόρμας** – τα PDF αποδίδουν το ίδιο σε Windows, macOS, Linux και κινητές συσκευές.  
- **Μειωμένα σφάλματα** – τα προειδοποιητικά μηνύματα για ελλιπείς γραμματοσειρές εξαφανίζονται, παράγοντας καθαρό αποτέλεσμα.

## Προαπαιτούμενα

### 1. Java Development Kit (JDK)

Βεβαιωθείτε ότι έχετε εγκατεστημένο το Java Development Kit (JDK) στο σύστημά σας. Μπορείτε να το κατεβάσετε από [εδώ](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) αν δεν το έχετε ήδη.

### 2. Aspose.Note for Java Library

Κατεβάστε και ρυθμίστε τη βιβλιοθήκη Aspose.Note for Java. Μπορείτε να τη κατεβάσετε από την [ιστοσελίδα](https://releases.aspose.com/note/java/).

## Import Packages

Βεβαιωθείτε ότι έχετε εισάγει τα απαραίτητα πακέτα στο έργο Java σας:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Τώρα ας αναλύσουμε κάθε παράδειγμα σε πολλαπλά βήματα για καλύτερη κατανόηση της διαδικασίας.

## Πώς να **αποθηκεύσετε OneNote ως PDF** χρησιμοποιώντας το Document Fonts Subsystem με προεπιλεγμένη γραμματοσειρά

### Βήμα 1: Αποθήκευση με Document Fonts Subsystem και προεπιλεγμένο όνομα γραμματοσειράς

Αυτό το βήμα δείχνει πώς να **αποθηκεύσετε OneNote ως PDF** με απλό τρόπο, καθορίζοντας το προεπιλεγμένο όνομα γραμματοσειράς.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Σε αυτό το βήμα:
- Το έγγραφο OneNote φορτώνεται χρησιμοποιώντας το Aspose.Note.
- Η **προεπιλεγμένη γραμματοσειρά** ορίζεται ως **"Times New Roman"**.
- Το έγγραφο αποθηκεύεται σε μορφή PDF με τη επιλεγμένη γραμματοσειρά.

### Βήμα 2: Αποθήκευση με Document Fonts Subsystem και προεπιλεγμένη γραμματοσειρά από αρχείο

Εδώ **φορτώνουμε ένα προσαρμοσμένο αρχείο γραμματοσειράς** και το χρησιμοποιούμε ως εναλλακτική λύση κατά τη μετατροπή σε PDF.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Βασικά σημεία:
- Το **προσαρμοσμένο αρχείο γραμματοσειράς** `geo_1.ttf` **φορτώνεται από τον δίσκο**.
- Η μέθοδος `usingDefaultFontFromFile` **καθορίζει προεπιλεγμένη γραμματοσειρά από αρχείο**, διασφαλίζοντας ότι το PDF θα χρησιμοποιήσει αυτή τη γραμματοσειρά όταν η αρχική λείπει.
- Το παραγόμενο PDF διατηρεί την επιθυμητή εμφάνιση.

### Βήμα 3: Αποθήκευση με Document Fonts Subsystem και προεπιλεγμένη γραμματοσειρά από ροή

Μερικές φορές η γραμματοσειρά μπορεί να βρίσκεται σε βάση δεδομένων ή να λαμβάνεται μέσω δικτύου. Αυτό το παράδειγμα δείχνει πώς να **χρησιμοποιήσετε ροή γραμματοσειράς**.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Τι συμβαίνει εδώ:
- Το αρχείο γραμματοσειράς ανοίγεται ως **InputStream**, χρήσιμο όταν η γραμματοσειρά βρίσκεται σε μη‑αρχείο πηγή.
- Η μέθοδος `usingDefaultFontFromStream` **χρησιμοποιεί ροή γραμματοσειράς** για να ορίσει την εναλλακτική γραμματοσειρά.
- Το αρχείο OneNote αποθηκεύεται ως PDF με τη γραμματοσειρά που προέρχεται από τη ροή.

## Συνηθισμένα Προβλήματα και Λύσεις

| Πρόβλημα | Γιατί συμβαίνει | Πώς να διορθώσετε |
|----------|----------------|-------------------|
| **Missing font warnings** | Το αρχείο .one αναφέρει γραμματοσειρά που δεν υπάρχει στο μηχάνημα. | Παρέχετε προεπιλεγμένη γραμματοσειρά μέσω `usingDefaultFont`, `usingDefaultFontFromFile` ή `usingDefaultFontFromStream`. |
| **File not found for custom font** | Λανθασμένη διαδρομή προς το αρχείο `.ttf`. | Χρησιμοποιήστε απόλυτες διαδρομές ή επαληθεύστε τη σχετική διαδρομή από τον τρέχοντα φάκελο εργασίας. |
| **Stream not closed** | Εξαίρεση προκύπτει πριν κληθεί το `close()`. | Χρησιμοποιήστε try‑with‑resources (`try (InputStream stream = ...) { ... }`) για αυτόματο κλείσιμο. |

## Συχνές Ερωτήσεις

**Ε: Μπορώ να καθορίσω διαφορετικές γραμματοσειρές για διαφορετικά τμήματα του εγγράφου;**  
Α: Ναι, μπορείτε να εφαρμόσετε προσαρμοσμένες ρυθμίσεις γραμματοσειράς σε μεμονωμένα στοιχεία πλούσιου κειμένου χρησιμοποιώντας την κλάση `Font` στο Aspose.Note.

**Ε: Είναι το Aspose.Note συμβατό με όλες τις εκδόσεις του OneNote;**  
Α: Το Aspose.Note υποστηρίζει αρχεία OneNote από πρόσφατες εκδόσεις desktop και mobile, εξασφαλίζοντας ευρεία συμβατότητα.

**Ε: Πώς μπορώ να διαχειριστώ ελλιπείς γραμματοσειρές κατά την αποθήκευση εγγράφων;**  
Α: Χρησιμοποιήστε τις μεθόδους του υποσυστήματος γραμματοσειρών που παρουσιάστηκαν παραπάνω (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`) για να παρέχετε εναλλακτική λύση.

**Ε: Μπορώ να προσαρμόσω τις ιδιότητες της γραμματοσειράς όπως το μέγεθος και το στυλ;**  
Α: Απόλυτα – το API σας επιτρέπει να ορίσετε μέγεθος, στυλ, χρώμα και άλλες ιδιότητες ανά τμήμα (run).

**Ε: Υπάρχει διαθέσιμη δοκιμαστική έκδοση του Aspose.Note for Java;**  
Α: Ναι, μπορείτε να κατεβάσετε δωρεάν δοκιμαστική έκδοση από την ιστοσελίδα της Aspose.

## Συμπέρασμα

Σε αυτό το tutorial μάθαμε πώς να **αποθηκεύσουμε OneNote ως PDF** ελέγχοντας το υποσύστημα γραμματοσειρών σε Java με το Aspose.Note. Ακολουθώντας τις τρεις προσεγγίσεις—καθορισμός προεπιλεγμένου ονόματος γραμματοσειράς, φόρτωση προσαρμοσμένου αρχείου γραμματοσειράς ή χρήση ροής γραμματοσειράς—μπορείτε να εξασφαλίσετε συνεπή αναπαράσταση γραμματοσειρών σε όλες τις πλατφόρμες κατά την εξαγωγή ή αποθήκευση των εγγράφων OneNote.

---

**Τελευταία ενημέρωση:** 2025-12-18  
**Δοκιμασμένο με:** Aspose.Note for Java 24.11  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}