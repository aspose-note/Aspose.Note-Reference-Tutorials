---
date: 2026-05-05
description: Apprenez à insérer une image dans les documents Aspose.Note en utilisant
  .NET. Ce guide étape par étape vous montre comment aligner l'image, ajouter une
  image à la page et améliorer le contenu visuel.
keywords:
- how to insert image
- how to align image
- append image to page
linktitle: Insérer des images dans les documents Aspose.Note
second_title: Aspose.Note .NET API
title: Comment insérer une image dans les documents Aspose.Note avec .NET
url: /fr/net/images/insert-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment insérer une image dans les documents Aspose.Note avec .NET

## Introduction

Si vous cherchez à rendre vos fichiers Aspose.Note plus attrayants, **how to insert image** est la première compétence que vous voudrez maîtriser. Dans ce tutoriel, nous parcourrons les étapes exactes nécessaires pour ajouter des images, contrôler leur taille, les positionner précisément, et même les aligner comme vous le souhaitez. À la fin, vous serez à l’aise pour insérer des images, les aligner et les ajouter à la page — le tout avec du code C# propre et lisible.

## Réponses rapides
- **Quelle bibliothèque est requise ?** Aspose.Note for .NET  
- **Puis-je définir la taille de l'image par programme ?** Oui – utilisez les propriétés Width et Height.  
- **Comment positionner une image ?** Ajustez HorizontalOffset, VerticalOffset ou utilisez les options d'alignement.  
- **Y a-t-il une limite sur les formats d'image ?** JPG, PNG, BMP, GIF et d'autres sont pris en charge.  
- **Ai-je besoin d'une licence pour la production ?** Une licence valide Aspose.Note est requise pour une utilisation commerciale.

## Qu'est-ce que l'insertion d'image dans Aspose.Note ?

Insérer une image signifie créer un objet Aspose.Note.Image, configurer ses propriétés visuelles et l'attacher à une page dans un fichier .one compatible OneNote. Cela vous permet d'enrichir les notes avec des captures d'écran, des diagrammes ou tout autre support visuel.

## Pourquoi insérer des images avec Aspose.Note ?

- **Meilleure communication :** Les visuels clarifient les idées complexes plus rapidement que le texte seul.  
- **Mise en page cohérente :** Le contrôle programmatique garantit que chaque document suit les mêmes normes de conception.  
- **Facile à automatiser :** Idéal pour générer des rapports, des tutoriels ou des blocs-notes traités par lots.

## Prérequis

1. Aspose.Note for .NET : Téléchargez et installez Aspose.Note for .NET depuis [here](https://releases.aspose.com/note/net/).  
2. Fichiers image : Ayez les fichiers image (JPG, PNG, etc.) que vous prévoyez d'intégrer prêts sur le disque.

## Importer les espaces de noms

Nous commençons par importer les espaces de noms qui nous donnent accès aux entrées/sorties de fichiers et à l'API Aspose.Note.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## Étape 1 : Charger le document et obtenir la page

Tout d'abord, ouvrez le document .one existant et récupérez la page où l'image sera placée.

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## Comment aligner l'image

Avant d'ajouter l'image, décidez comment elle doit s'aligner avec le reste du contenu. Aspose.Note propose des options d'alignement horizontal (Left, Center, Right). Vous pouvez également affiner le placement avec des valeurs de décalage.

## Étape 2 : Charger l'image et définir les propriétés

Créez l'objet Image, pointez-le vers votre fichier et définissez ses dimensions, décalages et alignement.

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // Set image width
    Height = 100,               // Set image height
    HorizontalOffset = 100,     // Set horizontal offset
    VerticalOffset = 400,       // Set vertical offset
    Alignment = HorizontalAlignment.Right  // Set image alignment
};
```

## Ajouter l'image à la page

Maintenant que l'image est entièrement configurée, attachez‑la à l'arbre d'éléments de la page.

```csharp
page.AppendChildLast(image);
```

## Pièges courants et conseils

- **Décalages incorrects :** Rappelez‑vous que les décalages sont mesurés depuis le coin supérieur gauche de la page. Un grand décalage vertical peut pousser l'image hors de l'écran.  
- **Format non pris en charge :** Si vous essayez un format non reconnu, Aspose.Note lèvera une exception — convertissez d'abord le fichier en JPG ou PNG.  
- **Avertissements de licence :** Exécuter sans licence ajoute un filigrane au document généré ; appliquez toujours votre licence en production.

## Conclusion

Vous avez maintenant appris **how to insert image** dans un document Aspose.Note, comment **how to align image**, et comment **append image to page** en utilisant quelques lignes simples de C#. Ces techniques vous permettent de créer automatiquement des blocs‑notes plus riches et plus professionnels.

## FAQ

### Q1 : Puis‑je insérer des images de n'importe quel format dans les documents Aspose.Note ?

A1 : Oui, Aspose.Note prend en charge divers formats d'image, notamment JPG, PNG, BMP, GIF, etc.

### Q2 : Est‑il possible de redimensionner les images insérées par programme ?

A2 : Absolument ! Vous pouvez ajuster la largeur et la hauteur des images selon vos préférences lors de l'insertion.

### Q3 : Aspose.Note offre‑t‑il des options pour modifier l'alignement des images ?

A3 : Oui, vous pouvez aligner les images à gauche, à droite ou au centre sur les pages de votre document.

### Q4 : Puis‑je insérer plusieurs images sur une même page de mon document ?

A4 : Bien sûr ! Vous pouvez insérer autant d'images que nécessaire sur une même page en utilisant Aspose.Note.

### Q5 : Existe‑t‑il une limite de taille de fichier pour les images pouvant être insérées ?

A5 : Aspose.Note n'impose pas de limites strictes sur la taille des fichiers image, mais il est recommandé d'optimiser les images pour de meilleures performances.

## Questions fréquemment posées

**Q : Comment charger une image depuis un flux au lieu d'un chemin de fichier ?**  
A : Utilisez le constructeur Image(Stream, Document) et passez un MemoryStream contenant les octets de l'image.

**Q : Puis‑je modifier l'image après qu'elle a été ajoutée à la page ?**  
A : Oui, vous pouvez modifier les propriétés Width, Height, HorizontalOffset, VerticalOffset et Alignment de l'objet Image existant, puis appeler page.Update().

**Q : Est‑il possible d'ajouter une légende sous l'image ?**  
A : Insérez un élément RichText après l'image et définissez son texte comme légende.

**Q : Aspose.Note prend‑il en charge les GIF animés ?**  
A : Les GIF animés sont traités comme des images statiques ; seule la première image est affichée.

**Q : Que faire si l'image apparaît floue ?**  
A : Assurez‑vous que l'image source a une résolution suffisante et évitez de l'agrandir au‑delà de sa taille originale.

---

**Last Updated:** 2026-05-05  
**Tested With:** Aspose.Note 23.12 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}