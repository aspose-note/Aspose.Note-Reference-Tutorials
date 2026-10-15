---
date: 2026-10-15
description: Μάθετε πώς να ορίσετε τον τίτλο σελίδας σε έγγραφο OneNote χρησιμοποιώντας
  το Aspose.Note για .NET. Ακολουθήστε τον βήμα‑βήμα οδηγό μας για τη δημιουργία σελίδων
  με τίτλο και την εφαρμογή του προεπιλεγμένου στυλ κειμένου.
keywords:
- how to set page title
- set default text style
- create titled page
- document with page title
lastmod: 2026-10-15
linktitle: Δημιουργία εγγράφου με τίτλο σελίδας στο Aspose.Note
og_description: Μάθετε πώς να ορίσετε τον τίτλο σελίδας σε έγγραφο OneNote χρησιμοποιώντας
  το Aspose.Note για .NET. Αυτός ο βήμα‑βήμα οδηγός σας δείχνει πώς να δημιουργήσετε
  μια σελίδα με τίτλο, να εφαρμόσετε το προεπιλεγμένο στυλ κειμένου και να αποθηκεύσετε
  το αρχείο.
og_image_alt: 'Aspose.Note tutorial: setting page title in OneNote document with .NET'
og_title: Πώς να ορίσετε τον τίτλο σελίδας σε έγγραφο OneNote χρησιμοποιώντας το Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-10-15'
  description: Learn how to set page title in a OneNote document using Aspose.Note
    for .NET. Follow our step‑by‑step guide for creating titled pages and applying
    default text style.
  headline: How to set page title in OneNote document using Aspose.Note
  type: TechArticle
- description: Learn how to set page title in a OneNote document using Aspose.Note
    for .NET. Follow our step‑by‑step guide for creating titled pages and applying
    default text style.
  name: How to set page title in OneNote document using Aspose.Note
  steps:
  - name: Download Visual Studio from the Microsoft website.
    text: Download Visual Studio from the Microsoft website.
  - name: Select the “.NET desktop development” workload during installation.
    text: Select the “.NET desktop development” workload during installation.
  - name: Create a new console‑application project (or any .NET project type you prefer).
    text: Create a new console‑application project (or any .NET project type you prefer).
  - name: 'Get Aspose.Note: Download the library from the [website](https://releases.aspose.com/note/net/).'
    text: 'Get Aspose.Note: Download the library from the [website](https://releases.aspose.com/note/net/).'
  - name: 'Install via NuGet Package Manager: search for **Aspose.Note** and install
      the latest version.'
    text: 'Install via NuGet Package Manager: search for **Aspose.Note** and install
      the latest version.'
  type: HowTo
