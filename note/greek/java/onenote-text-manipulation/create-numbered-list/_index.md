---
date: 2026-03-05
description: Μάθετε πώς να αποθηκεύετε το OneNote ως PDF ενώ δημιουργείτε αριθμημένη
  λίστα χρησιμοποιώντας το Aspose.Note για Java. Περιλαμβάνει βήματα για τον ορισμό
  του προεπιλεγμένου στυλ κειμένου και την προσαρμογή της αρίθμησης.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: Αποθήκευση του OneNote ως PDF – Δημιουργία αριθμημένης λίστας με το Aspose.Note
url: /el/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση OneNote ως PDF – Δημιουργία αριθμημένης λίστας με Aspose.Note

## Εισαγωγή
Το Aspose.Note for Java δίνει τη δυνατότητα στους προγραμματιστές Java να **αποθηκεύσουν OneNote ως PDF** και να εμπλουτίσουν το έγγραφο με προηγμένη μορφοποίηση, όπως αριθμημένες λίστες. Σε αυτό το tutorial, θα σας καθοδηγήσουμε μέσα από τη διαδικασία – από τον ορισμό προεπιλεγμένου στυλ κειμένου μέχρι την προσαρμογή της μορφής αρίθμησης – ώστε να μπορείτε να εξάγετε το OneNote σε PDF με επαγγελματική εμφάνιση.

## Γρήγορες Απαντήσεις
- **Τι καλύπτει αυτό το tutorial;** Δημιουργία αριθμημένης λίστας στο OneNote και αποθήκευση του αρχείου ως PDF χρησιμοποιώντας Aspose.Note for Java.  
- **Ποια είναι η κύρια λέξη-κλειδί;** *save onenote as pdf*  
- **Χρειάζομαι άδεια;** Διατίθεται δωρεάν δοκιμή· απαιτείται εμπορική άδεια για παραγωγική χρήση.  
- **Ποια έκδοση Java απαιτείται;** JDK 8 ή νεότερη.  
- **Πόσο διαρκεί η υλοποίηση;** Περίπου 10–15 λεπτά για μια βασική λίστα.

## Τι είναι η «αποθήκευση OneNote ως PDF»;
Η αποθήκευση OneNote ως PDF μετατρέπει τη σελίδα OneNote με πλούσιο κείμενο σε ένα φορητό, σταθερό έγγραφο που μπορεί να κοινοποιηθεί σε διαφορετικές πλατφόρμες χωρίς να απαιτείται το OneNote. Αυτό είναι ιδιαίτερα χρήσιμο για αρχειοθέτηση, αναφορές ή διανομή περιεχομένου σε χρήστες που δεν έχουν εγκατεστημένο το OneNote.

## Γιατί να δημιουργήσετε αριθμημένη λίστα πριν από την εξαγωγή;
Μια αριθμημένη λίστα προσθέτει δομή και αναγνωσιμότητα, κάνοντας το εξαγόμενο PDF να μοιάζει με επαγγελματική αναφορά. Με το Aspose.Note μπορείτε να **προσαρμόσετε τη μορφή αρίθμησης**, να ορίσετε γραμματοσειρές και να ελέγξετε το διάστημα – όλα διατηρώντας την αρχική διάταξη του OneNote.

