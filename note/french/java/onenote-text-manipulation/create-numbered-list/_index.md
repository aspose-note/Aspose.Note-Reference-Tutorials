---
title: Créer une liste numérotée dans OneNote - Aspose.Note
linktitle: Créer une liste numérotée dans OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Découvrez comment créer sans effort une liste numérotée dans OneNote avec Aspose.Note pour Java. Téléchargez un essai gratuit et plongez dans le monde du développement Java !
type: docs
weight: 14
url: /fr/java/onenote-text-manipulation/create-numbered-list/
---
## Introduction
Aspose.Note pour Java permet aux développeurs Java de travailler de manière transparente avec les fichiers Microsoft OneNote. Dans ce didacticiel, nous vous guiderons tout au long du processus de création d'une liste numérotée dans OneNote avec la puissante bibliothèque Aspose.Note pour Java.
## Conditions préalables
Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :
- Kit de développement Java (JDK) installé sur votre ordinateur.
-  Aspose.Note pour la bibliothèque Java téléchargée depuis[ici](https://releases.aspose.com/note/java/).
## Importation de packages
Tout d'abord, importons les packages nécessaires dans votre projet Java pour tirer le meilleur parti des fonctionnalités d'Aspose.Note. Incluez le code suivant dans votre projet :
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
## Étape 1 : initialisation des objets document, page et plan
```java
// Votre répertoire de documents
String dataDir = "Your Document Directory";
// Créer des objets Document, Page et Plan
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Définir le style de texte par défaut
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## Étape 2 : Définition du style de texte par défaut
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## Étape 3 : Création d'éléments de plan
Maintenant, créons les éléments de votre liste numérotée.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Répétez l’opération pour les autres éléments (outlineElem2 et outlineElem3)
```
## Étape 4 : Ajout d'éléments de plan au plan
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Étape 5 : Ajout d'un contour à la page
```java
page.appendChildLast(outline);
```
## Étape 6 : Sauvegarde du document
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
Suivez ces étapes méticuleusement et vous créerez sans effort une liste numérotée dans OneNote à l’aide d’Aspose.Note pour Java.
## Conclusion
Dans ce didacticiel, nous avons exploré le processus transparent de création d'une liste numérotée dans OneNote à l'aide d'Aspose.Note pour Java. Les fonctionnalités robustes de la bibliothèque en font un outil inestimable pour les développeurs Java travaillant avec des fichiers Microsoft OneNote.
## Questions fréquemment posées
### Q : Puis-je personnaliser le format de numérotation dans ma liste OneNote ?
R : Absolument ! Vous pouvez personnaliser le format de numérotation à l'aide de la classe NumberList fournie par Aspose.Note pour Java.
### Q : Existe-t-il une version d'essai disponible pour Aspose.Note pour Java ?
 R : Oui, vous pouvez télécharger un essai gratuit[ici](https://releases.aspose.com/).
### Q : Comment puis-je obtenir de l'assistance pour Aspose.Note pour Java ?
 R : Visitez le[Aspose.Note pour le forum Java](https://forum.aspose.com/c/note/28) pour le soutien de la communauté.
### Q : Où puis-je trouver une documentation détaillée pour Aspose.Note pour Java ?
 R : Reportez-vous au[Documentation](https://reference.aspose.com/note/java/) pour des informations complètes.
### Q : Comment puis-je acheter une licence pour Aspose.Note pour Java ?
 R : Vous pouvez acheter une licence[ici](https://purchase.aspose.com/buy).