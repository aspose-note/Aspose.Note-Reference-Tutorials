---
title: Explorer les révisions de page dans les documents Aspose.Note
linktitle: Explorer les révisions de page dans les documents Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment explorer les révisions de page dans les documents Aspose.Note à l'aide du framework .NET avec des conseils étape par étape.
type: docs
weight: 14
url: /fr/net/note-manipulation/page-revisions-exploration/
---
## Introduction

Dans ce didacticiel, nous allons explorer l'exploration des révisions de page dans les documents Aspose.Note à l'aide du framework .NET. Aspose.Note est une bibliothèque puissante qui permet aux développeurs de travailler avec des fichiers Microsoft OneNote par programme, offrant diverses fonctionnalités pour manipuler et extraire les données de ces fichiers.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir configuré les conditions préalables suivantes :

### 1. Téléchargez et installez Aspose.Note pour .NET

 Visiter le[page de téléchargement](https://releases.aspose.com/note/net/) et téléchargez la bibliothèque Aspose.Note pour .NET. Suivez les instructions d'installation fournies pour configurer la bibliothèque dans votre environnement de développement.

### 2. Charger les espaces de noms nécessaires

Assurez-vous d'importer les espaces de noms requis dans votre projet .NET pour accéder aux fonctionnalités Aspose.Note de manière transparente.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

Maintenant, décomposons le processus d'exploration des révisions de page en instructions étape par étape :

## Étape 1 : Charger le document

Tout d'abord, nous devons charger le document Aspose.Note, en veillant à activer le chargement de l'historique du document.

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## Étape 2 : Récupérer les révisions de la page

Une fois le document chargé, nous pouvons récupérer les révisions pour une page spécifique. Dans cet exemple, nous obtiendrons des révisions pour la première page.

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## Étape 3 : Parcourir les révisions

Dans la boucle, parcourez chaque révision de la page et accédez à ses propriétés telles que l'heure de la dernière modification, l'heure de création, le titre, le niveau et l'auteur.

## Conclusion

L'exploration des révisions de page dans les documents Aspose.Note à l'aide de .NET est un processus simple. En suivant les étapes décrites dans ce didacticiel, vous pouvez récupérer et analyser efficacement l'historique des révisions de vos fichiers OneNote par programme.

## FAQ

### Q1 : Puis-je utiliser Aspose.Note pour .NET pour créer de nouveaux documents OneNote ?

A1 : Oui, Aspose.Note pour .NET vous permet de créer, modifier et manipuler des documents OneNote par programme.

### Q2 : Aspose.Note prend-il en charge l’historique de chargement pour tous les types de fichiers OneNote ?

A2 : Aspose.Note prend en charge l’historique de chargement pour les formats de fichiers .one et .onepkg.

### Q3 : Existe-t-il un essai gratuit disponible pour Aspose.Note pour .NET ?

A3 : Oui, vous pouvez télécharger un essai gratuit d'Aspose.Note pour .NET à partir de[ici](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir une licence temporaire pour Aspose.Note pour .NET ?

 A4 : Vous pouvez demander une licence temporaire auprès de[ce lien](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis-je trouver de l'assistance pour Aspose.Note pour .NET ?

 A5 : Vous pouvez trouver de l'aide et des ressources sur le[Forum Aspose.Note](https://forum.aspose.com/c/note/28).