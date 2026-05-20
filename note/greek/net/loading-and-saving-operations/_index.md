---
date: 2026-05-20
description: Μάθετε πώς να φορτώνετε OneNote, να αποθηκεύετε OneNote ως PDF, να εξάγετε
  OneNote σε εικόνα και να προσθέτετε τίτλο σελίδας στο OneNote χρησιμοποιώντας το
  Aspose.Note για .NET.
keywords:
- how to load onenote
- save onenote as pdf
- export onenote to image
- convert onenote page image
- add page title onenote
linktitle: Λειτουργίες Φόρτωσης και Αποθήκευσης
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to load OneNote, save OneNote as PDF, export OneNote to image
    and add page title on OneNote using Aspose.Note for .NET.
  headline: How to Load OneNote Documents with Aspose.Note for .NET
  type: TechArticle
- questions:
  - answer: 'Pass the password to the `Document.Load` overload: `Document.Load("file.one",
      "password")`. Aspose.Note decrypts the notebook in memory.'
    question: How do I load an encrypted OneNote file?
  - answer: Yes, the PDF exporter preserves vector ink, images, and embedded media,
      ensuring the output matches the original notebook layout.
    question: Can I export a OneNote notebook to PDF without losing ink strokes?
  - answer: The library can stream notebooks up to **500 MB** without loading the
      entire file into RAM, thanks to its low‑memory processing engine.
    question: What is the maximum file size Aspose.Note can handle?
  - answer: Absolutely. Use `PdfSaveOptions` to set `Author`, `Title`, `Subject`,
      and custom XMP metadata before calling `Save`.
    question: Is it possible to add custom metadata when saving as PDF?
  - answer: No. A single Aspose.Note for .NET license covers .NET Framework, .NET
      Core, and .NET 5/6/7 applications.
    question: Do I need a separate license for each .NET platform?
  type: FAQPage
second_title: Aspose.Note .NET API
title: Πώς να φορτώσετε έγγραφα OneNote με το Aspose.Note για .NET
url: /el/net/loading-and-saving-operations/
weight: 25
---

{{< blocks/products/products-backtop-button >}}
{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να φορτώσετε έγγραφα OneNote με το Aspose.Note για .NET

## Εισαγωγή

Αν ψάχνετε για έναν αξιόπιστο τρόπο **πώς να φορτώσετε** αρχεία OneNote σε μια εφαρμογή .NET, βρίσκεστε στο σωστό μέρος. Αυτός ο οδηγός σας καθοδηγεί στη φόρτωση, αποθήκευση και εξαγωγή σημειωματάριων OneNote χρησιμοποιώντας το Aspose.Note για .NET, και σας παραπέμπει στα πιο χρήσιμα βήμα‑βήμα tutorials στη συλλογή μας.

## Γρήγορες Απαντήσεις
- **Πώς φορτώνω ένα αρχείο OneNote;** Χρησιμοποιήστε `Document.Load("file.one")` – το Aspose.Note διαβάζει το αρχείο στη μνήμη άμεσα.  
- **Μπορώ να αποθηκεύσω το OneNote ως PDF;** Ναι, καλέστε `doc.Save("output.pdf", SaveFormat.Pdf)`.  
- **Σε ποιες μορφές μπορώ να εξάγω;** Πάνω από 30 μορφές, συμπεριλαμβανομένων PDF, PNG, JPEG, TIFF και HTML.  
- **Πώς προσθέτω τίτλο σε σελίδα;** Ορίστε `page.Title = "My Title"` πριν την αποθήκευση.  
- **Χρειάζομαι άδεια για παραγωγή;** Απαιτείται εμπορική άδεια για μη‑αξιολογικές εκδόσεις.

## Πώς να φορτώσετε OneNote;

**Document** αντιπροσωπεύει ένα αρχείο OneNote στη μνήμη. Φορτώστε το σημειωματάριο OneNote σας με μία μόνο γραμμή κώδικα:  

```csharp
var doc = new Document("MyNotebook.one");
```  

Το Aspose.Note αναλύει το αρχείο, δημιουργεί ένα μοντέλο αντικειμένων στη μνήμη και σας δίνει πλήρη πρόσβαση σε ενότητες, σελίδες και πόρους. Αυτή η λειτουργία υποστηρίζει τόσο κρυπτογραφημένα όσο και μη κρυπτογραφημένα αρχεία, και λειτουργεί σε .NET 6+, .NET 5, .NET Core 3.1 και .NET Framework 4.6.2+.

## Γιατί να εξάγετε το OneNote σε PDF ή εικόνα;

Η εξαγωγή του OneNote σε μορφές PDF ή εικόνας είναι μια κοινή απαίτηση για αρχειοθέτηση, αναφορές ή κοινή χρήση περιεχομένου με χρήστες που δεν έχουν εγκατεστημένο το OneNote. Το Aspose.Note μπορεί να **εξάγει το OneNote σε PDF** και **εξάγει το OneNote σε εικόνα** σε λιγότερο από 2 δευτερόλεπτα για ένα σημειωματάριο 100 σελίδων σε τυπικό διακομιστή, διαχειριζόμενο σύνθετες διατάξεις, ενσωματωμένα αρχεία και γραφικά υψηλής ανάλυσης χωρίς απώλεια πιστότητας.  

Ποσοτική δήλωση: Το Aspose.Note υποστηρίζει **πάνω από 30 μορφές εξόδου** (PDF, PNG, JPEG, TIFF, BMP, GIF, SVG, HTML, XPS, DOCX και άλλα) και μπορεί να επεξεργαστεί σημειωματάρια έως **500 MB** χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη RAM, χάρη στην αρχιτεκτονική ροής του.

## Πώς να αποθηκεύσετε το OneNote ως PDF;

**SaveFormat** είναι μια απαρίθμηση που καθορίζει τη μορφή εξόδου του αρχείου. Αποθηκεύστε ένα φορτωμένο σημειωματάριο σε PDF με:  

```csharp
doc.Save("Report.pdf", SaveFormat.Pdf);
```  

Το API αντιστοιχίζει αυτόματα τις ενότητες OneNote σε σελίδες PDF, διατηρώντας πίνακες, στίγματα μελάνης και ενσωματωμένα μέσα. Μπορείτε επίσης να ρυθμίσετε λεπτομερώς το μέγεθος σελίδας, τη συμπίεση και τη συμμόρφωση PDF/A μέσω του **PdfSaveOptions**, το οποίο παρέχει επιλογές για τον έλεγχο της εξόδου PDF, όπως συμμόρφωση και συμπίεση.  

**Η εξαγωγή OneNote σε PDF** είναι ιδανική για νομικά έγγραφα, εταιρικές αναφορές ή οποιοδήποτε σενάριο που απαιτεί μορφή σταθερού layout, έτοιμη για εκτύπωση.

## Πώς να εξάγετε το OneNote σε εικόνα;

**ImageSaveOptions** ορίζει ρυθμίσεις για την εξαγωγή εικόνας όπως μορφή και DPI. Για να μετατρέψετε μια συγκεκριμένη σελίδα σε εικόνα, καλέστε:  

```csharp
page.Save("Page1.png", ImageSaveOptions.Png);
```  

Αυτή η ενιαία κλήση αποδίδει τη σελίδα στα 300 dpi εξ ορισμού, παράγοντας καθαρά PNG κατάλληλα για δημοσίευση στο web ή επεξεργασία OCR. Η δυνατότητα **μετατροπής εικόνας σελίδας OneNote** υποστηρίζει PNG, JPEG, TIFF και BMP, και μπορείτε να καθορίσετε προσαρμοσμένο DPI, βάθος χρώματος και επιλογές γκρι κλίμακας μέσω του `ImageSaveOptions`.

## Πώς να προσθέσετε τίτλο σελίδας στο OneNote;

Αναθέστε έναν τίτλο σε μια σελίδα πριν την αποθήκευση: `page.Title = "Quarterly Summary";`. Η προσθήκη τίτλου σελίδας βελτιώνει την πλοήγηση στο OneNote και σε επακόλουθες μορφές (PDF, HTML) επειδή ο τίτλος εμφανίζεται ως επικεφαλίδα ή σελιδοδείκτης.  

Το Aspose.Note επίσης σας επιτρέπει να ορίσετε **μεταδεδομένα** όπως συγγραφέας, ημερομηνία δημιουργίας και ετικέτες, τα οποία διατηρούνται όταν **αποθηκεύετε το OneNote ως PDF** ή **εξάγετε το OneNote σε εικόνα**.

## Κοινές Περιπτώσεις Χρήσης

- **Αυτοματοποιημένες αναφορές** – Φορτώστε ένα πρότυπο OneNote, ενσωματώστε δεδομένα και εξάγετε σε PDF για διανομή.  
- **Μεταφορά περιεχομένου** – Μετατρέψτε παλαιά σημειωματάρια OneNote σε HTML ή Markdown για σύγχρονες πλατφόρμες τεκμηρίωσης.  
- **Ψηφιακή αρχειοθέτηση** – Αποθηκεύστε σημειωματάρια ως αρχεία συμβατά με PDF/A‑2b για μακροπρόθεσμη διατήρηση.  
- **Δημιουργία εικόνων** – Δημιουργήστε PNG υψηλής ανάλυσης από επιλεγμένες σελίδες για παρουσιάσεις ή υλικό e‑learning.

## Εκπαιδεύσεις Λειτουργιών Φόρτωσης και Αποθήκευσης

### [Συνεχείς Λειτουργίες Εξαγωγής στο Aspose.Note](./consequent-export-operations/)
Περιηγηθείτε στις λεπτομέρειες [εδώ](./consequent-export-operations/).

### [Μετατροπή Συγκεκριμένης Σελίδας σε Εικόνα στο Aspose.Note](./convert-specific-page-to-image/)
Μάθετε πώς να μετατρέπετε συγκεκριμένες σελίδες εγγράφων Microsoft OneNote σε εικόνες προγραμματιστικά χρησιμοποιώντας το Aspose.Note για .NET. Εξερευνήστε τον οδηγό [εδώ](./convert-specific-page-to-image/).

### [Δημιουργία Εγγράφου με Πλούσιο Κείμενο στο Aspose.Note](./create-doc-with-rich-text/)
Δημιουργήστε έγγραφα OneNote με πλούσιο κείμενο χρησιμοποιώντας παραδείγματα κώδικα. Αναλυτικά βήματα είναι διαθέσιμα [εδώ](./create-doc-with-rich-text/).

### [Δημιουργία Εγγράφου με Τίτλο Σελίδας στο Aspose.Note](./create-doc-with-page-title/)
Δημιουργήστε έγγραφα με σελίδες με τίτλο και βελτιώστε την πλοήγηση. Ακολουθήστε τον οδηγό [εδώ](./create-doc-with-page-title/).

### [Δημιουργία Εγγράφου OneNote και Αποθήκευση σε HTML στο Aspose.Note](./create-onenote-doc-save-to-html/)

### [Εξαγωγή Περιεχομένου στο Aspose.Note](./extract-content/)

### [Φόρτωση Εγγράφου OneNote στο Aspose.Note](./load-onenote-document/)

### [Διαίρεση Σελίδων στο Aspose.Note](./page-splitting/)

### [Έγγραφο Προστατευμένο με Κωδικό στο Aspose.Note](./password-protected-document/)

### [Ανάκτηση Μορφής Αρχείου στο Aspose.Note](./retrieve-file-format/)

### [Αποθήκευση Εγγράφου σε Μορφή OneNote στο Aspose.Note](./save-doc-to-onenote-format/)

### [Αποθήκευση Εύρους Σελίδων ως PDF στο Aspose.Note](./save-range-pages-as-pdf/)

### [Αποθήκευση σε Δυαδική Εικόνα στο Aspose.Note](./save-to-binary-image/)

### [Αποθήκευση σε Εικόνα στο Aspose.Note](./save-to-image/)

### [Αποθήκευση σε Ασπρόμαυρη Εικόνα στο Aspose.Note](./save-to-grayscale-image/)

### [Αποθήκευση σε JPEG Εικόνα στο Aspose.Note](./save-to-jpeg-image/)

### [Αποθήκευση σε PDF στο Aspose.Note](./save-to-pdf/)

### [Αποθήκευση σε TIFF Εικόνα στο Aspose.Note](./save-to-tiff-image/)

### [Αποθήκευση με Καθορισμένες Γραμματοσειρές στο Aspose.Note](./save-using-specified-fonts/)

### [Αποθήκευση με Προεπιλεγμένες Ρυθμίσεις στο Aspose.Note](./save-with-default-settings/)

### [Καθορισμός Επιλογών Αποθήκευσης στο Aspose.Note](./specify-save-options/)

### [Κλήσεις Πίσω Κατά την Αποθήκευση από Χρήστη στο Aspose.Note](./user-saving-callbacks/)
Προσαρμόστε τις γραμματοσειρές, CSS και εικόνες κατά την αποθήκευση. Αναλυτικές οδηγίες είναι διαθέσιμες [εδώ](./user-saving-callbacks/).

## Συχνές Ερωτήσεις

**Ε: Πώς φορτώνω ένα κρυπτογραφημένο αρχείο OneNote;**  
Α: Περνάτε τον κωδικό στο υπερφορτωμένο `Document.Load`: `Document.Load("file.one", "password")`. Το Aspose.Note αποκρυπτογραφεί το σημειωματάριο στη μνήμη.

**Ε: Μπορώ να εξάγω ένα σημειωματάριο OneNote σε PDF χωρίς να χάσω τα στίγματα μελάνης;**  
Α: Ναι, ο εξαγωγέας PDF διατηρεί το διανυσματικό μελάνι, τις εικόνες και τα ενσωματωμένα μέσα, εξασφαλίζοντας ότι η έξοδος ταιριάζει με την αρχική διάταξη του σημειωματάριου.

**Ε: Ποιο είναι το μέγιστο μέγεθος αρχείου που μπορεί να διαχειριστεί το Aspose.Note;**  
Α: Η βιβλιοθήκη μπορεί να ρέει (stream) σημειωματάρια έως **500 MB** χωρίς να φορτώνει ολόκληρο το αρχείο στη RAM, χάρη στη μηχανή επεξεργασίας χαμηλής μνήμης.

**Ε: Είναι δυνατόν να προσθέσω προσαρμοσμένα μεταδεδομένα κατά την αποθήκευση ως PDF;**  
Α: Απόλυτα. Χρησιμοποιήστε το `PdfSaveOptions` για να ορίσετε `Author`, `Title`, `Subject` και προσαρμοσμένα μεταδεδομένα XMP πριν καλέσετε `Save`.

**Ε: Χρειάζομαι ξεχωριστή άδεια για κάθε πλατφόρμα .NET;**  
Α: Όχι. Μία άδεια Aspose.Note for .NET καλύπτει .NET Framework, .NET Core και εφαρμογές .NET 5/6/7.

**Τελευταία Ενημέρωση:** 2026-05-20  
**Δοκιμή Με:** Aspose.Note 24.12 for .NET  
**Συγγραφέας:** Aspose  

{{< blocks/products/pf/main-container >}}

## Σχετικές Εκπαιδεύσεις

- [Φόρτωση Εγγράφου OneNote στο Aspose.Note](/note/net/loading-and-saving-operations/load-onenote-document/)
- [Αποθήκευση Εγγράφου σε Μορφή OneNote στο Aspose.Note](/note/net/loading-and-saving-operations/save-doc-to-onenote-format/)
- [Μετατροπή Σημειωματάριων σε PDF στο Aspose Note .NET](/note/net/notebook-operations/convert-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}