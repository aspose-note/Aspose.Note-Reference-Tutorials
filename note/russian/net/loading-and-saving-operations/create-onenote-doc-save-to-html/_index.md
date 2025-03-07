---
title: Создайте документ OneNote и сохраните его в HTML в Aspose.Note.
linktitle: Создайте документ OneNote и сохраните его в HTML в Aspose.Note.
second_title: Aspose.Note .NET API
description: Узнайте, как создавать и сохранять документы Microsoft OneNote в формате HTML в приложениях .NET с помощью API Aspose.Note. Следуйте нашему подробному руководству с пошаговыми примерами.
weight: 14
url: /ru/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создайте документ OneNote и сохраните его в HTML в Aspose.Note.

## Введение

Aspose.Note для .NET — это мощный API, который позволяет разработчикам программно работать с документами Microsoft OneNote в своих .NET-приложениях. С помощью Aspose.Note вы можете легко создавать, манипулировать и конвертировать файлы OneNote. В этом руководстве мы рассмотрим, как создать документ OneNote и сохранить его в формате HTML, используя различные параметры, предоставляемые API Aspose.Note для .NET.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас есть следующие предварительные условия:

- Базовые знания языка программирования C#.
- Visual Studio установлена в вашей системе.
-  Aspose.Note для .NET API, установленного в вашем проекте. Вы можете скачать его с[здесь](https://releases.aspose.com/note/net/).
- Знакомство со структурой документов Microsoft OneNote.

## Импортировать пространства имен

Прежде чем мы углубимся в часть кодирования, давайте импортируем необходимые пространства имен:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Теперь давайте разобьем каждый пример на несколько шагов и посмотрим, как создать документ OneNote и сохранить его в формате HTML с помощью Aspose.Note для .NET.

## Шаг 1. Создайте документ OneNote с параметрами по умолчанию.

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Инициализировать документ OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Стиль по умолчанию для всего текста в документе.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Сохранить в формате HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

На этом этапе мы инициализируем новый документ OneNote, добавляем страницу с заголовком и сохраняем ее в формате HTML, используя параметры по умолчанию.

## Шаг 2. Создайте и сохраните определенный диапазон страниц в HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Инициализировать документ OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Стиль по умолчанию для всего текста в документе.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Сохранить в формате HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Здесь мы покажем, как создать документ и сохранить определенный диапазон страниц в формате HTML.

## Шаг 3. Сохранение в формате HTML в потоке памяти со встроенными ресурсами

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Загрузите документ OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Укажите параметры сохранения HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Сохраните документ в поток памяти
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

На этом шаге показано, как сохранить документ OneNote в формате HTML со встроенными ресурсами (CSS, шрифтами и изображениями) в поток памяти.

## Шаг 4. Сохраните файл в формате HTML с ресурсами в отдельных файлах.

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Загрузите документ OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Укажите параметры сохранения HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Сохраните документ в файл HTML с ресурсами, хранящимися в отдельных файлах.
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

На этом этапе мы сохраняем документ OneNote в формате HTML, при этом все ресурсы (CSS, шрифты и изображения) хранятся в отдельных файлах.

## Шаг 5. Сохраните как HTML в поток памяти с обратными вызовами для экономии ресурсов.

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Укажите конфигурацию сохранения обратных вызовов
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Укажите параметры сохранения HTML
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Загрузите документ OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Сохраните документ в формате HTML с ресурсами, управляемыми определяемыми пользователем обратными вызовами.
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Добавление данных в поток CSS вручную
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Здесь мы демонстрируем, как сохранить документ OneNote в формате HTML с ресурсами, управляемыми определяемыми пользователем обратными вызовами.

## Заключение

В этой статье мы рассмотрели, как работать с документами OneNote и сохранять их в формате HTML с помощью Aspose.Note для .NET. Следуя пошаговому руководству, вы легко сможете

 интегрируйте эту функцию в свои приложения .NET, что позволит вам эффективно манипулировать файлами OneNote.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я настроить внешний вид сохраненного HTML-файла?

О1: Да, вы можете настроить внешний вид, изменив таблицы стилей CSS, созданные в процессе преобразования.

### Вопрос 2: Поддерживает ли Aspose.Note преобразование в другие форматы, кроме HTML?

О2: Да, Aspose.Note поддерживает преобразование в различные форматы, такие как PDF, изображения и документы Microsoft Word.

### Вопрос 3. Совместим ли Aspose.Note с приложениями .NET Core?

О3: Да, Aspose.Note совместим как с приложениями .NET Framework, так и с .NET Core.

### Вопрос 4. Могу ли я извлечь текст и изображения из документов OneNote с помощью Aspose.Note?

О4: Да, вы можете извлекать текст и изображения, а также выполнять различные другие манипуляции с помощью API Aspose.Note.

### Вопрос 5: Существует ли пробная версия для тестирования функций Aspose.Note?

 О5: Да, вы можете загрузить бесплатную пробную версию с сайта[здесь](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
