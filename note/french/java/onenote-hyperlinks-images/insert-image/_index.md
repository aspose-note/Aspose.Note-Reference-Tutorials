---
date: 2026-03-19
description: Apprenez à ajouter une image à OneNote en utilisant Java avec Aspose.Note
  for Java, y compris comment définir les dimensions de l'image en Java et enregistrer
  OneNote au format PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Ajouter une image à OneNote avec Java
url: /fr/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Insérer une image dans un document OneNote avec Java

## Introduction

Dans ce tutoriel, vous apprendrez **comment ajouter une image à OneNote** de manière programmatique en utilisant Java et la bibliothèque Aspose.Note for Java. Intégrer des images dans les pages OneNote est pratique lorsque vous devez générer des comptes rendus de réunion, des rapports automatisés ou de la documentation qui combine texte et données visuelles. À la fin du guide, vous serez capable de charger un fichier OneNote existant, d’insérer une image, d’ajuster éventuellement sa taille et sa position, et même **d’enregistrer OneNote au format PDF** – le tout sans ouvrir l’interface OneNote.

## Réponses rapides
- **Quelle est la façon la plus simple d’ajouter une image à OneNote en utilisant Java ?**  
  Utilisez la classe `Image` d’Aspose.Note for Java et ajoutez‑la à une page.
- **Ai‑je besoin d’une licence pour une utilisation en production ?**  
  Oui, une licence commerciale est requise pour les déploiements en production.
- **Puis‑je définir des dimensions personnalisées pour l’image ?**  
  Absolument – appelez `setWidth()` et `setHeight()` sur l’objet `Image`.
- **Est‑il possible d’enregistrer le fichier OneNote au format PDF après avoir ajouté l’image ?**  
  Oui, appelez `save(..., SaveFormat.Pdf)` pour **enregistrer OneNote au format PDF**.
- **Quelle version de Java est prise en charge ?**  
  Aspose.Note for Java fonctionne avec JDK 8 et versions ultérieures.

## Pourquoi ajouter une image à OneNote ?

Ajouter des éléments visuels rend les notes plus faciles à comprendre et plus attrayantes. Les images peuvent illustrer des diagrammes, des captures d’écran ou des graphiques de données qui nécessiteraient autrement de longues descriptions textuelles. Automatiser cette étape fait gagner du temps, surtout lors de la génération de gros lots de notes à partir de sources de données.

## Prérequis

Avant de commencer, assurez‑vous d’avoir les éléments suivants prêts :

### 1. Kit de développement Java (JDK)

Installez JDK 8 ou une version plus récente. Vous pouvez le télécharger depuis le site d’Oracle ou utiliser une distribution OpenJDK.

### 2. Bibliothèque Aspose.Note for Java

Téléchargez la dernière bibliothèque Aspose.Note for Java et ajoutez‑la au classpath de votre projet. Des instructions d’installation détaillées sont disponibles dans la [documentation](https://reference.aspose.com/note/java/) officielle.

## Importer les packages

Commencez par importer les classes nécessaires. Ces importations vous donnent accès aux fonctionnalités principales d’Aspose.Note ainsi qu’aux utilitaires Java de base.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Guide étape par étape

Voici un guide concis, numéroté. Chaque étape comprend une brève explication suivie du code exact à copier.

### Étape 1 : Charger le document OneNote

Nous créons une instance de `LoadOptions` (utile pour de futures personnalisations) et ouvrons le fichier `.one` existant.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

### Étape 2 : Obtenir la page cible

Pour simplifier, nous travaillons avec la première page du document, mais vous pouvez naviguer vers n’importe quelle page souhaitée.

```java
Page page = oneFile.getFirstChild();
```

### Étape 3 : Charger l’image à intégrer

Instanciez un objet `Image` en passant la référence du document et le chemin du fichier image.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

### Étape 4 : Définir les dimensions de l’image Java (facultatif)

Si vous avez besoin que l’image s’ajuste à une zone spécifique, modifiez sa largeur, sa hauteur et ses décalages. C’est ici que le mot‑clé secondaire **set image dimensions java** prend tout son sens.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

### Étape 5 : Ajouter l’image à la page

La méthode `appendChildLast` ajoute l’image en tant que dernier élément de la page sélectionnée.

```java
page.appendChildLast(image);
```

### Étape 6 : Enregistrer le document – vous pouvez également enregistrer OneNote au format PDF

Enfin, persistez les modifications. L’exemple montre comment enregistrer le fichier au format PDF, répondant au mot‑clé secondaire **save onenote as pdf**.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Problèmes courants et solutions

| Symptom | Cause probable | Solution |
|---------|----------------|----------|
| `FileNotFoundException` lors du chargement de l’image | Chemin de l’image incorrect | Vérifiez que `dataDir` et le nom du fichier image sont corrects. |
| L’image apparaît déformée | Largeur/hauteur définie incorrectement | Utilisez les dimensions d’origine de l’image ou calculez un ratio d’aspect approprié avant d’appeler `setWidth`/`setHeight`. |
| La sortie PDF est vide | Licence manquante pour Aspose.Note | Appliquez une licence valide avant d’appeler `save`. |

## Questions fréquentes

### Q1 : Puis‑je insérer plusieurs images dans un même document OneNote avec cette méthode ?

**R :** Oui. Répétez simplement les Étapes 3‑5 pour chaque image que vous souhaitez ajouter, en ciblant la même page ou des pages différentes.

### Q2 : Aspose.Note for Java est‑il compatible avec toutes les versions de OneNote ?

**R :** Aspose.Note for Java prend en charge les fichiers OneNote créés avec Microsoft OneNote 2010 et les versions ultérieures.

### Q3 : Puis‑je insérer des images de différents formats, comme PNG ou GIF, dans un document OneNote ?

**R :** Absolument. La bibliothèque accepte les formats PNG, JPEG, GIF, BMP et plusieurs autres formats courants.

### Q4 : Existe‑t‑il une version d’essai d’Aspose.Note for Java disponible pour les tests ?

**R :** Oui, vous pouvez télécharger une version d’essai gratuite depuis le site d’Aspose pour évaluer l’API avant l’achat.

### Q5 : Comment obtenir le support technique pour Aspose.Note for Java ?

**R :** Vous pouvez obtenir de l’aide en visitant le [forum](https://forum.aspose.com/c/note/28) dédié aux produits Aspose.Note.

## Conclusion

Vous disposez maintenant d’un exemple complet, prêt pour la production, qui montre **comment ajouter une image à OneNote** en utilisant Java, personnaliser son apparence et, éventuellement, **enregistrer OneNote au format PDF**. N’hésitez pas à adapter le code à vos propres flux de travail—que vous construisiez un moteur de rapports, un système de documentation automatisé ou une application de prise de notes personnalisée.

---

**Dernière mise à jour :** 2026-03-19  
**Testé avec :** Aspose.Note for Java 24.10  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}