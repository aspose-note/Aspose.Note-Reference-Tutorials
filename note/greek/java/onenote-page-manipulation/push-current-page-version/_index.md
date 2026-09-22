---
date: 2026-08-08
description: Μάθετε πώς να αποθηκεύσετε την OneNote page version κάνοντας push την
  current page version με το Aspose.Note για Java. Περιλαμβάνει τη φόρτωση ενός OneNote
  αρχείου, την προσθήκη history, cloning μιας σελίδας, και updating του version history.
keywords:
- save onenote page version
- add history to onenote
- version control for onenote
lastmod: 2026-08-08
linktitle: Push Current Page Version στο OneNote - Aspose.Note
og_description: Αποθηκεύστε την OneNote page version με το Aspose.Note για Java. Αυτός
  ο οδηγός δείχνει πώς να προσθέσετε history στο OneNote, να κάνετε push την current
  page version, και να διατηρήσετε version control για OneNote αρχεία.
og_image_alt: Developer guide showing how to push a OneNote page version with Aspose.Note
  for Java
og_title: Αποθήκευση OneNote page version – push current page version χρησιμοποιώντας
  Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to save OneNote page version by pushing the current page
    version with Aspose.Note for Java. Includes loading a OneNote file, adding history,
    cloning a page, and updating version history.
  headline: How to save OneNote page version – push current page version in OneNote
    - Aspose.Note
  type: TechArticle
