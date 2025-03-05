---
title: Сохранить в PDF в Aspose.Note
linktitle: Сохранить в PDF в Aspose.Note
second_title: Aspose.Note .NET API
description: Узнайте, как сохранить документы Microsoft OneNote в формате PDF с помощью Aspose.Note для .NET. Пошаговое руководство с примерами кода для макетов страниц Letter и A4.
type: docs
weight: 26
url: /ru/net/loading-and-saving-operations/save-to-pdf/
---
## Введение

В этом уроке мы рассмотрим, как сохранять документы в формате PDF с помощью Aspose.Note для .NET. Aspose.Note — это мощная библиотека, которая позволяет разработчикам программно работать с файлами Microsoft OneNote. Мы рассмотрим предварительные требования, импортируем пространства имен и предоставим пошаговые руководства по сохранению документов в PDF с различными макетами страниц.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас есть следующее:

- Visual Studio установлена в вашей системе.
-  Библиотека Aspose.Note для .NET загружена и установлена. Вы можете скачать его с[здесь](https://releases.aspose.com/note/net/).
- Базовые знания языка программирования C#.

## Импортировать пространства имен

Сначала давайте импортируем необходимые пространства имен в наш код C#:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Теперь, когда у нас есть все необходимые условия и импортированы пространства имен, давайте приступим к сохранению документов в PDF с различными макетами страниц.

## Шаг 1. Сохраните в PDF, используя настройки страницы Letter.


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // Путь к каталогу документов.
    string dataDir = "Your Document Directory";

    // Загрузите документ в Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // Сохраните документ.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Объяснение:

- Загружаем документ OneNote в Aspose.Note.
- Определите путь назначения для сохраненного PDF-файла.
-  Сохраните документ в PDF, используя`PdfSaveOptions` с`PageSettings` установлен в`Letter`.

## Шаг 2. Сохраните в PDF, используя настройки страницы A4 без ограничения по высоте.

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // Путь к каталогу документов.
    string dataDir = "Your Document Directory";

    // Загрузите документ в Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // Сохраните документ.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Объяснение:

- Как и в предыдущем шаге, мы загружаем документ OneNote в Aspose.Note.
- Определите путь назначения для сохраненного PDF-файла.
-  Сохраните документ в PDF, используя`PdfSaveOptions` с`PageSettings` установлен в`A4NoHeightLimit`.

## Заключение

В этом уроке мы узнали, как сохранять документы в формате PDF с помощью Aspose.Note для .NET. Мы рассмотрели два разных макета страницы: Letter и A4 без ограничения по высоте. С помощью Aspose.Note разработчики могут легко манипулировать файлами OneNote программным способом, обеспечивая гибкость и эффективность в задачах управления документами.

## Часто задаваемые вопросы

### Вопрос 1. Может ли Aspose.Note обрабатывать сложные файлы OneNote?

О1: Да, Aspose.Note поддерживает различные функции и возможности для эффективной обработки сложных файлов OneNote.

### Вопрос 2: Подходит ли Aspose.Note для коммерческих проектов?

 A2: Конечно, Aspose.Note можно легко использовать в коммерческих проектах. Вы можете приобрести лицензию[здесь](https://purchase.aspose.com/buy).

### Вопрос 3: Предлагает ли Aspose.Note бесплатную пробную версию?

 О3: Да, вы можете изучить Aspose.Note, воспользовавшись бесплатной пробной версией.[здесь](https://releases.aspose.com/).

### Вопрос 4: Где я могу найти документацию для Aspose.Note?

 A4: Вы можете найти подробную документацию[здесь](https://reference.aspose.com/note/net/).

### В5: Нужна дополнительная помощь?

 A5: Не стесняйтесь задавать любые вопросы или обращаться за поддержкой на форуме Aspose.Note.[здесь](https://forum.aspose.com/c/note/28).