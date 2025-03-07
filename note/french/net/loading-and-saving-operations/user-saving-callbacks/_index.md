---
title: Rappels sauvegardés par l'utilisateur dans Aspose.Note
linktitle: Rappels sauvegardés par l'utilisateur dans Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment implémenter des rappels permettant d'enregistrer les utilisateurs dans Aspose.Note pour .NET afin de personnaliser l'enregistrement des polices, des CSS et des images.
weight: 31
url: /fr/net/loading-and-saving-operations/user-saving-callbacks/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rappels sauvegardés par l'utilisateur dans Aspose.Note

## Introduction

Dans ce didacticiel, nous explorerons comment implémenter des rappels permettant d'économiser l'utilisateur dans Aspose.Note pour .NET. Ces rappels vous permettent de personnaliser le processus d'enregistrement en fournissant des hooks pour intervenir à différentes étapes, telles que l'enregistrement des polices, des feuilles de style CSS et des images. En utilisant ces rappels, vous pouvez adapter le comportement d'enregistrement à vos besoins spécifiques, améliorant ainsi la flexibilité et le contrôle de la sortie.

## Conditions préalables

Avant de vous lancer dans la mise en œuvre de rappels permettant de sauvegarder les utilisateurs dans Aspose.Note, assurez-vous que les conditions préalables suivantes sont en place :

1.  Aspose.Note pour le SDK .NET : téléchargez et installez le SDK Aspose.Note pour .NET à partir du[page de téléchargement](https://releases.aspose.com/note/net/).
   
2. Environnement de développement : disposez d'un environnement de développement approprié, tel que Visual Studio ou tout autre environnement de développement .NET.

## Importer des espaces de noms

Pour commencer, assurez-vous d'importer les espaces de noms nécessaires dans votre projet pour accéder aux classes et méthodes requises depuis la bibliothèque Aspose.Note :

```csharp
using Aspose.Note.Saving.Html;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Maintenant, décomposons la mise en œuvre des rappels permettant d'économiser l'utilisateur en plusieurs étapes :

## Étape 1 : définir les propriétés de rappel

```csharp
public string RootFolder { get; set; }
public bool KeepCssStreamOpened { get; set; }
public string CssFolder { get; set; }
public Stream CssStream { get; private set; }
public string FontsFolder { get; set; }
public string ImagesFolder { get; set; }
```

Ici, nous définissons diverses propriétés pour spécifier le dossier racine, le dossier CSS, le dossier des polices, le dossier des images et d'autres paramètres pertinents.

## Étape 2 : implémenter le rappel d'enregistrement des polices

```csharp
public void FontSaving(FontSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.FontsFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = Path.Combine("..", uri).Replace("\\", "\\\\");
}
```

 Dans cette étape, nous mettons en œuvre le`FontSaving` méthode de rappel pour gérer la sauvegarde des polices. Il crée une ressource dans le dossier de polices spécifié et attribue le flux et l'URI en conséquence.

## Étape 3 : implémenter le rappel de sauvegarde CSS

```csharp
public void CssSaving(CssSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.CssFolder, args.FileName, out uri, out stream);
    args.Stream = this.CssStream = stream;
    args.KeepStreamOpen = this.KeepCssStreamOpened;
    args.Uri = uri;
}
```

 Ici, nous définissons le`CssSaving` méthode de rappel pour gérer la sauvegarde des feuilles de style CSS. Il crée une ressource dans le dossier CSS spécifié et définit le flux, l'URI et d'autres propriétés en conséquence.

## Étape 4 : implémenter le rappel d'enregistrement d'image

```csharp
public void ImageSaving(ImageSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.ImagesFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = uri;
}
```

 Enfin, nous mettons en œuvre le`ImageSaving` méthode de rappel pour gérer la sauvegarde des images. Semblable aux étapes précédentes, il crée une ressource dans le dossier d’images spécifié et attribue le flux et l’URI.

## Conclusion

Dans ce didacticiel, nous avons appris à implémenter des rappels permettant d'économiser l'utilisateur dans Aspose.Note pour .NET. En suivant les étapes fournies, vous pouvez personnaliser le processus d'enregistrement des polices, des feuilles de style CSS et des images, permettant ainsi une plus grande flexibilité et un plus grand contrôle sur la sortie.

## FAQ

### Q1 : Puis-je utiliser ces rappels pour personnaliser d’autres aspects du processus d’enregistrement ?

A1 : Oui, vous pouvez étendre ces rappels ou en implémenter d'autres pour personnaliser divers aspects du processus de sauvegarde en fonction de vos besoins.

### Q2 : Aspose.Note pour .NET est-il compatible avec d’autres frameworks .NET ?

A2 : Oui, Aspose.Note pour .NET est compatible avec divers frameworks .NET, notamment .NET Core et .NET Standard.

### Q3 : Comment puis-je gérer les erreurs ou les exceptions pendant le processus de sauvegarde ?

A3 : Vous pouvez intégrer des mécanismes de gestion des erreurs dans chaque méthode de rappel pour gérer efficacement toutes les erreurs ou exceptions qui peuvent survenir.

### Q4 : Y a-t-il des considérations en matière de performances lors de l'utilisation de ces rappels ?

A4 : Bien que ces rappels offrent de la flexibilité, assurez-vous qu'ils sont mis en œuvre efficacement pour éviter toute surcharge de performances, en particulier lorsque vous traitez des documents ou des ressources volumineux.

### Q5 : Puis-je modifier dynamiquement le comportement d'enregistrement en fonction des entrées de l'utilisateur ou d'autres conditions ?

A5 : Oui, vous pouvez incorporer une logique conditionnelle dans les méthodes de rappel pour ajuster le comportement d'enregistrement de manière dynamique en fonction de divers facteurs.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
