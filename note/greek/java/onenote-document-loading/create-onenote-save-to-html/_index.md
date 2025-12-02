---
date: 2025-12-02
description: Μάθετε πώς να εξάγετε γραμματοσειρές ενώ αποθηκεύετε το OneNote ως HTML
  χρησιμοποιώντας το Aspose.Note για Java. Αυτός ο οδηγός σας δείχνει πώς να δημιουργήσετε
  το OneNote προγραμματιστικά και να ενσωματώσετε γραμματοσειρές, CSS και εικόνες.
language: el
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Πώς να εξάγετε τις γραμματοσειρές κατά την αποθήκευση του OneNote ως HTML –
  Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Εξάγετε Γραμματοσειρές Κατά την Αποθήκευση του OneNote ως HTML – Java

## Εισαγωγή

Σε αυτό το σεμινάριο θα ανακαλύψετε **πώς να εξάγετε γραμματοσειρές** όταν **αποθηκεύετε το OneNote ως HTML** χρησιμοποιώντας το Aspose.Note for Java. Θα περάσουμε από τη δημιουργία ενός εγγράφου OneNote προγραμματιστικά, τη διαμόρφωση των επιλογών αποθήκευσης HTML και την ενσωμάτωση των απαιτούμενων αρχείων γραμματοσειρών ώστε το παραγόμενο HTML να φαίνεται ακριβώς όπως οι αρχικές σελίδες OneNote. Αυτή η προσέγγιση είναι ιδανική όταν χρειάζεται να διατηρήσετε την οπτική πιστότητα του περιεχομένου OneNote σε μορφή φιλική προς το web.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται την εξαγωγή;** Aspose.Note for Java  
- **Μπορούν οι γραμματοσειρές να ενσωματωθούν στο HTML;** Ναι – ορίστε `ExportFonts` σε `ExportEmbedded`  
- **Χρειάζομαι άδεια για παραγωγή;** Απαιτείται έγκυρη άδεια Aspose.Note για εμπορική χρήση  
- **Ποια έκδοση της Java υποστηρίζεται;** Java 8 ή νεότερη  
- **Μπορεί να αποθηκευτούν οι πόροι σε ξεχωριστά αρχεία;** Απόλυτα – ρυθμίστε το `ResourceExportType` ανάλογα  

## Τι σημαίνει «πώς να εξάγετε γραμματοσειρές» στο πλαίσιο της μετατροπής OneNote σε HTML;

Όταν μετατρέπετε ένα σημειωματάριο OneNote σε HTML, η οπτική εμφάνιση εξαρτάται από CSS, εικόνες και ιδιαίτερα τις γραμματοσειρές που χρησιμοποιούνται στις αρχικές σελίδες. **Η εξαγωγή γραμματοσειρών** σημαίνει την ενσωμάτωση των αρχείων γραμματοσειρών (π.χ., TTF) απευθείας στο πακέτο HTML, ώστε οι browsers να μπορούν να αποδώσουν το κείμενο ακριβώς όπως εμφανίζεται στο OneNote, ακόμη και αν ο τελικός χρήστης δεν έχει αυτές τις γραμματοσειρές εγκατεστημένες τοπικά.

## Γιατί να δημιουργήσετε OneNote προγραμματιστικά και να το αποθηκεύσετε ως HTML;

- **Αυτοματοποίηση:** Δημιουργήστε αναφορές, τεκμηρίωση ή άρθρα βάσης γνώσεων από το OneNote χωρίς χειροκίνητη αντιγραφή‑επικόλληση.  
- **Συνέπεια:** Διατηρήστε τη διάταξη, το στυλ και τις προσαρμοσμένες γραμματοσειρές σε όλες τις συσκευές.  
- **Φορητότητα:** Το HTML είναι καθολικά προβλέψιμο—δεν χρειάζεται ο πελάτης OneNote.  

## Προαπαιτούμενα

