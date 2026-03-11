---
date: 2025-12-25
description: Μάθετε πώς να μετατρέπετε το OneNote σε PNG χρησιμοποιώντας το Aspose.Note
  για Java. Αυτός ο οδηγός δείχνει πώς να ορίσετε την ανάλυση της εικόνας, να επίπεδοποιήσετε
  ένα σημειωματάριο και να αποθηκεύσετε το OneNote ως εικόνα αποδοτικά.
linktitle: How to Convert OneNote to PNG – Flatten Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: Πώς να μετατρέψετε το OneNote σε PNG – Εξομάλυνση σημειωματάριου σε εικόνα
  με το Aspose.Note
url: /el/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή Σημειωματάριου σε Επίπεδη Εικόνα στο OneNote - Aspose.Note

## Εισαγωγή

Σε αυτό το tutorial θα ανακαλύψετε πώς να **μετατρέψετε το OneNote σε PNG** μετατρέποντας ολόκληρο το σημειωματάριο σε μια ενιαία επίπεδη εικόνα χρησιμοποιώντας το Aspose.Note για Java. Αυτή η προσέγγιση είναι ιδανική όταν χρειάζεται να μοιραστείτε ένα σημειωματάριο ως στατική εικόνα, να το ενσωματώσετε σε αναφορές ή να το αρχειοθετήσετε χωρίς να χάσετε οπτικές λεπτομέρειες.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “flatten notebook”;** Συγχωνεύει όλα τα στοιχεία της σελίδας σε μία raster εικόνα.  
- **Ποια μορφή χρησιμοποιείται;** Η PNG είναι η προεπιλογή, προσφέροντας ποιότητα χωρίς απώλειες.  
- **Μπορώ να αλλάξω το DPI;** Ναι, χρησιμοποιήστε `setResolution` στο `ImageSaveOptions`.  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται εμπορική άδεια για παραγωγή.  
- **Υποστηρίζεται σε όλα τα λειτουργικά συστήματα;** Το Java API λειτουργεί όπου τρέχει η Java.

## Τι είναι η μετατροπή του OneNote σε PNG;

Η μετατροπή του OneNote σε PNG δημιουργεί μια bitmap αναπαράσταση κάθε σελίδας του σημειωματάριου, διατηρώντας κείμενο, σχέδια και ενσωματωμένα αντικείμενα σε ένα ενιαίο αρχείο εικόνας. Αυτό είναι ιδιαίτερα χρήσιμο για τεκμηρίωση, παρουσιάσεις ή αρχειοθέτηση συμμόρφωσης.

## Γιατί να μετατρέψετε το OneNote σε PNG με το Aspose.Note;

- **Full fidelity** – All visual elements are retained.  
- **Single‑file output** – No need to manage multiple page files.  
- **Customizable resolution** – Adjust DPI to meet quality requirements.  
- **No Office installation** – Works completely independent of Microsoft OneNote.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