## Προαπαιτούμενα
Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- Java Development Kit (JDK) εγκατεστημένο στον υπολογιστή σας.  
- Βιβλιοθήκη Aspose.Note for Java που έχετε κατεβάσει από [here](https://releases.aspose.com/note/java/).  

## Εισαγωγή Πακέτων
Πρώτα, εισάγετε τις απαιτούμενες κλάσεις ώστε να μπορείτε να εργάζεστε με αντικείμενα OneNote και τη μετατροπή σε PDF.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```

## Πώς να αποθηκεύσετε OneNote ως PDF με αριθμημένη λίστα;
Παρακάτω θα βρείτε έναν οδηγό βήμα‑βήμα που δείχνει **πώς να δημιουργήσετε στοιχεία λίστας**, **να ορίσετε προεπιλεγμένο στυλ κειμένου**, και τέλος **να εξάγετε το OneNote σε PDF**.

### Βήμα 1: Αρχικοποίηση Εγγράφου, Σελίδας και Αντικειμένων Outline
Ξεκινάμε δημιουργώντας τις βασικές δομές του OneNote. Αυτό επίσης δείχνει τη χρήση του **add outline element java**.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Συμβουλή:** Κρατήστε το μονοπάτι `dataDir` απόλυτο ή χρησιμοποιήστε `System.getProperty("user.dir")` για να αποφύγετε προβλήματα διαδρομής.

### Βήμα 2: Ορισμός Προεπιλεγμένου Στυλ Κειμένου
Ένα συνεπές στυλ εξασφαλίζει ότι η λίστα φαίνεται ομοιόμορφα σε όλα τα στοιχεία.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### Βήμα 3: Δημιουργία Στοιχείων Outline (Αριθμημένη Λίστα)
Εδώ **προσαρμόζουμε τη μορφή αρίθμησης** χρησιμοποιώντας το `NumberList`. Το μοτίβο `"{0})"` παράγει “1)”, “2)”, κ.λπ.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **Γιατί είναι σημαντικό:** Με την προσθήκη ενός `NumberList` σε κάθε `OutlineElement`, αποκτάτε πλήρη έλεγχο του στυλ αρίθμησης, της γραμματοσειράς και του μεγέθους.

### Βήμα 4: Προσθήκη Στοιχείων Outline στο Outline
Τώρα ενώνουμε τα μεμονωμένα στοιχεία λίστας σε ένα ενιαίο outline.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Βήμα 5: Συγκόλληση Outline στη Σελίδα
Το outline γίνεται μέρος της ιεραρχίας της σελίδας OneNote.

```java
page.appendChildLast(outline);
```

### Βήμα 6: Αποθήκευση Εγγράφου ως PDF
Τέλος, **αποθηκεύουμε το OneNote ως PDF**. Το αρχείο εξόδου θα περιέχει την αριθμημένη λίστα ακριβώς όπως ορίστηκε.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

Η εκτέλεση του παραπάνω κώδικα δημιουργεί ένα PDF με όνομα `CreateNumberedList_out.pdf` στον καθορισμένο φάκελό σας, διατηρώντας τη μορφή της αριθμημένης λίστας.

## Συχνά Προβλήματα & Λύσεις
| Πρόβλημα | Λύση |
|----------|------|
| **Το PDF είναι κενό** | Βεβαιωθείτε ότι το `doc.appendChildLast(page);` καλείται πριν από το `doc.save()`. |
| **Η αρίθμηση δεν εμφανίζεται** | Επαληθεύστε ότι το μοτίβο `NumberList` και το `NumberFormat` έχουν οριστεί σωστά. |
| **Σφάλμα αρχείου δεν βρέθηκε** | Χρησιμοποιήστε απόλυτο μονοπάτι για το `dataDir` ή δημιουργήστε τον φάκελο εκ των προτέρων. |
| **Ασυμφωνία γραμματοσειράς** | Εγκαταστήστε τη γραμματοσειρά (π.χ., Arial) στο μηχάνημα που εκτελεί τον κώδικα. |

## Συχνές Ερωτήσεις
### Ε: Μπορώ να προσαρμόσω τη μορφή αρίθμησης στη λίστα OneNote μου;
Α: Απόλυτα! Μπορείτε να προσαρμόσετε τη μορφή αρίθμησης χρησιμοποιώντας την κλάση `NumberList` που παρέχεται από το Aspose.Note for Java.

### Ε: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Note for Java;
Α: Ναι, μπορείτε να κατεβάσετε μια δωρεάν δοκιμή [here](https://releases.aspose.com/).

### Ε: Πώς μπορώ να λάβω υποστήριξη για το Aspose.Note for Java;
Α: Επισκεφθείτε το [Aspose.Note for Java forum](https://forum.aspose.com/c/note/28) για υποστήριξη από την κοινότητα.

### Ε: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.Note for Java;
Α: Ανατρέξτε στην [documentation](https://reference.aspose.com/note/java/) για ολοκληρωμένες πληροφορίες.

### Ε: Πώς μπορώ να αγοράσω άδεια για το Aspose.Note for Java;
Α: Μπορείτε να αγοράσετε άδεια [here](https://purchase.aspose.com/buy).

## Συμπέρασμα
Σε αυτό το tutorial δείξαμε πώς να **αποθηκεύσετε OneNote ως PDF** ενώ δημιουργείτε μια καθαρή, αριθμημένη λίστα χρησιμοποιώντας το Aspose.Note for Java. Ορίζοντας ένα προεπιλεγμένο στυλ κειμένου, προσαρμόζοντας τη μορφή αρίθμησης και ακολουθώντας τον βήμα‑βήμα οδηγό, μπορείτε να παράγετε επαγγελματικά PDF από σελίδες OneNote γρήγορα και αξιόπιστα.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Τελευταία ενημέρωση:** 2026-03-05  
**Δοκιμή με:** Aspose.Note for Java 24.11  
**Συγγραφέας:** Aspose  

---