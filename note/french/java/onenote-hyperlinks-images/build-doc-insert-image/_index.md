---
date: 2025-12-20
description: Apprenez à ajouter une image à OneNote en utilisant Aspose.Note pour
  Java. Guide étape par étape pour créer des documents OneNote et insérer des images
  par programmation.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Comment ajouter une image à OneNote avec Java – créer le document et insérer
  l'image
url: /fr/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajouter une image à OneNote avec Java – Créer le document et insérer l'image

## Introduction

Dans ce tutoriel, vous apprendrez **comment ajouter une image à OneNote** en utilisant l'API Aspose.Note pour Java. Nous parcourrons la création d'un document OneNote à partir de zéro, l'insertion d'une image, et l'enregistrement du résultat au format PDF. Que vous construisiez un outil de reporting, automatisiez la prise de notes, ou ayez simplement besoin d'intégrer des graphiques par programme, ce guide vous offre une voie claire et pratique.

## Réponses rapides
- **Quelle bibliothèque est‑elle nécessaire ?** Aspose.Note pour Java.  
- **Puis‑je insérer n’importe quel format d’image ?** JPEG, PNG, BMP, GIF et plus sont pris en charge.  
- **Quels formats de sortie sont disponibles ?** Vous pouvez enregistrer en OneNote, PDF, XPS, HTML, etc.  
- **Ai‑je besoin d’une licence pour la production ?** Oui, une licence commerciale est requise pour une utilisation non‑essai.  
- **Le code est‑il multiplateforme ?** Absolument – Java fonctionne sous Windows, Linux et macOS.

## Qu’est‑ce que « ajouter une image à OneNote » ?
Ajouter une image à OneNote signifie intégrer programmétiquement un fichier image dans une page OneNote afin qu’il apparaisse aux côtés du texte, des contours ou d’autres éléments. L’API Aspose.Note abstrait le format de fichier OneNote, vous permettant de vous concentrer sur le contenu plutôt que sur la structure XML sous‑jacente.

## Pourquoi ajouter une image à OneNote avec Java ?
- **Automatisation :** Générer automatiquement des comptes‑rendus de réunions avec captures d’écran.  
- **Cohérence :** Garantir que chaque page suit la même mise en page et la même identité visuelle.  
- **Intégration :** Combiner des données provenant d’autres systèmes (par ex. des graphiques) directement dans les carnets OneNote.  
- **Multiplateforme :** Java vous permet d’exécuter le même code sur n’importe quel serveur ou poste de travail.

## Pré‑requis

Avant de commencer, assurez‑vous de disposer de :

1. **Java Development Kit (JDK)** – toute version récente (8 ou supérieure).  
2. **Aspose.Note pour Java** – téléchargez‑le depuis le [site web](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, ou tout éditeur compatible Java que vous préférez.  

## Importer les packages

Commencez par importer les classes nécessaires dans votre fichier source Java :

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

Un *contour* agit comme un conteneur pour les éléments tels que le texte et les images. Nous définissons ses décalages à zéro afin que le contenu commence en haut à gauche.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Étape 3 : Charger et aligner l’image

Chargez l’image que vous souhaitez intégrer et alignez‑la à droite de la page. C’est ici que nous **ajoutons réellement une image à OneNote**.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Étape 4 : Attacher l’image à un élément de contour

Enveloppez l’image dans un `OutlineElement`. Cette étape lie l’objet visuel à la hiérarchie du contour du document.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Étape 5 : Assembler la structure du document

Ajoutez l’élément de contour au contour, puis attachez le contour à la page, et enfin ajoutez la page au document.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Étape 6 : Enregistrer le document OneNote

Persistez le document sur le disque. Dans cet exemple nous exportons en PDF, mais vous pouvez également enregistrer au format natif OneNote (`.one`) en modifiant le `SaveFormat`.

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
| **L’image n’apparaît pas** | Chemin de fichier incorrect ou format non pris en charge. | Vérifiez que `dataDir` pointe vers le bon dossier et utilisez un type d’image supporté (JPEG, PNG, etc.). |
| **Document enregistré en PDF vide** | Décalages du contour définis de façon incorrecte. | Assurez‑vous que `setVerticalOffset(0)` et `setHorizontalOffset(0)` sont appelés, ou ajustez les décalages pour placer le contenu à l’intérieur des limites de la page. |
| **IOException lors de l’enregistrement** | Le dossier de destination n’existe pas ou les permissions d’écriture sont insuffisantes. | Créez le dossier au préalable ou exécutez le programme avec les permissions appropriées. |

## Questions fréquentes

**Q1 : Où puis‑je trouver la documentation d’Aspose.Note pour Java ?**  
R1 : Vous pouvez accéder à la documentation [ici](https://reference.aspose.com/note/java/).

**Q2 : Comment télécharger Aspose.Note pour Java ?**  
R2 : Vous pouvez télécharger Aspose.Note pour Java depuis la [page de téléchargement](https://releases.aspose.com/note/java/).

**Q3 : Existe‑t‑il une version d’essai gratuite d’Aspose.Note pour Java ?**  
R3 : Oui, vous pouvez obtenir une version d’essai gratuite depuis le [site web](https://releases.aspose.com/).

**Q4 : Où obtenir du support pour Aspose.Note pour Java ?**  
R4 : Pour le support, visitez le [forum Aspose.Note](https://forum.aspose.com/c/note/28).

**Q5 : Puis‑je obtenir une licence temporaire pour Aspose.Note pour Java ?**  
R5 : Oui, vous pouvez demander une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

---

**Dernière mise à jour :** 2025-12-20  
**Testé avec :** Aspose.Note pour Java 24.12 (dernière version)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}