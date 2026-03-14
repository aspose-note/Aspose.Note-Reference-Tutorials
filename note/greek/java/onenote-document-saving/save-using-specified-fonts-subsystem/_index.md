---
date: 2026-03-14
description: Μάθετε πώς να **αποθηκεύσετε το OneNote ως PDF** χρησιμοποιώντας το υποσύστημα
  καθορισμένων γραμματοσειρών σε Java με το Aspose.Note. Αυτός ο οδηγός δείχνει επίσης
  πώς να μετατρέψετε το OneNote σε PDF, να φορτώσετε προσαρμοσμένα αρχεία γραμματοσειρών
  και να ορίσετε προεπιλεγμένες γραμματοσειρές.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: Αποθήκευση του OneNote ως PDF χρησιμοποιώντας το υποσύστημα καθορισμένων γραμματοσειρών
url: /el/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

.

**Author:** Aspose -> keep.

Then closing shortcodes.

Also include back the final shortcodes.

Make sure to keep all markdown formatting.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση OneNote ως PDF χρησιμοποιώντας το υποσύστημα καθορισμένων γραμματοσειρών

## Εισαγωγή

Σε πολλές επιχειρηματικές περιπτώσεις χρειάζεται να **αποθηκεύσετε το OneNote ως PDF** διατηρώντας την ακριβή εμφάνιση των αρχικών σελίδων. Το Aspose.Note for Java το κάνει απλό, επιτρέποντάς σας να ελέγχετε το υποσύστημα γραμματοσειρών κατά τη μετατροπή. Σε αυτό το tutorial θα περάσουμε από τρεις πρακτικούς τρόπους για **μετατροπή OneNote σε PDF**, καλύπτοντας πώς να **φορτώσετε προσαρμοσμένα αρχεία γραμματοσειρών**, **καθορίσετε προεπιλεγμένη γραμματοσειρά PDF**, και ακόμη **χρησιμοποιήσετε ροή γραμματοσειράς** όταν η γραμματοσειρά δεν είναι διαθέσιμη στο μηχάνημα-στόχο. Αυτές οι τεχνικές βοηθούν επίσης όταν χρειάζεται να **μετατρέψετε .one σε pdf** σε αυτοματοποιημένες διαδικασίες.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “save OneNote as PDF”;** Μετατρέπει ένα αρχείο .one σε PDF διατηρώντας τη διάταξη και το στυλ αμετάβλητα.  
- **Ποιο API διαχειρίζεται τις γραμματοσειρές;** `DocumentFontsSubsystem` σας επιτρέπει να ορίσετε προεπιλεγμένη γραμματοσειρά ή να φορτώσετε προσαρμοσμένο αρχείο/ροή γραμματοσειράς.  
- **Χρειάζομαι άδεια για παραγωγή;** Ναι, απαιτείται εμπορική άδεια Aspose.Note για χρήση εκτός δοκιμής.  
- **Μπορώ να μετατρέψω πολλαπλά αρχεία σε batch;** Απόλυτα – απλώς κάντε βρόχο πάνω στη λογική φόρτωσης και αποθήκευσης του `Document`.  
- **Ποια έκδοση Java απαιτείται;** Java 15 ή νεότερη (το παράδειγμα χρησιμοποιεί JDK 15).

## Τι είναι “save OneNote as PDF” με υποσύστημα γραμματοσειρών;

Η αποθήκευση OneNote ως PDF με υποσύστημα γραμματοσειρών σημαίνει ότι κατά τη διαδικασία μετατροπής το Aspose.Note αντικαθιστά τυχόν ελλιπείς γλύφους με τη γραμματοσειρά που παρέχετε. Αυτό εγγυάται ότι το PDF φαίνεται ταυτόσημο σε οποιαδήποτε συσκευή, ακόμη και όταν η αρχική γραμματοσειρά δεν είναι εγκατεστημένη.

## Γιατί να ελέγχετε το υποσύστημα γραμματοσειρών όταν **μετατρέπετε OneNote σε PDF**;

