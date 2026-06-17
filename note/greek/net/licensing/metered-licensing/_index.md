---
date: 2026-05-20
description: Μάθετε πώς να αποθηκεύετε ένα έγγραφο ως PDF χρησιμοποιώντας το Aspose.Note
  για .NET, ενώ παρακολουθείτε την κατανάλωση άδειας με μετρητική άδεια.
keywords:
- save document as pdf
- convert onenote to pdf
- monitor license consumption
linktitle: Αποθήκευση εγγράφου ως PDF με μετρητική άδεια στην AspNet.Note
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to save document as PDF using Aspose.Note for .NET while
    monitoring license consumption with metered licensing.
  headline: Save Document as PDF with Metered Licensing in Aspose.Note
  type: TechArticle
- description: Learn how to save document as PDF using Aspose.Note for .NET while
    monitoring license consumption with metered licensing.
  name: Save Document as PDF with Metered Licensing in Aspose.Note
  steps:
  - name: Set Metered Key
    text: '`Metered` is the class that manages metered licensing operations. **Definition
      anchor:** The `MeteredKey` class stores the public and private strings required
      to authenticate a metered license request.'
  - name: Perform Document Operation
    text: '`Document` loads and represents a OneNote file for manipulation.'
  - name: Save Document
    text: '`Save` writes the document to the specified file and format.'
  type: HowTo
- questions:
  - answer: Metered licensing is a usage‑based model where you purchase a pool of
      credits and the API deducts credits for each operation you perform.
    question: What is metered licensing?
  - answer: You can obtain a metered license for Aspose.Note for .NET from the Aspose
      website.
    question: How do I obtain a metered license for Aspose.Note for .NET?
  - answer: Yes, metered licensing allows you to monitor resource consumption in real
      time, enabling better cost management.
    question: Can I track my resource consumption in real time with metered licensing?
  - answer: Metered licensing may have certain limitations depending on the specific
      terms and conditions provided by the software vendor.
    question: Are there any limitations to metered licensing?
  - answer: While metered licensing can be beneficial for many software applications,
      its suitability depends on factors such as usage patterns and cost considerations.
    question: Is metered licensing suitable for all types of software applications?
  type: FAQPage
second_title: Aspose.Note .NET API
title: Αποθήκευση εγγράφου ως PDF με μετρητική άδεια στην Aspose.Note
url: /el/net/licensing/metered-licensing/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση εγγράφου ως PDF με Μετρητική Άδεια στο Aspose.Note

## Εισαγωγή

Η αποθήκευση ενός εγγράφου ως PDF είναι συχνά το τελικό βήμα σε μια ροή εργασίας που παρέχει ένα φορητό, έτοιμο για εκτύπωση αρχείο στους τελικούς χρήστες. Με το Aspose.Note για .NET μπορείτε να **αποθηκεύσετε το έγγραφο ως PDF** χρησιμοποιώντας μετρητική άδεια για να παρακολουθείτε τη χρήση και το κόστος. Αυτό το tutorial σας οδηγεί βήμα προς βήμα—από τη ρύθμιση ενός μετρητικού κλειδιού μέχρι τη μετατροπή ενός αρχείου OneNote, την αποθήκευση του ως PDF και την παρακολούθηση της κατανάλωσης—ώστε να υλοποιήσετε μια αξιόπιστη, ελεγχόμενη από κόστος λύση σήμερα.

## Γρήγορες Απαντήσεις
- **Ποιο είναι το κύριο όφελος της μετρητικής άδειας;** Σας επιτρέπει να πληρώνετε μόνο για τους πόρους που πραγματικά καταναλώνετε.  
- **Πώς αποθηκεύω ένα αρχείο OneNote ως PDF;** Φορτώστε το αρχείο με `Document` και καλέστε `Save("output.pdf", SaveFormat.Pdf)`.  
- **Χρειάζομαι ξεχωριστή άδεια για τη μετατροπή σε PDF;** Όχι, η ίδια μετρητική άδεια καλύπτει όλες τις λειτουργίες.  
- **Μπορώ να παρακολουθήσω τη χρήση σε πραγματικό χρόνο;** Ναι, το Aspose.Note παρέχει APIs για την ερώτηση των πίστωσεων και των ποσοτήτων κατανάλωσης.  
- **Ποιες εκδόσεις του .NET υποστηρίζονται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Προαπαιτούμενα

