---
date: 2026-01-28
description: Μάθετε πώς να δημιουργείτε περίγραμμα στο OneNote, να προσθέτετε ετικέτα
  στο OneNote και να δημιουργείτε PDF από το OneNote χρησιμοποιώντας το Aspose.Note
  για Java.
linktitle: Create Outline in OneNote and Add Tag – Aspose.Note
second_title: Aspose.Note Java API
title: Δημιουργία περιγράμματος στο OneNote και προσθήκη ετικέτας – Aspose.Note
url: /el/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δημιουργία περιγράμματος στο OneNote και προσθήκη ετικέτας – Aspose.Note

## Εισαγωγή
Αναζητάτε **να δημιουργήσετε περίγραμμα στο OneNote** και να ενισχύσετε τη συνεργασία με ετικέτες χρησιμοποιώντας Java; Το Aspose.Note for Java το κάνει απλό για την προσθήκη ετικετών, τη δομήση των σημειώσεών σας και ακόμη **να δημιουργήσετε PDF από αρχεία OneNote**. Σε αυτό το tutorial θα περάσουμε βήμα‑βήμα, θα εξηγήσουμε *γιατί* κάθε στοιχείο είναι σημαντικό και θα σας δείξουμε πώς να παραγάγετε ένα επαγγελματικό PDF στο τέλος.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “create outline in OneNote”;** Δημιουργεί μια ιεραρχική δομή (περιγράμματα) που οργανώνει το περιεχόμενο όπως τίτλους και υπο‑ενότητες.  
- **Ποια βιβλιοθήκη προσθέτει ετικέτες στο OneNote;** Το Aspose.Note for Java παρέχει την κλάση `NoteTag` για οπτικούς δείκτες.  
- **Μπορώ να εξάγω το αποτέλεσμα σε PDF;** Ναι – χρησιμοποιήστε `SaveFormat.Pdf` για **να δημιουργήσετε PDF από OneNote**.  
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Μια προσωρινή άδεια είναι διαθέσιμη για δοκιμές· απαιτείται πλήρης άδεια για εμπορική χρήση.  
- **Ποια είναι τα κύρια προαπαιτούμενα;** Εγκατεστημένο JDK, βιβλιοθήκη Aspose.Note for Java και βασικές γνώσεις Java.

## Τι είναι το “create outline in OneNote”;
Η δημιουργία περιγράμματος στο OneNote σημαίνει την προσθήκη αντικειμένων `Outline` και `OutlineElement` που ορίζουν μια δομή δέντρου για τις σημειώσεις σας. Αυτή η ιεραρχία σας επιτρέπει να συμπτύσσετε, να επεκτείνετε και να οργανώσετε πληροφορίες όπως τίτλους σε ένα έγγραφο.

## Γιατί να προσθέσετε ετικέτα στο OneNote;
Οι ετικέτες όπως αστέρια, σημεία ελέγχου ή προσαρμοσμένα εικονίδια παρέχουν στους αναγνώστες οπτικές ενδείξεις, βελτιώνουν την αναζητησιμότητα και βοηθούν τις ομάδες να δίνουν προτεραιότητα σε στοιχεία. Με το Aspose.Note μπορείτε προγραμματιστικά να συνδέσετε ένα `NoteTag` σε οποιοδήποτε κομμάτι κειμένου.

