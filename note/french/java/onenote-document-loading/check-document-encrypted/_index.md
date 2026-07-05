---
date: 2026-07-05
description: Apprenez comment vérifier le chiffrement OneNote à l'aide d'Aspose.Note
  pour Java. Détectez les fichiers OneNote chiffrés avant le chargement afin d'éviter
  les erreurs et d'améliorer l'expérience utilisateur.
keywords:
- check onenote encryption
- Aspose.Note encryption detection
- Java OneNote password check
linktitle: Vérifier si le document OneNote est chiffré - Java
second_title: Aspose.Note Java API
title: vérifier le chiffrement OneNote – Vérifier le chiffrement des documents OneNote
  avec Java
url: /fr/java/onenote-document-loading/check-document-encrypted/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}  
{{< blocks/products/pf/main-container >}}  
{{< blocks/products/pf/tutorial-page-section >}}  

# Vérifier si le document OneNote est chiffré – Java  

## Introduction  

Lorsque vous travaillez avec des fichiers OneNote dans une application Java, la première chose à savoir est **si le document est chiffré**. Tenter de charger un fichier chiffré sans le mot de passe approprié provoquera des exceptions et interrompra votre flux de travail. Dans ce tutoriel, nous vous expliquerons **comment vérifier le chiffrement OneNote** avec Aspose.Note for Java, afin que vous puissiez décider en toute sécurité s'il faut inviter l'utilisateur à saisir un mot de passe ou continuer le traitement du fichier.  

## Réponses rapides  

- **Quelle méthode détermine le chiffrement ?** `Document.isEncrypted`  
- **Ai-je besoin d'un mot de passe pour vérifier ?** Non, vous pouvez interroger l'état sans mot de passe.  
- **Quelle version de l'API fonctionne ?** Toute version récente d'Aspose.Note for Java (testée avec la 26.4).  
- **Puis-je vérifier à la fois les flux et les chemins de fichiers ?** Oui – l'API prend en charge les deux.  
- **Que se passe-t-il si le mot de passe est incorrect ?** La méthode renvoie `true`, indiquant que le fichier reste chiffré.  

## Qu'est-ce que la vérification du chiffrement OneNote ?  

Vérifier le chiffrement OneNote signifie déterminer de manière programmatique si un fichier OneNote (`.one`) est protégé par un mot de passe avant toute tentative de lecture de son contenu. Cette vérification rapide de l'état empêche les exceptions d'exécution, vous permet d'inviter les utilisateurs uniquement lorsque cela est nécessaire, et vous aide à rester conforme aux politiques de sécurité.  

## Pourquoi vérifier le chiffrement OneNote avant le chargement ?  

Charger un fichier OneNote chiffré sans fournir le mot de passe correct déclenche une exception qui peut faire planter votre service ou afficher une erreur déroutante à l'utilisateur. En vérifiant d'abord le drapeau de chiffrement, vous pouvez présenter une invite de mot de passe uniquement lorsque cela est nécessaire, réduire les entrées/sorties inutiles, et garantir que le contenu protégé est traité conformément aux règles de gouvernance d'entreprise.  

## Prérequis  