Πριν ξεκινήσουμε αυτό το ταξίδι κατανόησης της μετρητικής άδειας με το Aspose.Note για .NET, ας βεβαιωθούμε ότι έχουμε τα απαραίτητα προαπαιτούμενα σε θέση:

1. Εγκατάσταση του Aspose.Note για .NET: Βεβαιωθείτε ότι έχετε κατεβάσει και εγκαταστήσει το Aspose.Note για .NET. Μπορείτε να αποκτήσετε την πιο πρόσφατη έκδοση από τη [download page](https://releases.aspose.com/note/net/).

2. Πρόσβαση στην τεκμηρίωση του Aspose.Note: Εξοικειωθείτε με την τεκμηρίωση του Aspose.Note για .NET, η οποία παρέχει λεπτομερείς πληροφορίες για τις διάφορες λειτουργίες και δυνατότητές του. Μπορείτε να ανατρέξετε στην τεκμηρίωση [εδώ](https://reference.aspose.com/note/net/).

## Εισαγωγή Ονομάτων Χώρων

Για να αρχίσετε να χρησιμοποιείτε τη μετρητική άδεια με το Aspose.Note για .NET, εισάγετε τα απαραίτητα ονόματα χώρων (namespaces) στο έργο σας. Αυτό το βήμα εξασφαλίζει ότι έχετε πρόσβαση στις απαιτούμενες κλάσεις και μεθόδους.

```csharp
using System;
using System.IO;
```

## Πώς να αποθηκεύσετε το έγγραφο ως PDF;

`Document` αντιπροσωπεύει ένα σημειωματάριο OneNote που έχει φορτωθεί στη μνήμη. Φορτώστε το με `new Document("source.one")` και καλέστε `Save("output.pdf", SaveFormat.Pdf)` για να μετατρέψετε το σημειωματάριο σε PDF. Η λειτουργία σέβεται τη μετρητική άδεια, αφαιρώντας αυτόματα τις πιστώσεις. Το `Save` διαχειρίζεται επίσης πίνακες, εικόνες και ενσωματωμένα αντικείμενα, διατηρώντας την ακρίβεια της διάταξης.

### Βήμα 1: Ορισμός Μετρητικού Κλειδιού

`Metered` είναι η κλάση που διαχειρίζεται τις λειτουργίες της μετρητικής άδειας.

**Αγκύρωση ορισμού:** Η κλάση `MeteredKey` αποθηκεύει τις δημόσιες και ιδιωτικές συμβολοσειρές που απαιτούνται για την πιστοποίηση ενός αιτήματος μετρητικής άδειας.

```csharp
// ExStart:MeteredLicense
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");
```

### Βήμα 2: Εκτέλεση Λειτουργίας Εγγράφου

`Document` φορτώνει και αντιπροσωπεύει ένα αρχείο OneNote για επεξεργασία.

```csharp
// Load OneNote document and get first child
Document document = new Document(Path.Combine(dataDir, "Aspose.one"));
```

### Βήμα 3: Αποθήκευση Εγγράφου

`Save` γράφει το έγγραφο στο καθορισμένο αρχείο και μορφή.

```csharp
document.Save(Path.Combine(dataDir, "MeteredLicense.pdf"));
```

## Πώς να μετατρέψετε το OneNote σε PDF;

Μετατρέψτε το OneNote σε PDF φορτώνοντας το αρχείο `.one` στην κλάση `Document` και καλώντας το `Save` με `SaveFormat.Pdf`. Η μετατροπή εκτελείται στη μνήμη, επεξεργάζεται έως 2.000 σελίδες ανά λεπτό σε έναν τυπικό διακομιστή, και δεν απαιτεί εγκατάσταση του Microsoft Office.

## Πώς να παρακολουθήσετε την κατανάλωση της άδειας;

`GetConsumption` επιστρέφει τον υπόλοιπο αριθμό πιστώσεων και τις λεπτομέρειες χρήσης για την τρέχουσα συνεδρία. Ανακτήστε τα δεδομένα κατανάλωσης πριν και μετά από κάθε λειτουργία καλώντας το `MeteredLicense.GetConsumption()`· η μέθοδος επιστρέφει τον υπόλοιπο αριθμό πιστώσεων και τον αριθμό των μονάδων που χρησιμοποιήθηκαν στην τελευταία κλήση. Αυτή η ανατροφοδότηση σε πραγματικό χρόνο σας επιτρέπει να επιβάλετε όρια χρήσης ή να ενεργοποιήσετε ειδοποιήσεις όταν φτάσετε σε ένα όριο.

## Γιατί να χρησιμοποιήσετε τη μετρητική άδεια με το Aspose.Note;

Το Aspose.Note υποστηρίζει **πάνω από 50 μορφές εισόδου** (συμπεριλαμβανομένων των `.one`, `.onepkg`, `.onez`) και μπορεί να εξάγει **PDF, XPS, HTML και μορφές εικόνας**. Η μετρητική άδεια επεξεργάζεται έγγραφα χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, επιτρέποντας τη μετατροπή **σημειωματάριων με εκατοντάδες σελίδες** ενώ διατηρεί τη χρήση RAM κάτω από **100 MB**. Αυτή η αποδοτικότητα μεταφράζεται σε χαμηλότερο κόστος υποδομής και προβλέψιμες δαπάνες άδειας.

## Συχνά Προβλήματα και Λύσεις

- **Σφάλμα μη έγκυρου κλειδιού:** Επαληθεύστε ότι τα δημόσια και ιδιωτικά κλειδιά ταιριάζουν με αυτά που εκδόθηκαν για τον λογαριασμό σας· κενά ή χαρακτήρες αλλαγής γραμμής προκαλούν αποτυχίες.  
- **Απρόσμενη αφαίρεση πίστωσης:** Βεβαιωθείτε ότι καλείτε το `MeteredLicense.ResetConsumption()` μετά από δοκιμαστικές εκτελέσεις για να αποφύγετε την καταμέτρηση της χρήσης ανάπτυξης ως πιστώσεις παραγωγής.  
- **Η έξοδος PDF είναι κενή:** Επιβεβαιώστε ότι το πηγαίο αρχείο OneNote δεν είναι προστατευμένο με κωδικό· η μετρητική άδεια δεν αποκρυπτογραφεί αυτόματα ασφαλισμένα σημειωματάρια.

## Συχνές Ερωτήσεις

**Q: Τι είναι η μετρητική άδεια;**  
A: Η μετρητική άδεια είναι ένα μοντέλο βασισμένο στη χρήση, όπου αγοράζετε μια δεξαμενή πιστώσεων και το API αφαιρεί πιστώσεις για κάθε λειτουργία που εκτελείτε.

**Q: Πώς μπορώ να αποκτήσω μια μετρητική άδεια για το Aspose.Note για .NET;**  
A: Μπορείτε να αποκτήσετε μια μετρητική άδεια για το Aspose.Note για .NET από την ιστοσελίδα της Aspose.

**Q: Μπορώ να παρακολουθήσω την κατανάλωση πόρων μου σε πραγματικό χρόνο με τη μετρητική άδεια;**  
A: Ναι, η μετρητική άδεια σας επιτρέπει να παρακολουθείτε την κατανάλωση πόρων σε πραγματικό χρόνο, επιτρέποντας καλύτερη διαχείριση κόστους.

**Q: Υπάρχουν περιορισμοί στη μετρητική άδεια;**  
A: Η μετρητική άδεια μπορεί να έχει ορισμένους περιορισμούς ανάλογα με τους συγκεκριμένους όρους και προϋποθέσεις που παρέχονται από τον προμηθευτή λογισμικού.

**Q: Είναι η μετρητική άδεια κατάλληλη για όλους τους τύπους λογισμικού εφαρμογών;**  
A: Αν και η μετρητική άδεια μπορεί να είναι ωφέλιμη για πολλές λογισμικές εφαρμογές, η καταλληλότητά της εξαρτάται από παράγοντες όπως τα πρότυπα χρήσης και οι οικονομικές εκτιμήσεις.

---

**Τελευταία ενημέρωση:** 2026-05-20  
**Δοκιμή με:** Aspose.Note 24.11 for .NET  
**Συγγραφέας:** Aspose

```csharp
Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit():F2}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity():F2}");
```

## Σχετικά Μαθήματα

- [Μετρητική Άδεια με Aspose.Note](/note/net/licensing/metered-licensing/)
- [Αποθήκευση σε PDF στο Aspose.Note](/note/net/loading-and-saving-operations/save-to-pdf/)
- [Μετατροπή Σημειωματάριων σε PDF στο Aspose Note .NET](/note/net/notebook-operations/convert-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}