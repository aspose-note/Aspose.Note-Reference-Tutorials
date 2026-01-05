---
date: 2026-01-05
description: Apprenez comment définir la locale par défaut, charger un document OneNote,
  définir la licence Aspose, convertir OneNote en PNG et enregistrer OneNote en tant
  qu’image à l’aide d’Aspose.Note pour Java.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Définir la locale par défaut dans OneNote – Aspose.Note Java
url: /fr/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir la locale par défaut dans OneNote – Aspose.Note Java

## Introduction

Si vous devez **définir la locale par défaut** lors du traitement de fichiers OneNote, Aspose.Note pour Java rend cela très simple. Dans ce tutoriel, nous passerons en revue tout ce dont vous avez besoin — de la licence du produit au chargement d’un document OneNote, en passant par la modification de la locale, et enfin la conversion du fichier en image PNG. À la fin, vous pourrez personnaliser les paramètres de langue et générer des sorties spécifiques à la locale avec seulement quelques lignes de code.

## Quick Answers
- **Que fait « définir la locale par défaut » ?** Elle définit la langue et le formatage régional utilisés par Aspose.Note lors de la lecture ou de l’écriture de fichiers OneNote.  
- **Ai-je besoin d’une licence ?** Oui — définissez la licence Aspose pour débloquer toutes les fonctionnalités.  
- **Quelle version de Java est requise ?** Toute version JDK 8+ est prise en charge.  
- **Puis-je convertir OneNote en PNG ?** Absolument ; l’API vous permet d’enregistrer les pages sous forme d’images.  
- **Le processus est‑il thread‑safe ?** Définir la locale par défaut est global, il faut donc la configurer une seule fois au démarrage de l’application.

## Qu’est‑ce que « définir la locale par défaut » dans Aspose.Note ?

Définir la locale par défaut indique à Aspose.Note quelle langue et quelles conventions culturelles appliquer lors de l’analyse des dates, des nombres et du texte. C’est essentiel pour les applications multi‑régionales qui nécessitent un formatage cohérent entre les différentes locales des utilisateurs.

## Pourquoi définir la locale par défaut lors du travail avec OneNote ?

- **Représentation précise des données :** Les dates et les nombres s’affichent correctement pour le public cible.  
- **Chaînes d’interface cohérentes :** Le texte extrait de OneNote respecte les paramètres de langue.  
- **Conversion simplifiée :** Lorsque vous convertissez ultérieurement un fichier OneNote en PNG ou dans d’autres formats, la mise en page visuelle correspond à la locale attendue.

## Prérequis

- **Environnement de développement Java :** JDK installé et `JAVA_HOME` configuré.  
- **Bibliothèque Aspose.Note :** Téléchargez le dernier JAR depuis le [lien de téléchargement](https://releases.aspose.com/note/java/).  
- **Un fichier de licence Aspose valide** (l’essai gratuit fonctionne pour les tests).

## Import Packages

Avant d’écrire du code, importez les classes qui fournissent les fonctionnalités requises.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Étape 1 : Définir la licence Aspose

```java
License license = new License();
license.setLicense("licenseFile");
```

Définir la licence Aspose débloque toutes les fonctionnalités, y compris la gestion de la locale et la conversion d’images.

## Étape 2 : Définir la locale par défaut

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

Ici, nous **définissons la locale par défaut** sur l’anglais (`en`) avec le code pays `rs`. Ajustez les codes de langue et de pays pour correspondre à votre région cible.

## Étape 3 : Charger le document OneNote

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

Cette étape **charge le document OneNote** dans l’objet `Document` afin que vous puissiez travailler avec son contenu.

## Étape 4 : Convertir OneNote en PNG (conversion de fichier OneNote)

```java
oneFile.save("sample.png");
```

La méthode `save` effectue une **conversion de fichier onenote**, exportant le bloc‑note (ou une page spécifique) sous forme d’image PNG — ce qui correspond à **convertir onenote en png** et **enregistrer onenote en tant qu’image**.

## Problèmes courants et astuces

- **Licence introuvable :** Assurez‑vous que le chemin vers `licenseFile` est correct et que le fichier possède les permissions de lecture.  
- **Locale non appliquée :** Appelez `Locale.setDefault` **avant** de charger le document.  
- **Sortie d’image manquante :** Vérifiez que le fichier OneNote contient réellement des pages rendables ; les blocs‑notes vides produiront un PNG vierge.

## FAQ

**Q : Aspose.Note est‑il compatible avec différentes versions de Java ?**  
R : Oui, Aspose.Note prend en charge Java 8 et les versions ultérieures, assurant une large compatibilité avec les environnements de développement.

**Q : Puis‑je intégrer Aspose.Note avec d’autres bibliothèques Java ?**  
R : Absolument. L’API fonctionne parfaitement avec des bibliothèques populaires telles qu’Apache POI, Jackson et Spring.

**Q : Aspose.Note propose‑t‑il la prise en charge de différents formats de fichiers ?**  
R : Bien que son objectif principal soit les fichiers OneNote, la bibliothèque peut exporter vers PNG, JPEG, PDF et d’autres formats d’image.

**Q : Existe‑t‑il un forum communautaire pour les utilisateurs d’Aspose.Note afin de demander de l’aide et partager leurs connaissances ?**  
R : Oui, le forum communautaire d’Aspose offre une plateforme où les utilisateurs peuvent échanger avec des experts, poser des questions et collaborer sur des solutions. Consultez le [forum d’assistance](https://forum.aspose.com/c/note/28) pour obtenir de l’aide.

**Q : Puis‑je essayer Aspose.Note avant d’acheter ?**  
R : Bien sûr, vous pouvez explorer les fonctionnalités d’Aspose.Note en profitant de l’essai gratuit proposé sur le site web.

## Conclusion

En suivant ces étapes, vous avez appris à **définir la locale par défaut**, **charger un document OneNote**, **définir la licence Aspose**, et **convertir OneNote en PNG** en utilisant Aspose.Note pour Java. Ce flux de travail vous permet de générer des rapports et des images sensibles à la locale, adaptés à un public mondial.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-05  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose  

---