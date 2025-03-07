---
title: Transformation du thème sombre avec Aspose.Note pour .NET
linktitle: Appliquer un thème sombre au texte dans Aspose.Note
second_title: API Aspose.Note .NET
description: Transformez vos documents OneNote avec Aspose.Note pour .NET ! Appliquez un thème sombre et élégant sans effort. Téléchargez maintenant et améliorez votre expérience de prise de notes.
weight: 11
url: /fr/net/text-manipulation/apply-dark-theme-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Transformation du thème sombre avec Aspose.Note pour .NET

## Introduction
Bienvenue dans notre guide étape par étape sur l'application d'un thème sombre au texte dans Aspose.Note pour .NET. Aspose.Note est une puissante API .NET qui permet aux développeurs de travailler avec les fichiers Microsoft OneNote par programme. Dans ce didacticiel, nous explorerons comment donner à vos documents OneNote un aspect élégant et moderne en appliquant un thème sombre au texte.
## Conditions préalables
Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :
-  Aspose.Note pour .NET : assurez-vous que Aspose.Note pour .NET est installé. Sinon, vous pouvez le télécharger depuis le[Documentation Aspose.Note](https://reference.aspose.com/note/net/).
- Environnement de développement : configurez votre environnement de développement .NET préféré, tel que Visual Studio.
- Répertoire des documents : préparez le répertoire dans lequel se trouve votre document OneNote.
## Importer des espaces de noms
Dans votre projet .NET, importez les espaces de noms nécessaires pour travailler avec Aspose.Note :
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## Étape 1 : charger le document OneNote
Chargez votre document OneNote dans Aspose.Note en utilisant le code suivant :
```csharp
// Le chemin d'accès au répertoire des documents.
string dataDir = "Your Document Directory";
// Chargez le document dans Aspose.Note.
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## Étape 2 : définir la couleur d'arrière-plan
Définissez la couleur d'arrière-plan de chaque page sur noir :
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## Étape 3 : Ajuster la couleur du texte
Ajustez la couleur de la police du texte en blanc pour une meilleure visibilité :
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## Étape 4 : Enregistrez le document
Enregistrez le document OneNote modifié au format PDF :
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## Conclusion
Toutes nos félicitations! Vous avez appliqué avec succès un thème sombre au texte de votre document Aspose.Note. Cette amélioration simple mais efficace peut donner à vos fichiers OneNote une apparence plus sophistiquée.
## Questions fréquemment posées
### Puis-je appliquer un thème sombre à des sections spécifiques de mon document OneNote ?
Oui, vous pouvez personnaliser le code pour cibler des pages ou des sections spécifiques de votre document.
### Aspose.Note prend-il en charge d'autres formats d'exportation que le PDF ?
Absolument! Aspose.Note prend en charge divers formats d'exportation, notamment les images et Microsoft Word.
### Existe-t-il une limite à la taille du document qu'Aspose.Note peut gérer ?
Aspose.Note peut gérer des documents de différentes tailles et ses performances sont optimisées pour plus d'efficacité.
### Puis-je revenir au thème d’origine après avoir appliqué le thème sombre ?
Oui, vous pouvez modifier le code pour basculer entre les thèmes en fonction de vos préférences.
### Où puis-je obtenir de l'aide pour les requêtes liées à Aspose.Note ?
 Pour toute assistance, visitez le[Forum Aspose.Note](https://forum.aspose.com/c/note/28) ou explorez le[Documentation](https://reference.aspose.com/note/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
