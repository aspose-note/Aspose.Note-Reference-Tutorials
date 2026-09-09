---
date: 2026-03-08
description: Μάθετε πώς να αποθηκεύετε το OneNote ως PDF με μια κινεζική αριθμημένη
  λίστα χρησιμοποιώντας το Aspose.Note για Java. Οδηγός βήμα-βήμα που καλύπτει την
  αρίθμηση, τις δομές και την εξαγωγή PDF.
linktitle: Save OneNote as PDF with Chinese Numbered List – Aspose.Note
second_title: Aspose.Note Java API
title: Αποθήκευση του OneNote σε PDF με Κινέζικη αριθμημένη λίστα – Aspose.Note
url: /el/java/onenote-text-manipulation/create-chinese-numbered-list/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση OneNote ως PDF με Κινεζική Αριθμημένη Λίστα – Aspose.Note

## Εισαγωγή
Αν θέλετε να **αποθηκεύσετε το OneNote ως PDF** προσθέτοντας μια κινεζική αριθμημένη λίστα, το Aspose.Note for Java το κάνει εύκολο. Σε αυτό το tutorial, θα σας καθοδηγήσουμε βήμα προς βήμα για τη δημιουργία ενός κινεζικού στυλ διάρθρωσης, την εφαρμογή αρίθμησης και την εξαγωγή του εγγράφου OneNote σε PDF. Στο τέλος, θα κατανοήσετε **πώς να προσθέσετε αρίθμηση**, **πώς να προσθέσετε διάρθρωση στο OneNote**, και θα δείτε γιατί το **Aspose.Note Java** είναι η προτιμώμενη βιβλιοθήκη για αυτήν την εργασία.

## Γρήγορες Απαντήσεις
- **Τι καλύπτει αυτό το tutorial;** Δημιουργία μιας κινεζικής αριθμημένης λίστας στο OneNote και αποθήκευση της ως PDF με το Aspose.Note for Java.  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποια IDE υποστηρίζονται;** Οποιοδήποτε Java IDE όπως Eclipse, IntelliJ IDEA ή NetBeans.  
- **Μπορώ να προσαρμόσω το στυλ της λίστας;** Ναι – η γραμματοσειρά, το μέγεθος, το χρώμα και η μορφή αρίθμησης είναι πλήρως ρυθμιζόμενα.  
- **Πόσο χρόνο παίρνει η υλοποίηση;** Περίπου 10‑15 λεπτά για μια βασική λίστα.

## Τι είναι η “αποθήκευση OneNote ως PDF”;
Η αποθήκευση του OneNote ως PDF μετατρέπει τη διαδραστική σελίδα του σημειωματάριου σε ένα στατικό, ευρέως συμβατό έγγραφο. Αυτό είναι χρήσιμο για κοινή χρήση, αρχειοθέτηση ή εκτύπωση, διατηρώντας την αρχική διάταξη και τυχόν προσαρμοσμένη αρίθμηση που εφαρμόσατε.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για Java;
Το Aspose.Note παρέχει ένα πλούσιο, υψηλής απόδοσης API που σας επιτρέπει να δημιουργείτε προγραμματιστικά δομές OneNote, να εφαρμόζετε σύνθετη αρίθμηση (συμπεριλαμβανομένης της κινεζικής αρίθμησης) και να εξάγετε απευθείας σε PDF χωρίς χειροκίνητα βήματα UI. Λειτουργεί σε πολλαπλές πλατφόρμες, δεν απαιτεί εγκατάσταση Office και υποστηρίζει πλήρη έλεγχο στυλ.

