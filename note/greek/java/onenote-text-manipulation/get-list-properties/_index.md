---
date: 2026-03-08
description: Μάθετε πώς να εξάγετε τις ιδιότητες λιστών από έγγραφα OneNote χρησιμοποιώντας
  το Aspose.Note για Java. Αυτός ο οδηγός βήμα‑βήμα σας δείχνει τον ακριβή κώδικα
  και τις συμβουλές που χρειάζεστε.
linktitle: How to Extract List Properties in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Πώς να εξάγετε τις ιδιότητες λίστας στο OneNote - Aspose.Note
url: /el/java/onenote-text-manipulation/get-list-properties/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να εξάγετε ιδιότητες λίστας στο OneNote - Aspose.Note

## Εισαγωγή
Σε αυτό το **tutorial** θα ανακαλύψετε **πώς να εξάγετε λίστα** ιδιότητες από ένα αρχείο OneNote με το Aspose.Note για Java. Είτε χρειάζεστε να διαβάσετε λεπτομέρειες γραμματοσειράς, μορφοποίηση λίστας ή χαρακτηριστικά στυλ, αυτός ο οδηγός σας καθοδηγεί βήμα προς βήμα—από τη φόρτωση του εγγράφου μέχρι την εκτύπωση των εξαγόμενων τιμών. Στο τέλος, θα έχετε ένα έτοιμο κομμάτι κώδικα που μπορεί να ενσωματωθεί σε οποιοδήποτε pipeline επεξεργασίας εγγράφων βασισμένο σε Java.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “extract list”;** Σημαίνει την ανάγνωση των λεπτομερειών μορφοποίησης (γραμματοσειρά, μέγεθος, χρώμα, στυλ) των αριθμημένων ή κουκίδων λιστών που αποθηκεύονται σε ένα περίγραμμα OneNote.  
- **Ποια βιβλιοθήκη απαιτείται;** Aspose.Note for Java (τελευταία έκδοση).  
- **Χρειάζομαι άδεια για δοκιμή;** Ναι, συνιστάται προσωρινή άδεια για μη‑παραγωγικές εκτελέσεις.  
- **Μπορώ να το τρέξω σε οποιοδήποτε OS;** Το Java API λειτουργεί σε Windows, Linux και macOS.  
- **Πόσο χρόνο διαρκεί η υλοποίηση;** Συνήθως λιγότερο από 10 λεπτά για μια βασική ρύθμιση.

## Τι είναι το “πώς να εξάγετε λίστα” στο πλαίσιο του OneNote;
Το OneNote αποθηκεύει κάθε στοιχείο λίστας ως `OutlineElement` που μπορεί να περιέχει ένα αντικείμενο `NumberList`. Η εξαγωγή της λίστας σημαίνει την πρόσβαση στις ιδιότητες αυτού του αντικειμένου—όπως όνομα γραμματοσειράς, μέγεθος, χρώμα και μορφοποίηση—ώστε να μπορείτε να τα αναλύσετε ή να τα τροποποιήσετε προγραμματιστικά.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για Java για την εξαγωγή ιδιοτήτων λίστας;
- **Χωρίς COM interop** – Λειτουργεί πλήρως σε Java χωρίς την ανάγκη του πελάτη Windows OneNote.  
- **Πλήρης πιστότητα** – Διατηρεί όλες τις λεπτομέρειες μορφοποίησης, συμπεριλαμβανομένων προσαρμοσμένων γραμματοσειρών και χρωμάτων.  
- **Δια-πλατφόρμα** – Εκτελεί τον ίδιο κώδικα σε οποιοδήποτε περιβάλλον διακομιστή.  
- **Πλούσιο API** – Παρέχει άμεση πρόσβαση σε αντικείμενα λίστας, καθιστώντας την εξαγωγή ιδιοτήτων απλή.

## Προαπαιτούμενα
Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε τα εξής:

