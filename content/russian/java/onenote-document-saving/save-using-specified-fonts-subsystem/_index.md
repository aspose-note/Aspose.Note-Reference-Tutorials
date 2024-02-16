---
title: Сохранение с использованием указанной подсистемы шрифтов в OneNote
linktitle: Сохранение с использованием указанной подсистемы шрифтов в OneNote
second_title: Aspose.Note Java API
description: Узнайте, как сохранять документы OneNote с использованием указанной подсистемы шрифтов в Java с помощью Aspose.Note. Обеспечьте единообразное представление шрифтов на разных платформах без особых усилий.
type: docs
weight: 22
url: /ru/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---
## Введение

Aspose.Note для Java предоставляет надежные возможности для работы с документами OneNote. Одним из общих требований при работе с такими документами является обеспечение правильного сохранения шрифтов, особенно если документ необходимо экспортировать или сохранить в других форматах, например PDF. Это руководство проведет вас через процесс сохранения документов OneNote при указании подсистемы шрифтов, обеспечивая согласованное и точное представление текста на различных платформах.

## Предварительные условия

Прежде чем мы углубимся в руководство, убедитесь, что у вас настроены следующие предварительные условия:

### 1. Комплект разработки Java (JDK)

 Убедитесь, что в вашей системе установлен Java Development Kit (JDK). Вы можете скачать его с[здесь](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) если вы еще этого не сделали.

### 2. Aspose.Note для библиотеки Java

 Загрузите и настройте библиотеку Aspose.Note для Java. Вы можете скачать его с сайта[Веб-сайт](https://releases.aspose.com/note/java/).

## Импортировать пакеты

Обязательно импортируйте необходимые пакеты в свой Java-проект:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Теперь давайте разобьем каждый пример на несколько этапов, чтобы лучше понять процесс.

## Шаг 1. Сохранение с использованием подсистемы шрифтов документа с именем шрифта по умолчанию

На этом шаге показано, как сохранить документ в формате PDF, используя указанное имя шрифта по умолчанию.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Загрузите документ в Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Укажите шрифт по умолчанию.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Сохраните документ в формате PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

На этом этапе:
- Документ OneNote загружается с помощью Aspose.Note.
- Шрифт по умолчанию указан как «Times New Roman».
- Документ сохраняется в формате PDF с указанным шрифтом.

## Шаг 2. Сохранение с использованием подсистемы шрифтов документа со шрифтом по умолчанию из файла

На этом шаге показано, как сохранить документ в формате PDF, используя шрифт по умолчанию, загруженный из файла.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Загрузите документ в Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Укажите путь к файлу шрифта.
    String fontFile = "geo_1.ttf";

    // Укажите шрифт по умолчанию из файла.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Сохраните документ в формате PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

На этом этапе:
- Загружен файл шрифта «geo_1.ttf».
- Шрифт по умолчанию указывается из загруженного файла шрифта.
- Документ сохраняется в формате PDF с указанным шрифтом.

## Шаг 3. Сохранение с использованием подсистемы шрифтов документа со шрифтом по умолчанию из потока

На этом шаге показано, как сохранить документ в формате PDF, используя шрифт по умолчанию, загруженный из потока.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Загрузите документ в Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Укажите путь к файлу шрифта.
    String fontFile = "geo_1.ttf";

    // Загрузите файл шрифта как поток.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Укажите шрифт по умолчанию из потока.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Сохраните документ в формате PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

На этом этапе:
- Файл шрифта «geo_1.ttf» загружается как поток.
- Шрифт по умолчанию указывается из загруженного потока.
- Документ сохраняется в формате PDF с указанным шрифтом.

## Заключение

В этом уроке мы узнали, как сохранять документы OneNote с использованием указанной подсистемы шрифтов в Java с помощью Aspose.Note. Выполнив эти шаги, вы сможете обеспечить единообразное представление шрифтов на различных платформах при экспорте или сохранении документов.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я указать разные шрифты для разных частей документа?

О1: Да, вы можете указать разные шрифты для разных частей документа, используя Aspose.Note для Java.

### Вопрос 2. Совместим ли Aspose.Note со всеми версиями OneNote?

О2: Aspose.Note поддерживает различные версии OneNote, обеспечивая совместимость в различных средах.

### Вопрос 3. Как устранить отсутствие шрифтов при сохранении документов?

A3: Aspose.Note предоставляет возможность указать шрифты по умолчанию для эффективной обработки отсутствующих шрифтов во время сохранения документа.

### Вопрос 4. Могу ли я настроить свойства шрифта, такие как размер и стиль?

О4: Да, вы можете настроить свойства шрифта, такие как размер, стиль и цвет, с помощью Aspose.Note для Java.

### Вопрос 5: Доступна ли пробная версия Aspose.Note для Java?

О5: Да, вы можете получить бесплатную пробную версию Aspose.Note для Java на веб-сайте.