- questions:
  - answer: Yes, you can change the font name, size, and color through the `DefaultTextStyle`
      object before assigning the title.
    question: Can I customize the title text style?
  - answer: Absolutely. The library supports .NET Core, .NET 5+, and .NET 6+, enabling
      cross‑platform development.
    question: Is Aspose.Note compatible with .NET Core?
  - answer: Yes. Use the `Image` and `Attachment` classes to embed multimedia content
      alongside your titled page.
    question: Can I add images and attachments to the document?
  - answer: It does. You can load a `.one` file, modify its pages (including titles),
      and save it back.
    question: Does Aspose.Note support reading existing OneNote files?
  - answer: You can find support and assistance on the [Aspose.Note forum](https://forum.aspose.com/c/note/28),
      where experts and community members help with queries.
    question: Where can I find support if I encounter any issues?
  type: FAQPage
second_title: Aspose.Note .NET API
tags:
- Aspose.Note
- OneNote API
- page title
- .NET
- document creation
title: Πώς να ορίσετε τον τίτλο σελίδας σε έγγραφο OneNote χρησιμοποιώντας το Aspose.Note
url: /el/net/loading-and-saving-operations/create-doc-with-page-title/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να ορίσετε τίτλο σελίδας σε έγγραφο OneNote χρησιμοποιώντας το Aspose.Note

## Εισαγωγή

Σε αυτό το σεμινάριο θα μάθετε **πώς να ορίσετε τίτλο σελίδας** κατά τη δημιουργία ενός εγγράφου OneNote με το Aspose.Note για .NET. Η ρύθμιση του τίτλου σελίδας βελτιώνει την πλοήγηση, την δυνατότητα αναζήτησης και τη συνολική αναγνωσιμότητα των σημειωματάριων OneNote. Θα περάσουμε από κάθε βήμα, από τη ρύθμιση του έργου μέχρι την αποθήκευση του τελικού αρχείου, και θα σας δείξουμε πώς να εφαρμόσετε ένα προεπιλεγμένο στυλ κειμένου στον τίτλο.

## Γρήγορες απαντήσεις
- **Τι σημαίνει “page title”;** Το κείμενο που εμφανίζεται στην κορυφή μιας σελίδας OneNote και λειτουργεί ως επικεφαλίδα της.  
- **Ποια κλάση API δημιουργεί τον τίτλο;** Η ιδιότητα `PageTitle` της κλάσης `Page`.  
- **Χρειάζομαι άδεια για να εκτελέσω το παράδειγμα;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.  
- **Υποστηρίζεται το .NET Core;** Ναι – το Aspose.Note λειτουργεί σε .NET Core, .NET 5+ και .NET 6+.  
- **Μπορώ να προσαρμόσω τη γραμματοσειρά του τίτλου;** Απόλυτα – μπορείτε να ορίσετε το όνομα, το μέγεθος και το χρώμα της γραμματοσειράς μέσω του αντικειμένου `DefaultTextStyle`.

## Τι είναι η ρύθμιση τίτλου σελίδας;
**how to set page title** είναι η διαδικασία ανάθεσης μιας συμβολοσειράς επικεφαλίδας στο στοιχείο `Title` μιας σελίδας OneNote μέσω του API του Aspose.Note. Αυτή η ενέργεια εκτελείται πριν προστεθεί η σελίδα στην ιεραρχία του εγγράφου, και εξασφαλίζει ότι ο τίτλος εμφανίζεται σωστά στη διεπαφή του OneNote και μπορεί να χρησιμοποιηθεί για αναζήτηση και οργάνωση των σελίδων μέσα σε ένα σημειωματάριο.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για τον ορισμό τίτλου σελίδας;
Το Aspose.Note υποστηρίζει **πάνω από 30 μορφές εισόδου και εξόδου** και μπορεί να χειριστεί σημειωματάρια που περιέχουν **έως 10.000 σελίδες** χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη. Η βιβλιοθήκη διαχειρίζεται αυτόματα χαρακτήρες Unicode, γραφές από δεξιά προς αριστερά και σύνθετη μορφοποίηση, κάτι που σας εξοικονομεί το γράψιμο χαμηλού επιπέδου κώδικα XML του OneNote.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε εγκαταστήσει και ρυθμίσει τα παρακάτω προαπαιτούμενα:

### Εγκατάσταση Visual Studio

1. Κατεβάστε το Visual Studio από την ιστοσελίδα της Microsoft.  
2. Επιλέξτε το workload “.NET desktop development” κατά την εγκατάσταση.  
3. Δημιουργήστε ένα νέο έργο console‑application (ή οποιονδήποτε τύπο .NET έργου προτιμάτε).

### Εγκατάσταση Aspose.Note

1. Αποκτήστε το Aspose.Note: Κατεβάστε τη βιβλιοθήκη από το [website](https://releases.aspose.com/note/net/).  
2. Εγκαταστήστε μέσω του NuGet Package Manager: αναζητήστε **Aspose.Note** και εγκαταστήστε την πιο πρόσφατη έκδοση.

## Εισαγωγή namespaces

Τα παρακάτω namespaces σας δίνουν πρόσβαση στις βασικές κλάσεις του Aspose.Note:

```text
using Aspose.Note;
using Aspose.Note.Drawing;
using Aspose.Note.Rendering;
```

Τώρα, ας αναλύσουμε τη διαδικασία δημιουργίας ενός εγγράφου με τίτλο σελίδας σε πολλαπλά βήματα:

## Πώς να ορίσετε τίτλο σελίδας σε έγγραφο OneNote

Φορτώστε ένα νέο αντικείμενο `Document`, δημιουργήστε ένα `Page`, ορίστε το κείμενο του τίτλου, εφαρμόστε ένα προεπιλεγμένο στυλ και, τέλος, αποθηκεύστε το αρχείο. Ολόκληρη αυτή η ροή εργασίας απαιτεί μόνο λίγες γραμμές κώδικα και δεν χρειάζεται χειροκίνητη διαχείριση XML.

## Βήμα 1: δημιουργία αντικειμένου εγγράφου

Η κλάση `Document` αντιπροσωπεύει ένα σημειωματάριο OneNote στη μνήμη, το οποίο μπορεί να περιέχει πολλαπλές σελίδες και ενότητες.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

## Βήμα 2: αρχικοποίηση αντικειμένου κλάσης Page

Τα αντικείμενα `Page` μοντελοποιούν μεμονωμένες σελίδες μέσα σε ένα σημειωματάριο OneNote και περιέχουν περιεχόμενο όπως τίτλο, περιγράμματα και εικόνες.

```csharp
// Create an object of the Document class
Document doc = new Aspose.Note.Document();
```

## Βήμα 3: ορισμός προεπιλεγμένου στυλ για κείμενο

Το `DefaultTextStyle` ορίζει την προεπιλεγμένη οικογένεια γραμματοσειράς, το μέγεθος και το χρώμα που εφαρμόζονται στα στοιχεία κειμένου όταν δημιουργούνται.

```csharp
// Initialize Page class object
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Βήμα 4: ορισμός ιδιοτήτων τίτλου σελίδας

Η ιδιότητα `Title` ενός `Page` περιέχει τις πληροφορίες της επικεφαλίδας, συμπεριλαμβανομένου του κειμένου, της ημερομηνίας και της ώρας.

```csharp
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## Βήμα 5: προσθήκη κόμβου σελίδας στο έγγραφο

Η μέθοδος `Document.Pages.Add` εισάγει τη νεοδημιουργημένη `Page` στη συλλογή σελίδων του σημειωματάριου, καθορίζοντας τη θέση της.

```csharp
// Set page title properties
page.Title = new Title()
{
    TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
};
```

## Βήμα 6: αποθήκευση εγγράφου OneNote

Η μέθοδος `Document.Save` γράφει το σημειωματάριο σε αρχείο με τη συγκεκριμένη μορφή, όπως `.one` για το OneNote.

```csharp
// Append Page node in the document
doc.AppendChildLast(page);
```

## Συχνά προβλήματα και λύσεις

- **Ο τίτλος δεν εμφανίζεται** – Βεβαιωθείτε ότι έχετε ορίσει την ιδιότητα `Title` *πριν* προσθέσετε τη σελίδα στο έγγραφο.  
- **Λανθασμένη απόδοση γραμματοσειράς** – Επαληθεύστε ότι η γραμματοσειρά που καθορίζετε είναι εγκατεστημένη στον προορισμό; διαφορετικά το Aspose.Note θα επιστρέψει σε προεπιλεγμένη γραμματοσειρά.  
- **Μεγάλα σημειωματάρια προκαλούν πίεση μνήμης** – Χρησιμοποιήστε το `Document.Load` με τις `LoadOptions` που ενεργοποιούν lazy loading για πολύ μεγάλα αρχεία.

## Συχνές ερωτήσεις

**Q: Μπορώ να προσαρμόσω το στυλ κειμένου του τίτλου;**  
A: Ναι, μπορείτε να αλλάξετε το όνομα, το μέγεθος και το χρώμα της γραμματοσειράς μέσω του αντικειμένου `DefaultTextStyle` πριν αναθέσετε τον τίτλο.

**Q: Είναι το Aspose.Note συμβατό με το .NET Core;**  
A: Απόλυτα. Η βιβλιοθήκη υποστηρίζει .NET Core, .NET 5+ και .NET 6+, επιτρέποντας ανάπτυξη πολλαπλών πλατφορμών.

**Q: Μπορώ να προσθέσω εικόνες και συνημμένα στο έγγραφο;**  
A: Ναι. Χρησιμοποιήστε τις κλάσεις `Image` και `Attachment` για να ενσωματώσετε πολυμέσα μαζί με τη σελίδα με τίτλο.

**Q: Υποστηρίζει το Aspose.Note την ανάγνωση υπαρχόντων αρχείων OneNote;**  
A: Ναι. Μπορείτε να φορτώσετε ένα αρχείο `.one`, να τροποποιήσετε τις σελίδες του (συμπεριλαμβανομένων των τίτλων) και να το αποθηκεύσετε ξανά.

**Q: Πού μπορώ να βρω υποστήριξη αν αντιμετωπίσω προβλήματα;**  
A: Μπορείτε να βρείτε υποστήριξη και βοήθεια στο [Aspose.Note forum](https://forum.aspose.com/c/note/28), όπου ειδικοί και μέλη της κοινότητας βοηθούν με ερωτήματα.

---

**Τελευταία ενημέρωση:** 2026-10-15  
**Δοκιμάστηκε με:** Aspose.Note 24.11 for .NET  
**Συγγραφέας:** Aspose  

```csharp
// Save OneNote document
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## Σχετικά Σεμινάρια

- [Αλλαγή στυλ τίτλου σελίδας στο Aspose.Note](/note/net/text-manipulation/change-page-title-style/)
- [Δημιουργία τίτλου με στυλ MS στο Aspose.Note](/note/net/text-manipulation/create-title-ms-style/)
- [Ορισμός προεπιλεγμένου στυλ παραγράφου στο Aspose.Note](/note/net/text-manipulation/set-default-paragraph-style/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}