- **Συνεπής branding** – τα εταιρικά έγγραφα διατηρούν την ακριβή γραμματοσειρά.  
- **Αξιοπιστία跨‑πλατφόρμα** – τα PDF αποδίδουν το ίδιο σε Windows, macOS, Linux και κινητά.  
- **Μείωση σφαλμάτων** – οι προειδοποιήσεις για ελλιπείς γραμματοσειρές εξαφανίζονται, παράγοντας καθαρό αποτέλεσμα.  
- **Καθορισμός προεπιλεγμένης γραμματοσειράς PDF** – εσείς αποφασίζετε ποια fallback γραμματοσειρά θα χρησιμοποιήσει ο μετατροπέας, αποφεύγοντας εκπλήξεις.

## Συνηθισμένες περιπτώσεις χρήσης

| Σενάριο | Γιατί θα χρησιμοποιούσατε το υποσύστημα γραμματοσειρών |
|----------|-----------------------------------|
| Αυτοματοποιημένη δημιουργία αναφορών | Εγγυάται την ίδια εμφάνιση σε όλους τους διακομιστές χωρίς εγκατάσταση γραμματοσειρών. |
| Αρχεία OneNote παλαιού τύπου | Επιτρέπει τη μετατροπή παλιών αρχείων που αναφέρονται σε γραμματοσειρές που δεν είναι πλέον διαθέσιμες. |
| Πλατφόρμα SaaS πολλαπλών ενοικιαστών | Κάθε ενοικιαστής μπορεί να παρέχει τη δική του γραμματοσειρά μάρκας μέσω ροής ή αρχείου. |

## Προαπαιτούμενα

### 1. Java Development Kit (JDK)

Βεβαιωθείτε ότι έχετε εγκατεστημένο το Java Development Kit (JDK) στο σύστημά σας. Μπορείτε να το κατεβάσετε από [εδώ](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) αν δεν το έχετε ήδη.

### 2. Aspose.Note for Java Library

