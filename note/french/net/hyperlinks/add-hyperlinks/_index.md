---
date: 2026-04-03
description: Apprenez à ajouter des hyperliens dans les documents Aspose.Note en utilisant
  Aspose.Note pour .NET, à personnaliser l’apparence des hyperliens et à insérer plusieurs
  hyperliens pour des fichiers OneNote plus riches.
keywords:
- how to add hyperlink
- insert multiple hyperlinks
- add hyperlink to onenote
- customize hyperlink appearance
- generate one file hyperlink
linktitle: Comment ajouter un hyperlien dans les documents Aspose.Note
second_title: Aspose.Note .NET API
title: Comment ajouter un hyperlien dans les documents Aspose.Note
url: /fr/net/hyperlinks/add-hyperlinks/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajouter un hyperlien dans les documents Aspose.Note

## Introduction

Dans ce tutoriel, vous découvrirez **comment ajouter un hyperlien** au texte à l’intérieur des documents Aspose.Note avec l’API .NET. Ajouter un hyperlien transforme des notes statiques en contenu interactif et cliquable—idéal pour créer des liens vers des ressources web, des sections internes ou des fichiers externes. Nous parcourrons chaque étape, vous montrerons comment **personnaliser l’apparence des hyperliens**, et expliquerons comment **insérer plusieurs hyperliens** lorsque vous avez besoin de pages OneNote plus riches.

## Réponses rapides
- **Quelle est la classe principale pour créer un fichier OneNote ?** `Document` d’Aspose.Note.
- **Quelle propriété fait que le texte se comporte comme un hyperlien ?** `IsHyperlink = true` sur `TextStyle`.
- **Puis‑je créer un lien vers des sites Web externes ?** Oui, définissez `HyperlinkAddress` sur une URL comme `https://www.google.com`.
- **Ai‑je besoin d’une licence pour une utilisation en production ?** Une licence valide d’Aspose.Note est requise pour les builds non‑évaluation.
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.

## Qu’est‑ce que « comment ajouter un hyperlien » dans Aspose.Note ?
Ajouter un hyperlien signifie associer une URL à un morceau de texte afin que, lorsqu’un utilisateur clique dessus dans OneNote, la ressource liée s’ouvre dans un navigateur ou une autre application. Aspose.Note expose le drapeau `TextStyle.IsHyperlink` et la propriété `HyperlinkAddress` pour rendre cela possible programmatiquement.

## Pourquoi ajouter des hyperliens aux documents OneNote ?
- **Navigation améliorée :** Accédez directement aux pages Web ou sections liées.
- **Documentation enrichie :** Fournissez des références, tutoriels ou fichiers sources sans quitter la note.
- **Aspect professionnel :** Des couleurs et styles personnalisables permettent aux hyperliens de s’intégrer à la conception de votre document.

## Prérequis

1. Connaissances de base en C# et Visual Studio.  
2. Bibliothèque Aspose.Note pour .NET installée – téléchargez‑la depuis [ici](https://releases.aspose.com/note/net/).  
3. Compréhension de la structure des documents Aspose.Note (pages, contours, texte enrichi).

## Importer les espaces de noms

Tout d’abord, importez les espaces de noms qui vous donnent accès aux classes principales d’Aspose.Note et aux types .NET de base.

```csharp
using System;
using System.Drawing;
```

## Guide étape par étape

### Étape 1 : créer un nouvel objet Document

Instanciez un `Document` qui contiendra toutes vos pages et votre contenu.

```csharp
Document doc = new Document();
```

### Étape 2 : définir les styles de texte (y compris le style d’hyperlien)

Créez deux objets `TextStyle` — un pour le texte normal et un pour l’hyperlien.  
Ici, nous **personnalisons également l’apparence de l’hyperlien** en définissant la couleur de la police.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

> **Conseil pro :** Pour insérer **plusieurs hyperliens**, définissez des objets `TextStyle` supplémentaires avec des valeurs `HyperlinkAddress` différentes et réutilisez‑les dans les segments `RichText` ultérieurs.

### Étape 3 : créer des objets RichText

Construisez le paragraphe qui mélange texte normal et hyperlien. La méthode `Append` vous permet de chaîner des fragments stylisés.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

### Étape 4 : créer un contour et un élément de contour

Les contours agissent comme des conteneurs pour les éléments visuels sur une page. Définissez la taille et la position selon les besoins.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

### Étape 5 : ajouter des éléments à une page

Chaque fichier OneNote se compose de pages. Nous créons un `Title` et une `Page`, puis attachons le contour.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

### Étape 6 : enregistrer le document

Choisissez un dossier, composez le nom complet du fichier, puis appelez `Save`. Le fichier de sortie sera un fichier OneNote `.one` valide contenant votre hyperlien.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| L’hyperlien ne s’ouvre pas | Assurez‑vous que `HyperlinkAddress` inclut le protocole (`http://` ou `https://`). |
| La couleur du texte n’est pas appliquée | Définissez `FontColor` sur le `TextStyle` utilisé pour l’hyperlien. |
| Besoin de plusieurs liens sur une même page | Créez plusieurs objets `TextStyle`, chacun avec son propre `HyperlinkAddress`, et ajoutez‑les au même ou à différents objets `RichText`. |
| Le document ne se charge pas dans OneNote | Vérifiez que vous utilisez une version prise en charge de OneNote (2010+). |

## Foire aux questions

**Q : Puis‑je ajouter plusieurs hyperliens dans le même document en utilisant Aspose.Note ?**  
R : Oui, créez simplement des instances supplémentaires de `TextStyle` avec des valeurs `HyperlinkAddress` différentes et ajoutez‑les à vos objets `RichText`.

**Q : Comment puis‑je personnaliser l’apparence des hyperliens ?**  
R : Utilisez des propriétés comme `FontColor`, `FontName` et `FontSize` sur le `TextStyle` qui a `IsHyperlink = true`. Cela vous permet d’harmoniser les hyperliens avec l’identité visuelle de votre document.

**Q : Aspose.Note prend‑il en charge les hyperliens vers des sites Web externes ?**  
R : Absolument. Définissez `HyperlinkAddress` sur n’importe quelle URL valide (incluant `http://` ou `https://`) pour créer un lien sortant du fichier OneNote.

**Q : Est‑il possible de générer un seul fichier OneNote contenant de nombreux hyperliens ?**  
R : Oui. En ajoutant de façon répétée des segments `RichText` stylisés avec des adresses d’hyperlien différentes, vous pouvez **générer une collection d’hyperliens** dans un seul fichier.

**Q : Aspose.Note est‑il compatible avec les dernières versions de OneNote ?**  
R : La bibliothèque fonctionne avec OneNote 2010 et versions ultérieures, y compris la version UWP de Windows 10.

**Dernière mise à jour :** 2026-04-03  
**Testé avec :** Aspose.Note for .NET 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}