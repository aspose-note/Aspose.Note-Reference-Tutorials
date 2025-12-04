---
date: 2025-12-04
description: Μάθετε πώς να εξάγετε εικόνες από αρχεία OneNote και να μετατρέψετε το
  OneNote σε κείμενο σε Java χρησιμοποιώντας το Aspose.Note. Οδηγός βήμα‑προς‑βήμα
  με παραδείγματα κώδικα.
language: el
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Εξαγωγή εικόνων από το OneNote με χρήση του Document Visitor - Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή Εικόνων από το OneNote χρησιμοποιώντας Document Visitor - Java

## Εισαγωγή

Το Aspose.Note for Java καθιστά εύκολη την **εξαγωγή εικόνων από το OneNote** σημειωματάρια καθώς και την ανάγνωση του υποκείμενου αρχείου `.one` σε Java. Σε αυτό το tutorial θα σας καθοδηγήσουμε βήμα‑βήμα με ένα πλήρες, πρακτικό παράδειγμα που δείχνει πώς να φορτώσετε ένα αρχείο OneNote, να διασχίσετε τη δομή του με ένα προσαρμοσμένο `DocumentVisitor` και να εξάγετε τόσο εικόνες όσο και απλό κείμενο. Στο τέλος θα γνωρίζετε επίσης πώς να **μετατρέψετε το OneNote σε κείμενο** εάν χρειάζεστε μόνο το κειμενικό περιεχόμενο.

## Γρήγορες Ατήσεις
- **Τι βιβλιοθήκη χρειάζομαι;** Aspose.Note for Java (σύνδεσμος λήψης παρακάτω).  
- **Μπορώ να εξάγω μόνο εικόνες;** Ναι – υλοποιήστε τη μέθοδο `VisitImageStart` σε ένα `DocumentVisitor`.  
- **Πώς διαβάζω ένα αρχείο .one σε Java;** Χρησιμοποιήστε `new Document(path, new LoadOptions())`.  
- **Χρειάζομαι άδεια για παραγωγή;** Απαιτείται εμπορική άδεια για μη‑δοκιμαστική χρήση.  
- **Ποια έκδοση Java υποστηρίζεται;** JDK 8 ή νεότερη.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

