---
date: 2026-09-24
description: Μάθετε πώς να προσθέσετε tag onenote, να δημιουργήσετε outline στο OneNote
  και να εξάγετε το OneNote σε PDF χρησιμοποιώντας το Aspose.Note για Java.
keywords:
- add tag onenote
- how to add tag
- how to create outline
- export onenote pdf
- java convert onenote pdf
lastmod: 2026-09-24
linktitle: Πώς να προσθέσετε tag onenote και να δημιουργήσετε outline στο OneNote
og_description: Προσθέστε tag onenote και δημιουργήστε outline στο OneNote χρησιμοποιώντας
  το Aspose.Note για Java, στη συνέχεια εξάγετε το σημειωματάριο σε PDF. Ακολουθήστε
  κώδικα βήμα‑βήμα και βέλτιστες πρακτικές.
og_image_alt: Screenshot showing OneNote outline with tags created via Aspose.Note
  Java API
og_title: Προσθήκη tag onenote και δημιουργία outline στο OneNote – Οδηγός Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-24'
  description: Learn how to add tag onenote, create outline in OneNote, and export
    OneNote to PDF using Aspose.Note for Java.
  headline: How to add tag onenote and create outline in OneNote
  type: TechArticle
- questions:
  - answer: Aspose.Note primarily targets Java, but equivalent libraries exist for
      .NET and other platforms.
    question: Can I use Aspose.Note for Java with other programming languages?
  - answer: Yes—its API is well‑documented, and the step‑by‑step approach in this
      guide is friendly for developers of any skill level.
    question: Is Aspose.Note suitable for beginners?
  - answer: You can get a temporary license from the **[temporary license page](https://purchase.aspose.com/temporary-license/)**.
    question: How do I obtain a temporary license for Aspose.Note for Java?
  - answer: Visit the **[Aspose.Note forum](https://forum.aspose.com/c/note/28)**
      for community help and official assistance.
    question: Where can I find additional support?
  - answer: Yes—download a trial version from the **[Aspose releases page](https://releases.aspose.com/)**.
    question: Is a free trial available?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote tagging
- Aspose.Note
- Java note processing
title: Πώς να προσθέσετε tag onenote και να δημιουργήσετε outline στο OneNote
url: /el/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να προσθέσετε ετικέτα στο OneNote και να δημιουργήσετε περίγραμμα στο OneNote

## Εισαγωγή
Σε αυτό το σεμινάριο θα μάθετε πώς να **προσθέσετε ετικέτα στο OneNote** και να δημιουργήσετε ένα δομημένο περίγραμμα μέσα σε ένα σημειωματάριο OneNote χρησιμοποιώντας το Aspose.Note for Java. Θα περάσουμε από κάθε βήμα, θα εξηγήσουμε γιατί κάθε κλήση API είναι σημαντική, και θα ολοκληρώσουμε **εξάγοντας το σημειωματάριο σε PDF** ώστε να μπορείτε να μοιραστείτε ένα επαγγελματικό, αναζητήσιμο έγγραφο με τους συναδέλφους.

## Γρήγορες απαντήσεις
- **Τι σημαίνει “create outline in OneNote”;** Δημιουργεί ένα ιεραρχικό δέντρο από επικεφαλίδες και υπο‑ενότητες που μπορείτε να επεκτείνετε ή να συμπτύξετε.  
- **Ποια κλάση προσθέτει ετικέτες στο OneNote;** Χρησιμοποιήστε την κλάση `NoteTag` από το Aspose.Note for Java.  
- **Μπορώ να εξάγω το αποτέλεσμα σε PDF;** Ναι – καλέστε `doc.save("output.pdf", SaveFormat.Pdf)`.  
- **Χρειάζομαι άδεια για παραγωγή;** Διατίθεται προσωρινή άδεια για δοκιμές· απαιτείται πλήρης άδεια για εμπορική χρήση.  
- **Ποιες είναι οι κύριες προαπαιτήσεις;** Εγκατεστημένο JDK, βιβλιοθήκη Aspose.Note for Java και βασικές γνώσεις Java.

## Τι είναι το “create outline in OneNote”;
Η δημιουργία ενός περιγράμματος στο OneNote σημαίνει την προσθήκη αντικειμένων `Outline` και `OutlineElement` που ορίζουν μια δομή δέντρου για τις σημειώσεις σας. Αυτή η ιεραρχία σας επιτρέπει να συμπτύχετε, να επεκτείνετε και να οργανώσετε πληροφορίες όπως οι επικεφαλίδες σε ένα έγγραφο. Επίσης επιτρέπει προγραμματιστική πλοήγηση και υποστηρίζει την εξαγωγή της ιεραρχίας σε μορφές όπως PDF, όπου κάθε επίπεδο μπορεί να γίνει σελιδοδείκτης.

## Γιατί να προσθέσετε ετικέτα στο OneNote;
Η προσθήκη ετικέτας στο OneNote σας παρέχει ένα οπτικό σήμα—όπως αστέρι, σημάδι ελέγχου ή προσαρμοσμένο εικονίδιο—που αμέσως τραβά την προσοχή, βελτιώνει την αναζητησιμότητα και βοηθά τις ομάδες να προτεραιοποιούν εργασίες. Με το Aspose.Note μπορείτε προγραμματιστικά να συνδέσετε ένα `NoteTag` σε οποιοδήποτε κείμενο, εξασφαλίζοντας συνέπεια σε πολλές σελίδες.

## Ποσοτικοποιημένα οφέλη του Aspose.Note
Το Aspose.Note υποστηρίζει **πάνω από 30 μορφές εισόδου και εξόδου** (συμπεριλαμβανομένων DOCX, PDF, HTML και τύπων εικόνων) και μπορεί να επεξεργαστεί σημειωματάρια με **έως 500 σελίδες** χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, παρέχοντας υψηλής απόδοσης μετατροπές σε τυπικό εξοπλισμό διακομιστών.

## Προαπαιτήσεις
- Java Development Kit (JDK) 8 ή νεότερο.  
- Βιβλιοθήκη Aspose.Note for Java – κατεβάστε την από τη **[Aspose.Note for Java download page](https://releases.aspose.com/note/java/)**.  
- Βασική εξοικείωση με τη σύνταξη Java και τη ρύθμιση έργου Maven/Gradle.

## Εισαγωγή πακέτων
Οι κλάσεις `Document`, `Page`, `Outline`, `OutlineElement`, `RichText` και `NoteTag` βρίσκονται στο χώρο ονομάτων `com.aspose.note`. Εισάγετέ τις στην αρχή του αρχείου Java:

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

Ας αναλύσουμε το βήμα εισαγωγής βήμα‑βήμα.

## Βήμα 1: Ρύθμιση εγγράφου και σελίδας
`Document` αντιπροσωπεύει ολόκληρο το σημειωματάριο OneNote στη μνήμη, ενώ `Page` είναι ένας μοναδικός καμβάς μέσα στο σημειωματάριο.  

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

Η κλάση `Document` αντιπροσωπεύει ολόκληρο το αρχείο OneNote στη μνήμη, ενώ το αντικείμενο `Page` είναι ο καμβάς όπου τοποθετούνται τα περιγράμματα και οι ετικέτες.

## Βήμα 2: Δημιουργία περιγράμματος
`Outline` είναι ένας κοντέινερ που περιέχει μια ιεραρχία αντικειμένων `OutlineElement`, σχηματίζοντας το δομικό δέντρο του σημειωματάριου.  

```java
Outline outline = new Outline();
```

Τα περιγράμματα παρέχουν τη δομική στήριξη που σας επιτρέπει να **δημιουργήσετε περίγραμμα στο OneNote** και να διατηρείτε τις πληροφορίες οργανωμένες.

## Βήμα 3: Αρχικοποίηση στοιχείου περιγράμματος και στυλ παραγράφου
`OutlineElement` αντιπροσωπεύει έναν μεμονωμένο κόμβο (επικεφαλίδα) σε ένα περίγραμμα, και το `ParagraphStyle` ορίζει τη γραμματοσειρά, το μέγεθος και την εσοχή του.  

```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```

`OutlineElement` αντιπροσωπεύει έναν μοναδικό κόμβο (επικεφαλίδα) μέσα στο περίγραμμα, και το `ParagraphStyle` ελέγχει τη γραμματοσειρά, το μέγεθος και την εσοχή.

## Βήμα 4: Προσθήκη μορφοποιημένου κειμένου με ετικέτα σημειώματος
`RichText` αποθηκεύει το πραγματικό περιεχόμενο κειμένου, και το `NoteTag` συνδέει μια οπτική ετικέτα (εικονίδιο) σε αυτό το κείμενο.  

```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```

`RichText` περιέχει το πραγματικό κείμενο, ενώ το `NoteTag` **προσθέτει ετικέτα στο OneNote** ως οπτική ένδειξη δίπλα στο κείμενο.

## Βήμα 5: Κατασκευή δομής περιγράμματος
Προσθέστε τον κόμβο `RichText` στο `OutlineElement`, στη συνέχεια προσθέστε το στοιχείο στο `Outline`, και τέλος συνδέστε το περίγραμμα στη σελίδα.  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

Αυτό το βήμα ολοκληρώνει τη ιεραρχική διάταξη, ολοκληρώνοντας τη ροή εργασίας **create outline in OneNote**.

## Βήμα 6: Αποθήκευση του εγγράφου ως PDF
`SaveFormat.Pdf` λέει στο Aspose.Note να γράψει το σημειωματάριο ως αρχείο PDF.  

```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```

Το παραγόμενο PDF διατηρεί την ιεραρχία του περιγράμματος και τις οπτικές ετικέτες, καθιστώντας το αναζητήσιμο και εκτυπώσιμο.

## Συνηθισμένα προβλήματα και αντιμετώπιση
- **Η ετικέτα δεν εμφανίζεται:** Βεβαιωθείτε ότι προσθέτετε το `NoteTag` στο αντικείμενο `RichText` *πριν* συνδέσετε το κείμενο στο στοιχείο του περιγράμματος.  
- **Το περίγραμμα δεν συμπτύσσεται σε PDF:** Οι προβολείς PDF δεν υποστηρίζουν το διαδραστικό περίγραμμα του OneNote· η ιεραρχία διατηρείται ως σελιδοδείκτες.  
- **Τα μεγάλα σημειωματάρια προκαλούν πίεση μνήμης:** Χρησιμοποιήστε `Document.saveOptions.setLoadOnDemand(true)` για να επεξεργάζεστε τις σελίδες αργά.

## Συχνές ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω το Aspose.Note for Java με άλλες γλώσσες προγραμματισμού;**  
A: Το Aspose.Note στοχεύει κυρίως στη Java, αλλά υπάρχουν ισοδύναμες βιβλιοθήκες για .NET και άλλες πλατφόρμες.

**Q: Είναι το Aspose.Note κατάλληλο για αρχάριους;**  
A: Ναι—το API του είναι καλά τεκμηριωμένο, και η προσέγγιση βήμα‑βήμα σε αυτόν τον οδηγό είναι φιλική για προγραμματιστές κάθε επιπέδου.

**Q: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.Note for Java;**  
A: Μπορείτε να λάβετε μια προσωρινή άδεια από τη **[temporary license page](https://purchase.aspose.com/temporary-license/)**.

**Q: Πού μπορώ να βρω επιπλέον υποστήριξη;**  
A: Επισκεφθείτε το **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** για βοήθεια της κοινότητας και επίσημη υποστήριξη.

**Q: Υπάρχει δωρεάν δοκιμή;**  
A: Ναι—κατεβάστε μια δοκιμαστική έκδοση από τη **[Aspose releases page](https://releases.aspose.com/)**.

**Q: Μπορώ να προσαρμόσω το εικονίδιο της ετικέτας;**  
A: Ναι—το Aspose.Note παρέχει προεπιλεγμένα εικονίδια μέσω του enum `TagIcon` και επίσης επιτρέπει την παροχή προσαρμοσμένων εικόνων.

**Q: Πώς αλλάζω τις ρυθμίσεις εξόδου PDF;**  
A: Χρησιμοποιήστε `PdfSaveOptions` για να προσαρμόσετε την ποιότητα εικόνας, τη συμπίεση και την ασφάλεια πριν καλέσετε `doc.save`.

**Q: Είναι δυνατόν να προσθέσω πολλαπλές ετικέτες στο ίδιο κείμενο;**  
A: Απόλυτα. Καλέστε `richText.getTags().add()` πολλές φορές με διαφορετικές εμφανίσεις του `NoteTag`.

---

## Σχετικά Σεμινάρια

- [Προσθήκη ετικετών στο OneNote – Δημιουργία Ετικετοποιημένου Εγγράφου OneNote με Aspose.Note](/note/java/onenote-tag-operations/)
- [Πώς να δημιουργήσετε έγγραφο OneNote - Προσθήκη κόμβου κειμένου με ετικέτα χρησιμοποιώντας Aspose.Note](/note/java/onenote-tag-operations/add-text-node-with-tag/)
- [Δημιουργία προτύπου σημειώσεων συνάντησης με Aspose.Note for Java – Δημιουργία περιγράμματος στο OneNote](/note/java/onenote-tag-operations/generate-template-for-meeting-notes/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}