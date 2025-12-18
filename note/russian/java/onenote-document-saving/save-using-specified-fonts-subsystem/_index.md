---
date: 2025-12-18
description: Узнайте, как **сохранить OneNote в PDF** с использованием подсистемы
  указанных шрифтов в Java с Aspose.Note. Это руководство также показывает, как конвертировать
  OneNote в PDF, загружать пользовательские файлы шрифтов и задавать шрифты по умолчанию.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: Сохранить OneNote в PDF с использованием подсистемы указанных шрифтов
url: /ru/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Сохранить OneNote как PDF с использованием подсистемы указанных шрифтов

## Introduction

В многих бизнес‑сценариях вам необходимо **сохранить OneNote как PDF**, сохраняя точный вид оригинальных страниц. Aspose.Note for Java упрощает это, позволяя управлять подсистемой шрифтов во время конвертации. В этом руководстве мы рассмотрим три практических способа **конвертации OneNote в PDF**, включая **загрузку пользовательских файлов шрифтов**, **указание шрифта по умолчанию** и даже **использование потока шрифта**, когда шрифт недоступен на целевой машине.

## Quick Answers
- **Что означает «сохранить OneNote как PDF»?** Он преобразует файл .one в PDF, сохраняя макет и стили нетронутыми.  
- **Какой API управляет шрифтами?** `DocumentFontsSubsystem` позволяет задать шрифт по умолчанию или загрузить пользовательский файл/поток шрифта.  
- **Нужна ли лицензия для продакшна?** Да, для использования не в пробном режиме требуется коммерческая лицензия Aspose.Note.  
- **Можно ли конвертировать несколько файлов пакетно?** Конечно — просто выполните цикл по загрузке и сохранению `Document`.  
- **Какая версия Java требуется?** Java 15 или новее (пример использует JDK 15).

## What is “save OneNote as PDF” with a fonts subsystem?

Сохранение OneNote как PDF с подсистемой шрифтов означает, что во время процесса конвертации Aspose.Note заменяет любые отсутствующие глифы шрифтом, который вы предоставляете. Это гарантирует, что PDF будет выглядеть одинаково на любом устройстве, даже если оригинальный шрифт не установлен.

## Why control the fonts subsystem when you **convert OneNote to PDF**?

- **Последовательный брендинг** — корпоративные документы сохраняют точный шрифт.  
- **Надёжность кроссплатформенно** — PDF отображаются одинаково в Windows, macOS, Linux и на мобильных устройствах.  
- **Снижение ошибок** — предупреждения о недостающих шрифтах исчезают, получая чистый вывод.

## Prerequisites

### 1. Java Development Kit (JDK)

Убедитесь, что на вашей системе установлен Java Development Kit (JDK). Вы можете скачать его [здесь](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html), если ещё не сделали этого.

### 2. Aspose.Note for Java Library

Скачайте и настройте библиотеку Aspose.Note for Java. Вы можете загрузить её с [веб‑сайта](https://releases.aspose.com/note/java/).

## Import Packages

Убедитесь, что импортировали необходимые пакеты в ваш Java‑проект:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Теперь разберём каждый пример на несколько шагов, чтобы лучше понять процесс.

## How to **save OneNote as PDF** using Document Fonts Subsystem with a default font

### Step 1: Save Using Document Fonts Subsystem with Default Font Name

Шаг 1: Сохранить, используя подсистему шрифтов документа с именем шрифта по умолчанию

This step demonstrates how to **save OneNote as PDF** in a simple way by specifying a default font name.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

In this step:
- Документ OneNote загружается с помощью Aspose.Note.
- **Шрифт по умолчанию** задаётся как **"Times New Roman"**.
- Документ сохраняется в формате PDF с выбранным шрифтом.

### Step 2: Save Using Document Fonts Subsystem with Default Font from File

Шаг 2: Сохранить, используя подсистему шрифтов документа с шрифтом по умолчанию из файла

Here we **load a custom font file** and use it as the fallback when converting to PDF.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Key points:
- **Пользовательский файл шрифта** `geo_1.ttf` **загружается с диска**.
- `usingDefaultFontFromFile` **устанавливает шрифт по умолчанию из файла**, гарантируя, что PDF использует этот шрифт, если оригинальный отсутствует.
- Полученный PDF сохраняет задуманное отображение.

### Step 3: Save Using Document Fonts Subsystem with Default Font from Stream

Шаг 3: Сохранить, используя подсистему шрифтов документа с шрифтом по умолчанию из потока

Sometimes the font may be stored in a database or received over a network. This example shows how to **use a font stream**.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

What happens here:
- Файл шрифта открывается как **InputStream**, что полезно, когда шрифт находится в не файловом источнике.
- `usingDefaultFontFromStream` **использует поток шрифта** для определения шрифта‑запасного.
- Файл OneNote сохраняется как PDF с использованием шрифта из потока.

## Common Issues and Solutions

| Проблема | Почему происходит | Как исправить |
|----------|-------------------|---------------|
| **Предупреждения о недостающих шрифтах** | Исходный файл .one ссылается на шрифт, который отсутствует на машине. | Укажите шрифт по умолчанию через `usingDefaultFont`, `usingDefaultFontFromFile` или `usingDefaultFontFromStream`. |
| **Файл пользовательского шрифта не найден** | Неправильный путь к файлу `.ttf`. | Используйте абсолютные пути или проверьте относительный путь от рабочей директории. |
| **Поток не закрыт** | Исключение происходит до вызова `close()`. | Используйте try‑with‑resources (`try (InputStream stream = ...) { ... }`) для автоматического закрытия. |

## Frequently Asked Questions

**Q: Можно ли указать разные шрифты для разных частей документа?**  
A: Да, вы можете применять пользовательские настройки шрифта к отдельным элементам rich‑text, используя класс `Font` в Aspose.Note.

**Q: Совместим ли Aspose.Note со всеми версиями OneNote?**  
A: Aspose.Note поддерживает файлы OneNote из последних настольных и мобильных версий, обеспечивая широкую совместимость.

**Q: Как обрабатывать недостающие шрифты при сохранении документов?**  
A: Используйте методы подсистемы шрифтов, показанные выше (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`), чтобы предоставить запасной шрифт.

**Q: Можно ли настроить свойства шрифта, такие как размер и стиль?**  
A: Абсолютно — API позволяет задавать размер, стиль, цвет и другие атрибуты для каждого отдельного run.

**Q: Доступна ли пробная версия Aspose.Note for Java?**  
A: Да, бесплатную пробную версию можно скачать с сайта Aspose.

## Conclusion

В этом руководстве мы узнали, как **сохранить OneNote как PDF**, контролируя подсистему шрифтов в Java с помощью Aspose.Note. Следуя трем подходам — указанию имени шрифта по умолчанию, загрузке пользовательского файла шрифта или использованию потока шрифта — вы можете гарантировать согласованное отображение шрифтов на разных платформах при экспорте или сохранении ваших документов OneNote.

---

**Последнее обновление:** 2025-12-18  
**Тестировано с:** Aspose.Note for Java 24.11  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}