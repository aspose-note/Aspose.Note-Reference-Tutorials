---
date: 2026-04-03
description: Apprenez à définir une icône personnalisée et à joindre des fichiers
  dans Aspose.Note pour .NET, y compris l’enregistrement de fichiers OneNote et l’utilisation
  d’images comme icônes.
keywords:
- set custom icon
- attach multiple files
- use image as icon
- save onenote file
- embed text file
linktitle: Joindre un fichier et définir une icône dans Aspose.Note
second_title: Aspose.Note .NET API
title: Définir une icône personnalisée et joindre un fichier dans Aspose.Note
url: /fr/net/attachments/attach-file-set-icon/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir une icône personnalisée et joindre un fichier dans Aspose.Note

## Introduction

Si vous devez **définir une icône personnalisée** pour une pièce jointe dans une page OneNote, Aspose.Note pour .NET simplifie la tâche. En joignant un fichier et en attribuant une image comme icône, vous pouvez créer des notes plus riches et informatives qui ont exactement l'apparence souhaitée. Dans ce tutoriel, nous parcourrons le processus complet — à partir d’un document vierge, en ajoutant une pièce jointe, en appliquant une icône JPEG personnalisée, puis en enregistrant le fichier OneNote.

## Réponses rapides
- **Que signifie « définir une icône personnalisée » ?** Cela vous permet de remplacer la vignette par défaut de la pièce jointe par une image que vous fournissez.  
- **Puis‑je joindre plusieurs fichiers ?** Oui, répétez les étapes de jointure pour chaque fichier.  
- **Quels formats d’image sont pris en charge pour les icônes ?** Tout format compatible .NET tel que JPEG, PNG, BMP ou GIF.  
- **Ai‑je besoin d’une licence ?** Une licence valide d’Aspose.Note est requise pour une utilisation en production ; une version d’essai gratuite suffit pour l’évaluation.  
- **Comment enregistrer le fichier OneNote ?** Utilisez `Document.Save()` et indiquez un chemin de fichier *.one*.

## Qu'est-ce que « définir une icône personnalisée » dans Aspose.Note ?

Définir une icône personnalisée consiste à attribuer une image spécifique (par ex., un JPEG) pour représenter un fichier joint dans une page OneNote. Cela améliore les repères visuels pour les utilisateurs et peut être utilisé pour afficher des logos de type de fichier ou des images de marque.

## Pourquoi définir une icône personnalisée pour les pièces jointes ?

- **Contexte visuel amélioré :** Les utilisateurs reconnaissent instantanément le type ou l’objectif du fichier joint.  
- **Cohérence de la marque :** Utilisez le logo de votre entreprise comme icône pour tous les documents associés.  
- **Expérience utilisateur améliorée :** Les notes apparaissent soignées et professionnelles, notamment dans les blocs‑notes partagés.

## Prérequis

- Connaissances de base en programmation C#.
- Bibliothèque Aspose.Note pour .NET installée.
- Visual Studio (ou tout IDE compatible .NET) prêt pour le développement.

## Importer les espaces de noms

