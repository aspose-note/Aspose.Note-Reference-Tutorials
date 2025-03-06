---
title: Créer un document et insérer une image avec Stream dans OneNote - Java
linktitle: Créer un document et insérer une image avec Stream dans OneNote - Java
second_title: API Java Aspose.Note
description: Découvrez comment intégrer sans effort des images dans des documents OneNote à l'aide d'Aspose.Note pour Java. Tutoriel étape par étape pour les développeurs Java.
weight: 13
url: /fr/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer un document et insérer une image avec Stream dans OneNote - Java

## Introduction

Bienvenue dans notre didacticiel complet sur l'utilisation d'Aspose.Note pour Java pour créer des documents et insérer des images à l'aide de flux d'images dans OneNote ! Dans ce didacticiel, nous vous guiderons étape par étape tout au long du processus, en veillant à ce que vous ayez une compréhension claire de chaque étape. À la fin, vous serez en mesure d'intégrer sans effort des images dans vos documents OneNote à l'aide de Java.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

### Kit de développement Java (JDK)

Assurez-vous que le kit de développement Java (JDK) est installé sur votre système. Vous pouvez le télécharger sur le site Web d'Oracle.

### Aspose.Note pour la bibliothèque Java

 Téléchargez et installez la bibliothèque Aspose.Note pour Java à partir du[lien](https://releases.aspose.com/note/java/).

### Configuration de l'EDI

Configurez votre environnement de développement intégré (IDE) avec les configurations nécessaires pour travailler avec des projets Java.

## Importer des packages

Pour commencer, importez les packages requis dans votre projet Java. Ces packages fourniront les fonctionnalités nécessaires pour travailler avec les documents et les images OneNote.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Étape 1 : configurer le répertoire de documents

 Définissez le répertoire où se trouvent votre document et vos images. Remplacer`"Your Document Directory"` avec le chemin d'accès à votre répertoire.

```java
String dataDir = "Your Document Directory";
```

## Étape 2 : Créer un objet de document

 Initialiser une instance du`Document` classe pour commencer à travailler avec votre document OneNote.

```java
Document doc = new Document();
```

## Étape 3 : initialiser l'objet de page

 Créer un`Page` objet pour représenter la page dans le document.

```java
Page page = new Page();
```

## Étape 4 : Créer un contour

 Initialiser un`Outline` objet pour structurer le contenu de la page.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Étape 5 : Créer un élément de plan

 Créé un`OutlineElement` pour maintenir l'image et spécifier sa position.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Étape 6 : Charger le flux d’images

 Chargez le flux d'images à l'aide du`FileInputStream` pour l'image désirée.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Étape 7 : Insérer une image

 Insérez l'image dans le document en créant un`Image` objet et définir son alignement.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Étape 8 : Ajouter une image à l'élément de contour

Ajoutez l’image à l’élément de contour.

```java
outlineElem1.appendChildLast(image);
```

## Étape 9 : Ajouter un élément de plan au plan

Ajoutez l'élément de contour au contour.

```java
outline1.appendChildLast(outlineElem1);
```

## Étape 10 : Ajouter le plan à la page

Ajoutez le plan à la page.

```java
page.appendChildLast(outline1);
```

## Étape 11 : Ajouter une page au document

Enfin, ajoutez la page au document.

```java
doc.appendChildLast(page);
```

## Étape 12 : Enregistrer le document

Enregistrez le document modifié en précisant le format souhaité (par exemple, PDF).

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

En suivant ces étapes, vous pouvez facilement créer des documents et insérer des images à l'aide de flux d'images dans OneNote à l'aide d'Aspose.Note pour Java.

## Conclusion

En conclusion, maîtriser l'intégration d'images dans vos documents OneNote à l'aide de Java peut améliorer considérablement votre processus de création de documents. Avec Aspose.Note pour Java, vous disposez d'un outil puissant pour accomplir cette tâche de manière transparente.

## FAQ

### Q1 : Aspose.Note pour Java est-il compatible avec toutes les versions de OneNote ?

A1 : Aspose.Note pour Java prend en charge différentes versions de OneNote, garantissant la compatibilité entre différents environnements.

### Q2 : Puis-je personnaliser l’apparence des images insérées dans les documents OneNote à l’aide d’Aspose.Note pour Java ?

A2 : Oui, vous pouvez personnaliser divers aspects des images insérées, tels que l'alignement, la taille et l'orientation, pour répondre à vos besoins spécifiques.

### Q3 : Aspose.Note pour Java prend-il en charge d'autres formats de documents que le PDF ?

A3 : Oui, Aspose.Note pour Java prend en charge un large éventail de formats de documents, notamment DOCX, HTML, etc., vous offrant ainsi une flexibilité dans vos tâches de gestion de documents.

### Q4 : Où puis-je trouver des ressources supplémentaires et une assistance pour Aspose.Note pour Java ?

A4 : Vous pouvez accéder à la documentation, aux liens de téléchargement, aux forums d'assistance et aux licences temporaires pour Aspose.Note pour Java via les liens fournis.

### Q5 : Existe-t-il une version d'essai disponible pour Aspose.Note pour Java ?

A5 : Oui, vous pouvez obtenir un essai gratuit d'Aspose.Note pour Java pour explorer ses fonctionnalités et capacités avant de prendre une décision d'achat.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
