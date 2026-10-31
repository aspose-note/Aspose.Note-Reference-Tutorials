---
date: 2026-10-31
description: Μάθετε πώς να αποθηκεύσετε το OneNote ως PDF χρησιμοποιώντας το προεπιλεγμένο
  υποσύστημα γραμματοσειρών PDF σε Java με το Aspose.Note. Περιλαμβάνει τη μετατροπή
  .one σε pdf, τη φόρτωση προσαρμοσμένων γραμματοσειρών και τον καθορισμό προεπιλεγμένων
  γραμματοσειρών.
keywords:
- default pdf font
- convert .one to pdf
- how to convert onenote
- save onenote pdf
- convert onenote files pdf
lastmod: 2026-10-31
linktitle: Χρησιμοποιήστε το Aspose.Note για Java για να αποθηκεύσετε το OneNote ως
  PDF με το καθορισμένο υποσύστημα γραμματοσειρών
og_description: Μάθετε πώς να αποθηκεύσετε το OneNote ως PDF με το προεπιλεγμένο υποσύστημα
  γραμματοσειρών PDF σε Java χρησιμοποιώντας το Aspose.Note. Περιλαμβάνει τη μετατροπή
  .one σε pdf και τη φόρτωση προσαρμοσμένων γραμματοσειρών.
og_image_alt: Guide showing Java code to save OneNote as PDF with custom fonts
og_title: Προεπιλεγμένη γραμματοσειρά PDF – αποθήκευση του OneNote ως PDF χρησιμοποιώντας
  Java
schemas:
- author: Aspose
  dateModified: '2026-10-31'
  description: Learn how to save OneNote as PDF using the default PDF font subsystem
    in Java with Aspose.Note. Includes converting .one to pdf, loading custom fonts,
    and specifying default fonts.
  headline: Default PDF font – save OneNote as PDF using specified fonts subsystem
  type: TechArticle
- description: Learn how to save OneNote as PDF using the default PDF font subsystem
    in Java with Aspose.Note. Includes converting .one to pdf, loading custom fonts,
    and specifying default fonts.
  name: Default PDF font – save OneNote as PDF using specified fonts subsystem
  steps:
  - name: save using document fonts subsystem with default font name
    text: 'The `DocumentFontsSubsystem` class is Aspose.Note’s entry point for controlling
      font fallback during PDF export. In this step we specify a default font name.
      In this step: - The OneNote document is loaded using Aspose.Note. - The **default
      PDF font** is specified as **"Times New Roman"**. - The docu'
  - name: save using document fonts subsystem with default font from file
    text: '`usingDefaultFontFromFile` sets a custom font file as the default fallback
      font. This demonstrates the **load custom font java** scenario. Key points:
      - The **custom font file** `geo_1.ttf` is **loaded from disk**. - `usingDefaultFontFromFile`
      **specifies default font from file**, ensuring the PDF u'
  - name: save using document fonts subsystem with default font from stream
    text: '`usingDefaultFontFromStream` sets a custom font stream as the default fallback
      font. This example shows how to **use a font stream**—a common **load custom
      font java** technique. What happens here: - The font file is opened as an **InputStream**,
      which is useful when the font resides in a non‑file s'
  type: HowTo
- questions:
  - answer: Yes, you can apply custom font settings to individual rich‑text elements
      using the `Font` class in Aspose.Note.
    question: Can I specify different fonts for different parts of the document?
  - answer: Aspose.Note supports OneNote files from recent desktop and mobile versions,
      ensuring broad compatibility.
    question: Is Aspose.Note compatible with all versions of OneNote?
  - answer: Use the fonts subsystem methods shown above (`usingDefaultFont`, `usingDefaultFontFromFile`,
      `usingDefaultFontFromStream`) to provide a fallback.
    question: How can I handle missing fonts when saving documents?
  - answer: Absolutely – the API lets you set size, style, color, and other attributes
      on a per‑run basis.
    question: Can I customize the font properties such as size and style?
  - answer: Yes, a free trial can be downloaded from the Aspose website.
    question: Is there a trial version available for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- default pdf font
- Aspose.Note
- Java document processing
title: Προεπιλεγμένη γραμματοσειρά PDF – αποθήκευση του OneNote ως PDF χρησιμοποιώντας
  το καθορισμένο υποσύστημα γραμματοσειρών
url: /el/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση OneNote ως PDF χρησιμοποιώντας το προεπιλεγμένο σύστημα γραμματοσειρών PDF