## Προαπαιτούμενα
Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:
- Εγκατεστημένο Java Development Kit (JDK).
- Κατεβάσει τη βιβλιοθήκη Aspose.Note for Java. Μπορείτε να τη βρείτε [εδώ](https://releases.aspose.com/note/java/).
- Βασική κατανόηση του προγραμματισμού Java.

## Εισαγωγή Πακέτων
Βεβαιωθείτε ότι εισάγετε τα απαραίτητα πακέτα για να ξεκινήσετε το έργο σας:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
Ας αναλύσουμε τον παραπάνω κώδικα βήμα‑βήμα.

## Βήμα 1: Ρύθμιση Εγγράφου και Σελίδας
Ξεκινήστε δημιουργώντας ένα νέο αντικείμενο `Document` και αρχικοποιώντας ένα αντικείμενο `Page`:
```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```
Εδώ ορίζουμε τη διαδρομή του καταλόγου εγγράφων, δημιουργούμε ένα νέο `Document` και αρχικοποιούμε μια `Page`.

## Βήμα 2: Δημιουργία Περιγράμματος
Στη συνέχεια, δημιουργήστε ένα αντικείμενο `Outline` για να δομήσετε το περιεχόμενό σας:
```java
Outline outline = new Outline();
```
Τα περιγράμματα παρέχουν ιεραρχική δομή στο έγγραφό σας, διευκολύνοντας το **create outline in OneNote** και τη διατήρηση των πληροφοριών οργανωμένων.

## Βήμα 3: Αρχικοποίηση OutlineElement και ParagraphStyle
Τώρα, αρχικοποιήστε ένα `OutlineElement` και ορίστε `ParagraphStyle` για τη μορφοποίηση του κειμένου:
```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```
Το `OutlineElement` αντιπροσωπεύει ένα στοιχείο μέσα στο περίγραμμα, ενώ το `ParagraphStyle` ορίζει τις ιδιότητες μορφοποίησης του κειμένου.

## Βήμα 4: Προσθήκη RichText με NoteTag
Δημιουργήστε ένα αντικείμενο `RichText`, προσθέστε το κείμενο OneNote και προσθέστε ένα `NoteTag`:
```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
Το `RichText` σας επιτρέπει να ενσωματώσετε μορφοποιημένο κείμενο, και το `NoteTag` **adds tag to OneNote** ως οπτική ένδειξη.

## Βήμα 5: Κατασκευή Δομής Περιγράμματος
Προσθέστε τον κόμβο κειμένου, τον κόμβο στοιχείου περιγράμματος και τον κόμβο περιγράμματος για να δημιουργήσετε τη δομή του εγγράφου:
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```
Αυτό το βήμα εξασφαλίζει ότι το περιεχόμενό σας είναι οργανωμένο μέσα στο έγγραφο, ολοκληρώνοντας τη διαδικασία **create outline in OneNote**.

## Βήμα 6: Αποθήκευση Εγγράφου
Αποθηκεύστε το έγγραφο σε μορφή PDF, το οποίο **generates PDF from OneNote**:
```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```
Τώρα, το έγγραφο OneNote με τις προστιθέμενες ετικέτες αποθηκεύεται ως PDF.

Ακολουθώντας αυτά τα βήματα, μπορείτε εύκολα να βελτιώσετε τα έγγραφα OneNote χρησιμοποιώντας το Aspose.Note for Java.

## Συμπέρασμα
Σε αυτό το tutorial εξερευνήσαμε πώς να **create outline in OneNote**, να προσθέσουμε ετικέτα στο OneNote και στη συνέχεια να **generate PDF from OneNote** χρησιμοποιώντας το Aspose.Note for Java. Η χρήση της Java σας δίνει πλήρη έλεγχο πάνω στη δομή των σημειώσεων, την οπτική σήμανση και τις επιλογές εξαγωγής, καθιστώντας τις σημειώσεις σας πιο οργανωμένες και διαμοιραζόμενες.

## Συχνές Ερωτήσεις
### 1. Μπορώ να χρησιμοποιήσω το Aspose.Note for Java με άλλες γλώσσες προγραμματισμού;
Το Aspose.Note υποστηρίζει κυρίως Java, αλλά υπάρχουν επίσης εκδόσεις διαθέσιμες για .NET.

### 2. Είναι το Aspose.Note for Java κατάλληλο για αρχάριους;
Ναι, το Aspose.Note for Java παρέχει εκτενή τεκμηρίωση και υποστήριξη, καθιστώντας το προσβάσιμο τόσο για αρχάριους όσο και για έμπειρους προγραμματιστές.

### 3. Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.Note for Java;
Μπορείτε να λάβετε μια προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

### 4. Πού μπορώ να βρω επιπλέον υποστήριξη;
Για ερωτήσεις ή βοήθεια, επισκεφθείτε το [φόρουμ Aspose.Note](https://forum.aspose.com/c/note/28).

### 5. Υπάρχει δωρεάν δοκιμή;
Ναι, μπορείτε να δοκιμάσετε δωρεάν [εδώ](https://releases.aspose.com/).

**Πρόσθετες Ε/Ρ**

**Ε: Μπορώ να προσαρμόσω το εικονίδιο της ετικέτας;**  
Α: Ναι – το Aspose.Note παρέχει πολλά προεπιλεγμένα εικονίδια μέσω του `TagIcon` και επιτρέπει επίσης προσαρμοσμένες εικόνες.

**Ε: Πώς αλλάζω τις ρυθμίσεις εξόδου PDF;**  
Α: Χρησιμοποιήστε το `PdfSaveOptions` για να ελέγξετε την ποιότητα εικόνας, τη συμπίεση και την ασφάλεια πριν καλέσετε `doc.save`.

**Ε: Είναι δυνατόν να προσθέσω πολλαπλές ετικέτες στο ίδιο κείμενο;**  
Α: Απόλυτα. Καλέστε `text.getTags().add()` πολλές φορές με διαφορετικές εμφανίσεις `NoteTag`.

---

**Τελευταία ενημέρωση:** 2026-01-28  
**Δοκιμασμένο με:** Aspose.Note for Java 24.12  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}