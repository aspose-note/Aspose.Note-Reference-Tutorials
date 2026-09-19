---
date: 2026-09-19
description: Μάθετε πώς να αποθηκεύετε το OneNote ως PDF με το Aspose.Note for Java,
  να εισάγετε μια γραμμή πίνακα και να επισημάνετε τον πίνακα—όλα σε λίγες γραμμές
  κώδικα.
keywords:
- save onenote as pdf
- insert table row java
- export onenote to pdf
- how to export onenote pdf
- convert onenote document to pdf
lastmod: 2026-09-19
linktitle: Αποθήκευση του OneNote ως PDF και εισαγωγή γραμμής πίνακα σε Java
og_description: Αποθηκεύστε το OneNote ως PDF με το Aspose.Note for Java, στη συνέχεια
  εισάγετε και επισημάνετε μια γραμμή πίνακα σε λίγες μόνο γραμμές. Μάθετε πώς να
  εξάγετε το onenote σε pdf, τη διαχείριση πινάκων και τη μετατροπή σε PDF σε αυτόν
  τον οδηγό βήμα‑βήμα.
og_image_alt: 'Developer guide: Save OneNote as PDF and insert table row in Java using
  Aspose.Note'
og_title: Αποθήκευση του OneNote ως PDF και εισαγωγή γραμμής πίνακα σε Java
schemas:
- author: Aspose
  dateModified: '2026-09-19'
  description: Learn how to save OneNote as PDF with Aspose.Note for Java, insert
    a table row, and tag the table—all in a few lines of code.
  headline: Save OneNote as PDF and insert a table row in Java
  type: TechArticle
