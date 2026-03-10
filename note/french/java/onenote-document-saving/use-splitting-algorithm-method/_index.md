---
date: 2025-12-18
description: Apprenez à exporter des pages OneNote au format PDF à l'aide d'Aspose.Note
  pour Java. Choisissez les algorithmes de division, définissez le fractionnement
  des pages et générez facilement des fichiers PDF.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Exporter les pages OneNote avec la méthode d’algorithme de fractionnement –
  Aspose.Note
url: /fr/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter des pages OneNote avec la méthode d'algorithme de fractionnement – Aspose.Note

## Introduction

Si vous devez **exporter des pages OneNote** vers un document PDF de façon programmatique, Aspose.Note for Java le rend simple. Dans ce tutoriel, nous parcourrons la Méthode d'algorithme de fractionnement, qui vous permet de contrôler comment le contenu est découpé entre les pages, garantissant une sortie PDF propre et lisible. Vous verrez comment définir les options d’enregistrement PDF, choisir le bon algorithme de fractionnement de page, puis générer le fichier PDF — le tout en quelques lignes de code Java.

## Réponses rapides
- **What does the Splitting Algorithm do?** It determines how objects that span page boundaries are handled when exporting OneNote pages to PDF.  
- **Which library is required?** Aspose.Note for Java (download from the official Aspose site).  
- **Do I need a license?** A temporary or full license is required for production use; a free trial is available.  
- **Can I export large OneNote notebooks?** Yes – the library efficiently processes large files and lets you set page‑splitting rules.  
- **What output formats are supported?** PDF, JPEG, PNG, XPS, and more; this guide focuses on PDF export.

## Qu’est‑ce que **exporter des pages OneNote** ?
Exporter des pages OneNote signifie convertir le format natif `.one` en un format plus portable tel que le PDF. Cela est utile pour partager, archiver ou imprimer le contenu sans nécessiter l’application OneNote.

## Pourquoi utiliser l'algorithme de fractionnement pour **exporter des pages OneNote** ?
L'algorithme vous offre un contrôle fin sur la façon dont les objets complexes (tables, images, dessins) sont gérés aux sauts de page. En sélectionnant l'algorithme approprié, vous pouvez :

* Conserver la mise en page visuelle de chaque page.  
* Éviter le contenu tronqué qui serait autrement coupé.  
* Réduire le nombre de pages générées lorsque les objets peuvent être déplacés proprement vers la page suivante.  

## Prérequis

Avant de commencer, assurez‑vous de disposer des prérequis suivants :

1. Java Development Kit (JDK) : Assurez‑vous que le JDK est installé sur votre système. Vous pouvez le télécharger depuis le [site web](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Bibliothèque Aspose.Note for Java : Téléchargez et installez la bibliothèque Aspose.Note for Java depuis le [lien de téléchargement](https://releases.aspose.com/note/java/).

## Importer les packages

Dans votre projet Java, importez les packages nécessaires pour exploiter les fonctionnalités d’Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Étape 1 : définir le répertoire du document

Configurez le répertoire où se trouve votre document OneNote.

```java
String dataDir = "Your Document Directory";
```

## Étape 2 : charger le document OneNote

Chargez le document OneNote en utilisant la classe `Document` d’Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Étape 3 : définir les options d’enregistrement PDF

Créez une instance de `PdfSaveOptions` pour spécifier les options d’enregistrement du document au format PDF. C’est ici que vous **définissez le fractionnement de page** et d’autres paramètres liés au PDF.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Étape 4 : définir l'algorithme de fractionnement de page

Choisissez l’algorithme de fractionnement approprié selon vos besoins. Ici, nous utilisons `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, qui conserve une partie d’un objet sur la page actuelle et clone le reste sur la page suivante.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Étape 5 : enregistrer le document

Enregistrez le document avec les options PDF spécifiées. Cette étape **génère une sortie PDF OneNote** que vous pouvez ouvrir, partager ou imprimer.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Objects are cut off at page boundaries** | Try a different algorithm such as `AlwaysSplitObjectsAlgorithm` or increase the threshold value in `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **Output PDF is blank** | Verify that the source `.one` file is not corrupted and that the `dataDir` path is correct. |
| **Performance is slow with large notebooks** | Use `pdfSaveOptions.setCompressImages(true)` to reduce memory usage, and consider processing the notebook in smaller sections. |

## Questions fréquentes

**Q : Puis‑je utiliser Aspose.Note for Java avec d’autres langages de programmation ?**  
R : Oui, Aspose.Note est également disponible pour .NET, C++ et Python.

**Q : Aspose.Note est‑il adapté au traitement de gros fichiers OneNote ?**  
R : Absolument. La bibliothèque est optimisée pour gérer efficacement de grands blocs‑notes.

**Q : Où puis‑je trouver des ressources supplémentaires et de l’assistance pour Aspose.Note ?**  
R : Vous pouvez consulter la [documentation](https://reference.aspose.com/note/java/) et le [forum](https://forum.aspose.com/c/note/28) pour obtenir de l’aide et des conseils.

**Q : Puis‑je essayer Aspose.Note avant de l’acheter ?**  
R : Oui, vous pouvez profiter d’un [essai gratuit](https://releases.aspose.com/) pour explorer les fonctionnalités avant d’effectuer un achat.

**Q : Comment obtenir une licence temporaire pour Aspose.Note ?**  
R : Vous pouvez demander une [licence temporaire](https://purchase.aspose.com/temporary-license/) afin d’évaluer le produit pendant une période d’essai.

---

**Dernière mise à jour :** 2025-12-18  
**Testé avec :** Aspose.Note 24.12 for Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}