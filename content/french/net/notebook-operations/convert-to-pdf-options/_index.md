---
title: Convertir des blocs-notes en PDF avec les options d'Aspose Note .NET
linktitle: Convertir des blocs-notes en PDF avec les options d'Aspose Note .NET
second_title: API Aspose.Note .NET
description: Découvrez comment convertir des blocs-notes Microsoft OneNote au format PDF à l'aide de la bibliothèque Aspose.Note pour .NET avec des options personnalisables.
type: docs
weight: 16
url: /fr/net/notebook-operations/convert-to-pdf-options/
---
## Introduction

Dans ce didacticiel, nous allons parcourir le processus de conversion des blocs-notes au format PDF à l'aide de la bibliothèque Aspose.Note pour .NET. Aspose.Note pour .NET fournit un ensemble puissant de fonctionnalités pour travailler avec les fichiers Microsoft OneNote par programme.

## Conditions préalables

Avant de commencer, assurez-vous de disposer des prérequis suivants :

### 1. Aspose.Note pour la bibliothèque .NET
 Assurez-vous d'avoir téléchargé et installé la bibliothèque Aspose.Note pour .NET. Vous pouvez le télécharger depuis le[site web](https://releases.aspose.com/note/net/).

### 2. Environnement de développement
Vous devez disposer d'un environnement de développement configuré, tel que Visual Studio, avec le framework .NET nécessaire installé.

## Importer des espaces de noms

Avant de commencer à utiliser Aspose.Note pour .NET dans notre projet, importons les espaces de noms requis :

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

Maintenant, décomposons le processus de conversion des blocs-notes en PDF avec des options en plusieurs étapes :

## Étape 1 : Charger le bloc-notes

Tout d’abord, nous devons charger le bloc-notes OneNote que nous souhaitons convertir en fichier PDF.

```csharp
// Le chemin d'accès au répertoire des documents.
string dataDir = "Your Document Directory";

// Charger un bloc-notes OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Étape 2 : Spécifier les options d'enregistrement PDF

Ensuite, nous spécifierons les options d'enregistrement du bloc-notes sous forme de fichier PDF. Nous pouvons personnaliser divers paramètres tels que l'algorithme de fractionnement des pages, les marges et la taille de la page.

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## Étape 3 : Enregistrez le cahier au format PDF

Nous allons maintenant enregistrer le bloc-notes sous forme de fichier PDF en utilisant les options spécifiées.

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

// Enregistrez le bloc-notes
notebook.Save(dataDir, notebookSaveOptions);
```

## Étape 4 : Vérifier la conversion

Enfin, vérifions que la conversion a réussi et imprimons l'emplacement où le fichier PDF est enregistré.

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## Conclusion

Dans ce didacticiel, nous avons appris à convertir des blocs-notes OneNote au format PDF à l'aide de la bibliothèque Aspose.Note pour .NET. En suivant les étapes décrites ci-dessus, vous pouvez facilement intégrer cette fonctionnalité dans vos applications .NET.

## FAQ

### Q1 : Aspose.Note pour .NET est-il compatible avec toutes les versions de Microsoft OneNote ?

A1 : Oui, Aspose.Note pour .NET prend en charge différentes versions de Microsoft OneNote, notamment les formats .one et .onetoc2.

### Q2 : Puis-je personnaliser l’apparence de la sortie PDF ?

A2 : Oui, vous pouvez spécifier diverses options telles que la taille de la page, les marges et l'algorithme de fractionnement des pages pour personnaliser l'apparence de la sortie PDF.

### Q3 : Aspose.Note pour .NET prend-il en charge d'autres formats de fichiers ?

A3 : Oui, Aspose.Note pour .NET prend en charge la conversion vers divers autres formats tels que les images, HTML et les documents Microsoft Word.

### Q4 : Existe-t-il un essai gratuit disponible pour Aspose.Note pour .NET ?

A4 : Oui, vous pouvez télécharger un essai gratuit d'Aspose.Note pour .NET à partir du site Web pour évaluer ses fonctionnalités avant de faire un achat.

### Q5 : Comment puis-je obtenir une assistance technique pour Aspose.Note pour .NET ?

 A5 : Vous pouvez obtenir une assistance technique pour Aspose.Note pour .NET en visitant le[Forum Aspose.Note](https://forum.aspose.com/c/note/28) ou en contactant directement l'équipe d'assistance Aspose.