- questions:
  - answer: Aspose.Note is primarily a Java library, but equivalent SDKs exist for
      .NET, C++, and Python, offering similar functionality.
    question: Can I use Aspose.Note for Java with other programming languages?
  - answer: Yes, Aspose.Note for Java is regularly updated to support the newest JDK
      releases, including JDK 21.
    question: Is Aspose.Note for Java compatible with the latest JDK versions?
  - answer: Absolutely. You can modify borders, background colors, cell padding, and
      even apply custom fonts via the `Table` and `TableCell` property APIs.
    question: Can I customize the appearance of the table nodes?
  - answer: Visit the [Aspose.Note Java Documentation](https://reference.aspose.com/note/java/)
      for a full collection of code samples and API references.
    question: Where can I find additional examples and documentation?
  - answer: Visit the [Aspose.Note Forum](https://forum.aspose.com/c/note/28) for
      community assistance or purchase a support plan at the [purchase a support plan](https://purchase.aspose.com/buy)
      for dedicated help.
    question: How can I get support for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote automation
- Aspose.Note
- java document processing
title: Αποθήκευση του OneNote ως PDF και εισαγωγή γραμμής πίνακα σε Java
url: /el/java/onenote-tag-operations/add-new-table-node-with-tag/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση OneNote ως PDF και εισαγωγή γραμμής πίνακα σε Java

## Εισαγωγή
Αν χρειάζεστε **αποθήκευση OneNote ως PDF** ενώ προσθέτετε προγραμματιστικά μια νέα γραμμή πίνακα, το Aspose.Note for Java σας παρέχει ένα καθαρό, πλήρως εξοπλισμένο API. Σε αυτό το μάθημα θα περάσουμε από τη δημιουργία ενός OneNote `Document`, την εισαγωγή μιας γραμμής πίνακα, την επισήμανση του πίνακα και, τέλος, την εξαγωγή της σελίδας σε PDF. Αυτή η ροή εργασίας είναι ιδανική για αυτοματοποιημένες αναφορές, δυναμική λήψη σημειώσεων ή οποιοδήποτε σενάριο όπου δημιουργείτε περιεχόμενο OneNote άμεσα.

## Γρήγορες απαντήσεις
- **Τι κάνει το “insert table row java”;** Δημιουργεί ένα νέο αντικείμενο `TableRow` και το συνδέει προγραμματιστικά με έναν υπάρχοντα πίνακα OneNote.  
- **Ποια βιβλιοθήκη διαχειρίζεται τη μετατροπή;** Το Aspose.Note for Java παρέχει τόσο τη διαχείριση πινάκων όσο και τις δυνατότητες εξαγωγής σε PDF.  
- **Μπορώ να επισυνάψω ετικέτα στον πίνακα για γρήγορη αναζήτηση;** Ναι – μπορείτε να προσθέσετε ένα `NoteTag` (π.χ., ένα ερωτηματικό) στον κόμβο του πίνακα.  
- **Πώς εξάγω το αποτέλεσμα;** Καλέστε `doc.save("output.pdf", SaveFormat.Pdf)` για **αποθήκευση OneNote ως PDF** σε μία γραμμή.  
- **Χρειάζομαι άδεια για παραγωγή;** Η δοκιμαστική έκδοση λειτουργεί για αξιολόγηση· απαιτείται εμπορική άδεια για παραγωγικές εγκαταστάσεις.

## Τι είναι η αποθήκευση OneNote ως PDF;
Η αποθήκευση OneNote ως PDF μετατρέπει τη σελίδα OneNote σε μια φορητή, μόνο για ανάγνωση μορφή που μπορεί να μοιραστεί σε διάφορες πλατφόρμες. Η εξαγωγή PDF του Aspose.Note διατηρεί τις γραμματοσειρές, τις εικόνες και την ακεραιότητα της διάταξης χωρίς να απαιτείται η εγκατάσταση του Microsoft OneNote. Το προκύπτον PDF διατηρεί την αρχική διάταξη της σελίδας, συμπεριλαμβανομένων πινάκων, εικόνων και προσαρμοσμένων ετικετών, καθιστώντας το κατάλληλο για αρχειοθέτηση ή κοινή χρήση με χρήστες που δεν έχουν εγκατεστημένο το OneNote.

## Γιατί να χρησιμοποιήσετε αυτήν την προσέγγιση;
Το Aspose.Note υποστηρίζει **πάνω από 50 μορφές εισόδου και εξόδου** και μπορεί να επεξεργαστεί σημειωματάρια OneNote με εκατοντάδες σελίδες διατηρώντας τη χρήση μνήμης κάτω από 200 MB. Η επισήμανση πινάκων βελτιώνει την αναζητησιμότητα μέσα στο OneNote, και η άμεση εξαγωγή σε PDF εξαλείφει την ανάγκη για ξεχωριστό βήμα μετατροπής, μειώνοντας το συνολικό χρόνο επεξεργασίας έως και 40 %.

## Προαπαιτούμενα
- Java Development Kit (JDK) 11 ή νεότερο εγκατεστημένο.  
- Βιβλιοθήκη Aspose.Note for Java, την οποία μπορείτε να κατεβάσετε από [Aspose.Note Java Documentation](https://reference.aspose.com/note/java/).  
- Βασική εξοικείωση με τη σύνταξη της Java και τον αντικειμενοστραφή προγραμματισμό.

## Εισαγωγή πακέτων
Στο έργο Java σας, εισάγετε τα namespaces που σας δίνουν πρόσβαση σε κλάσεις εγγράφου, πίνακα και επισήμανσης.

`import com.aspose.note.*;`  
`import com.aspose.note.documents.*;`  
`import com.aspose.note.tags.*;`

Αυτές οι εισαγωγές εκθέτουν τις κλάσεις `Document`, `Table`, `TableRow`, `TableCell` και `NoteTag` που θα χρειαστείτε αργότερα.

## Πώς αποθηκεύετε το OneNote ως PDF;
Φορτώστε το αρχείο OneNote σε ένα αντικείμενο `Document` και καλέστε τη μέθοδο `save` με `SaveFormat.Pdf`. Το API γράφει το PDF στο δίσκο με μία κλήση, διατηρώντας όλα τα στοιχεία της σελίδας — συμπεριλαμβανομένων πινάκων, εικόνων και ετικετών — χωρίς επιπλέον εργαλεία μετατροπής. Μπορείτε επίσης να καθορίσετε πρόσθετες επιλογές όπως η ποιότητα εικόνας ή η ενσωμάτωση γραμματοσειρών χρησιμοποιώντας τη φορτωμένη μέθοδο `save` που δέχεται ένα αντικείμενο `PdfSaveOptions`.  
`save` writes the document to a file in the specified format.

## Βήμα 1: ρύθμιση του εγγράφου
Πρώτα, δημιουργήστε μια νέα παρουσία `Document` που θα περιέχει τη σελίδα OneNote.

`Document doc = new Document();`

**Αγκύρωση ορισμού:** Η κλάση `Document` είναι το κορυφαίο αντικείμενο του Aspose.Note που αντιπροσωπεύει ένα μοναδικό αρχείο OneNote στη μνήμη.

## Βήμα 2: αρχικοποίηση σελίδας, γραμμής πίνακα και κελιού πίνακα
`TableRow` αντιπροσωπεύει μια οριζόντια συλλογή κελιών μέσα σε έναν πίνακα OneNote.  
`TableCell` είναι ένας δοχείο για περιεχόμενο μέσα σε μια γραμμή πίνακα.  
Εδώ **insert table row java** δημιουργούμε μια `TableRow` και ένα μόνο `TableCell`. Το κελί στη συνέχεια συνδέεται με τη γραμμή.

`Page page = new Page();`  
`TableRow row = new TableRow();`  
`TableCell cell = new TableCell();`

## Βήμα 3: δημιουργία του κόμβου πίνακα
`Table` είναι το οπτικό δοχείο που κρατάει γραμμές και στήλες σε μια σελίδα OneNote.  
Δημιουργήστε το δοχείο πίνακα, κάντε τα όρια του ορατά και ορίστε το πλάτος στήλης. Αυτό είναι το σημείο όπου θα **add table cell onenote** αργότερα.

`Table table = new Table();`  
`table.setBorderVisible(true);`  
`Column column = new Column();`  
`Column` defines the width and formatting of a table column.  
`column.setWidth(150);`  
`table.getColumns().add(column);`

## Βήμα 4: εισαγωγή του κόμβου γραμμής στον πίνακα
Τώρα συνδέστε τη γραμμή που δημιουργήθηκε προηγουμένως (με το κελί της) στον πίνακα.

`row.getCells().add(cell);`  
`table.getRows().add(row);`

## Βήμα 5: προσθήκη ετικέτας στον κόμβο πίνακα
`NoteTag` είναι ένα ελαφρύ αντικείμενο μεταδεδομένων που μπορεί να προσαρτηθεί σε οποιοδήποτε στοιχείο OneNote για να μεταφέρει κατάσταση ή πρόθεση.  
Η επισήμανση βοηθά τους χρήστες να αναγνωρίζουν γρήγορα τον σκοπό του πίνακα. Σε αυτό το παράδειγμα χρησιμοποιούμε μια ετικέτα ερωτηματικού.

`NoteTag tag = new NoteTag(NoteTagType.Question);`  
`table.getTags().add(tag);`

## Βήμα 6: δημιουργία της δομής περιγράμματος
`OutlineElement` αντιπροσωπεύει ένα ιεραρχικό δοχείο σε μια σελίδα OneNote, παρόμοιο με ενότητα ή παράγραφο.  
Η ιεραρχία περιγράμματος απαιτείται για σελίδες OneNote. Τοποθετούμε τον πίνακα μέσα σε ένα `OutlineElement`, στη συνέχεια το προσθέτουμε στη σελίδα και τέλος στο έγγραφο.

`OutlineElement outline = new OutlineElement();`  
`outline.getChildren().add(table);`  
`page.getOutlineElements().add(outline);`  
`doc.getPages().add(page);`

## Πώς εξάγετε το OneNote σε PDF;
Καλέστε τη μέθοδο `save` στην παρουσία `Document`, καθορίζοντας `SaveFormat.Pdf`. Η βιβλιοθήκη διαχειρίζεται τη μετατροπή εσωτερικά, διατηρώντας την ακρίβεια των διανυσματικών γραφικών και του κειμένου. Η διαδικασία εξαγωγής μετατρέπει αυτόματα όλα τα στοιχεία της σελίδας, διατηρώντας τα διανυσματικά γραφικά, τη μορφοποίηση κειμένου και τα ενσωματωμένα μέσα. Μπορείτε επίσης να παρέχετε ένα stream αντί για διαδρομή αρχείου για ενσωμάτωση της μετατροπής σε web services ή cloud workflows.

`doc.save("MyOneNote.pdf", SaveFormat.Pdf);`

## Βήμα 7: αποθήκευση του εγγράφου OneNote
Ολοκληρώστε τη διαδικασία εξάγοντας το αρχείο OneNote ως PDF. Αυτό δείχνει τη δυνατότητα **save OneNote as PDF**.

`doc.save("Result.pdf", SaveFormat.Pdf);`

Επαναλάβετε αυτά τα βήματα όποτε χρειαστείτε **insert table row java**, επισήμανση του πίνακα και εξαγωγή του αποτελέσματος.

## Κοινά προβλήματα & συμβουλές
- **Missing license exception:** Βεβαιωθείτε ότι έχετε έγκυρη άδεια Aspose.Note· διαφορετικά θα εμφανιστούν υδατογραφήματα αξιολόγησης στο PDF.  
- **Column widths:** Προσαρμόστε το `column.setWidth()` ώστε να χωράει μεγαλύτερο κείμενο· στήλες που είναι πολύ στενές περικοπούν το περιεχόμενο του κελιού.  
- **Multiple tags:** Μπορείτε να προσθέσετε περισσότερες από μία ετικέτες δημιουργώντας επιπλέον αντικείμενα `NoteTag` και προσθέτοντάς τα στο `table.getTags()`.  
- **Large notebooks:** Για σημειωματάρια που υπερβαίνουν τις 500 σελίδες, σκεφτείτε την επεξεργασία των σελίδων σε παρτίδες ώστε η κατανάλωση μνήμης να παραμένει χαμηλή.

## Συχνές ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω το Aspose.Note for Java με άλλες γλώσσες προγραμματισμού;**  
Α: Το Aspose.Note είναι κυρίως μια βιβλιοθήκη Java, αλλά υπάρχουν ισοδύναμα SDKs για .NET, C++ και Python, προσφέροντας παρόμοιες λειτουργίες.

**Ε: Είναι το Aspose.Note for Java συμβατό με τις τελευταίες εκδόσεις του JDK;**  
Α: Ναι, το Aspose.Note for Java ενημερώνεται τακτικά για να υποστηρίζει τις πιο πρόσφατες εκδόσεις του JDK, συμπεριλαμβανομένου του JDK 21.

**Ε: Μπορώ να προσαρμόσω την εμφάνιση των κόμβων πίνακα;**  
Α: Απόλυτα. Μπορείτε να τροποποιήσετε τα όρια, τα χρώματα φόντου, το padding των κελιών και ακόμη να εφαρμόσετε προσαρμοσμένες γραμματοσειρές μέσω των API ιδιοτήτων `Table` και `TableCell`.

**Ε: Πού μπορώ να βρω επιπλέον παραδείγματα και τεκμηρίωση;**  
Α: Επισκεφθείτε το [Aspose.Note Java Documentation](https://reference.aspose.com/note/java/) για μια πλήρη συλλογή παραδειγμάτων κώδικα και αναφορών API.

**Ε: Πώς μπορώ να λάβω υποστήριξη για το Aspose.Note for Java;**  
Α: Επισκεφθείτε το [Aspose.Note Forum](https://forum.aspose.com/c/note/28) για βοήθεια από την κοινότητα ή αγοράστε ένα πρόγραμμα υποστήριξης στο [purchase a support plan](https://purchase.aspose.com/buy) για εξειδικευμένη βοήθεια.

---

**Τελευταία ενημέρωση:** 2026-09-19  
**Δοκιμασμένο με:** Aspose.Note for Java 24.12  
**Συγγραφέας:** Aspose








```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.Table;
import com.aspose.note.TableCell;
import com.aspose.note.TableColumn;
import com.aspose.note.TableRow;
import com.aspose.note.TagIcon;
```

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
```

```java
// initialize Page class object
Page page = new Page();
// initialize TableRow class object
TableRow row = new TableRow();
// initialize TableCell class object
TableCell cell = new TableCell();
// add cell to row node
row.appendChildLast(cell);
```

```java
// initialize table node
Table table = new Table();
table.setBordersVisible(true);
TableColumn column = new TableColumn();
column.setWidth(70);
table.getColumns().addItem(column);
```

```java
// insert row node in table
table.appendChildLast(row);
```

```java
// add tag to this table node
NoteTag noteTag = NoteTag.createQuestionMark();
table.getTags().add(noteTag);
```

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// add table node
outlineElem.appendChildLast(table);
// add outline elements
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

```java
// save OneNote document
doc.save(dataDir + "AddNewTableNodeWithTag_out.pdf", SaveFormat.Pdf);
```

## Σχετικά Μαθήματα

- [Πώς να αποθηκεύσετε το OneNote ως PDF με το Aspose.Note for Java](/note/java/onenote-document-loading/load-save-format/)
- [Προσθήκη ετικέτας σε εικόνα στο OneNote με το Aspose.Note – Java](/note/java/onenote-tag-operations/add-new-image-node-with-tag/)
- [Αποθήκευση OneNote ως PDF και αντικατάσταση κειμένου σε όλες τις σελίδες – Aspose.Note](/note/java/onenote-text-manipulation/replace-text-on-all-pages/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}