## Εισαγωγή

Σε πολλές επιχειρηματικές περιπτώσεις χρειάζεται να **αποθηκεύσετε το OneNote ως PDF** διατηρώντας την ακριβή εμφάνιση των αρχικών σελίδων. Το Aspose.Note for Java το καθιστά απλό, επιτρέποντάς σας να ελέγχετε το σύστημα γραμματοσειρών κατά τη μετατροπή. Σε αυτό το tutorial θα εξετάσουμε τρεις πρακτικούς τρόπους για **μετατροπή OneNote σε PDF**, καλύπτοντας πώς να **φορτώσετε προσαρμοσμένα αρχεία γραμματοσειρών**, **καθορίσετε μια προεπιλεγμένη γραμματοσειρά PDF**, και ακόμη **χρησιμοποιήσετε ροή γραμματοσειράς** όταν η γραμματοσειρά δεν είναι διαθέσιμη στο στόχο. Αυτές οι τεχνικές βοηθούν επίσης όταν χρειάζεται να **μετατρέψετε .one σε pdf** σε αυτοματοποιημένες αλυσίδες.

## Σύντομες απαντήσεις
- **Τι σημαίνει “αποθήκευση OneNote ως PDF”;** Μετατρέπει ένα αρχείο .one σε PDF διατηρώντας τη διάταξη και το στυλ αμετάβλητα.  
- **Ποιο API διαχειρίζεται τις γραμματοσειρές;** Το `DocumentFontsSubsystem` σας επιτρέπει να ορίσετε μια προεπιλεγμένη γραμματοσειρά ή να φορτώσετε προσαρμοσμένο αρχείο/ροή γραμματοσειράς.  
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Ναι, απαιτείται εμπορική άδεια Aspose.Note για χρήση εκτός δοκιμής.  
- **Μπορώ να μετατρέψω πολλαπλά αρχεία σε batch;** Απόλυτα – απλώς κάντε βρόχο πάνω στη λογική φόρτωσης και αποθήκευσης του `Document`.  
- **Ποια έκδοση Java απαιτείται;** Java 8 ή νεότερη (το παράδειγμα χρησιμοποιεί JDK 8).  

Η κλάση **DocumentFontsSubsystem** ελέγχει την εναλλακτική γραμματοσειρά κατά την εξαγωγή σε PDF.

## Τι είναι η “αποθήκευση OneNote ως PDF” με σύστημα γραμματοσειρών;

Η αποθήκευση OneNote ως PDF με σύστημα γραμματοσειρών σημαίνει ότι κατά τη διαδικασία μετατροπής το Aspose.Note αντικαθιστά τυχόν ελλιπείς γλύφους με τη γραμματοσειρά που παρέχετε. Αυτό εγγυάται ότι το PDF φαίνεται ταυτόσημο σε οποιαδήποτε συσκευή, ακόμη και όταν η αρχική γραμματοσειρά δεν είναι εγκατεστημένη.

## Γιατί να ελέγχετε το σύστημα γραμματοσειρών όταν μετατρέπετε το OneNote σε PDF;

Ο έλεγχος του συστήματος γραμματοσειρών εξασφαλίζει συνεπή branding, αξιοπιστία μεταξύ πλατφορμών και εξαλείφει τις προειδοποιήσεις για ελλιπείς γραμματοσειρές. Καθορίζοντας μια **προεπιλεγμένη γραμματοσειρά PDF** αποφασίζετε ποια εναλλακτική γραμματοσειρά θα χρησιμοποιήσει ο μετατροπέας, αποφεύγοντας εκπλήξεις και παράγοντας καθαρό αποτέλεσμα κάθε φορά. Αυτό βοηθά επίσης στη διατήρηση οπτικής πιστότητας μεταξύ διαφορετικών λειτουργικών συστημάτων και μειώνει την ανάγκη εγκατάστασης πολλών γραμματοσειρών σε κάθε διακομιστή των αυτοματοποιημένων αλυσίδων.

## Κοινές περιπτώσεις χρήσης

| Σενάριο | Γιατί να χρησιμοποιήσετε το σύστημα γραμματοσειρών |
|----------|-----------------------------------|
| Αυτόματη δημιουργία αναφορών | Εγγυάται την ίδια εμφάνιση σε όλους τους διακομιστές χωρίς εγκατάσταση γραμματοσειρών. |
| Αρχεία OneNote παλαιού τύπου | Επιτρέπει τη μετατροπή παλαιών αρχείων που αναφέρονται σε γραμματοσειρές που δεν είναι πλέον διαθέσιμες. |
| Πλατφόρμα SaaS πολλαπλών ενοικιαστών | Κάθε ενοικιαστής μπορεί να παρέχει τη δική του γραμματοσειρά brand μέσω ροής ή αρχείου. |

