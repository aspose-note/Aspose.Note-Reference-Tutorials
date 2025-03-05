---
title: Импортируйте PDF-документы в Aspose.Note.
linktitle: Импортируйте PDF-документы в Aspose.Note.
second_title: Aspose.Note .NET API
description: Узнайте, как легко импортировать PDF-документы в Aspose.Note для .NET, используя различные варианты слияния для бесшовной интеграции.
type: docs
weight: 10
url: /ru/net/import/import-pdf-documents/
---
## Введение

Учитывая огромное количество доступного сегодня цифрового контента, беспрепятственная интеграция PDF-документов в ваши проекты имеет решающее значение. Aspose.Note для .NET предоставляет мощные функции для эффективного импорта PDF-документов. В этом уроке мы шаг за шагом рассмотрим, как импортировать PDF-документы с помощью Aspose.Note для .NET.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующее:

1.  Aspose.Note для .NET: Загрузите и установите библиотеку с сайта[здесь](https://releases.aspose.com/note/net/).
2. Базовые знания C# и .NET Framework: понимание языка программирования C# и .NET Framework будет полезным.

## Импортировать пространства имен

Обязательно импортируйте необходимые пространства имен для доступа к классам и методам, необходимым для функции импорта PDF:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;

using Aspose.Note.Importing;

```

## Шаг 1. Импортируйте PDF-документы с помощью простого слияния.

Подход Simple Merge позволяет постранично импортировать все страницы из нескольких PDF-документов:

```csharp
public static void ImportSetOfFiles_SimpleMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    d.Import(Path.Combine(dataDir, "sampleText.pdf"))
     .Import(Path.Combine(dataDir, "sampleImage.pdf"))
     .Import(Path.Combine(dataDir, "sampleTable.pdf"));

    d.Save(Path.Combine(dataDir, "sample_SimpleMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## Шаг 2. Импортируйте PDF-документы с помощью структурированного слияния

Структурированное слияние импортирует все страницы из документов PDF, вставляя страницы из каждого документа как дочерние элементы страницы OneNote верхнего уровня:

```csharp
public static void ImportSetOfFiles_StructuredMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    foreach (var file in new[] { "sampleText.pdf", "sampleImage.pdf", "sampleTable.pdf" })
    {
        d.AppendChildLast(new Page()).Title = new Title() { TitleText = new RichText() { ParagraphStyle = ParagraphStyle.Default }.Append(file) };
        d.Import(Path.Combine(dataDir, file), new PdfImportOptions(), new MergeOptions() { InsertAt = int.MaxValue, InsertAsChild = true });
    }

    d.Save(Path.Combine(dataDir, "sample_StructuredMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## Шаг 3. Импортируйте PDF-документы с помощью слияния одной страницы

Single Page Merge объединяет содержимое нескольких PDF-документов на одну страницу OneNote:

```csharp
public static void ImportSetOfFiles_SinglePageMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    var importOptions = new PdfImportOptions();
    var mergeOptions = new MergeOptions() { ImportAsSinglePage = true, PageSpacing = 100 };

    d.Import(Path.Combine(dataDir, "sampleText.pdf"), importOptions, mergeOptions)
     .Import(Path.Combine(dataDir, "sampleImage.pdf"), importOptions, mergeOptions)
     .Import(Path.Combine(dataDir, "sampleTable.pdf"), importOptions, mergeOptions);

    d.Save(Path.Combine(dataDir, "sample_SinglePageMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## Шаг 4. Импортируйте PDF-документы с помощью пользовательского слияния

Пользовательское объединение позволяет группировать страницы PDF-документов в отдельные страницы OneNote на основе пользовательских критериев:

```csharp
public static void ImportSetOfFiles_CustomMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    var mergeOptions = new MergeOptions() { ImportAsSinglePage = true, PageSpacing = 100 };

    IEnumerable<Page> pages = PdfImporter.Import(Path.Combine(dataDir, "SampleGrouping.pdf"));
    while (pages.Any())
    {
        d.Merge(pages.Take(5), mergeOptions);
        pages = pages.Skip(5);
    }

    d.Save(Path.Combine(dataDir, "sample_CustomMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## Заключение

Интеграция PDF-документов в ваши .NET-приложения с помощью Aspose.Note — это простой процесс, предлагающий различные варианты слияния, адаптированные к требованиям вашего проекта. Если вам нужно импортировать несколько страниц или организовать контент иерархически, Aspose.Note предоставляет необходимые инструменты для плавной интеграции.

## Часто задаваемые вопросы

### Вопрос 1. Могу ли я импортировать зашифрованные PDF-документы?

О1: Да, Aspose.Note поддерживает импорт зашифрованных PDF-документов. Убедитесь, что вы предоставили необходимые учетные данные для расшифровки.

### Вопрос 2. Существуют ли какие-либо ограничения на размер импортируемого PDF-файла?

О2: Aspose.Note не имеет ограничений на размер PDF-файла для импорта. Однако примите во внимание системные ресурсы и влияние на производительность больших PDF-файлов.

### Вопрос 3. Могу ли я настроить внешний вид импортированного содержимого PDF?

О3: Да, вы можете настроить внешний вид импортированного PDF-содержимого, используя различные параметры, предоставляемые Aspose.Note, такие как стили шрифтов, цвета и настройки макета.

### Вопрос 4. Совместим ли Aspose.Note с .NET Core?

О4: Да, Aspose.Note совместим с .NET Core, что позволяет интегрировать функцию импорта PDF в кроссплатформенные приложения.

### Вопрос 5. Где я могу найти дополнительную поддержку или ресурсы?

 A5: Для получения дополнительной поддержки, документации или помощи сообщества посетите[Форум Aspose.Note](https://forum.aspose.com/c/note/28).