1. Java Development Kit (JDK) 8 ή νεότερο εγκατεστημένο.  
2. Βιβλιοθήκη Aspose.Note for Java – κατεβάστε από [here](https://releases.aspose.com/note/java/).  
3. Ένα δείγμα αρχείου OneNote (`.one`) για φόρτωση, ή μπορείτε να δημιουργήσετε ένα νέο προγραμματιστικά.  

## Εισαγωγή Πακέτων

Πρώτα, εισάγετε τις απαιτούμενες κλάσεις στο έργο Java σας:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Πώς να Εξάγετε Γραμματοσειρές Κατά την Αποθήκευση του OneNote ως HTML;

Παρακάτω υπάρχει ένας οδηγός βήμα‑βήμα που σας δείχνει **πώς να εξάγετε γραμματοσειρές** και άλλους πόρους.

### Βήμα 1: Δημιουργία εγγράφου OneNote προγραμματιστικά  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Αυτή η γραμμή φορτώνει ένα υπάρχον αρχείο `.one`. Αν χρειαστεί να **δημιουργήσετε OneNote προγραμματιστικά**, μπορείτε να δημιουργήσετε ένα νέο αντικείμενο `Document` και να προσθέσετε ενότητες/σελίδες μέσω του API (δεν εμφανίζεται εδώ για να διατηρηθεί η εστίαση στην εξαγωγή γραμματοσειρών).

### Βήμα 2: Αποθήκευση σε ροή μνήμης με ενσωματωμένες γραμματοσειρές  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` λέει στο Aspose.Note να **εξάγει γραμματοσειρές** απευθείας στο πακέτο HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` εξασφαλίζει ότι χρησιμοποιούνται TrueType γραμματοσειρές, οι οποίες υποστηρίζονται ευρέως από τους browsers.

### Βήμα 3: Αποθήκευση ως HTML με ξεχωριστά αρχεία πόρων (συνεχίζοντας την εξαγωγή γραμματοσειρών)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Ακόμη και αν τα CSS και οι εικόνες είναι ενσωματωμένα, μπορείτε να αλλάξετε το `ResourceExportType` σε `ExportExternal` εάν προτιμάτε ξεχωριστά αρχεία για ευκολότερη caching. Το βασικό μέρος—**η εξαγωγή γραμματοσειρών**—παραμένει αμετάβλητο.

### Βήμα 4: Χρήση callbacks για έλεγχο του πού αποθηκεύεται κάθε πόρος  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Η κλάση `UserSavingCallbacks` (θα χρειαστεί να υλοποιήσετε `ICssSavingCallback`, `IImageSavingCallback` και `IFontSavingCallback`) σας δίνει πλήρη έλεγχο στη δομή των φακέλων, επιτρέποντάς σας να κρατήσετε τις γραμματοσειρές σε έναν αφιερωμένο φάκελο `fonts` ενώ εξακολουθείτε να **εξάγετε γραμματοσειρές** σωστά.

## Κοινά Προβλήματα & Συμβουλές

- **Λείπουν γραμματοσειρές στο αποτέλεσμα:** Επαληθεύστε ότι το `setExportFonts(ResourceExportType.ExportEmbedded)` είναι ορισμένο και ότι το πηγαίο αρχείο OneNote χρησιμοποιεί πράγματι ενσωματωμένες γραμματοσειρές.  
- **Μεγάλα αρχεία HTML:** Η ενσωμάτωση γραμματοσειρών μπορεί να αυξήσει το μέγεθος. Αν το εύρος ζώνης είναι πρόβλημα, αλλάξτε το `ExportFonts` σε `ExportExternal` και φιλοξενήστε τις γραμματοσειρές σε CDN.  
- **Σφάλματα υλοποίησης callbacks:** Βεβαιωθείτε ότι οι κλάσεις callbacks γράφουν σωστά τη ροή και κλείνουν τους πόρους για να αποφύγετε τη διαφθορά αρχείων.  

## Συχνές Ερωτήσεις

**Ε: Μπορώ να μετατρέψω πολλά έγγραφα OneNote σε HTML με μία ενέργεια;**  
Α: Ναι, κάντε βρόχο σε κάθε αντικείμενο `Document` και εφαρμόστε τις ίδιες `HtmlSaveOptions`.  

**Ε: Υποστηρίζει το Aspose.Note for Java άλλες μορφές εξόδου εκτός από HTML;**  
Α: Απόλυτα. Μπορείτε να εξάγετε σε PDF, DOCX, PNG, JPEG και άλλα χρησιμοποιώντας τις αντίστοιχες επιλογές αποθήκευσης.  

**Ε: Υπάρχει δοκιμαστική έκδοση του Aspose.Note for Java;**  
Α: Ναι, κατεβάστε μια δωρεάν δοκιμή από [here](https://releases.aspose.com/).  

**Ε: Πού μπορώ να λάβω υποστήριξη για το Aspose.Note for Java;**  
Α: Επισκεφθείτε το [Aspose.Note forum](https://forum.aspose.com/c/note/28) για κοινότητα και επίσημη βοήθεια.  

**Ε: Πώς μπορώ να αγοράσω άδεια για το Aspose.Note for Java;**  
Α: Οι άδειες διατίθενται στην [Aspose website](https://purchase.aspose.com/buy).  

## Συμπέρασμα

Τώρα γνωρίζετε **πώς να εξάγετε γραμματοσειρές** ενώ **αποθηκεύετε το OneNote ως HTML** χρησιμοποιώντας το Aspose.Note for Java. Διαμορφώνοντας τις `HtmlSaveOptions` και, προαιρετικά, χρησιμοποιώντας callbacks, μπορείτε να διατηρήσετε την ακριβή εμφάνιση των σελίδων OneNote—συμπεριλαμβανομένων των προσαρμοσμένων γραμματοσειρών—κατά τη διανομή τους στο web. Μη διστάσετε να πειραματιστείτε με διαφορετικές ρυθμίσεις `ResourceExportType` ώστε να ταιριάζουν στις απαιτήσεις απόδοσης και αποθήκευσης του έργου σας.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Τελευταία Ενημέρωση:** 2025-12-02  
**Δοκιμάστηκε Με:** Aspose.Note for Java 24.12  
**Συγγραφέας:** Aspose  

---