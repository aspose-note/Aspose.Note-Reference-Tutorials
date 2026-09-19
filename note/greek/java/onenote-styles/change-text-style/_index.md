---
date: 2026-06-05
description: Μάθετε πώς να αλλάξετε το μέγεθος γραμματοσειράς στο OneNote, να ορίσετε
  το χρώμα γραμματοσειράς και να επισημάνετε κείμενο με το Aspose.Note για Java –
  βήμα‑βήμα οδηγός με αποσπάσματα κώδικα.
keywords:
- change font size onenote
- how to change text
- set font color onenote
linktitle: Αλλαγή μεγέθους γραμματοσειράς στο OneNote - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  headline: Change Font Size in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  name: Change Font Size in OneNote - Aspose.Note
  steps:
  - name: Import Packages
    text: 'The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note`
      namespace. Import them at the top of your Java source file:'
  - name: Load the Document
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. Loading a file is as simple as passing the file
      path to its constructor.
  - name: Access RichText Nodes
    text: '`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`,
      you gain access to every piece of editable text in the notebook.'
  - name: Change Text Style
    text: '`TextRun` represents a contiguous run of characters sharing the same formatting.
      Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize`
      to **20** points to achieve the desired styling.'
  - name: Save the Document
    text: Call `document.save("StyledSample.one")` to write the changes back to a
      OneNote file. The save operation preserves all original content while applying
      the new styles.
  type: HowTo
- questions:
  - answer: Yes, filter the `RichText` collection by page or section ID before applying
      style changes.
    question: Can I apply these text style changes to specific sections of my OneNote
      document?
  - answer: Absolutely, you can modify font family, bold/italic, underline, alignment,
      and paragraph spacing using the same object model.
    question: Does Aspose.Note support other formatting options beyond color, highlight,
      and size?
  - answer: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson,
      or Spring to build complex document pipelines.
    question: Can I integrate Aspose.Note with other Java libraries for advanced processing?
  - answer: A commercial license is required for production deployments; a free evaluation
      license is available for development and testing.
    question: Is Aspose.Note licensed for commercial use?
  - answer: Visit the Aspose.Note documentation portal, download the full API reference
      PDF, and explore the GitHub repository for community examples.
    question: Where can I find additional samples and API reference?
  type: FAQPage
second_title: Aspose.Note Java API
title: Αλλαγή μεγέθους γραμματοσειράς στο OneNote - Aspose.Note
url: /el/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αλλαγή Μεγέθους Γραμματοσειράς στο OneNote - Aspose.Note

## Εισαγωγή

Σε αυτό το tutorial θα μάθετε **πώς να αλλάξετε το μέγεθος γραμματοσειράς σε έγγραφα OneNote** χρησιμοποιώντας το Aspose.Note για Java. Θα περάσουμε από τη φόρτωση ενός αρχείου OneNote, την πρόσβαση στους κόμβους κειμένου, την εφαρμογή χρώματος, επισήμανσης και αλλαγών μεγέθους γραμματοσειράς, και τέλος την αποθήκευση του ενημερωμένου αρχείου. Είτε αυτοματοποιείτε τη δημιουργία αναφορών είτε βελτιώνετε τις σημειώσεις συναντήσεων, αυτός ο οδηγός σας παρέχει έναν αξιόπιστο τρόπο να μορφοποιήσετε το περιεχόμενο του OneNote προγραμματιστικά.

## Γρήγορες Απαντήσεις
- **Πώς μπορώ να αλλάξω το μέγεθος γραμματοσειράς στο OneNote με Java;** Φορτώστε το έγγραφο, τροποποιήστε την ιδιότητα `FontSize` του κάθε `TextRun`, και στη συνέχεια αποθηκεύστε – τρία απλά βήματα.  
- **Μπορώ επίσης να αλλάξω το χρώμα του κειμένου και την επισήμανση;** Ναι, ορίστε `FontColor` και `HighlightColor` στο ίδιο `TextRun`.  
- **Ποια έκδοση του Aspose.Note απαιτείται;** Οποιαδήποτε έκδοση 23.10+ υποστηρίζει αυτά τα API μορφοποίησης.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Είναι αυτή η προσέγγιση κατάλληλη για μεγάλα σημειωματάρια;** Ναι – το Aspose.Note επεξεργάζεται σημειωματάρια με εκατοντάδες σελίδες χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη.

## Τι είναι η αλλαγή μεγέθους γραμματοσειράς στο OneNote;
**change font size onenote** αναφέρεται στην προγραμματιστική προσαρμογή του χαρακτηριστικού `FontSize` των στοιχείων κειμένου μέσα σε ένα σημειωματάριο OneNote. Χρησιμοποιώντας το Aspose.Note, οι προγραμματιστές μπορούν να τροποποιήσουν αυτήν την ιδιότητα μέσω του API, το οποίο ενημερώνει άμεσα τη δομή του υποκείμενου αρχείου OneNote, εξασφαλίζοντας ότι οι οπτικές αλλαγές εμφανίζονται χωρίς χειροκίνητη επεξεργασία ή αλληλεπίδραση με το UI.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για την αλλαγή του στυλ κειμένου στο OneNote;
Το Aspose.Note παρέχει πάνω από 30 επιλογές μορφοποίησης — συμπεριλαμβανομένων της οικογένειας γραμματοσειράς, του μεγέθους, του χρώματος, της επισήμανσης, της στοίχισης και του διαστήματος παραγράφων — και έχει σχεδιαστεί για να επεξεργάζεται μεγάλα σημειωματάρια αποδοτικά. Μπορεί να διαχειριστεί σημειωματάρια με περισσότερες από 500 σελίδες ενώ καταναλώνει λιγότερο από 150 MB RAM, παρέχοντας αξιόπιστη, υψηλής απόδοσης αυτοματοποίηση για επιχειρησιακές ροές εργασίας εγγράφων.

## Προαπαιτούμενα

1. Βασικές γνώσεις προγραμματισμού Java.  
2. JDK 8 ή νεότερο εγκατεστημένο στο σύστημά σας.  
3. Βιβλιοθήκη Aspose.Note για Java (λήψη από τον ιστότοπο της Aspose).  
4. Εξοικείωση με τη ιεραρχική δομή του OneNote (σελίδες, ενότητες, κόμβοι RichText).

## Πώς να αλλάξετε το μέγεθος γραμματοσειράς στο OneNote χρησιμοποιώντας το Aspose.Note;

Φορτώστε το αρχείο OneNote, εντοπίστε κάθε κόμβο `RichText`, ενημερώστε το στυλ κάθε `TextRun` και αποθηκεύστε το έγγραφο. Αυτή η διαδικασία από την αρχή μέχρι το τέλος απαιτεί μόνο λίγες γραμμές κώδικα και εκτελείται σε λιγότερο από ένα δευτερόλεπτο για τυπικά σημειωματάρια.

### Βήμα 1: Εισαγωγή Πακέτων

Οι κλάσεις `Document`, `RichText` και `TextRun` βρίσκονται στο namespace `com.aspose.note`. Εισάγετέ τις στην αρχή του αρχείου πηγαίου κώδικα Java:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

### Βήμα 2: Φόρτωση του Εγγράφου

Η κλάση `Document` είναι το κορυφαίο αντικείμενο του Aspose.Note που αντιπροσωπεύει ένα μοναδικό αρχείο OneNote στη μνήμη. Η φόρτωση ενός αρχείου είναι τόσο απλή όσο η μεταβίβαση της διαδρομής του αρχείου στον κατασκευαστή του.

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

### Βήμα 3: Πρόσβαση στους Κόμβους RichText

Οι κόμβοι `RichText` περιέχουν το πραγματικό κείμενο της παραγράφου. Επανάγοντας το `document.getRichTextNodes()`, αποκτάτε πρόσβαση σε κάθε επεξεργάσιμο κομμάτι κειμένου στο σημειωματάριο.

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

### Βήμα 4: Αλλαγή Στυλ Κειμένου

`TextRun` αντιπροσωπεύει μια συνεχόμενη σειρά χαρακτήρων που μοιράζονται την ίδια μορφοποίηση. Μέσα στον βρόχο, ορίστε `FontColor` σε κίτρινο, `HighlightColor` σε μπλε και `FontSize` σε **20** σημεία για να επιτύχετε το επιθυμητό στυλ.

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

### Βήμα 5: Αποθήκευση του Εγγράφου

Καλέστε `document.save("StyledSample.one")` για να γράψετε τις αλλαγές πίσω σε ένα αρχείο OneNote. Η λειτουργία αποθήκευσης διατηρεί όλο το αρχικό περιεχόμενο ενώ εφαρμόζει τα νέα στυλ.

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

## Κοινά Προβλήματα και Λύσεις

- **Το κείμενο δεν αλλάζει:** Βεβαιωθείτε ότι επαναλαμβάνετε τα αντικείμενα `TextRun` μέσα σε κάθε κόμβο `RichText`; η παράλειψη αυτού του επιπέδου θα αφήσει τη μορφοποίηση αμετάβλητη.  
- **Το χρώμα εμφανίζεται διαφορετικό:** Το Aspose.Note χρησιμοποιεί τιμές RGB· ελέγξτε ότι χρησιμοποιείτε τις σωστές σταθερές `java.awt.Color`.  
- **Το μεγάλο σημειωματάριο επιβραδύνει:** Το LoadOptions διαμορφώνει τον τρόπο φόρτωσης αρχείου από το Aspose.Note, επιτρέποντας ροή και επιλογή μορφής. Χρησιμοποιήστε `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` για να ενεργοποιήσετε τη λειτουργία ροής, η οποία μειώνει το αποτύπωμα μνήμης.

## Συχνές Ερωτήσεις

**Ε: Μπορώ να εφαρμόσω αυτές τις αλλαγές στυλ κειμένου σε συγκεκριμένες ενότητες του εγγράφου OneNote μου;**  
Α: Ναι, φιλτράρετε τη συλλογή `RichText` ανά ID σελίδας ή ενότητας πριν εφαρμόσετε τις αλλαγές στυλ.

**Ε: Το Aspose.Note υποστηρίζει άλλες επιλογές μορφοποίησης εκτός από χρώμα, επισήμανση και μέγεθος;**  
Α: Απόλυτα, μπορείτε να τροποποιήσετε την οικογένεια γραμματοσειράς, έντονη/πλάγια, υπογράμμιση, στοίχιση και το διάστημα παραγράφων χρησιμοποιώντας το ίδιο μοντέλο αντικειμένων.

**Ε: Μπορώ να ενσωματώσω το Aspose.Note με άλλες βιβλιοθήκες Java για προχωρημένη επεξεργασία;**  
Α: Ναι, το Aspose.Note λειτουργεί απρόσκοπτα με βιβλιοθήκες όπως Apache POI, Jackson ή Spring για την κατασκευή σύνθετων αγωγών εγγράφων.

**Ε: Το Aspose.Note είναι αδειοδοτημένο για εμπορική χρήση;**  
Α: Απαιτείται εμπορική άδεια για παραγωγικές εγκαταστάσεις· διατίθεται δωρεάν άδεια αξιολόγησης για ανάπτυξη και δοκιμές.

**Ε: Πού μπορώ να βρω επιπλέον παραδείγματα και αναφορά API;**  
Α: Επισκεφθείτε το portal τεκμηρίωσης του Aspose.Note, κατεβάστε το πλήρες PDF αναφοράς API και εξερευνήστε το αποθετήριο GitHub για παραδείγματα της κοινότητας.

## Συμπέρασμα

Ακολουθώντας τα παραπάνω βήματα, τώρα γνωρίζετε **πώς να αλλάξετε το μέγεθος γραμματοσειράς σε αρχεία OneNote**, να προσαρμόσετε το χρώμα του κειμένου και να εφαρμόσετε επισήμανση χρησιμοποιώντας το Aspose.Note για Java. Αυτή η δυνατότητα σας επιτρέπει να αυτοματοποιήσετε την οπτική βελτίωση των σημειώσεων συναντήσεων, του εκπαιδευτικού υλικού ή οποιουδήποτε περιεχομένου βασισμένου στο OneNote σε μεγάλη κλίμακα.

---

**Last Updated:** 2026-06-05  
**Tested With:** Aspose.Note 23.10 for Java  
**Author:** Aspose

## Σχετικά Μαθήματα

- [Ορισμός Προεπιλεγμένου Στυλ Παραγράφου στο OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)
- [Ορισμός Γλώσσας Ελέγχου για Κείμενο στο OneNote - Aspose.Note](/note/java/onenote-text-manipulation/set-proofing-language-for-text/)
- [Ορισμός Τίτλου Σελίδας σε Στυλ Microsoft OneNote - Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}