## Προαπαιτούμενα
1. **Περιβάλλον Ανάπτυξης Java** – JDK 8+ και το αγαπημένο σας IDE.  
2. **Βιβλιοθήκη Aspose.Note** – Κατεβάστε το τελευταίο JAR από την επίσημη ιστοσελίδα [here](https://releases.aspose.com/note/java/).  
3. **Βασική εξοικείωση** με τη σύνταξη της Java και τις αντικειμενοστραφείς έννοιες.

## Εισαγωγή Πακέτων
Ξεκινήστε εισάγοντας τα απαραίτητα πακέτα στο έργο Java σας. Αυτές οι εισαγωγές σας δίνουν πρόσβαση σε λειτουργίες δημιουργίας εγγράφου, στυλ και αρίθμησης.

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

Τώρα, ας αναλύσουμε την υλοποίηση βήμα προς βήμα.

## Πώς να αποθηκεύσετε το OneNote ως PDF με Κινεζική Αριθμημένη Λίστα
Παρακάτω υπάρχει ένας λεπτομερής, αριθμημένος οδηγός. Κάθε βήμα περιλαμβάνει μια σύντομη εξήγηση ακολουθούμενη από τον ακριβή κώδικα που πρέπει να αντιγράψετε.

### Βήμα 1: Δημιουργία Αντικειμένου Document
Ξεκινάμε δημιουργώντας μια κενή παρουσία `Document` που θα περιέχει το περιεχόμενο του OneNote.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
```

### Βήμα 2: Αρχικοποίηση Αντικειμένου Page
Μια σελίδα OneNote λειτουργεί ως καμβάς για διαρθρώσεις και άλλα στοιχεία.

```java
// initialize Page class object
Page page = new Page();
```

### Βήμα 3: Αρχικοποίηση Αντικειμένου Outline
Οι διαρθρώσεις είναι τα δοχεία για τα στοιχεία λίστας. Σκεφτείτε τα ως το “κουμπί/αριθμός” που κρατά.

```java
// initialize Outline class object
Outline outline = new Outline();
```

### Βήμα 4: Αρχικοποίηση Αντικειμένου TextStyle
Ορίστε ένα προεπιλεγμένο στυλ παραγράφου που θα εφαρμόζεται σε κάθε στοιχείο λίστας.

```java
// initialize TextStyle class object and set formatting properties
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

### Βήμα 5: Αρχικοποίηση Αντικειμένων OutlineElement και Εφαρμογή Αρίθμησης
Εδώ δημιουργούμε τρία αντικείμενα OutlineElement, το καθένα αντιπροσωπεύει ένα στοιχείο λίστας. Χρησιμοποιούμε `NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10)` για να πάρουμε την κινεζική αρίθμηση (一、二、三…).

```java
// initialize OutlineElement class objects and apply numbering
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement();
outlineElem2.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text2 = new RichText().append("Second");
text2.setParagraphStyle(defaultStyle);
outlineElem2.appendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement();
outlineElem3.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text3 = new RichText().append("Third");
text3.setParagraphStyle(defaultStyle);
outlineElem3.appendChildLast(text3);
```

### Βήμα 6: Προσθήκη Στοιχείων Outline
Συνδέστε κάθε αριθμημένο στοιχείο με το δοχείο της διαρρύθμισης.

```java
// add outline elements
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Βήμα 7: Προσθήκη Κόμβου Outline στη Σελίδα
Τώρα τοποθετούμε ολόκληρη τη διαρρύθμιση στη σελίδα.

```java
// add Outline node
page.appendChildLast(outline);
```

### Βήμα 8: Προσθήκη Κόμβου Σελίδας στο Έγγραφο
Η σελίδα γίνεται μέρος του συνολικού εγγράφου OneNote.

```java
// add Page node
doc.appendChildLast(page);
```

### Βήμα 9: Αποθήκευση του Εγγράφου ως PDF
Τέλος, εξάγουμε το έγγραφο OneNote σε PDF χρησιμοποιώντας τη μέθοδο `save`. Αυτό είναι το βήμα όπου **αποθηκεύουμε το OneNote ως PDF**.

```java
// save the document
doc.save(dataDir + "CreateChineseNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateChineseNumberedList_out.pdf");
```

Η εκτέλεση του παραπάνω κώδικα παράγει ένα αρχείο PDF (`CreateChineseNumberedList_out.pdf`) που περιέχει μια κινεζική αριθμημένη λίστα, ακριβώς όπως θα τη δείτε σε μια σελίδα OneNote.

## Συχνά Προβλήματα και Λύσεις
- **Λάθος μορφή αρίθμησης:** Βεβαιωθείτε ότι χρησιμοποιείτε `NumberFormat.ChineseCounting`. Άλλες μορφές (Αραβική, Ρωμαϊκή) θα παράγουν διαφορετικά αποτελέσματα.  
- **Σφάλμα αρχείου δεν βρέθηκε:** Ελέγξτε ότι το `dataDir` δείχνει σε έναν υπάρχοντα, εγγράψιμο φάκελο.  
- **Λείπει η γραμματοσειρά:** Εάν η καθορισμένη γραμματοσειρά (π.χ., "Arial") δεν είναι εγκατεστημένη στον διακομιστή, το PDF μπορεί να επιστρέψει σε προεπιλεγμένη γραμματοσειρά. Εγκαταστήστε τη γραμματοσειρά ή επιλέξτε άλλη.

## Συχνές Ερωτήσεις

### Είναι το Aspose.Note συμβατό με διαφορετικά Java IDEs;
Ναι, το Aspose.Note είναι συμβατό με δημοφιλή Java IDE όπως το Eclipse και το IntelliJ IDEA.

### Μπορώ να προσαρμόσω τη μορφοποίηση της αριθμημένης λίστας;
Απόλυτα. Όπως φαίνεται στο tutorial, μπορείτε να προσαρμόσετε τη γραμματοσειρά, το χρώμα και το μέγεθος ώστε να καλύψετε τις συγκεκριμένες απαιτήσεις σας.

### Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Note;
Ναι, μπορείτε να εξερευνήσετε τη δοκιμαστική έκδοση [here](https://releases.aspose.com/).

### Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.Note;
Ανατρέξτε στην τεκμηρίωση [here](https://reference.aspose.com/note/java/).

### Πώς μπορώ να λάβω υποστήριξη για το Aspose.Note;
Επισκεφθείτε το φόρουμ υποστήριξης [here](https://forum.aspose.com/c/note/28) για οποιαδήποτε βοήθεια ή ερωτήσεις.

## Πρόσθετες Συχνές Ερωτήσεις (AI‑Optimized)

**Ε: Μπορώ να χρησιμοποιήσω αυτόν τον κώδικα για να προσθέσω αρίθμηση άλλων γλωσσών;**  
Ναι, αντικαταστήστε το `NumberFormat.ChineseCounting` με την κατάλληλη τιμή του enum `NumberFormat` (π.χ., `NumberFormat.RomanUpper`).

**Ε: Διατηρεί το PDF την ιεραρχία της διαρρύθμισης;**  
Το εξαγόμενο PDF διατηρεί την οπτική ιεραρχία, αλλά η διαδραστική πλοήγηση στη διαρρύθμιση δεν είναι διαθέσιμη σε στατικά PDF.

**Ε: Πώς αλλάζω το στυλ της κουκκίδας αντί για αριθμούς;**  
Χρησιμοποιήστε το `NumberList` με μια προσαρμοσμένη συμβολοσειρά μορφής όπως "• " και ορίστε `NumberFormat.None`.

**Ε: Είναι δυνατόν να προσθέσω εικόνες στην ίδια σελίδα;**  
Ναι, μπορείτε να εισάγετε αντικείμενα `Image` στη σελίδα πριν την αποθήκευση σε PDF.

**Ε: Ποια έκδοση του Aspose.Note απαιτείται;**  
Η τελευταία σταθερή έκδοση (ως το 2026) υποστηρίζει όλες τις λειτουργίες που παρουσιάζονται εδώ.

---

**Τελευταία Ενημέρωση:** 2026-03-08  
**Δοκιμάστηκε Με:** Aspose.Note for Java 24.12  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}