Tout d'abord, importez les espaces de noms requis afin de pouvoir travailler avec les fichiers, les images et les objets OneNote.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing.Imaging;
```

## Guide étape par étape pour joindre un fichier et définir son icône

### Étape 1 : créer un objet Document

Une nouvelle instance `Document` représente le fichier OneNote que vous allez créer.

```csharp
Document doc = new Document();
```

### Étape 2 : initialiser un objet Page

Chaque fichier OneNote contient une ou plusieurs pages. Ici, nous créons la première page.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### Étape 3 : initialiser un objet Outline

Les outlines servent de conteneurs pour les blocs de contenu sur une page.

```csharp
Outline outline = new Outline(doc);
```

### Étape 4 : initialiser un objet OutlineElement

Cet élément contiendra le fichier joint ainsi que son icône personnalisée.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

### Étape 5 : lire l’image d’icône et initialiser l’objet AttachedFile

Nous ouvrons le flux d’image (l’icône personnalisée) et indiquons le fichier que nous souhaitons intégrer.

```csharp
string dataDir = "Your Document Directory";
using (var stream = File.OpenRead(dataDir + "icon.jpg"))
{
    AttachedFile attachedFile = new AttachedFile(doc, dataDir + "attachment.txt", stream, ImageFormat.Jpeg);
}
```

> **Astuce :** Remplacez `ImageFormat.Jpeg` par `ImageFormat.Png` si vous préférez une icône PNG.

### Étape 6 : ajouter le fichier joint à l’OutlineElement

Le fichier (avec son icône) devient maintenant un enfant de l’élément outline.

```csharp
outlineElem.AppendChildLast(attachedFile);
```

### Étape 7 : ajouter l’OutlineElement à l’Outline

Cela imbrique l’élément à l’intérieur du conteneur outline.

```csharp
outline.AppendChildLast(outlineElem);
```

### Étape 8 : ajouter l’Outline à la Page

Attachez toute la hiérarchie d’outline à la page.

```csharp
page.AppendChildLast(outline);
```

### Étape 9 : ajouter la Page au Document

Ajoutez la page complétée à la structure du document.

```csharp
doc.AppendChildLast(page);
```

### Étape 10 : enregistrer le document OneNote

Enfin, écrivez le document sur le disque sous forme de fichier *.one*.

```csharp
dataDir = dataDir + "AttachFileAndSetIcon_out.one";
doc.Save(dataDir);
```

## Cas d’utilisation courants

- **Intégration de contrats :** Joignez un PDF et utilisez une icône de logo de contrat.  
- **Partage d’extraits de code :** Joignez un fichier `.txt` avec une icône « code » personnalisée.  
- **Documentation de projet :** Joignez des fichiers de conception et définissez une vignette correspondant au type de fichier.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Icône non affichée** | Vérifiez que le format de l’image correspond au `ImageFormat` fourni (par ex., JPEG vs PNG). |
| **Erreurs de chemin de fichier** | Utilisez `Path.Combine(dataDir, "file.ext")` pour éviter les problèmes de slash manquant. |
| **Les pièces jointes volumineuses ralentissent les performances** | Compressez le fichier au préalable ou divisez‑le en plusieurs pièces jointes plus petites. |

## Questions fréquentes

**Q : Puis‑je joindre plusieurs fichiers à une même note avec Aspose.Note pour .NET ?**  
R : Oui. Répétez simplement le bloc « Lire l’image d’icône et initialiser l’objet AttachedFile » pour chaque fichier et ajoutez chaque `AttachedFile` au même `OutlineElement` ou créez des éléments séparés.

**Q : Est‑il possible de définir des icônes personnalisées pour les pièces jointes ?**  
R : Absolument. Le constructeur `AttachedFile` vous permet de fournir un flux d’image et de spécifier le format d’image, vous donnant un contrôle total sur l’icône.

**Q : Aspose.Note prend‑il en charge d’autres formats d’image pour définir les icônes ?**  
R : Oui. En plus du JPEG, vous pouvez utiliser PNG, BMP, GIF ou tout format pris en charge par `System.Drawing.Imaging.ImageFormat`.

**Q : Puis‑je joindre des fichiers depuis des URL externes ?**  
R : Bien qu’Aspose.Note fonctionne avec des flux locaux, vous pouvez télécharger un fichier via `HttpClient`, le stocker dans un `MemoryStream`, puis transmettre ce flux à `AttachedFile`.

**Q : Existe‑t‑il une limite de taille pour les pièces jointes ?**  
R : Aspose.Note n’impose pas de limite stricte, mais les fichiers très volumineux peuvent affecter l’utilisation de la mémoire et les performances. Envisagez de compresser les pièces jointes importantes.

---

**Dernière mise à jour :** 2026-04-03  
**Testé avec :** Aspose.Note 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}