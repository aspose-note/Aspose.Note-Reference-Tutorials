---
date: 2026-02-10
description: Μάθετε πώς να μετατρέπετε το OneNote σε κείμενο και να εξάγετε εικόνες
  με το Aspose.Note για Java. Ο οδηγός δείχνει πώς να διαβάζετε αρχεία .one σε Java
  και να εκτελείτε εξαγωγή κειμένου από το OneNote.
linktitle: Convert OneNote to Text and Extract Images using Document Visitor - Java
second_title: Aspose.Note Java API
title: Μετατροπή OneNote σε κείμενο και εξαγωγή εικόνων με το Document Visitor - Java
url: /el/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή OneNote σε Κείμενο και Εξαγωγή Εικόνων χρησιμοποιώντας Document Visitor - Java

## Εισαγωγή

Το Aspose.Note for Java καθιστά εύκολη τη **μετατροπή OneNote σε κείμενο** ενώ επίσης **εξάγει εικόνες από τα σημειωματάρια OneNote**. Σε αυτόν τον οδηγό θα σας καθοδηγήσουμε μέσα από ένα πλήρες, πρακτικό παράδειγμα που δείχνει πώς να φορτώσετε ένα αρχείο OneNote, να διασχίσετε τη δομή του με ένα προσαρμοσμένο `DocumentVisitor` και να εξάγετε τόσο εικόνες όσο και απλό κείμενο. Στο τέλος θα γνωρίζετε επίσης πώς να **διαβάσετε .one file java** έργα και γιατί αυτή η προσέγγιση είναι ιδανική για αυτοματοποιημένη μεταφορά περιεχομένου ή αναφορές.

## Γρήγορες Απαντήσεις
- **What library do I need?** Aspose.Note for Java (download link below).  
- **Can I extract images only?** Yes – implement the `VisitImageStart` method in a `DocumentVisitor`.  
- **How do I read a .one file in Java?** Use `new Document(path, new LoadOptions())`.  
- **Do I need a license for production?** A commercial license is required for non‑trial use.  
- **What Java version is supported?** JDK 8 or higher.

## Τι είναι η μετατροπή OneNote σε κείμενο;

Η μετατροπή OneNote σε κείμενο σημαίνει την εξαγωγή του ακατέργαστου κειμενικού περιεχομένου από ένα σημειωματάριο `.one` και την αποθήκευσή του ως απλό Unicode κείμενο. Αυτό είναι χρήσιμο όταν χρειάζεστε αρχεία αναζήτησης, ελαφριές ροές δεδομένων ή απλές περιλήψεις χωρίς τη μορφοποίηση του OneNote.

## Γιατί να χρησιμοποιήσετε το Document Visitor του Aspose.Note για εξαγωγή κειμένου από OneNote;

- **Fine‑grained control:** Το πρότυπο visitor σας επιτρέπει να αποφασίσετε ακριβώς ποιοι κόμβοι (σελίδες, outlines, εικόνες, πλούσιο κείμενο) θέλετε να επεξεργαστείτε.  
- **Performance:** Αποφεύγετε τη φόρτωση ολόκληρου του εγγράφου στη μνήμη ως ένα ενιαίο blob· κάθε κόμβος επισκέπτεται κατά απαίτηση.  
- **Versatility:** Ο ίδιος visitor μπορεί να επεκταθεί για εξαγωγή εικόνων, πινάκων ή προσαρμοσμένων μεταδεδομένων, καθιστώντας το μια ολοκληρωμένη λύση τόσο για **convert onenote to text** όσο και για **how to extract images** εργασίες.

## Προαπαιτούμενα

