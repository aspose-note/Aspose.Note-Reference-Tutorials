---
title: Récupérer une liste de puces ou de numéros dans Aspose.Note Text
linktitle: Récupérer une liste de puces ou de numéros dans Aspose.Note Text
second_title: API Aspose.Note .NET
description: Libérez le potentiel d'Aspose.Note pour .NET avec notre guide étape par étape sur la récupération de listes à puces ou de numéros. Élevez vos compétences en manipulation de documents OneNote !
type: docs
weight: 23
url: /fr/net/text-manipulation/retrieve-bullet-number-list/
---
## Introduction
Bienvenue dans le monde d'Aspose.Note pour .NET, une bibliothèque robuste et polyvalente qui permet aux développeurs de gérer sans effort la manipulation de documents OneNote. Dans ce didacticiel, nous approfondirons le processus de récupération de listes à puces ou de numéros à l'aide d'Aspose.Note pour .NET. Que vous soyez un développeur chevronné ou un passionné de codage, ce guide vous fournira les connaissances nécessaires pour naviguer dans les subtilités de l'utilisation des listes dans Aspose.Note.
## Conditions préalables
Avant de nous lancer dans ce voyage de codage, assurez-vous d'avoir les conditions préalables suivantes en place :
-  Aspose.Note pour .NET : assurez-vous que la bibliothèque Aspose.Note est installée. Sinon, vous pouvez le télécharger depuis le[Aspose.Note pour la documentation .NET](https://reference.aspose.com/note/net/).
- Environnement de développement : disposez d'un environnement de développement fonctionnel, de préférence Microsoft Visual Studio, configuré sur votre ordinateur.
- Connaissance de base de C# : Familiarisez-vous avec C# car ce tutoriel est écrit dans ce langage.
## Importer des espaces de noms
Afin d'interagir avec Aspose.Note pour .NET, vous devez importer les espaces de noms nécessaires dans votre projet. Incluez les espaces de noms suivants au début de votre code :
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
Maintenant, décomposons étape par étape le processus de récupération des listes à puces ou à numéros :
## Étape 1 : définissez votre répertoire de documents
```csharp
// Le chemin d'accès au répertoire des documents.
string dataDir = "Your Document Directory";
```
 Remplacer`"Your Document Directory"` avec le chemin réel où se trouve votre document Aspose.Note.
## Étape 2 : Charger le document
```csharp
// Chargez le document dans Aspose.Note.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 Assurez-vous de remplacer`"ApplyNumberingOnText.one"` avec le nom de votre document OneNote spécifique.
## Étape 3 : Récupérer la collection de nœuds
```csharp
// Récupère une collection de nœuds de l’élément de contour.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
Cette étape récupère une collection de nœuds de plan du document chargé.
## Étape 4 : Parcourir chaque nœud
```csharp
// Parcourez chaque nœud.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Passez aux étapes suivantes...
    }
}
```
Cette boucle garantit que nous traitons uniquement avec des nœuds contenant une liste de numéros.
## Étape 5 : Récupérer les informations sur la police
```csharp
// Récupérer le nom de la police
Console.WriteLine("Font Name: " + list.Font);
// Récupérer la longueur de la police
Console.WriteLine("Font Length: " + list.Font.Length);
// Récupérer la taille de la police
Console.WriteLine("Font Size: " + list.FontSize);
// Récupérer la couleur de la police
Console.WriteLine("Font Color: " + list.FontColor);
// Récupérer le format
Console.WriteLine("Font format: " + list.Format);
// Cochez en gras
Console.WriteLine("Is bold: " + list.IsBold);
// Cocher italique
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
Ces lignes de code extraient diverses informations relatives aux polices de la liste de numéros.
## Conclusion
 Toutes nos félicitations! Vous avez appris avec succès comment récupérer des listes de puces ou de numéros à l'aide d'Aspose.Note pour .NET. Tout en poursuivant votre exploration, référez-vous au[Documentation](https://reference.aspose.com/note/net/) pour des informations et des fonctionnalités plus approfondies.
## FAQ
### Puis-je utiliser Aspose.Note pour .NET avec d’autres langages de programmation ?
Aspose.Note prend principalement en charge .NET, mais il existe d'autres versions de la bibliothèque adaptées à différentes plates-formes et langages.
### Aspose.Note est-il compatible avec les derniers formats OneNote ?
Oui, Aspose.Note prend en charge une large gamme de formats OneNote, garantissant la compatibilité avec les dernières versions.
### Comment puis-je obtenir une licence temporaire pour Aspose.Note ?
 Visite[ce lien](https://purchase.aspose.com/temporary-license/) pour obtenir une licence temporaire à des fins d'évaluation.
### Quelles options d'assistance sont disponibles pour les utilisateurs d'Aspose.Note ?
 Vous pouvez explorer et demander de l'aide dans le[Forum Aspose.Note](https://forum.aspose.com/c/note/28) pour toute question ou problème que vous pourriez rencontrer.
### Existe-t-il une version d’essai gratuite d’Aspose.Note pour .NET ?
 Oui, vous pouvez accéder à la version d'essai gratuite d'Aspose.Note pour .NET[ici](https://releases.aspose.com/).