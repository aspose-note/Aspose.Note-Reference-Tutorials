---
title: Check if OneNote Document is Encrypted - Java
linktitle: Check if OneNote Document is Encrypted - Java
second_title: Aspose.Note Java API
description: Learn how to check if a OneNote document is encrypted in Java using Aspose.Note. Follow our step-by-step guide for efficient document processing.
weight: 10
url: /java/onenote-document-loading/check-document-encrypted/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Check if OneNote Document is Encrypted - Java

## Introduction

When working with OneNote documents in Java, it's crucial to ensure that the document is not encrypted before processing it. Encrypting documents can add an extra layer of security, but it can also complicate the processing steps if not handled correctly. In this tutorial, we'll guide you through the process of checking whether a OneNote document is encrypted using Aspose.Note for Java.

## Prerequisites

Before you begin, make sure you have the following prerequisites in place:

1. Java Development Kit (JDK): Ensure that you have Java installed on your system. You can download it from [here](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

2. Aspose.Note for Java Library: Download and set up the Aspose.Note for Java library. You can find the download link [here](https://releases.aspose.com/note/java/).

## Import Packages

To begin, import the necessary packages in your Java project:

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```

Let's break down the process into multiple steps:

## Step 1: Check if Document from Stream is Encrypted

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

Explanation:

- This method checks if a document loaded from a stream is encrypted.
- It sets the document password using `setDocumentPassword` method of `LoadOptions` class.
- The `Document.isEncrypted` method is used to determine whether the document is encrypted or not.

## Step 2: Check if Document from File is Encrypted

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

Explanation:

- This method checks if a document loaded from a file is encrypted.
- It uses the `Document.isEncrypted` method similarly to the previous step but with a file path and password parameter.

## Conclusion

In this tutorial, we learned how to check if a OneNote document is encrypted in Java using Aspose.Note. By following the step-by-step guide and utilizing the provided code examples, you can efficiently determine the encryption status of your documents, ensuring smooth processing in your Java applications.

## FAQ's

### Q1: Can I check encryption status without providing a password?

A1: Yes, you can check the encryption status without providing a password. The `Document.isEncrypted` method allows you to do so.

### Q2: What happens if I provide an incorrect password?

A2: If you provide an incorrect password when checking encryption status, the method will return `true`, indicating that the document is encrypted, but the provided password is incorrect.

### Q3: Is it possible to decrypt an encrypted document programmatically?

A3: Yes, you can decrypt an encrypted document programmatically by providing the correct password during document loading.

### Q4: Can I use Aspose.Note for other document formats besides OneNote?

A4: No, Aspose.Note is specifically designed for working with OneNote documents only.

### Q5: Where can I find more resources and support for Aspose.Note for Java?

A5: You can visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for community support and documentation.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