1. Java Development Kit (JDK) εγκατεστημένο στο σύστημά σας.  
2. Βιβλιοθήκη Aspose.Note for Java ληφθείσα και ρυθμισμένη στο έργο Java. Μπορείτε να κατεβάσετε τη βιβλιοθήκη από [here](https://releases.aspose.com/note/java/).  
3. Βασικές γνώσεις προγραμματισμού Java.

## Εισαγωγή Πακέτων

Για να ξεκινήσετε, πρέπει να εισάγετε τα απαραίτητα πακέτα από το Aspose.Note for Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Βήμα 1: Ρύθμιση Καταλόγου Εγγράφου

Αρχικά, ορίστε τον κατάλογο όπου βρίσκεται το αρχείο του σημειωματάριου:

```java
String dataDir = "Your Document Directory";
```

Αντικαταστήστε το `"Your Document Directory"` με τη διαδρομή προς το αρχείο του σημειωματάριου.

## Βήμα 2: Φόρτωση Σημειωματάριου

Στη συνέχεια, φορτώστε το αρχείο του σημειωματάριου χρησιμοποιώντας την κλάση `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Βεβαιωθείτε ότι αντικαθιστάτε το `"test.onetoc2"` με το όνομα του αρχείου του σημειωματάριου σας.

## Βήμα 3: Ρύθμιση Επιλογών Αποθήκευσης Εικόνας

Τώρα, ρυθμίστε τις επιλογές για αποθήκευση του σημειωματάριου ως εικόνα. Θα ορίσουμε τη μορφή αποθήκευσης ως PNG και την ανάλυση στα 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Μπορείτε να προσαρμόσετε την ανάλυση σύμφωνα με τις απαιτήσεις σας. Εδώ είναι που **ορίζετε την ανάλυση της εικόνας** για να ελέγξετε την ποιότητα εξόδου.

## Βήμα 4: Επίπεδη Μετατροπή Σημειωματάριου

Για να διασφαλίσετε ότι όλα τα στοιχεία θα επίπεδονται σε μία εικόνα, ορίστε την επιλογή `flatten` σε `true`:

```java
saveOptions.setFlatten(true);
```

Ορίζοντας το `flatten` σε `true` εγγυάται ότι το παραγόμενο PNG διατηρεί την ακριβή διάταξη του σημειωματάριου σας.

## Βήμα 5: Αποθήκευση Εικόνας

Τέλος, αποθηκεύστε το σημειωματάριο ως επίπεδη εικόνα:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Αντικαταστήστε το `"ExportImageasFlattenedNotebook_out.png"` με το επιθυμητό όνομα αρχείου εξόδου. Αυτό το βήμα **αποθηκεύει το OneNote ως εικόνα** που μπορείτε να μοιραστείτε ή να ενσωματώσετε οπουδήποτε.

## Κοινές Περιπτώσεις Χρήσης

- **Documentation:** Embed the notebook image in technical manuals or user guides.  
- **Presentations:** Use a high‑resolution PNG slide in PowerPoint without worrying about font or object compatibility.  
- **Archiving:** Store a read‑only snapshot of a notebook for compliance audits.

## Συμβουλές Επίλυσης Προβλημάτων

- **File not found:** Double‑check the `dataDir` path and ensure the `.onetoc2` file exists.  
- **Low quality image:** Increase the DPI by changing `documentSaveOptions.setResolution(600);`.  
- **Missing elements:** Verify that `saveOptions.setFlatten(true);` is enabled; otherwise, some layers may remain separate.

## Συχνές Ερωτήσεις

**Q1: Μπορώ να προσαρμόσω την ανάλυση της εικόνας εξόδου;**  
A1: Ναι, μπορείτε να προσαρμόσετε την ανάλυση σύμφωνα με τις απαιτήσεις σας τροποποιώντας την παράμετρο της μεθόδου `setResolution`.

**Q2: Υποστηρίζει το Aspose.Note άλλες μορφές εικόνας για εξαγωγή;**  
A2: Ναι, το Aspose.Note υποστηρίζει διάφορες μορφές εικόνας όπως PNG, JPEG, BMP κ.λπ., για εξαγωγή σημειωματάριων.

**Q3: Μπορώ να προσαρμόσω περαιτέρω την εικόνα εξόδου;**  
A3: Ναι, το Aspose.Note παρέχει εκτενείς επιλογές προσαρμογής της εικόνας εξόδου, συμπεριλαμβανομένου του μεγέθους σελίδας, του προσανατολισμού και των ρυθμίσεων ποιότητας.

**Q4: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Note for Java;**  
A4: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμαστική έκδοση από [here](https://releases.aspose.com/).

**Q5: Πού μπορώ να βρω υποστήριξη για το Aspose.Note for Java;**  
A5: Μπορείτε να βρείτε υποστήριξη και πόρους στο φόρουμ Aspose.Note [here](https://forum.aspose.com/c/note/28).

---

**Τελευταία Ενημέρωση:** 2025-12-25  
**Δοκιμή Με:** Aspose.Note for Java 24.12  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}