- description: Learn how to save OneNote page version by pushing the current page
    version with Aspose.Note for Java. Includes loading a OneNote file, adding history,
    cloning a page, and updating version history.
  name: How to save OneNote page version – push current page version in OneNote -
    Aspose.Note
  steps:
  - name: Basic knowledge of Java programming.
    text: Basic knowledge of Java programming.
  - name: Java Development Kit (JDK) installed on your machine.
    text: Java Development Kit (JDK) installed on your machine.
  - name: Aspose.Note for Java library – download it from the [Aspose.Note for Java
      release page](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download it from the [Aspose.Note for Java
      release page](https://releases.aspose.com/note/java/).
  - name: A sample OneNote document (e.g., `Sample1.one`) that you want to version.
    text: A sample OneNote document (e.g., `Sample1.one`) that you want to version.
  type: HowTo
- questions:
  - answer: Yes, the library supports opening both encrypted and unencrypted OneNote
      documents.
    question: Can I use Aspose.Note for Java with encrypted OneNote files?
  - answer: Aspose.Note strives to stay compatible with the newest OneNote file formats,
      including the 2023‑02 release.
    question: Is the API compatible with the latest OneNote releases?
  - answer: Absolutely. Edit the page content first, then push a new version to capture
      the changes.
    question: Can I manipulate text and images while versioning?
  - answer: Yes, you can convert to PDF, HTML, or image formats directly from the
      API.
    question: Does Aspose.Note allow conversion of OneNote files to other formats?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      community assistance or contact Aspose support.
    question: Where can I get help if I run into issues?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- save onenote page version
- Aspose.Note
- java onenote versioning
title: Πώς να αποθηκεύσετε την OneNote page version – push current page version στο
  OneNote - Aspose.Note
url: /el/java/onenote-page-manipulation/push-current-page-version/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να αποθηκεύσετε την έκδοση σελίδας OneNote – προώθηση τρέχουσας έκδοσης σελίδας στο OneNote

Σε αυτό το tutorial θα μάθετε **πώς να αποθηκεύσετε την έκδοση σελίδας OneNote** προωθώντας την τρέχουσα έκδοση σελίδας χρησιμοποιώντας το Aspose.Note for Java. Είτε χρειάζεστε ένα ίχνος ελέγχου για συμμόρφωση, ένα συνεργατικό ιστορικό επεξεργασιών, ή μια αξιόπιστη στρατηγική αντιγράφων ασφαλείας, τα παρακάτω βήματα σας καθοδηγούν στη φόρτωση ενός αρχείου OneNote, την προσθήκη καταχωρήσεων ιστορικού, την κλωνοποίηση της σελίδας και την αποθήκευση της ενημερωμένης έκδοσης προγραμματιστικά.

## Γρήγορες απαντήσεις
- **Τι σημαίνει “προώθηση τρέχουσας έκδοσης σελίδας”;** Προσθέτει ένα στιγμιότυπο της ενεργής σελίδας στο ιστορικό εκδόσεων του εγγράφου, δημιουργώντας μια νέα αμετάβλητη καταχώρηση.  
- **Γιατί να χρησιμοποιήσετε το Aspose.Note for Java;** Η βιβλιοθήκη προσφέρει ένα καθαρό Java API που λειτουργεί χωρίς το Microsoft Office, υποστηρίζοντας πάνω από 50 δυνατότητες του OneNote έτοιμες για χρήση.  
- **Χρειάζομαι άδεια για να το δοκιμάσω;** Διατίθεται δωρεάν δοκιμή, αλλά απαιτείται εμπορική άδεια για παραγωγικές εγκαταστάσεις.  
- **Μπορώ να αυτοματοποιήσω την έκδοση για πολλές σελίδες;** Ναι—πραγματοποιήστε βρόχο μέσω των σελίδων του εγγράφου και καλέστε το ίδιο API για καθεμία.  
- **Είναι το αποθηκευμένο αρχείο συμβατό με το τελευταίο OneNote;** Το Aspose.Note διατηρεί τη συμβατότητα με την τρέχουσα μορφή αρχείου OneNote (έκδοση 2023‑02 και μεταγενέστερη).

## Τι είναι η αποθήκευση έκδοσης σελίδας OneNote;
Η αποθήκευση έκδοσης σελίδας OneNote σημαίνει την αποθήκευση ενός στιγμιότυπου μόνο για ανάγνωση της σελίδας σε συγκεκριμένη χρονική στιγμή, ώστε να μπορείτε αργότερα να δείτε ή να επαναφέρετε αυτήν την ακριβή κατάσταση. Η κλάση `PageHistory` του Aspose.Note καταγράφει κάθε στιγμιότυπο ως ξεχωριστή καταχώρηση έκδοσης. Κάθε καταχώρηση είναι αμετάβλητη και μπορεί να προσπελαστεί αργότερα μέσω του UI του OneNote.

## Γιατί να προωθήσετε την τρέχουσα έκδοση σελίδας;
Η προώθηση της τρέχουσας έκδοσης σελίδας δημιουργεί μια αμετάβλητη εγγραφή του περιεχομένου της σελίδας τη στιγμή που καλείτε το API. Αυτό επιτρέπει **ελεγχόμενη καταγραφή** (παρακολούθηση ποιος άλλαξε τι και πότε), **διαφάνεια συνεργασίας** (τα μέλη της ομάδας βλέπουν μια σαφή χρονογραμμή επεξεργασιών) και **ασφάλεια δεδομένων** (τα τυχαία αντικαταστάσεις μπορούν να επαναφερθούν αμέσως).

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε:

1. Βασικές γνώσεις προγραμματισμού Java.  
2. Εγκατεστημένο Java Development Kit (JDK) στον υπολογιστή σας.  
3. Βιβλιοθήκη Aspose.Note for Java – κατεβάστε την από τη [Aspose.Note for Java release page](https://releases.aspose.com/note/java/).  
4. Ένα δείγμα εγγράφου OneNote (π.χ., `Sample1.one`) που θέλετε να εκδοποιήσετε.

## Εισαγωγή πακέτων

Η κλάση `Document` αντιπροσωπεύει ένα αρχείο OneNote στη μνήμη, ενώ η `PageHistory` διαχειρίζεται τις καταχωρήσεις εκδόσεων για κάθε σελίδα. Εισάγετε τους απαιτούμενους χώρους ονομάτων πριν αρχίσετε να εργάζεστε με το API.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Βήμα 1: Φόρτωση του εγγράφου OneNote

Η φόρτωση του αρχείου OneNote είναι το πρώτο βήμα στο **πώς να προσθέσετε ιστορικό**. Το API διαβάζει το αρχείο `.one` σε ένα αντικείμενο `Document`, παρέχοντάς σας πλήρη προγραμματιστική πρόσβαση σε σελίδες, ενότητες και μεταδεδομένα.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

> **Συμβουλή:** Το `dataDir` πρέπει να δείχνει στο φάκελο που περιέχει το αρχείο OneNote. Προσαρμόστε το όνομα του αρχείου εάν εργάζεστε με διαφορετικό έγγραφο.

## Βήμα 2: Λήψη της τρέχουσας σελίδας και του ιστορικού της

Για να διαχειριστείτε το ιστορικό εκδόσεων χρειάζεστε μια αναφορά στη σελίδα που θέλετε να εκδοποιήσετε και το σχετικό αντικείμενο `PageHistory`. Η μέθοδος `getFirstChild()` ανακτά την πρώτη σελίδα, και το `getPageHistory(page)` επιστρέφει το δοχείο όπου αποθηκεύονται τα στιγμιότυπα.

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

> **Γιατί είναι σημαντικό:** Το `PageHistory` περιέχει μια λίστα από αντικείμενα `PageVersion`; κάθε έκδοση είναι ένα βαθύ αντίγραφο της σελίδας τη στιγμή που προωθήθηκε.

## Βήμα 3: Προώθηση της τρέχουσας έκδοσης σελίδας

Τώρα θα **πώς να κλωνοποιήσετε τη σελίδα** και να την προωθήσετε στο ιστορικό. Η κλωνοποίηση δημιουργεί ένα βαθύ αντίγραφο, διασφαλίζοντας ότι το στιγμιότυπο είναι ανεξάρτητο από μελλοντικές επεξεργασίες. Χρησιμοποιήστε το `deepClone()` για να καταγράψετε όλα τα ενσωματωμένα στοιχεία όπως κείμενο, εικόνες και πίνακες.

```java
pageHistory.addItem(page.deepClone());
```

> **Επαγγελματική συμβουλή:** Η χρήση του `deepClone()` εγγυάται ότι όλα τα ενσωματωμένα στοιχεία (κείμενο, εικόνες, πίνακες) καταγράφονται στην καταχώρηση έκδοσης, αποτρέποντας μελλοντικές τροποποιήσεις να επηρεάσουν το αποθηκευμένο στιγμιότυπο.

## Βήμα 4: Αποθήκευση του εγγράφου

Τέλος, **ενημερώστε την έκδοση OneNote** αποθηκεύοντας το έγγραφο. Η μέθοδος `save()` γράφει το Document σε καθορισμένη διαδρομή αρχείου στο δίσκο.

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

Όταν ανοίξετε το `PushCurrentPageVersion_out.one` στο OneNote, θα δείτε το ιστορικό εκδόσεων προσβάσιμο μέσω του πίνακα **History** του UI.

## Συνηθισμένα προβλήματα & πώς να τα αποφύγετε

- **Έλλειψη δικαιωμάτων εγγραφής:** Βεβαιωθείτε ότι ο φάκελος εξόδου είναι εγγράψιμος· διαφορετικά το `save()` θα ρίξει εξαίρεση.  
- **Λάθος διαδρομή αρχείου:** Ελέγξτε ξανά ότι το `dataDir` τελειώνει με διαχωριστικό διαδρομής (`/` ή `\`).  
- **Μεγάλα έγγραφα:** Για αρχεία OneNote με εκατοντάδες σελίδες, σκεφτείτε να κλωνοποιήσετε μόνο τις σελίδες που χρειάζεστε για έκδοση, ώστε να μειώσετε την κατανάλωση μνήμης και να βελτιώσετε την απόδοση.

## Συμπέρασμα

Τώρα γνωρίζετε **πώς να αποθηκεύσετε την έκδοση σελίδας OneNote** προωθώντας την τρέχουσα έκδοση σελίδας, προσθέτοντας ουσιαστικά **ιστορικό στο OneNote** και ενεργοποιώντας ισχυρό **έλεγχο εκδόσεων για το OneNote** χρησιμοποιώντας το Aspose.Note for Java. Αυτό το πρότυπο μπορεί να ενσωματωθεί σε αυτοματοποιημένες γραμμές αναφοράς, λύσεις αντιγράφων ασφαλείας ή εργαλεία συνεργατικής επεξεργασίας, παρέχοντάς σας ακριβή έλεγχο της εξέλιξης του εγγράφου.

## Συχνές ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω το Aspose.Note for Java με κρυπτογραφημένα αρχεία OneNote;**  
A: Ναι, η βιβλιοθήκη υποστηρίζει το άνοιγμα τόσο κρυπτογραφημένων όσο και μη κρυπτογραφημένων εγγράφων OneNote.

**Q: Είναι το API συμβατό με τις τελευταίες εκδόσεις του OneNote;**  
A: Το Aspose.Note προσπαθεί να παραμείνει συμβατό με τις πιο πρόσφατες μορφές αρχείων OneNote, συμπεριλαμβανομένης της έκδοσης 2023‑02.

**Q: Μπορώ να χειριστώ κείμενο και εικόνες κατά τη διάρκεια της έκδοσης;**  
A: Απόλυτα. Επεξεργαστείτε πρώτα το περιεχόμενο της σελίδας, στη συνέχεια προωθήστε μια νέα έκδοση για να καταγράψετε τις αλλαγές.

**Q: Επιτρέπει το Aspose.Note τη μετατροπή αρχείων OneNote σε άλλες μορφές;**  
A: Ναι, μπορείτε να μετατρέψετε σε PDF, HTML ή μορφές εικόνας απευθείας από το API.

**Q: Πού μπορώ να λάβω βοήθεια εάν αντιμετωπίσω προβλήματα;**  
A: Επισκεφθείτε το [Aspose.Note forum](https://forum.aspose.com/c/note/28) για βοήθεια από την κοινότητα ή επικοινωνήστε με την υποστήριξη της Aspose.

---

**Τελευταία ενημέρωση:** 2026-08-08  
**Δοκιμάστηκε με:** Aspose.Note for Java 24.11  
**Συγγραφέας:** Aspose

## Σχετικά Tutorials

- [How to modify onenote page history with Aspose.Note](/note/java/onenote-page-manipulation/modify-page-history/)
- [Change OneNote Page Background – Aspose.Note for Java](/note/java/onenote-page-manipulation/set-page-background-color/)
- [Aspose Note Java: OneNote Document Manipulation](/note/java/onenote-document-saving/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}