---
date: 2025-12-04
description: Apprenez à extraire des images des fichiers OneNote et à convertir OneNote
  en texte en Java avec Aspose.Note. Guide étape par étape avec des exemples de code.
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Extraire des images de OneNote à l'aide de Document Visitor - Java
url: /fr/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extraire des images de OneNote à l'aide du Document Visitor - Java

## Introduction

Aspose.Note for Java facilite **l'extraction d'images de OneNote** ainsi que la lecture du fichier `.one` sous-jacent en Java. Dans ce tutoriel, nous vous guiderons à travers un exemple complet et pratique montrant comment charger un fichier OneNote, parcourir sa structure avec un `DocumentVisitor` personnalisé, et extraire à la fois les images et le texte brut. À la fin, vous saurez également comment **convertir OneNote en texte** si vous avez seulement besoin du contenu textuel.

## Réponses rapides
- **Quelle bibliothèque faut‑il ?** Aspose.Note for Java (lien de téléchargement ci‑dessous).  
- **Puis‑je extraire uniquement les images ?** Oui – implémentez la méthode `VisitImageStart` dans un `DocumentVisitor`.  
- **Comment lire un fichier .one en Java ?** Utilisez `new Document(path, new LoadOptions())`.  
- **Ai‑je besoin d’une licence pour la production ?** Une licence commerciale est requise pour une utilisation hors période d’essai.  
- **Quelle version de Java est prise en charge ?** JDK 8 ou supérieur.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

1. Java Development Kit (JDK) 8 ou plus récent installé.  
2. Bibliothèque Aspose.Note for Java téléchargée. Vous pouvez la télécharger **[ici](https://releases.aspose.com/note/java/)**.  
3. Un document OneNote (fichier `.one`) dont vous souhaitez extraire les images ou convertir en texte.

## Importer les packages

Tout d'abord, importez les classes nécessaires depuis l'API Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## Étape 1 : Configurer un Document Visitor personnalisé

Créez une classe qui étend `DocumentVisitor`. Cette classe sera appelée pour chaque nœud du document OneNote, vous permettant d'**extraire des images de OneNote** et, éventuellement, de collecter du texte.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## Étape 2 : Implémenter les méthodes du visiteur

Ajoutez des surcharges pour les types de nœuds qui vous intéressent. Ci‑dessous, nous gérons le texte enrichi, les images, les titres, les pages, les contours et les éléments de contour. La méthode `VisitImageStart` est celle où l'extraction d'image se produit.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### Pourquoi implémenter ces méthodes ?

- **Extraire des images de OneNote :** `VisitImageStart` vous donne un accès direct aux octets bruts de l'image.  
- **Convertir OneNote en texte :** `VisitRichTextStart` collecte le contenu textuel, permettant une opération simple de **conversion de OneNote en texte**.  
- **Lire un fichier .one en Java :** Le pattern visiteur abstrait la structure sous‑jacente du fichier `.one`, vous n’avez donc pas besoin d’analyser vous‑même le format binaire.

## Étape 3 : Exécuter le visiteur depuis votre méthode main

Chargez le fichier `.one`, créez une instance de votre visiteur, et démarrez le parcours.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Cas d'utilisation courants

- **Rapports automatisés :** Extraire les images et le texte d'un cahier de réunion OneNote pour générer un résumé PDF ou HTML.  
- **Migration de contenu :** Convertir les archives OneNote héritées en fichiers texte brut pour l'indexation ou l'ingestion par les moteurs de recherche.  
- **Extraction d'actifs numériques :** Récolter les captures d'écran, diagrammes ou photos intégrés pour les réutiliser dans d'autres applications.

## Dépannage et astuces

- **Cahiers volumineux :** Si vous rencontrez des problèmes de mémoire, traitez les pages individuellement vérifiant `VisitPageStart` et en chargeant les ressources au niveau de la page uniquement lorsque nécessaire.  
- **Formats d'image :** L'objet `Image` renvoie des octets bruts ; il peut être nécessaire de détecter le format (PNG, JPEG) avant l'enregistrement.  
- **Erreurs de licence :** Assurez‑vous d'avoir défini la licence Aspose (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) avant de charger le document en production.

## Questions fréquemment posées

**Q : Puis‑je extraire des types de contenu spécifiques du document OneNote ?**  
R : Oui – en surchargeant uniquement les méthodes du visiteur dont vous avez besoin (par ex., `VisitImageStart` pour les images, `VisitRichTextStart` pour le texte).

**Q : Aspose.Note for Java est‑il compatible avec différentes versions de documents OneNote ?**  
R : Absolument. La bibliothèque prend en charge toutes les principales versions de fichiers OneNote, vous pouvez donc lire en toute sécurité des projets **read .one file Java** quel que soit la version d'origine du OneNote.

**Q : Puis‑je intégrer ce processus d'extraction dans mon application Java ?**  
R : Oui. Le pattern visiteur fonctionne de manière transparente dans n'importe quel code Java ; il suffit d'ajouter le JAR de la bibliothèque et d'appeler l'exemple ci‑dessus.

**Q : Aspose.Note for Java offre‑t‑il un support pour la gestion de documents OneNote complexes ?**  
R : Oui. Les contours imbriqués, les médias intégrés et les données personnalisées sont tous exposés via l'API du visiteur.

**Q : Existe‑t‑il une limite de taille du document OneNote pouvant être traité ?**  
R : Il n'y a pas de limite stricte, mais les cahiers extrêmement volumineux peuvent nécessiter plus de mémoire du tas ; envisagez de les traiter page par page.

**Q : Comment convertir le texte extrait en fichier texte brut ?**  
R : Après que `myConverter.GetText()` renvoie une `String`, écrivez‑la dans un fichier en utilisant les I/O Java standard (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Dernière mise à jour :** 2025-12-04  
**Testé avec :** Aspose.Note for Java 24.10  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}