1. **Java Development Kit (JDK)** – Java 11 ou version ultérieure est requis. Téléchargez-le depuis [ici](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.Note for Java** – obtenez la bibliothèque depuis la page officielle de téléchargement [ici](https://releases.aspose.com/note/java/).  

## Importer les packages  

La classe `Document` représente un fichier OneNote et fournit des méthodes pour charger et inspecter son contenu.  

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```  

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```  

## Comment vérifier le statut de chiffrement d'un document chargé depuis un flux ?  

`Document.isEncrypted` est une méthode statique qui renvoie un booléen indiquant si un fichier OneNote est chiffré. Chargez votre flux OneNote de type PDF et appelez la méthode statique `Document.isEncrypted`. La méthode renvoie un booléen indiquant le chiffrement et, lorsque le fichier n'est pas chiffré, remplit un tableau de référence avec l'instance `Document` chargée afin que vous n'ayez pas besoin d'un second appel de chargement.  

**Réponse directe (40‑70 mots) :**  
Appelez `Document.isEncrypted(inputStream, loadOptions, ref)` – cela indique instantanément si le flux est protégé par un mot de passe. Si le résultat est `false`, `ref[0]` contient l'objet `Document` prêt à l'emploi, vous permettant de poursuivre le traitement sans I/O supplémentaire. Si le résultat est `true`, le flux est chiffré et vous devez demander un mot de passe avant de continuer.  

**Explication**  

- `LoadOptions` vous permet de fournir éventuellement un mot de passe (`setDocumentPassword`).  
- `Document.isEncrypted(stream, loadOptions, ref)` vérifie le statut de chiffrement du flux.  
- Le tableau `ref` reçoit une référence au `Document` chargé lorsque le fichier n'est **pas** chiffré, vous permettant de poursuivre le traitement sans second appel de chargement.  

```java
public static void CheckIfDocumentFromStreamIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromStreamIsEncrypted
    String dataDir = "Your Document Directory";

    LoadOptions loadOptions = new LoadOptions();
    loadOptions.setDocumentPassword("password");

    FileInputStream stream = new FileInputStream(Paths.get(dataDir, "Sample1.one").toString());

    try {
        Document ref[] = { null };
        if (!Document.isEncrypted(stream, loadOptions, ref)) {
            System.out.println("The document is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Provide a password.");
        }
    } finally {
        stream.close();
    }
    // ExEnd:CheckIfDocumentFromStreamIsEncrypted
}
```  

## Comment vérifier le statut de chiffrement d'un document chargé depuis un chemin de fichier ?  

`Document.isEncrypted` propose également une surcharge qui fonctionne directement avec un chemin de fichier et une chaîne de mot de passe. Cette surcharge suit le même schéma de retour booléen, remplissant le tableau de référence uniquement lorsque le fichier n'est pas chiffré.  

**Réponse directe (40‑70 mots) :**  
Appelez `Document.isEncrypted(filePath, password, ref)` – l'appel renvoie `true` si le fichier est chiffré (ou si le mot de passe est incorrect) et `false` sinon. Lorsque le résultat est `false`, `ref[0]` contient le `Document` entièrement chargé, prêt à être manipulé. Cette approche évite une étape de chargement séparée et garde votre code concis.  

**Explication**  

- Cette surcharge fonctionne directement avec un chemin de fichier et une chaîne de mot de passe.  
- Si le fichier n'est **pas** chiffré, `isEncrypted` renvoie `false` et la référence `ref[0]` contient le document chargé.  
- Si le mot de passe est incorrect, la méthode renvoie toujours `true`, indiquant que le fichier reste chiffré.  

```java
public static void CheckIfDocumentFromFileIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromFileIsEncrypted
    String dataDir = "Your Document Directory";

    Document ref[] = { null };
    if (!Document.isEncrypted(Paths.get(dataDir, "Sample1.one").toString(), "VerySecretPassword", ref)) {
        if (ref[0] != null) {
            System.out.println("The document is decrypted. It is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Invalid password was provided.");
        }
    } else {
        System.out.println("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
    // ExEnd:CheckIfDocumentFromFileIsEncrypted
}
```  

## Pièges courants et conseils  

- **Ne jamais coder en dur les mots de passe** dans le code de production ; récupérez‑les de manière sécurisée (par ex., depuis un coffre).  
- Fermez toujours les flux dans un bloc `finally` ou utilisez try‑with‑resources pour éviter les fuites de ressources.  
- Si vous recevez `true` de `isEncrypted` et que `ref[0]` est `null`, le fichier est soit chiffré **ou** le mot de passe fourni est incorrect. Demandez à l'utilisateur le bon mot de passe et réessayez.  

## Questions fréquemment posées  

**Q : Puis-je vérifier le statut de chiffrement sans fournir de mot de passe ?**  
R : Oui. Appelez `Document.isEncrypted` avec une instance `LoadOptions` qui ne définit pas de mot de passe ; la méthode indiquera simplement si le fichier est chiffré.  

**Q : Que se passe-t-il si je fournis un mot de passe incorrect ?**  
R : La méthode renvoie `true`, indiquant que le document reste chiffré, et `ref[0]` sera `null`.  

**Q : Existe-t-il un moyen de déchiffrer le document programmatiquement ?**  
R : Oui. Une fois le bon mot de passe connu, transmettez‑le à `LoadOptions` (ou à la surcharge qui accepte un mot de passe) et chargez le document ; l'API le déchiffrera à la volée.  

**Q : Aspose.Note fonctionne-t-il avec d'autres formats Microsoft ?**  
R : Aspose.Note est conçu spécifiquement pour les fichiers OneNote (`.one`) uniquement. Pour Word, Excel, PowerPoint, etc., envisagez respectivement Aspose.Words, Aspose.Cells, Aspose.Slides.  

**Q : Où puis-je trouver plus d'exemples et d'assistance ?**  
R : Consultez le [forum Aspose.Note](https://forum.aspose.com/c/note/28) pour l'aide de la communauté, et vérifiez la documentation officielle pour des exemples de code supplémentaires.  

## Conclusion  

Dans ce guide, nous avons démontré **comment vérifier le chiffrement OneNote** à l'aide d'Aspose.Note for Java, en couvrant les scénarios basés sur les flux et sur les fichiers. En intégrant ces vérifications dans votre application, vous pouvez gérer élégamment les fichiers OneNote chiffrés, améliorer l'expérience utilisateur et maintenir votre pipeline de traitement robuste.  

---  

**Dernière mise à jour :** 2026-07-05  
**Testé avec :** Aspose.Note 26.4 for Java  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Créer un document OneNote – Charger le carnet avec Aspose.Note](/note/java/onenote-notebook-operations/loading-notebook/)
- [Protéger par mot de passe OneNote avec Aspose.Note for Java](/note/java/onenote-notebook-operations/write-password-protected-document/)
- [Obtenir les informations de format de fichier Aspose Note depuis OneNote avec Java](/note/java/onenote-document-loading/get-file-format-info/)


{{< /blocks/products/pf/tutorial-page-section >}}  
{{< /blocks/products/pf/main-container >}}  
{{< /blocks/products/pf/main-wrap-class >}}