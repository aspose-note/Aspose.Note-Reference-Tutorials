---
date: 2026-03-19
description: Apprenez comment ajouter une image à OneNote en utilisant Aspose.Note
  pour Java. Ce guide étape par étape montre comment créer des documents OneNote,
  insérer une image dans OneNote et enregistrer OneNote au format PDF.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Comment ajouter une image à OneNote avec Java – Créer le document et insérer
  l’image
url: /fr/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajouter une image à OneNote avec Java – Créer un document et insérer une image

## Introduction

Dans ce tutoriel, vous apprendrez **comment ajouter une image à OneNote** en utilisant l'API Aspose.Note Java. Nous parcourrons la création d'un document OneNote à partir de zéro, l'insertion d'une image, et l'enregistrement du résultat au format PDF. Que vous construisiez un outil de reporting, automatisiez la prise de notes, ou ayez simplement besoin d'intégrer des graphiques par programmation, ce guide vous offre une voie claire et pratique.

## Réponses rapides
- **Quelle bibliothèque est nécessaire ?** Aspose.Note for Java.  
- **Puis-je insérer n'importe quel format d'image ?** JPEG, PNG, BMP, GIF et plus sont pris en charge.  
- **Quels formats de sortie sont disponibles ?** Vous pouvez enregistrer en OneNote, PDF, XPS, HTML, etc.  
- **Ai‑je besoin d'une licence pour la production ?** Oui, une licence commerciale est requise pour une utilisation non‑essai.  
- **Le code est‑il multiplateforme ?** Absolument – Java fonctionne sous Windows, Linux et macOS.

## Comment ajouter une image à OneNote avec Java

Ajouter une image à OneNote signifie intégrer de façon programmatique un fichier image dans une page OneNote afin qu'il apparaisse aux côtés du texte, des contours ou d'autres éléments. L'API Aspose.Note abstrait le format de fichier OneNote, vous permettant de vous concentrer sur le contenu plutôt que sur la structure XML sous‑jacente.

### Pourquoi intégrer une image dans OneNote ?

- **Automatisation :** Générer automatiquement des comptes‑rendus de réunions avec captures d'écran.  
- **Cohérence :** Garantir que chaque page suit la même mise en page et la même identité visuelle.  
- **Intégration :** Combiner des données provenant d'autres systèmes (par ex. des graphiques) directement dans les carnets OneNote.  
- **Multiplateforme :** Java vous permet d'exécuter le même code sur n'importe quel serveur ou poste de travail.

## Prérequis

Avant de commencer, assurez‑vous de disposer de ce qui suit :

1. **Java Development Kit (JDK)** – toute version récente (8 ou supérieure).  
2. **Aspose.Note for Java library** – téléchargez‑la depuis le [site web](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, ou tout éditeur compatible Java que vous préférez.  

## Importer les packages

Commencez par importer les classes nécessaires dans votre fichier source Java :

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Guide étape par étape

### Étape 1 : Configurer le document

Créez un nouveau document OneNote et un conteneur de page où le contenu sera placé.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Étape 2 : Initialiser le contour

Un *outline* agit comme un conteneur pour des éléments tels que le texte et les images. Nous définissons ses décalages à zéro afin que le contenu commence en haut à gauche.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Étape 3 : Charger et aligner l'image

Chargez l'image que vous souhaitez intégrer et alignez‑la sur le côté droit de la page. C’est ici que nous **ajoutons réellement une image à OneNote**. Le constructeur `Image` montre comment **charger un fichier image en Java** côté code.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Étape 4 : Attacher l'image à un élément d'outline

Enveloppez l'image dans un `OutlineElement`. Cette étape lie l'objet visuel à la hiérarchie d'outline du document et **insère effectivement l'image dans OneNote**.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Étape 5 : Assembler la structure du document

Ajoutez l'élément d'outline à l'outline, puis attachez l'outline à la page, et enfin ajoutez la page au document.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Étape 6 : Enregistrer le document OneNote

Persistez le document sur le disque. Dans cet exemple nous exportons en PDF, ce qui montre comment **enregistrer OneNote en PDF** ou **convertir OneNote en PDF**. Vous pouvez également enregistrer au format natif OneNote (`.one`) en modifiant le `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **Image non affichée** | Chemin de fichier incorrect ou format non pris en charge. | Vérifiez que `dataDir` pointe vers le bon dossier et utilisez un type d'image supporté (JPEG, PNG, etc.). |
| **Document enregistré en PDF vide** | Décalages de l'outline définis incorrectement. | Assurez‑vous que `setVerticalOffset(0)` et `setHorizontalOffset(0)` sont appelés, ou ajustez les décalages pour placer le contenu à l'intérieur des limites de la page. |
| **IOException lors de l'enregistrement** | Le dossier de destination n'existe pas ou n'a pas les permissions d'écriture. | Créez le dossier au préalable ou exécutez le programme avec les permissions appropriées. |

## Questions fréquentes

**Q1 : Où puis‑je trouver la documentation d'Aspose.Note pour Java ?**  
R1 : Vous pouvez accéder à la documentation [ici](https://reference.aspose.com/note/java/).

**Q2 : Comment télécharger Aspose.Note pour Java ?**  
R2 : Vous pouvez télécharger Aspose.Note pour Java depuis la [page de téléchargement](https://releases.aspose.com/note/java/).

**Q3 : Existe‑t‑il une version d'essai gratuite d'Aspose.Note pour Java ?**  
R3 : Oui, vous pouvez obtenir une version d'essai gratuite depuis le [site web](https://releases.aspose.com/).

**Q4 : Où puis‑je obtenir du support pour Aspose.Note pour Java ?**  
R4 : Pour le support, visitez le [forum Aspose.Note](https://forum.aspose.com/c/note/28).

**Q5 : Puis‑je obtenir une licence temporaire pour Aspose.Note pour Java ?**  
R5 : Oui, vous pouvez demander une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

**Q6 : Puis‑je utiliser ce code pour **enregistrer OneNote en PDF** sur un serveur Linux ?**  
R6 : Absolument. La bibliothèque Aspose.Note est indépendante de la plateforme, donc le même code fonctionne sous Windows, Linux et macOS.

**Q7 : L'API prend‑elle en charge **l'intégration d'image dans OneNote** avec des PNG transparents ?**  
R7 : Oui, les fichiers PNG avec canal alpha sont entièrement pris en charge et conservent leur transparence lorsqu'ils sont insérés.

---

**Dernière mise à jour :** 2026-03-19  
**Testé avec :** Aspose.Note for Java 24.12 (latest)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}