1. Java Development Kit (JDK) 8 ή νεότερο εγκατεστημένο.  
2. Βιβλιοθήκη Aspose.Note for Java ληφθείσα. Μπορείτε να τη κατεβάσετε **[εδώ](https://releases.aspose.com/note/java/)**.  
3. Ένα έγγραφο OneNote (`.one` αρχείο) από το οποίο θέλετε να εξάγετε εικόνες ή να μετατρέψετε σε κείμενο.

## Εισαγωγή Πακέτων

Πρώτα, εισάγετε τις απαραίτητες κλάσεις από το API του Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## Βήμα 1: Ρύθμιση Προσαρμοσμένου Document Visitor

Δημιουργήστε μια κλάση που κληρονομεί το `DocumentVisitor`. Αυτή η κλάση θα κληθεί για κάθε κόμβο στο έγγραφο OneNote, επιτρέποντάς σας να **εξάγετε εικόνες OneNote** και προαιρετικά να συλλέξετε κείμενο.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## Βήμα 2: Υλοποίηση Μεθόδων Visitor

Προσθέστε παρακάμψεις (overrides) για τους τύπους κόμβων που σας ενδιαφέρουν. Παρακάτω διαχειριζόμαστε πλούσιο‑κείμενο, εικόνες, τίτλους, σελίδες, outlines και στοιχεία outline. Η μέθοδος `VisitImageStart` είναι εκεί όπου πραγματοποιείται η εξαγωγή της εικόνας.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### Γιατί να υλοποιήσετε αυτές τις μεθόδους;

- **Extract images from OneNote:** `VisitImageStart` σας δίνει άμεση πρόσβαση στα ακατέργαστα bytes της εικόνας.  
- **Convert OneNote to text:** `VisitRichTextStart` συλλέγει το κειμενικό περιεχόμενο, επιτρέποντας μια απλή λειτουργία **convert OneNote to text**.  
- **Read .one file Java:** Το πρότυπο visitor αφαιρεί την ανάγκη να αναλύσετε τη δομή του αρχείου `.one` μόνοι σας.

## Βήμα 3: Εκτέλεση του Visitor από τη Μέθοδο Main

Φορτώστε το αρχείο `.one`, δημιουργήστε το visitor σας και ξεκινήστε τη διάσχιση.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Κοινές Περιπτώσεις Χρήσης

- **Automated reporting:** Αποσπάστε εικόνες και κείμενο από ένα σημειωματάριο OneNote συνάντησης για να δημιουργήσετε μια σύνοψη σε PDF ή HTML.  
- **Content migration:** Μετατρέψτε παλιά αρχεία OneNote σε αρχεία απλού κειμένου για ευρετηρίαση ή εισαγωγή σε μηχανές αναζήτησης.  
- **Digital asset extraction:** Συλλέξτε ενσωματωμένα screenshots, διαγράμματα ή φωτογραφίες για επαναχρησιμοποίηση σε άλλες εφαρμογές.  

## Αντιμετώπιση Προβλημάτων & Συμβουλές

- **Large notebooks:** Εάν αντιμετωπίσετε προβλήματα μνήμης, επεξεργαστείτε τις σελίδες ξεχωριστά ελέγχοντας το `VisitPageStart` και φορτώνοντας πόρους επιπέδου σελίδας μόνο όταν χρειάζεται.  
- **Image formats:** Το αντικείμενο `Image` επιστρέφει ακατέργαστα bytes· ίσως χρειαστεί να εντοπίσετε τη μορφή (PNG, JPEG) πριν αποθηκεύσετε.  
- **License errors:** Βεβαιωθείτε ότι έχετε ορίσει την άδεια Aspose (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) πριν φορτώσετε το έγγραφο σε παραγωγικό περιβάλλον.  
- **How to extract images efficiently:** Φιλτράρετε τους κόμβους μέσα στο `VisitImageStart` κατά μέγεθος ή μορφή εάν χρειάζεστε μόνο συγκεκριμένους τύπους εικόνων.  

## Συχνές Ερωτήσεις

**Q: Μπορώ να εξάγω συγκεκριμένους τύπους περιεχομένου από το έγγραφο OneNote;**  
A: Ναι – παρακάμπτοντας μόνο τις μεθόδους visitor που χρειάζεστε (π.χ., `VisitImageStart` για εικόνες, `VisitRichTextStart` για κείμενο).

**Q: Είναι το Aspose.Note for Java συμβατό με διαφορετικές εκδόσεις εγγράφων OneNote;**  
A: Απόλυτα. Η βιβλιοθήκη υποστηρίζει όλες τις κύριες εκδόσεις αρχείων OneNote, ώστε να μπορείτε με ασφάλεια να **read .one file java** έργα ανεξαρτήτως της αρχικής έκδοσης OneNote.

**Q: Μπορώ να ενσωματώσω αυτή τη διαδικασία εξαγωγής στην εφαρμογή μου Java;**  
A: Ναι. Το πρότυπο visitor λειτουργεί αβίαστα σε οποιοδήποτε κώδικα Java· απλώς προσθέστε το JAR της βιβλιοθήκης και καλέστε το παράδειγμα που φαίνεται παραπάνω.

**Q: Παρέχει το Aspose.Note for Java υποστήριξη για τη διαχείριση σύνθετων εγγράφων OneNote;**  
A: Ναι. Τα ένθετα outlines, τα ενσωματωμένα μέσα και τα προσαρμοσμένα δεδομένα εκτίθενται όλα μέσω του API visitor.

**Q: Υπάρχει κάποιο όριο στο μέγεθος του εγγράφου OneNote που μπορεί να επεξεργαστεί;**  
A: Δεν υπάρχει σκληρό όριο, αλλά εξαιρετικά μεγάλα σημειωματάρια μπορεί να απαιτούν περισσότερη μνήμη heap· σκεφτείτε την επεξεργασία τους σελίδα‑με‑σελίδα.

**Q: Πώς μετατρέπω το εξαγόμενο κείμενο σε αρχείο απλού κειμένου;**  
A: Αφού το `myConverter.GetText()` επιστρέψει ένα `String`, γράψτε το σε αρχείο χρησιμοποιώντας το τυπικό Java I/O (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---

**Last Updated:** 2026-02-10  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}