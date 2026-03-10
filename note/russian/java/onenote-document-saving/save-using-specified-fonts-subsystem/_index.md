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

## Введение

Во многих бизнес-сценариях вам необходимо **сохранить OneNote в формате PDF**, сохранив целостность оригинальных страниц. Aspose.Note для Java позволяет управлять подсистемой шрифтов во время конвертации. В этом руководстве мы рассмотрим три практических способа **конвертации OneNote в PDF**, включая **загрузку файлов шрифтов**, **указание шрифта по умолчанию** и даже **использование потока шрифта**, когда шрифт недоступен на включенной машине.

## Быстрые ответы
- **Что означает «сохранить OneNote как PDF»?** Он преобразует файл .one в PDF, сохраняя макет и стили нетронутыми.
- **Какой API-интерфейс шрифтов?** `DocumentFontsSubsystem` позволяет задать шрифт по умолчанию или загрузить пользовательский файл/поток шрифта.
- **Нужна ли лицензия для продакшна?** Да, для использования не в пробном режиме требуется коммерческая лицензия Aspose.Note.
- **Можно ли конвертировать несколько файлов пакетно?** Конечно — просто выполните цикл по функции и сохраните `Document`.
- **Какая версия Java требуется?** Java15 или новая версия (пример использует JDK15).

## Что такое «сохранить OneNote как PDF» с подсистемой шрифтов?

Сохранение OneNote как PDF с подсистемой шрифта означает, что во время процесса конвертации Aspose.Note заменяет любые отсутствующие глифы шрифтом, который вы предоставляете. Это гарантирует, что PDF будет выглядеть одинаково на любом устройстве, даже если оригинальный шрифт не установлен.

## Зачем контролировать подсистему шрифтов при **преобразовании OneNote в PDF**?

- **Последовательный брендинг** — корпоративные документы, сохраняющие британский шрифт.
- **Надёжность кроссплатформенно** — PDF-файл аналогичного формата в Windows, macOS, Linux и на мобильных устройствах.
- **Снижение ошибок** — ссылаясь на отсутствие ошибок в шрифтах, получая чистый вывод.

## Предварительные условия

### 1. Комплект разработки Java (JDK)

Убедитесь, что в вашей системе установлен Java Development Kit (JDK). Вы можете скачать его [здесь](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html), если ещё не сделали этого.

### 2. Aspose.Note для библиотеки Java

скачать и настроить функционал Aspose.Note для Java. Вы можете загрузить ее с [веб‑сайта](https://releases.aspose.com/note/java/).

## Импорт пакетов

Убедитесь, что в ваш Java‑проект импортированы необходимые пакеты:

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

## Как **сохранить OneNote в формате PDF** с помощью подсистемы шрифтов документа со шрифтом по умолчанию

### Шаг 1: Сохранить, используя подсистему шрифтов документа с именем шрифта по умолчанию

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

На этом этапе:
- Документ OneNote загружается с помощью Aspose.Note.
- **Шрифт по умолчанию** задаётся как **"Times New Roman"**.
- Документ сохраняется в формате PDF с выбранным шрифтом.

### Шаг 2: Сохранить, используя подсистему шрифтов документа со шрифтом по умолчанию из файла

Здесь мы **загружаем файл пользовательского шрифта** и используем его в качестве запасного варианта при преобразовании в PDF.

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

Ключевые моменты:
- **Пользовательский файл шрифта** `geo_1.ttf` ** загружается с диска**.
- `usingDefaultFontFromFile` **устанавливает шрифт по умолчанию из файла**, гарантируя, что PDF использует этот шрифт, если оригинальный отсутствует.
- Полученный PDF-файл решил сохранить запертое устройство.

### Шаг 3: Сохранить, используя подсистему шрифтов документа со шрифтом по умолчанию из потока

Иногда шрифт может храниться в базе данных или быть получен по сети. В этом примере показано, как **использовать поток шрифтов**.

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

Что здесь происходит:
- Шрифт файла открывается как **InputStream**, что полезно, когда шрифт находится не в источнике файлов.
- `usingDefaultFontFromStream` **использует шрифт потока** для определения шрифта-запасного.
- Файл OneNote сохраняется в формате PDF с использованием шрифтов потока.

## Распространенные проблемы и решения

| Проблема | Почему происходит | Как исправить |
|----------|-------------------|---------------|
| **Предупреждения о недостающих шрифтах** | Исходный файл .one ссылается на шрифт, который отсутствует на машине. | Укажите шрифт по умолчанию через `usingDefaultFont`, `usingDefaultFontFromFile` или `usingDefaultFromStream`. |
| **Файл пользовательского шрифта не найден** | Неправильный путь к файлу `.ttf`. | Используйте абсолютные пути или проверьте соответствующий путь из рабочего руководства. |
| **Поток не закрыт** | Исключение происходит до вызова `close()`. | Используйте try-with-resources (`try (InputStreamstream = ...) { ... }`) для закрытия ручки. |

## Часто задаваемые вопросы

**Вопрос: Можно ли указывать разные шрифты для разных частей документа?**
О: Да, вы можете применить пользовательские настройки шрифта к отдельным элементам форматированного текста, используя класс `Font` в Aspose.Note.

**Вопрос: Совместим ли Aspose.Note со всеми версиями OneNote?**
Ответ: Aspose.Note поддерживает файлы OneNote из последних настольных и мобильных версий, вызывая изменение конфигурации.

**В: Как обрабатывать недостающие шрифты при сохранении документов?**
A: Используйте методы подсистемы шрифтов, показанные выше (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`), чтобы выбрать запасной шрифт.

**В: Можно ли настроить свойства шрифта, такие как размер и стиль?**
О: Абсолютно — API позволяет задавать размер, стиль, цвет и другие атрибуты для каждого отдельного пробега.

**В: Доступна ли пробная версия Aspose.Note для Java?**
О: Да, бесплатную пробную версию можно скачать с сайта Aspose.

## Заключение

В этом руководстве мы узнали, как **сохранить OneNote как PDF**, контролируя подсистему шрифтов в Java с помощью Aspose.Note. Следуя трем подходам — указанию имени шрифта по умолчанию, загрузке пользовательского файла шрифта или использованию потока шрифта — вы можете гарантировать согласованное отображение шрифтов на разных платформах при экспорте или сохранении ваших документов OneNote.

---

**Последнее обновление:** 2025-12-18  
**Тестировано с:** Aspose.Note for Java 24.11  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}