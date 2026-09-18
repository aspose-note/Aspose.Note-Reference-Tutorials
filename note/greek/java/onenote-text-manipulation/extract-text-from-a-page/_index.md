---
date: 2026-03-08
description: Μάθετε πώς να εξάγετε κείμενο OneNote από μια σελίδα και να μετατρέψετε
  το OneNote σε κείμενο χρησιμοποιώντας το Aspose.Note για Java. Οδηγός βήμα‑προς‑βήμα
  για την ανάγνωση αρχείων .one σε έργα Java.
linktitle: Extract Text from a Page in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Πώς να εξάγετε κείμενο OneNote από μια σελίδα – Aspose.Note Java
url: /el/java/onenote-text-manipulation/extract-text-from-a-page/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να εξάγετε κείμενο OneNote από μια σελίδα – Aspose.Note Java

## Εισαγωγή
Αν ψάχνετε να **πώς να εξάγετε onenote** περιεχόμενο γρήγορα και αξιόπιστα με Java, βρίσκεστε στο σωστό μέρος. Αυτό το σεμινάριο σας καθοδηγεί στη διαδικασία εξαγωγής κειμένου από μια σελίδα OneNote χρησιμοποιώντας το Aspose.Note for Java, μια βιβλιοθήκη που καθιστά εύκολη την ανάγνωση αρχείων .one, τη μετατροπή του OneNote σε κείμενο και την λήψη του κειμένου της σελίδας OneNote για περαιτέρω επεξεργασία.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη χρησιμοποιεί ο κώδικας;** Aspose.Note for Java.  
- **Ποια μορφή αρχείου διαβάζεται;** Το εγγενές αρχείο `.one` του OneNote.  
- **Πόσες γραμμές κώδικα απαιτούνται;** Περίπου 30 γραμμές σε τέσσερα απλά βήματα.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Μπορώ να το εκτελέσω σε οποιαδήποτε έκδοση Java;** Ναι, υποστηρίζεται οποιοδήποτε runtime Java 8+.

## Τι είναι το “πώς να εξάγετε onenote”;
Η εξαγωγή OneNote σημαίνει προγραμματιστική ανάγνωση του περιεχομένου που αποθηκεύεται μέσα σε ένα σημειωματάριο OneNote (αρχείο .one) και η μετατροπή του σε απλό κείμενο. Αυτό είναι χρήσιμο όταν χρειάζεται να ευρετηριάσετε σημειώσεις, να πραγματοποιήσετε αναζήτηση ή να μεταφέρετε το περιεχόμενο σε άλλα συστήματα.

## Γιατί να χρησιμοποιήσετε το Aspose.Note for Java;
- **Δεν απαιτείται εγκατάσταση Office** – λειτουργεί εξ ολοκλήρου στην πλευρά του διακομιστή.  
- **Πλήρης πιστότητα** – διατηρεί πλούσιο κείμενο, πίνακες και ενσωματωμένα αντικείμενα ενώ παρέχει εξαγωγή απλού κειμένου.  
- **Διαπλατφορμική** – εκτελείται σε Windows, Linux και macOS με το ίδιο API.  