- Aspose.Note for Java: Κατεβάστε την τελευταία έκδοση **[εδώ](https://releases.aspose.com/note/java/)**.  
- Ένα περιβάλλον ανάπτυξης Java (JDK 8 ή νεότερο).  
- Ένα έγγραφο OneNote (π.χ., `Sample1.one`) τοποθετημένο σε γνωστό φάκελο.

## Εισαγωγή Πακέτων
Αρχικά, εισάγετε τις κλάσεις που θα χρειαστείτε. Αυτό σας δίνει πρόσβαση στη βασική λειτουργικότητα του Aspose.Note.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.OutlineElement;
```

Τώρα ας περάσουμε από την υλοποίηση βήμα προς βήμα.

## Πώς να εξάγετε ιδιότητες λίστας – Οδηγός βήμα‑βήμα

### Βήμα 1: Φόρτωση του εγγράφου OneNote
Δώστε τη σωστή διαδρομή προς το αρχείο `.one` και δημιουργήστε μια παρουσία `Document`.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Συμβουλή:** Χρησιμοποιήστε απόλυτες διαδρομές ή ρυθμίστε μια σχετική διαδρομή βάσει του φακέλου πόρων του έργου σας για να αποφύγετε το `FileNotFoundException`.

### Βήμα 2: Ανάκτηση της συλλογής κόμβων περιγράμματος
Κάθε λίστα βρίσκεται μέσα σε ένα `OutlineElement`. Αντλήστε όλα τα τέτοια στοιχεία από το έγγραφο.

```java
// Retrieve a collection of nodes of the outline element
List<OutlineElement> nodes = oneFile.getChildNodes(OutlineElement.class);
```

### Βήμα 3: Επανάληψη στους κόμβους και εντοπισμός λιστών
Κάντε επανάληψη σε κάθε κόμβο, ελέγχοντας αν περιέχει ένα `NumberList`. Όταν το βρείτε, αποθηκεύστε την αναφορά για μεταγενέστερη εξαγωγή.

```java
// Iterate through each node
for (OutlineElement node : nodes) {
    if (node.getNumberList() != null) {
        NumberList list = node.getNumberList();
        // Continue with further operations on list properties
    }
}
```

### Βήμα 4: Εξαγωγή των επιθυμητών ιδιοτήτων λίστας
Μέσα στον βρόχο, μπορείτε τώρα να διαβάσετε οποιοδήποτε χαρακτηριστικό εκτίθεται από την κλάση `NumberList`.

```java
// Retrieve font name
System.out.println("Font Name: " + list.getFont());
// Retrieve font length (character count)
System.out.println("Font Length: " + list.getFont());
// Retrieve font size
System.out.println("Font Size: " + list.getFontSize());
// Retrieve font color
System.out.println("Font Color: " + list.getFontColor());
// Retrieve format (e.g., decimal, lowerLetter)
System.out.println("Font format: " + list.getFormat());
// Check bold style
System.out.println("Is bold: " + list.isBold());
// Check italic style
System.out.println("Is italic: " + list.isItalic());
```

Η έξοδος της κονσόλας θα εμφανίσει κάθε ιδιότητα, επιτρέποντάς σας να την καταγράψετε, αναλύσετε ή επεξεργαστείτε περαιτέρω τις πληροφορίες στυλ της λίστας.

## Συχνά Προβλήματα & Αντιμετώπιση
| Συμπτωμα | Πιθανή Αιτία | Διόρθωση |
|----------|--------------|----------|
| `NullPointerException` στο `list.getFont()` | Ο κόμβος δεν περιέχει `NumberList`. | Προσθέστε έλεγχο null (`if (node.getNumberList() != null)`). |
| Δεν εμφανίζεται έξοδος | Το `dataDir` δείχνει σε λάθος φάκελο. | Επαληθεύστε τη διαδρομή και βεβαιωθείτε ότι το `Sample1.one` υπάρχει. |
| Το χρώμα γραμματοσειράς εμφανίζεται ως `null` | Η λίστα χρησιμοποιεί το προεπιλεγμένο χρώμα θέματος. | Χρησιμοποιήστε `list.getFontColor()` με εναλλακτική λύση στο θέμα του εγγράφου. |

## Συχνές Ερωτήσεις

**Ε: Είναι το Aspose.Note συμβατό με διαφορετικές εκδόσεις του OneNote;**  
Α: Ναι, το Aspose.Note υποστηρίζει μια ευρεία γκάμα μορφών αρχείων OneNote, από παλαιότερες εκδόσεις 2007 μέχρι τις πιο πρόσφατες εκδόσεις του Office 365.

**Ε: Μπορώ να προσαρμόσω ποιες ιδιότητες γραμματοσειράς θα ανακτηθούν;**  
Α: Απόλυτα. Μπορείτε να καλέσετε μόνο τα getters που χρειάζεστε (π.χ., `getFontSize()` ή `isBold()`) και να αγνοήσετε τα υπόλοιπα.

**Ε: Πού μπορώ να βρω πρόσθετη υποστήριξη ή βοήθεια;**  
Α: Για οποιεσδήποτε ερωτήσεις ή προβλήματα, επισκεφθείτε το [φόρουμ Aspose.Note](https://forum.aspose.com/c/note/28) για άμεση βοήθεια.

**Ε: Χρειάζομαι προσωρινή άδεια για δοκιμή;**  
Α: Ναι, μπορείτε να αποκτήσετε μια προσωρινή άδεια **[εδώ](https://purchase.aspose.com/temporary-license/)** για σκοπούς αξιολόγησης.

**Ε: Τι κάνω αν θέλω να αγοράσω το Aspose.Note για Java;**  
Α: Μπορείτε να αγοράσετε το προϊόν **[εδώ](https://purchase.aspose.com/buy)** για να ξεκλειδώσετε το πλήρες δυναμικό του στα έργα σας.

**Τελευταία ενημέρωση:** 2026-03-08  
**Δοκιμή με:** Aspose.Note for Java (τελευταία έκδοση)  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}