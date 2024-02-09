---
title: Générer un document à partir d'un modèle dans Aspose.Note
linktitle: Générer un document à partir d'un modèle dans Aspose.Note
second_title: API Aspose.Note .NET
description: Générez des documents dynamiques sans effort avec Aspose.Note pour .NET. Suivez notre guide étape par étape pour la création de documents personnalisés et basés sur les données.
type: docs
weight: 18
url: /fr/net/text-manipulation/generate-document-from-template/
---
## Introduction
Dans le paysage en constante évolution de la création de documents, Aspose.Note pour .NET se distingue comme un outil puissant pour générer des documents dynamiques sans effort. Que vous traitiez de rapports, de factures ou de documents personnalisés, ce didacticiel vous guidera tout au long du processus de génération d'un document à partir d'un modèle à l'aide d'Aspose.Note pour .NET.
## Conditions préalables
Avant de plonger dans le guide étape par étape, assurez-vous d'avoir les conditions préalables suivantes en place :
1.  Aspose.Note pour la bibliothèque .NET : téléchargez et installez la bibliothèque à partir du[Aspose.Note pour la documentation .NET](https://reference.aspose.com/note/net/).
2. Modèle de document : préparez un modèle de document au format OneNote (avec une extension .one). Cela servira de base à votre document généré dynamiquement.
## Importer des espaces de noms
Assurez-vous d'inclure les espaces de noms nécessaires dans votre projet :
```csharp
    using System;
    using System.Collections.Generic;
    using System.IO;
```
Maintenant, décomposons chaque étape du guide.
## Étape 1 : définissez votre répertoire de documents
```csharp
string dataDir = "Your Document Directory";
```
Remplacez « Votre répertoire de documents » par le chemin où vous souhaitez enregistrer votre document généré.
## Étape 2 : Créer un dictionnaire avec des valeurs de remplacement
```csharp
var templateData = new Dictionary<string, string>
{
    { "Company", "Atlas Shrugged Ltd" },
    { "CandidateName", "John Galt" },
    { "JobTitle", "Chief Entrepreneur Officer" },
    { "Department", "Sales" },
    { "Salary", "123456 USD" },
    { "Vacation", "30" },
    { "StartDate", "29 Feb 2024" },
    { "YourName", "Ayn Rand" }
};
```
Définissez un dictionnaire dans lequel les clés sont des espaces réservés dans votre modèle et les valeurs sont les données par lesquelles vous souhaitez les remplacer.

## Étape 3 : Charger le document modèle
```csharp
var templateDocument = new Document(Path.Combine(dataDir, "JobOffer.one"));
```
Chargez votre modèle de document OneNote dans Aspose.Note.

## Étape 4 : Remplacer les mots du modèle par des données dynamiques
```csharp
foreach (var paragraph in templateDocument.GetChildNodes<RichText>())
{
    foreach (var replacement in templateData)
    {
        paragraph.Replace($"${{{replacement.Key}}}", replacement.Value);
    }
}
```
Parcourez chaque paragraphe du modèle, en remplaçant les espaces réservés par des données dynamiques.

## Étape 5 : Enregistrez le document généré
```csharp
templateDocument.Save(Path.Combine(dataDir, "JobOffer_out.one"));
```
Enregistrez le document généré dynamiquement dans votre répertoire spécifié.

## Conclusion
Toutes nos félicitations! Vous avez généré avec succès un document dynamique à l'aide d'Aspose.Note pour .NET. Ce processus ouvre un monde de possibilités pour créer de manière transparente des documents personnalisés et basés sur les données.

## Questions fréquemment posées
### Puis-je utiliser Aspose.Note pour .NET avec d’autres formats de document ?
Oui, Aspose.Note pour .NET traite principalement des documents OneNote, mais Aspose propose diverses bibliothèques pour différents formats.
### Existe-t-il un essai gratuit disponible pour Aspose.Note pour .NET ?
 Oui, vous pouvez explorer les capacités d'Aspose.Note pour .NET avec un essai gratuit. Visite[ici](https://releases.aspose.com/) pour plus d'informations.
### Comment puis-je obtenir de l’assistance pour Aspose.Note pour .NET ?
 Visiter le[Aspose.Note pour le forum .NET](https://forum.aspose.com/c/note/28) pour obtenir l’aide de la communauté et des experts.
### Des licences temporaires sont-elles disponibles pour Aspose.Note pour .NET ?
 Oui, vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/) à des fins de tests et d’évaluation.
### Où puis-je trouver une documentation complète pour Aspose.Note pour .NET ?
 Se référer au[Documentation](https://reference.aspose.com/note/net/) pour des informations détaillées sur l’utilisation d’Aspose.Note pour .NET.