1. Εγκατεστημένο Java Development Kit (JDK) 8 ή νεότερο.  
2. Τη βιβλιοθήκη Aspose.Note for Java να έχει ληφθεί. Μπορείτε να τη κατεβάσετε **[εδώ](https://releases.aspose.com/note/java/)**.  
3. Ένα έγγραφο OneNote (αρχείο `.one`) από το οποίο θέλετε να εξάγετε εικόνες ή να το μετατρέψετε σε κείμενο.

## Εισαγωγή Πακέτων

Αρχικά, εισάγετε τις απαραίτητες κλάσεις από το API του Aspose.Note.

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

Δημιουργήστε μια κλάση που επεκτείνει το `DocumentVisitor`. Αυτή η κλάση θα κληθεί για κάθε κόμβο του εγγράφου OneNote, επιτρέποντάς σας να **εξάγετε εικόνες από το OneNote** και προαιρετικά να συλλέξετε κείμενο.

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

Προσθέστε παρακάμψεις (overrides) για τους τύπους κόμβων που σας ενδιαφέρουν. Παρακάτω διαχειριζόμαστε πλούσιο κείμενο, εικόνες, τίτλους, σελίδες, outlines και στοιχεία outline. Η μέθοδος `VisitImageStart` είναι εκεί όπου γίνεται η εξαγωγή της εικόνας.

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

- **Εξαγωγή εικόνων από το OneNote:** Η `VisitImageStart` σας δίνει άμεση πρόσβαση στα ακατέργαστα bytes της εικόνας.  
- **Μετατροπή OneNote σε κείμενο:** Η `VisitRichTextStart` συλλέγει το κειμενικό περιεχόμενο, επιτρέποντας μια απλή λειτουργία **μετατροπής OneNote σε κείμενο**.  
- **Ανάγνωση αρχείου .one σε Java:** Το πρότυπο visitor αφαιρεί την πολυπλοκότητα της υποκείμενης δομής του αρχείου `.one`, ώστε να μην χρειάζεται να αναλύετε εσείς το δυαδικό φορμά.

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

## Συνηθισμένες Περιπτώσεις Χρήσης

- **Αυτοματοποιημένη αναφορά:** Εξάγετε εικόνες και κείμενο από ένα σημειωματάριο OneNote συνάντησης για να δημιουργήσετε μια σύνοψη PDF ή HTML.  
- **Μεταφορά περιεχομένου:** Μετατρέψτε παλαιά αρχεία OneNote σε αρχεία απλού κειμένου για ευρετηρίαση ή εισαγωγή σε μηχανές αναζήτησης.  
- **Εξαγωγή ψηφιακών πόρων:** Συλλέξτε ενσωματωμένα στιγμιότυπα, διαγράμματα ή φωτογραφίες για επαναχρησιμοποίηση σε άλλες εφαρμογές.

## Αντιμετώπιση Προβλημάτων & Συμβουλές

- **Μεγάλα σημειωματάρια:** Εάν αντιμετωπίσετε προβλήματα μνήμης, επεξεργαστείτε τις σελίδες ξεχωριστά ελέγχοντας το `VisitPageStart` και φορτώνοντας πόρους σε επίπεδο σελίδας μόνο όταν χρειάζεται.  
- **Μορφές εικόνας:** Το αντικείμενο `Image` επιστρέφει ακατέργαστα bytes· ίσως χρειαστεί να ανιχνεύσετε τη μορφή (PNG, JPEG) πριν αποθηκεύσετε.  
- **Σφάλματα άδειας:** Βεβαιωθείτε ότι έχετε ορίσει την άδεια Aspose (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) πριν φορτώσετε το έγγραφο σε παραγωγικό περιβάλλον.

## Συχνές Ερωτήσεις

**Ε: Μπορώ να εξάγω συγκεκριμένους τύπους περιεχομένου από το έγγραφο OneNote;**  
Α: Ναι – παρακάμπτοντας μόνο τις μεθόδους visitor που χρειάζεστε (π.χ., `VisitImageStart` για εικόνες, `VisitRichTextStart` για κείμενο).

**Ε: Είναι το Aspose.Note for Java συμβατό με διαφορετικές εκδόσεις εγγράφων OneNote;**  
Α: Απόλυτα. Η βιβλιοθήκη υποστηρίζει όλες τις κύριες εκδόσεις αρχείων OneNote, ώστε να μπορείτε με ασφάλεια **να διαβάζετε .one αρχεία σε Java** έργα ανεξάρτητα από την προέλευση της έκδοσης OneNote.

**Ε: Μπορώ να ενσωματώσω αυτή τη διαδικασία εξαγωγής στην εφαρμογή μου Java;**  
Α: Ναι. Το πρότυπο visitor λειτουργεί άψογα σε οποιοδήποτε κώδικα Java· απλώς προσθέστε το JAR της βιβλιοθήκης και καλέστε το παράδειγμα που φαίνεται παραπάνω.

**Ε: Παρέχει το Aspose.Note for Java υποστήριξη για την επεξεργασία σύνθετων εγγράφων OneNote;**  
Α: Ναι. Τα ένθετα outlines, τα ενσωματωμένα μέσα και τα προσαρμοσμένα δεδομένα εκτίθενται όλα μέσω του visitor API.

**Ε: Υπάρχει κάποιο όριο στο μέγεθος του εγγράφου OneNote που μπορεί να επεξεργαστεί;**  
Α: Δεν υπάρχει σκληρό όριο, αλλά εξαιρετικά μεγάλα σημειωματάρια μπορεί να απαιτούν περισσότερη μνήμη heap· σκεφτείτε την επεξεργασία τους σελίδα προς σελίδα.

**Ε: Πώς μετατρέπω το εξαγόμενο κείμενο σε αρχείο απλού κειμένου;**  
Α: Αφού η `myConverter.GetText()` επιστρέψει ένα `String`, γράψτε το σε αρχείο χρησιμοποιώντας το τυπικό Java I/O (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}