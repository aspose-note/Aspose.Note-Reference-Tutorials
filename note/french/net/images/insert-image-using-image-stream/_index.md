---
date: 2026-04-13
description: Apprenez à ajouter une image aux documents OneNote en utilisant des flux
  d'images dans .NET avec Aspose.Note. Ce guide étape par étape couvre le chargement
  d'images depuis un flux, leur ajout aux outlines et l'enregistrement du fichier.
keywords:
- add image to onenote
- how to insert image
- load image from stream
- append image to outline
- image stream .net
linktitle: Ajouter une image à OneNote via un flux d’image avec Aspose.Note
second_title: Aspose.Note .NET API
title: Ajouter une image à OneNote via un flux d’image avec Aspose.Note
url: /fr/net/images/insert-image-using-image-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter une image à OneNote via le flux d'image avec Aspose.Note

## Introduction

Dans ce tutoriel, vous découvrirez **comment ajouter une image à OneNote** dans des documents en chargeant une image depuis un flux et en l'ajoutant à un contour avec Aspose.Note pour .NET. Que vous construisiez un outil de reporting, une application de prise de notes ou que vous automatisiez la documentation, insérer des images de manière programmatique rend vos fichiers OneNote beaucoup plus attrayants et utiles.

## Réponses rapides
- **Quelle bibliothèque faut‑il ?** Aspose.Note for .NET (essai gratuit disponible).  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Puis‑je charger des images depuis un flux ?** Oui – utilisez `FileStream` ou toute implémentation de `Stream`.  
- **Comment contrôler l'alignement de l'image ?** Définissez la propriété `Alignment` (par ex., `HorizontalAlignment.Right`).  
- **Quel format de fichier est produit ?** Un fichier OneNote (`.one`) qui peut être ouvert dans Microsoft OneNote.

## Qu’est‑ce que “ajouter une image à OneNote” ?

Ajouter une image à un fichier OneNote signifie intégrer un élément visuel directement dans la hiérarchie de contenu d’une page. Avec Aspose.Note, vous travaillez avec des objets tels que `Document`, `Page`, `Outline` et `OutlineElement`. En insérant un objet `Image` dans un `OutlineElement`, l’image devient partie intégrante de la mise en page de la page OneNote.

## Pourquoi utiliser Aspose.Note pour l’insertion d'images ?

- **Aucune installation d’Office requise** – générez ou modifiez des fichiers OneNote sur un serveur.  
- **Contrôle total de la mise en page** – alignez, redimensionnez et positionnez les images exactement où vous le souhaitez.  
- **Compatible avec les flux** – fonctionne avec n’importe quel `Stream`, parfait pour le stockage cloud ou les scénarios en mémoire uniquement.  
- **Multi‑plateforme** – compatible avec les environnements .NET sous Windows, Linux et macOS.

## Prérequis

1. **Environnement de développement** – Visual Studio 2022 ou tout IDE compatible .NET.  
2. **Bibliothèque Aspose.Note** – téléchargez‑la depuis le site officiel [ici](https://releases.aspose.com/note/net/).  
3. **Fichiers image** – au moins une image (JPG, PNG, BMP, GIF ou TIFF) que vous souhaitez intégrer.  
4. **Connaissances de base en C#** – familiarité avec la gestion de fichiers et la programmation orientée objet.

## Importer les espaces de noms
Tout d'abord, importez les espaces de noms qui nous donnent accès aux classes Aspose.Note et aux utilitaires d'E/S standard de .NET.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Maintenant, parcourons le processus étape par étape.

### Étape 1 : Initialiser l’objet Document
Nous commençons par créer une nouvelle instance de `Document` qui contiendra le fichier OneNote.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

### Étape 2 : Créer l’objet Page
Un fichier OneNote se compose d’une ou plusieurs pages. Ici, nous créons une nouvelle page pour héberger notre contenu.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### Étape 3 : Initialiser les objets Outline et OutlineElement
Les contours (Outline) sont des conteneurs pour du contenu riche (texte, images, tableaux). Un `OutlineElement` est un enfant qui détient réellement les éléments.

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```

### Étape 4 : Charger l’image depuis un flux
En utilisant un `FileStream` (ou tout `Stream`) nous lisons le fichier image et créons un objet `Image`. C’est ici que le mot‑clé **load image from stream** brille.

```csharp
using (FileStream fs = File.OpenRead(dataDir + "image.jpg"))
{
    Aspose.Note.Image image1 = new Aspose.Note.Image(doc, "Penguins.jpg", fs)
    {
        Alignment = HorizontalAlignment.Right
    };
    outlineElem1.AppendChildLast(image1);
}
```

### Étape 5 : Ajouter l’image à OutlineElement
L’image fait maintenant partie du `OutlineElement`. Cette étape montre la fonctionnalité **append image to outline**.

```csharp
outlineElem1.AppendChildLast(image1);
```

### Étape 6 : Ajouter OutlineElement à Outline
Nous attachons maintenant l’élément (avec l’image) au conteneur Outline.

```csharp
outline1.AppendChildLast(outlineElem1);
```

### Étape 7 : Ajouter Outline à la Page
Le contour, contenant l’image, est ajouté à la page.

```csharp
page.AppendChildLast(outline1);
```

### Étape 8 : Ajouter la Page au Document
Une fois la page prête, nous l’insérons dans la hiérarchie du document.

```csharp
doc.AppendChildLast(page);
```

### Étape 9 : Enregistrer le Document
Enfin, nous enregistrons le fichier OneNote sur le disque. Le fichier résultant peut être ouvert dans Microsoft OneNote.

```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **Image non affichée** | Le flux a été fermé avant que l’image ne soit ajoutée. | Conservez le bloc `using` autour de l’appel `AppendChildLast` (comme indiqué). |
| **Alignement incorrect** | La propriété `Alignment` n’est pas définie ou est écrasée plus tard. | Définissez `Alignment` lors de la création de l’`Image` ou modifiez `image1.Alignment` avant l’ajout. |
| **Format d’image non pris en charge** | Tentative de chargement d’un format non reconnu par Aspose.Note. | Convertissez l’image en JPG, PNG, BMP, GIF ou TIFF d’abord. |
| **Erreurs de chemin de fichier** | `dataDir` pointe vers un dossier inexistant. | Utilisez `Path.Combine` et vérifiez que le dossier existe avant d’exécuter. |

## Questions fréquentes

**Q : Puis‑je insérer plusieurs images dans un même document avec cette méthode ?**  
R : Oui. Répétez simplement les étapes *Load Image from Stream* et *Append Image to OutlineElement* pour chaque image.

**Q : Aspose.Note prend‑il en charge d’autres formats d’image que le JPG ?**  
R : Absolument. PNG, BMP, GIF et TIFF sont tous pris en charge.

**Q : Puis‑je personnaliser l’alignement et la taille des images insérées ?**  
R : Oui. En plus de `Alignment`, vous pouvez définir les propriétés `Width`, `Height` et `Scale` sur l’objet `Image`.

**Q : Aspose.Note est‑il compatible avec toutes les versions de .NET ?**  
R : Il fonctionne avec .NET Framework 4.5+, .NET Core 3.1+, .NET 5 et .NET 6+.

**Q : Où puis‑je trouver des ressources supplémentaires et du support pour Aspose.Note ?**  
R : Vous pouvez trouver une documentation complète, des forums et du support sur le [Aspose Forum](https://forum.aspose.com/c/note/28).

---

**Dernière mise à jour :** 2026-04-13  
**Testé avec :** Aspose.Note 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}