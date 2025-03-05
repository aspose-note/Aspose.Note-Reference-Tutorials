---
title: Ajouter un nouveau nœud d'image avec une balise dans OneNote - Aspose.Note
linktitle: Ajouter un nouveau nœud d'image avec une balise dans OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Découvrez comment ajouter un nouveau nœud d'image avec une balise dans OneNote à l'aide d'Aspose.Note pour Java. Élevez vos compétences en programmation Java sans effort.
type: docs
weight: 10
url: /fr/java/onenote-tag-operations/add-new-image-node-with-tag/
---
## Introduction
Dans le domaine de la programmation Java, Aspose.Note se distingue comme un outil puissant pour gérer facilement les documents OneNote. Si vous souhaitez améliorer vos compétences et apprendre à ajouter un nouveau nœud d'image avec une balise dans OneNote à l'aide d'Aspose.Note, vous êtes au bon endroit. Ce guide étape par étape vous guidera tout au long du processus, en vous assurant de bien comprendre chaque concept.
## Conditions préalables
Avant de plonger dans le didacticiel, assurons-nous que vous disposez de tout ce dont vous avez besoin :
1.  Aspose.Note pour Java : assurez-vous que la bibliothèque Aspose.Note est installée. Sinon, vous pouvez le télécharger[ici](https://releases.aspose.com/note/java/).
2. Environnement de développement Java : assurez-vous de disposer d'un environnement de développement Java fonctionnel configuré sur votre ordinateur.
Maintenant que nous avons les prérequis en place, passons aux étapes suivantes.
## Importer des packages
Dans votre projet Java, commencez par importer les packages nécessaires :
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Étape 1 : Créer un objet de document
```java
// Le chemin d'accès au répertoire des documents.
String dataDir = "Your Document Directory";
// créer un objet de la classe Document
Document doc = new Document();
```
## Étape 2 : initialiser l'objet de classe de page
```java
// initialiser l'objet de classe Page
Page page = new Page();
```
## Étape 3 : initialiser l'objet de classe Outline
```java
// initialiser l'objet de classe Outline
Outline outline = new Outline();
```
## Étape 4 : initialiser l'objet de classe OutlineElement
```java
// initialiser l'objet de classe OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Étape 5 : Charger et insérer une image
```java
// charger une image
Image image = new Image(null, dataDir + "Input.jpg");
// insérer une image dans le nœud du document
outlineElem.appendChildLast(image);
```
## Étape 6 : ajouter une balise de note à l'image
```java
// ajouter une balise de note étoile jaune à l'image
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Étape 7 : Ajouter un nœud d'élément de plan
```java
// ajouter un nœud d'élément de contour
outline.appendChildLast(outlineElem);
```
## Étape 8 : Ajouter un nœud de plan
```java
// ajouter un nœud de plan
page.appendChildLast(outline);
```
## Étape 9 : ajouter un nœud de page
```java
// ajouter un nœud de page
doc.appendChildLast(page);
```
## Étape 10 : Enregistrer le document OneNote
```java
// enregistrer le document OneNote au format PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Toutes nos félicitations! Vous avez ajouté avec succès un nouveau nœud d'image avec une balise dans OneNote à l'aide d'Aspose.Note pour Java.
## Conclusion
 La maîtrise d'Aspose.Note pour Java ouvre des possibilités passionnantes dans la manipulation de documents OneNote. En suivant ce tutoriel, vous avez acquis une compétence pratique qui peut être appliquée à divers projets. Continuez à explorer la documentation Aspose.Note[ici](https://reference.aspose.com/note/java/)pour des fonctionnalités et des possibilités plus avancées.
## FAQ
### Où puis-je trouver la documentation Aspose.Note ?
 Vous pouvez trouver la documentation[ici](https://reference.aspose.com/note/java/).
### Comment télécharger Aspose.Note pour Java ?
 Vous pouvez le télécharger depuis la page des versions[ici](https://releases.aspose.com/note/java/).
### Existe-t-il un essai gratuit disponible ?
 Oui, vous pouvez accéder à l'essai gratuit[ici](https://releases.aspose.com/).
### Où puis-je obtenir de l’aide pour Aspose.Note ?
 Visitez le forum communautaire[ici](https://forum.aspose.com/c/note/28) pour le soutien.
### Ai-je besoin d’un permis temporaire ?
 Si nécessaire, vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).