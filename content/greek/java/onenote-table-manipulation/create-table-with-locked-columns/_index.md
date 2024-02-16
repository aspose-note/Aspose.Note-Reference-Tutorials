---
title: Δημιουργία πίνακα με κλειδωμένες στήλες στο OneNote - Aspose.Note
linktitle: Δημιουργία πίνακα με κλειδωμένες στήλες στο OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Βελτιώστε την εμπειρία σας στο OneNote με το Aspose.Note για Java. Μάθετε πώς να δημιουργείτε πίνακες με κλειδωμένες στήλες χρησιμοποιώντας έναν οδηγό βήμα προς βήμα. Κατεβάστε τη δωρεάν δοκιμή σας τώρα!
type: docs
weight: 12
url: /el/java/onenote-table-manipulation/create-table-with-locked-columns/
---
## Εισαγωγή
Το OneNote είναι ένα ισχυρό εργαλείο για την οργάνωση πληροφοριών και το Aspose.Note για Java ενισχύει τις δυνατότητές του παρέχοντας έναν απρόσκοπτο τρόπο δημιουργίας πινάκων με κλειδωμένες στήλες. Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία χρήσης του Aspose.Note για Java για τη δημιουργία ενός πίνακα με κλειδωμένες στήλες στο OneNote.
## Προαπαιτούμενα
Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)εγκατεστημένο στο μηχάνημά σας.
- [Aspose.Note για Java](https://downloads.aspose.com/note/java) κατεβάστηκε και προστέθηκε στο έργο σας.
## Εισαγωγή πακέτων
Στο έργο σας Java, εισαγάγετε τα απαραίτητα πακέτα για την εργασία με το Aspose.Σημείωση:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Βήμα 1: Ρύθμιση του έργου σας
Ξεκινήστε δημιουργώντας ένα νέο έργο Java και προσθέτοντας τη βιβλιοθήκη Aspose.Note στη διαδρομή της τάξης σας. Βεβαιωθείτε ότι το έργο σας έχει ρυθμιστεί ώστε να χρησιμοποιεί το JDK.
## Βήμα 2: Αρχικοποίηση αντικειμένων εγγράφου και σελίδας
```java
// Η διαδρομή προς τον κατάλογο εγγράφων.
String dataDir = "Your Document Directory";
//Δημιουργήστε ένα αντικείμενο της κλάσης Document
Document doc = new Document();
// Αρχικοποίηση αντικειμένου κλάσης σελίδας
Page page = new Page();
```
## Βήμα 3: Δημιουργήστε σειρές και κελιά πίνακα
```java
// Αρχικοποίηση αντικειμένου κλάσης TableRow
TableRow row1 = new TableRow();
// Εκκινήστε το αντικείμενο κλάσης TableCell και ορίστε περιεχόμενο κειμένου
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Αρχικοποίηση αντικειμένου κλάσης TableRow
TableRow row2 = new TableRow();
// Εκκινήστε το αντικείμενο κλάσης TableCell και ορίστε περιεχόμενο κειμένου
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Βήμα 4: Δημιουργήστε και προσαρμόστε τον πίνακα
```java
// Αρχικοποίηση αντικειμένου κλάσης πίνακα
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Προσθήκη σειρών
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Βήμα 5: Προσθήκη πίνακα στο περίγραμμα και τη σελίδα
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Προσθήκη κόμβου πίνακα
outlineElem.appendChildLast(table);
// Προσθήκη κόμβου στοιχείου περιγράμματος
outline.appendChildLast(outlineElem);
// Προσθήκη κόμβου περιγράμματος
page.appendChildLast(outline);
// Προσθήκη κόμβου σελίδας
doc.appendChildLast(page);
```
## Βήμα 6: Αποθηκεύστε το έγγραφο
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Συγχαρητήρια! Έχετε δημιουργήσει επιτυχώς έναν πίνακα με κλειδωμένες στήλες στο OneNote χρησιμοποιώντας το Aspose.Note για Java.
## συμπέρασμα
Σε αυτό το σεμινάριο, εξερευνήσαμε τη διαδικασία χρήσης του Aspose.Note για Java για να βελτιώσουμε την εμπειρία σας στο OneNote δημιουργώντας πίνακες με κλειδωμένες στήλες. Αυτή η λειτουργία προσθέτει ένα νέο επίπεδο οργάνωσης και δομής στις σημειώσεις σας.
## Συχνές ερωτήσεις
### Είναι το Aspose.Note για Java συμβατό με όλες τις εκδόσεις Java;
Ναι, το Aspose.Note για Java είναι συμβατό με Java 6 και νεότερες εκδόσεις.
### Μπορώ να προσαρμόσω περαιτέρω την εμφάνιση του πίνακα;
Απολύτως! Το Aspose.Note για Java παρέχει εκτενείς επιλογές για την προσαρμογή πινάκων, όπως προσαρμογή περιγραμμάτων, απόσταση κελιών και άλλα.
### Υπάρχει διαθέσιμη δοκιμαστική έκδοση πριν την αγορά;
 Ναι μπορείς[κατεβάστε μια δωρεάν δοκιμή](https://releases.aspose.com/) για να εξερευνήσετε τις δυνατότητες του Aspose.Note για Java.
### Πού μπορώ να βρω πρόσθετη υποστήριξη ή συζητήσεις στην κοινότητα;
 Επισκέψου το[Aspose.Note φόρουμ](https://forum.aspose.com/c/note/28) για υποστήριξη και κοινοτικές συζητήσεις.
### Πώς μπορώ να αποκτήσω μια προσωρινή άδεια χρήσης για το Aspose.Note για Java;
 Επίσκεψη[αυτός ο σύνδεσμος](https://purchase.aspose.com/temporary-license/) για την απόκτηση προσωρινής άδειας για σκοπούς δοκιμών.