Κατεβάστε και ρυθμίστε τη βιβλιοθήκη Aspose.Note for Java. Μπορείτε να την κατεβάσετε από το [website](https://releases.aspose.com/note/java/).

## Εισαγωγή Πακέτων

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

Τώρα ας αναλύσουμε κάθε παράδειγμα σε πολλαπλά βήματα για να κατανοήσουμε καλύτερα τη διαδικασία.

## Πώς να **αποθηκεύσετε OneNote ως PDF** χρησιμοποιώντας το Document Fonts Subsystem με προεπιλεγμένη γραμματοσειρά

### Βήμα 1: Αποθήκευση χρησιμοποιώντας Document Fonts Subsystem με όνομα προεπιλεγμένης γραμματοσειράς

Αυτό το βήμα δείχνει πώς να **αποθηκεύσετε OneNote ως PDF** με απλό τρόπο, καθορίζοντας το όνομα της προεπιλεγμένης γραμματοσειράς.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the .one document into Aspose.Note.
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
- Η **προεπιλεγμένη γραμματοσειρά PDF** ορίζεται ως **"Times New Roman"**.
- Το έγγραφο αποθηκεύεται σε μορφή PDF με την επιλεγμένη γραμματοσειρά.

### Βήμα 2: Αποθήκευση χρησιμοποιώντας Document Fonts Subsystem με προεπιλεγμένη γραμματοσειρά από αρχείο

Εδώ **φορτώνουμε ένα προσαρμοσμένο αρχείο γραμματοσειράς** και το χρησιμοποιούμε ως fallback κατά τη μετατροπή σε PDF. Αυτό δείχνει το σενάριο **load custom font java**.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the .one document into Aspose.Note.
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

Κύρια σημεία:
- Το **αρχείο προσαρμοσμένης γραμματοσειράς** `geo_1.ttf` **φορτώνεται από το δίσκο**.
- `usingDefaultFontFromFile` **καθορίζει την προεπιλεγμένη γραμματοσειρά από αρχείο**, εξασφαλίζοντας ότι το PDF χρησιμοποιεί αυτή τη γραμματοσειρά όταν η αρχική λείπει.
- Το παραγόμενο PDF διατηρεί την επιθυμητή εμφάνιση.

### Βήμα 3: Αποθήκευση χρησιμοποιώντας Document Fonts Subsystem με προεπιλεγμένη γραμματοσειρά από ροή

Μερικές φορές η γραμματοσειρά μπορεί να αποθηκευτεί σε βάση δεδομένων ή να ληφθεί μέσω δικτύου. Αυτό το παράδειγμα δείχνει πώς να **χρησιμοποιήσετε ροή γραμματοσειράς**—μια κοινή τεχνική **load custom font java**.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the .one document into Aspose.Note.
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
- `usingDefaultFontFromStream` **χρησιμοποιεί ροή γραμματοσειράς** για να ορίσει τη γραμματοσειρά εφεδρείας.
- Το αρχείο OneNote αποθηκεύεται ως PDF με τη γραμματοσειρά που προέρχεται από τη ροή.

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Γιατί συμβαίνει | Πώς να διορθώσετε |
|----------|----------------|-------------------|
| **Προειδοποιήσεις για ελλιπείς γραμματοσειρές** | Το αρχείο .one αναφέρει μια γραμματοσειρά που δεν υπάρχει στη μηχανή. | Παρέχετε μια προεπιλεγμένη γραμματοσειρά μέσω `usingDefaultFont`, `usingDefaultFontFromFile` ή `usingDefaultFontFromStream`. |
| **Δεν βρέθηκε το αρχείο προσαρμοσμένης γραμματοσειράς** | Λανθασμένη διαδρομή προς το αρχείο `.ttf`. | Χρησιμοποιήστε απόλυτες διαδρομές ή επαληθεύστε τη σχετική διαδρομή από τον τρέχοντα φάκελο. |
| **Η ροή δεν κλείνει** | Εξαίρεση συμβαίνει πριν κληθεί η `close()`. | Χρησιμοποιήστε try‑with‑resources (`try (InputStream stream = ...) { ... }`) για αυτόματο κλείσιμο. |

## Συχνές Ερωτήσεις

**Ε: Μπορώ να ορίσω διαφορετικές γραμματοσειρές για διαφορετικά τμήματα του εγγράφου;**  
Α: Ναι, μπορείτε να εφαρμόσετε προσαρμοσμένες ρυθμίσεις γραμματοσειράς σε μεμονωμένα στοιχεία πλούσιου κειμένου χρησιμοποιώντας την κλάση `Font` στο Aspose.Note.

**Ε: Είναι το Aspose.Note συμβατό με όλες τις εκδόσεις του OneNote;**  
Α: Το Aspose.Note υποστηρίζει αρχεία OneNote από πρόσφατες εκδόσεις επιφάνειας εργασίας και κινητών, εξασφαλίζοντας ευρεία συμβατότητα.

**Ε: Πώς μπορώ να διαχειριστώ τις ελλιπείς γραμματοσειρές κατά την αποθήκευση εγγράφων;**  
Α: Χρησιμοποιήστε τις μεθόδους του υποσυστήματος γραμματοσειρών που εμφανίστηκαν παραπάνω (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`) για να παρέχετε εναλλακτική.

**Ε: Μπορώ να προσαρμόσω τις ιδιότητες της γραμματοσειράς όπως το μέγεθος και το στυλ;**  
Α: Απόλυτα – το API σας επιτρέπει να ορίσετε μέγεθος, στυλ, χρώμα και άλλες ιδιότητες ανά τμήμα.

**Ε: Υπάρχει δοκιμαστική έκδοση του Aspose.Note for Java;**  
Α: Ναι, μια δωρεάν δοκιμαστική έκδοση μπορεί να ληφθεί από την ιστοσελίδα της Aspose.

## Συμπέρασμα

Σε αυτό το tutorial μάθαμε πώς να **αποθηκεύσουμε OneNote ως PDF** ελέγχοντας το υποσύστημα γραμματοσειρών σε Java με το Aspose.Note. Ακολουθώντας τις τρεις προσεγγίσεις—καθορισμός ονόματος προεπιλεγμένης γραμματοσειράς, φόρτωση προσαρμοσμένου αρχείου γραμματοσειράς ή χρήση ροής γραμματοσειράς—μπορείτε να εγγυηθείτε συνεπή αναπαράσταση γραμματοσειρών σε όλες τις πλατφόρμες όταν **convert .one to pdf** ή σε οποιοδήποτε άλλο σενάριο μετατροπής OneNote.

---

**Last Updated:** 2026-03-14  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}