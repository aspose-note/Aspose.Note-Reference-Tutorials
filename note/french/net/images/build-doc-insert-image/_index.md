---
date: 2026-04-06
description: Apprenez à créer un document OneNote et à insérer une image de façon
  programmatique en utilisant Aspose.Note pour .NET. Suivez des étapes simples pour
  ajouter des images, définir l’alignement et bien plus encore.
keywords:
- create onenote document
- how to insert image
- insert image onenote
- set image alignment
- multiple images onenote
linktitle: Construire le document et insérer une image dans Aspose.Note
second_title: Aspose.Note .NET API
title: Créer un document OneNote et insérer une image avec Aspose.Note
url: /fr/net/images/build-doc-insert-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer un document OneNote et insérer une image avec Aspose.Note

## Introduction

Dans ce tutoriel, vous **créerez un document OneNote** et apprendrez **comment insérer une image** dans celui‑ci en utilisant Aspose.Note pour .NET. Aspose.Note vous donne un contrôle total sur les fichiers OneNote, facilitant l’ajout de contenu riche tel que des images, des tableaux et des mises en page personnalisées de manière programmatique.

## Réponses rapides
- **Quel est le but principal ?** Créer un document OneNote et insérer une image avec un alignement personnalisé.  
- **Quelle bibliothèque est requise ?** Aspose.Note pour .NET (télécharger [ici](https://releases.aspose.com/note/net/)).  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour le développement ; une licence payante est requise pour la production.  
- **Puis‑je ajouter plusieurs images ?** Oui – répétez les étapes d’insertion pour chaque image (voir l’astuce « multiple images onenote »).  
- **La conversion en PDF est‑elle prise en charge ?** Absolument – vous pouvez ensuite convertir le document OneNote en PDF en utilisant la méthode `Save` d’Aspose.Note avec le format PDF.

## Prérequis

Avant de commencer, assurez‑vous de disposer des prérequis suivants :

1. **Visual Studio** – un IDE complet pour le développement .NET.  
2. **Aspose.Note pour .NET** – téléchargez et installez la bibliothèque depuis le site officiel.  
3. **Compréhension de base du C#** – la familiarité avec la syntaxe C# vous aidera à suivre les exemples de code.

## Importer les espaces de noms

Commençons par importer les espaces de noms nécessaires dans votre projet C#. Ces espaces de noms contiennent des classes et des méthodes que nous utiliserons pour effectuer des tâches de manipulation de documents.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Maintenant, détaillons le processus de création d’un document et d’insertion d’une image en plusieurs étapes :

## Étape 1 : Créer l’objet Document

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document();
```

Cette ligne de code initialise une nouvelle instance de la classe `Document`, qui représente un document OneNote.

## Étape 2 : Initialiser l’objet Page

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

Ici, nous initialisons une nouvelle instance de la classe `Page`, qui représente une page du document OneNote.

## Étape 3 : Initialiser l’objet Outline

```csharp
Outline outline = new Outline(doc);
```

La classe `Outline` représente un nœud de plan dans la hiérarchie du document. Nous créons un nouvel objet outline pour structurer notre document.

## Étape 4 : Initialiser l’objet OutlineElement

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

Un `OutlineElement` représente un élément au sein d’un outline. Ici, nous créons un nouvel élément outline pour ajouter du contenu à notre document.

## Étape 5 : Charger l’image

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg");
```

Nous chargeons un fichier image depuis le chemin spécifié en utilisant le constructeur de la classe `Image`.

## Étape 6 : Définir l’alignement de l’image

```csharp
image.Alignment = HorizontalAlignment.Right;
```

Cette ligne définit l’**alignement de l’image** sur le côté droit de la page. Vous pouvez également choisir `Left` ou `Center` selon les besoins de votre mise en page.

## Étape 7 : Ajouter l’image à l’OutlineElement

```csharp
outlineElem.AppendChildLast(image);
```

Ici, nous ajoutons l’image à l’OutlineElement, la plaçant dans la structure du document.

## Étape 8 : Ajouter l’OutlineElement à l’Outline

```csharp
outline.AppendChildLast(outlineElem);
```

Nous ajoutons l’OutlineElement, ainsi que l’image insérée, à la structure outline du document.

## Étape 9 : Ajouter l’Outline à la Page

```csharp
page.AppendChildLast(outline);
```

L’outline, contenant l’image, est ajouté à la structure de la page du document.

## Étape 10 : Ajouter la Page au Document

```csharp
doc.AppendChildLast(page);
```

Enfin, nous ajoutons la page, complète avec son contenu, au document.

## Étape 11 : Enregistrer le Document

```csharp
dataDir = dataDir + "BuildDocAndInsertImage_out.one";
doc.Save(dataDir);
```

Cette ligne enregistre le document OneNote modifié à l’emplacement spécifié. Vous pouvez ensuite **convertir OneNote en PDF** en appelant `doc.Save("output.pdf")`.

## Pourquoi cela importe

- **Automatisation** – Créer des documents OneNote de façon programmatique fait gagner du temps par rapport à l’édition manuelle.  
- **Cohérence** – Utiliser du code garantit que chaque document suit les mêmes règles de mise en page et de style.  
- **Scalabilité** – La même approche peut être étendue pour insérer **multiple images onenote** dans des documents ou générer des rapports en masse.

## Pièges courants et astuces

- **Problèmes de chemin** – Vérifiez toujours que `dataDir` pointe vers un dossier valide ; sinon le chargement de l’image échouera.  
- **Taille de l’image** – Les images volumineuses peuvent augmenter considérablement la taille du fichier ; envisagez de redimensionner avant l’insertion.  
- **Images multiples** – Pour ajouter plus d’une image, répétez les Étapes 5‑7 pour chaque image et ajoutez‑les au même ou à un autre `OutlineElement`.

## Questions fréquentes

### Q1 : Puis‑je insérer plusieurs images dans un même document en utilisant Aspose.Note pour .NET ?

R1 : Absolument ! Vous pouvez insérer autant d’images que nécessaire dans un document en suivant les mêmes étapes d’insertion pour chaque image.

### Q2 : Aspose.Note prend‑il en charge d’autres formats de fichier en plus de OneNote ?

R2 : Oui, Aspose.Note offre une prise en charge étendue de divers formats de fichier, notamment PDF, DOCX, HTML, et plus encore.

### Q3 : Aspose.Note est‑il adapté aux solutions de gestion de documents de niveau entreprise ?

R3 : Certainement ! Aspose.Note propose des fonctionnalités robustes et d’excellentes performances, ce qui en fait un choix idéal pour la gestion de documents d’entreprise.

### Q4 : Puis‑je personnaliser l’apparence des images insérées dans le document ?

R4 : Oui, Aspose.Note offre des options complètes pour personnaliser l’apparence des images, y compris l’alignement, la taille et la rotation.

### Q5 : Où puis‑je trouver des ressources supplémentaires et du support pour Aspose.Note pour .NET ?

R5 : Vous pouvez explorer la documentation Aspose.Note [ici](https://reference.aspose.com/note/net/) et demander de l’aide sur le forum communautaire Aspose [ici](https://forum.aspose.com/c/note/28/).

---

**Dernière mise à jour :** 2026-04-06  
**Testé avec :** Aspose.Note 24.11 for .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}