## Προαπαιτούμενα
Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- Βασική κατανόηση του προγραμματισμού Java.  
- Εγκατεστημένο Aspose.Note for Java. Μπορείτε να το κατεβάσετε [εδώ](https://releases.aspose.com/note/java/).  

## Εισαγωγή Πακέτων
Ξεκινήστε εισάγοντας τα απαραίτητα πακέτα στο έργο Java σας για να αξιοποιήσετε τις λειτουργίες του Aspose.Note:

```java
import com.aspose.note.Document;
import com.aspose.note.Node;
import com.aspose.note.NodeType;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import java.util.List;
import java.util.stream.Collectors;
```

Τώρα, ας αναλύσουμε κάθε βήμα λεπτομερώς.

## Βήμα 1: Ορισμός Καταλόγου Εγγράφου
Βεβαιωθείτε ότι έχετε έναν καθορισμένο κατάλογο εγγράφων όπου αποθηκεύεται το αρχείο OneNote. Αντικαταστήστε το `"Your Document Directory"` με την πραγματική διαδρομή.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

## Βήμα 2: Φόρτωση Εγγράφου OneNote
Χρησιμοποιήστε την κλάση `Document` του Aspose.Note για να φορτώσετε το έγγραφο OneNote. Αυτό το βήμα επιδεικνύει τη λειτουργία **read .one file java**.

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

Αντικαταστήστε το `"Sample1.one"` με το όνομα του αρχείου OneNote σας.

## Βήμα 3: Ανάκτηση Κόμβων Σελίδας
Λάβετε τη λίστα των κόμβων σελίδας από το φορτωμένο έγγραφο. Αυτό σας δίνει πρόσβαση σε κάθε σελίδα ώστε να μπορείτε να **get onenote page text** αργότερα.

```java
List<Node> nodes = oneFile.getChildNodes(Node.class);
```

## Βήμα 4: Έλεγχος και Εξαγωγή Κειμένου
Ελέγξτε αν το έγγραφο έχει σελίδες και, αν ναι, ανακτήστε το κείμενο. Εδώ είναι που **extract text from onenote** και μπορεί επίσης να χρησιμοποιηθεί για **convert onenote to text** για επεξεργασία downstream.

```java
if (nodes.size() > 0 && nodes.get(0).getNodeType() == NodeType.Page)
{
    Page page = (Page)nodes.get(0);
    // Retrieve text
    List<RichText> textNodes = (List<RichText>) page.getChildNodes(RichText.class);
    StringBuilder text = new StringBuilder();
    for (RichText richText : textNodes) {
        text = text.append(richText.getText().toString());
    }
    
    // Print text on the output screen
    System.out.println(text);
}
```

Αυτό το απόσπασμα ελέγχει αν ο πρώτος κόμβος είναι σελίδα, εξάγει όλα τα στοιχεία `RichText`, τα συνενώνει και εκτυπώνει το προκύπτον απλό κείμενο.

## Κοινά Προβλήματα και Λύσεις
| Συμπτωμα | Πιθανή Αιτία | Διόρθωση |
|----------|--------------|----------|
| `FileNotFoundException` | Λανθασμένο `dataDir` ή όνομα αρχείου | Επαληθεύστε τη διαδρομή και βεβαιωθείτε ότι το αρχείο `.one` υπάρχει. |
| Δεν εκτυπώθηκε έξοδος | Το έγγραφο δεν έχει σελίδες ή ο δείκτης κόμβου είναι λανθασμένος | Επανάληψη μέσω των `nodes` και έλεγχος του τύπου κάθε κόμβου. |
| Το κείμενο εμφανίζεται παραμορφωμένο | Χρήση παλιάς έκδοσης Aspose.Note | Ενημερώστε στην τελευταία έκδοση Aspose.Note for Java. |

## Συχνές Ερωτήσεις
### Μπορώ να χρησιμοποιήσω το Aspose.Note for Java με άλλες γλώσσες προγραμματισμού;
Το Aspose.Note υποστηρίζει κυρίως Java, αλλά διαθέτει εκδόσεις για άλλες γλώσσες όπως .NET. Ελέγξτε την τεκμηρίωση για τη συμβατότητα γλωσσών.

### Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Note for Java;
Ναι, μπορείτε να εξερευνήσετε μια δωρεάν δοκιμαστική έκδοση [εδώ](https://releases.aspose.com/).

### Πού μπορώ να βρω υποστήριξη για το Aspose.Note for Java;
Επισκεφθείτε το [φόρουμ](https://forum.aspose.com/c/note/28) του Aspose.Note για υποστήριξη κοινότητας και συζητήσεις.

### Πώς μπορώ να αγοράσω το Aspose.Note for Java;
Μπορείτε να αγοράσετε το προϊόν [εδώ](https://purchase.aspose.com/buy).

### Χρειάζομαι προσωρινή άδεια για το Aspose.Note for Java;
Αν χρειάζεστε προσωρινή άδεια, μπορείτε να την αποκτήσετε [εδώ](https://purchase.aspose.com/temporary-license/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Τελευταία Ενημέρωση:** 2026-03-08  
**Δοκιμάστηκε Με:** Aspose.Note for Java 24.10 (latest at time of writing)  
**Συγγραφέας:** Aspose