## Προαπαιτούμενα

### 1. Java Development Kit (JDK)

Βεβαιωθείτε ότι έχετε εγκατεστημένο το Java Development Kit (JDK) στο σύστημά σας. Μπορείτε να το κατεβάσετε από τη [Oracle Java downloads page](https://www.oracle.com/java/technologies/downloads/) αν δεν το έχετε ήδη.

### 2. Aspose.Note for Java library

Κατεβάστε και ρυθμίστε τη βιβλιοθήκη Aspose.Note for Java. Μπορείτε να τη κατεβάσετε από τη **Aspose.Note for Java release page**(https://releases.aspose.com/note/java/).

## Εισαγωγή πακέτων

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

## Πώς να αποθηκεύσετε το OneNote ως PDF χρησιμοποιώντας το σύστημα γραμματοσειρών του Document με προεπιλεγμένη γραμματοσειρά;

Η μέθοδος `Document.load` φορτώνει ένα αρχείο .one σε αντικείμενο Document. Η **DocumentFontsSubsystem** διαχειρίζεται την αντικατάσταση γραμματοσειρών κατά τη μετατροπή. Φορτώστε το αρχείο OneNote με `Document.load("sample.one")`, ορίστε τη προεπιλεγμένη γραμματοσειρά PDF σε **Times New Roman**, και καλέστε `save` – αυτή είναι η πλήρης μετατροπή σε δύο γραμμές. Η χρήση προεπιλεγμένης γραμματοσειράς PDF εγγυάται ότι τυχόν ελλιπείς γλύφοι θα αποδοθούν με τη συγκεκριμένη γραμματοσειρά, έτσι το παραγόμενο PDF ταιριάζει με το αρχικό σχέδιο σε κάθε πλατφόρμα.

### Βήμα 1: αποθήκευση χρησιμοποιώντας το σύστημα γραμματοσειρών του εγγράφου με προεπιλεγμένο όνομα γραμματοσειράς

Η κλάση `DocumentFontsSubsystem` είναι το σημείο εισόδου του Aspose.Note για τον έλεγχο της εναλλακτικής γραμματοσειράς κατά την εξαγωγή σε PDF. Σε αυτό το βήμα καθορίζουμε ένα προεπιλεγμένο όνομα γραμματοσειράς.

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
- Το έγγραφο αποθηκεύεται σε μορφή PDF με τη επιλεγμένη γραμματοσειρά.

### Βήμα 2: αποθήκευση χρησιμοποιώντας το σύστημα γραμματοσειρών του εγγράφου με προεπιλεγμένη γραμματοσειρά από αρχείο

Η μέθοδος `usingDefaultFontFromFile` ορίζει ένα προσαρμοσμένο αρχείο γραμματοσειράς ως προεπιλεγμένη εναλλακτική γραμματοσειρά. Αυτό δείχνει το σενάριο **φόρτωσης προσαρμοσμένης γραμματοσειράς java**.

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

Βασικά σημεία:
- Το **προσαρμοσμένο αρχείο γραμματοσειράς** `geo_1.ttf` **φορτώνεται από το δίσκο**.
- Η `usingDefaultFontFromFile` **καθορίζει προεπιλεγμένη γραμματοσειρά από αρχείο**, διασφαλίζοντας ότι το PDF χρησιμοποιεί αυτή τη γραμματοσειρά όταν η αρχική λείπει.
- Το παραγόμενο PDF διατηρεί την προγραμματισμένη εμφάνιση.

### Βήμα 3: αποθήκευση χρησιμοποιώντας το σύστημα γραμματοσειρών του εγγράφου με προεπιλεγμένη γραμματοσειρά από ροή

Η μέθοδος `usingDefaultFontFromStream` ορίζει μια προσαρμοσμένη ροή γραμματοσειράς ως προεπιλεγμένη εναλλακτική γραμματοσειρά. Αυτό το παράδειγμα δείχνει πώς να **χρησιμοποιήσετε ροή γραμματοσειράς**—μια κοινή τεχνική **φόρτωσης προσαρμοσμένης γραμματοσειράς java**.

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
- Η `usingDefaultFontFromStream` **χρησιμοποιεί ροή γραμματοσειράς** για να ορίσει τη γραμματοσειρά εναλλακτικής χρήσης.
- Το αρχείο OneNote αποθηκεύεται ως PDF με τη γραμματοσειρά που προέρχεται από τη ροή.

## Συνηθισμένα προβλήματα και λύσεις

| Πρόβλημα | Γιατί συμβαίνει | Πώς να το διορθώσετε |
|----------|----------------|----------------------|
| **Προειδοποιήσεις ελλιπών γραμματοσειρών** | Το αρχείο .one αναφέρει μια γραμματοσειρά που δεν υπάρχει στη μηχανή. | Παρέχετε προεπιλεγμένη γραμματοσειρά μέσω `usingDefaultFont`, `usingDefaultFontFromFile` ή `usingDefaultFontFromStream`. |
| **Αρχείο γραμματοσειράς δεν βρέθηκε** | Λανθασμένη διαδρομή προς το αρχείο `.ttf`. | Χρησιμοποιήστε απόλυτες διαδρομές ή επαληθεύστε τη σχετική διαδρομή από τον τρέχοντα φάκελο εργασίας. |
| **Ροή δεν κλείνει** | Εξαίρεση προκύπτει πριν κληθεί το `close()`. | Χρησιμοποιήστε try‑with‑resources (`try (InputStream stream = ...) { ... }`) για αυτόματο κλείσιμο. |

## Συχνές ερωτήσεις

**Ε: Μπορώ να ορίσω διαφορετικές γραμματοσειρές για διαφορετικά τμήματα του εγγράφου;**  
Α: Ναι, μπορείτε να εφαρμόσετε προσαρμοσμένες ρυθμίσεις γραμματοσειράς σε μεμονωμένα στοιχεία πλούσιου κειμένου χρησιμοποιώντας την κλάση `Font` στο Aspose.Note.

**Ε: Είναι το Aspose.Note συμβατό με όλες τις εκδόσεις του OneNote;**  
Α: Το Aspose.Note υποστηρίζει αρχεία OneNote από πρόσφατες εκδόσεις επιφάνειας εργασίας και κινητών, εξασφαλίζοντας ευρεία συμβατότητα.

**Ε: Πώς μπορώ να διαχειριστώ ελλιπείς γραμματοσειρές κατά την αποθήκευση εγγράφων;**  
Α: Χρησιμοποιήστε τις μεθόδους του συστήματος γραμματοσειρών που παρουσιάστηκαν παραπάνω (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`) για να παρέχετε εναλλακτική γραμματοσειρά.

**Ε: Μπορώ να προσαρμόσω ιδιότητες γραμματοσειράς όπως μέγεθος και στυλ;**  
Α: Απόλυτα – το API σας επιτρέπει να ορίσετε μέγεθος, στυλ, χρώμα και άλλες ιδιότητες ανά τμήμα κειμένου.

**Ε: Υπάρχει διαθέσιμη δοκιμαστική έκδοση του Aspose.Note for Java;**  
Α: Ναι, μπορείτε να κατεβάσετε δωρεάν δοκιμαστική έκδοση από την ιστοσελίδα του Aspose.

## Συμπέρασμα

Σε αυτό το tutorial μάθαμε πώς να **αποθηκεύσουμε το OneNote ως PDF** ελέγχοντας το σύστημα γραμματοσειρών σε Java με το Aspose.Note. Ακολουθώντας τις τρεις προσεγγίσεις—καθορισμός προεπιλεγμένου ονόματος γραμματοσειράς, φόρτωση προσαρμοσμένου αρχείου γραμματοσειράς ή χρήση ροής γραμματοσειράς—μπορείτε να εγγυηθείτε συνεπή αναπαράσταση γραμματοσειρών μεταξύ πλατφορμών όταν **μετατρέπετε .one σε pdf** ή σε οποιοδήποτε άλλο σενάριο μετατροπής OneNote.

---

**Τελευταία ενημέρωση:** 2026-10-31  
**Δοκιμασμένο με:** Aspose.Note for Java 26.4  
**Συγγραφέας:** Aspose

## Σχετικά Tutorials

- [Convert OneNote to PDF Using Page Settings with Aspose.Note for Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)
- [Save Specific Pages PDF in OneNote – Aspose.Note](/note/java/onenote-document-saving/specify-save-options/)
- [default font size onenote – Set Default Paragraph Style in OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}