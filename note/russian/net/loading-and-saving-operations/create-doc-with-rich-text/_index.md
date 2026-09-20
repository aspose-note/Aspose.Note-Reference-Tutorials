---
date: 2026-06-20
description: Узнайте, как создавать документы в формате rich text и программно генерировать
  файлы OneNote с помощью Aspose.Note for .NET. Пошаговое руководство с примерами
  кода.
keywords:
- create rich text document
- create onenote file
- set paragraph style
- apply font color
- create document outline
linktitle: Создать документ в формате Rich Text с помощью Aspose.Note for .NET
schemas:
- author: Aspose
  dateModified: '2026-06-20'
  description: Learn how to create rich text documents and generate OneNote files
    programmatically with Aspose.Note for .NET. Step‑by‑step guide with code snippets.
  headline: Create Rich Text Document with Aspose.Note for .NET
  type: TechArticle
- description: Learn how to create rich text documents and generate OneNote files
    programmatically with Aspose.Note for .NET. Step‑by‑step guide with code snippets.
  name: Create Rich Text Document with Aspose.Note for .NET
  steps:
  - name: '**Development Environment** – Visual Studio 2022 or any compatible .NET
      IDE.'
    text: '**Development Environment** – Visual Studio 2022 or any compatible .NET
      IDE.'
  - name: '**Aspose.Note for .NET** – Download from the [download link](https://releases.aspose.com/note/net/).'
    text: '**Aspose.Note for .NET** – Download from the [download link](https://releases.aspose.com/note/net/).'
  - name: '**Basic C# Knowledge** – You should be comfortable with classes, objects,
      and inline code.'
    text: '**Basic C# Knowledge** – You should be comfortable with classes, objects,
      and inline code.'
  type: HowTo
- questions:
  - answer: Yes. By creating multiple `TextRun` objects with distinct `TextStyle`
      settings, you can mix bold, color, and size in a single paragraph.
    question: Can I apply different formatting styles within the same text string?
  - answer: Absolutely. The library processes multi‑hundred‑page OneNote files using
      a streaming model that keeps memory usage low.
    question: Is Aspose.Note suitable for handling large‑scale document processing
      tasks?
  - answer: Yes. Aspose.Note works seamlessly with ASP.NET Core, WPF, and any .NET
      Standard‑compatible library.
    question: Can I integrate Aspose.Note with other .NET libraries or frameworks?
  - answer: While the core API runs locally, you can host it in Azure Functions or
      AWS Lambda to build cloud‑enabled services.
    question: Does Aspose.Note provide support for cloud‑based document processing?
  - answer: You can explore the [Aspose.Note forum](https://forum.aspose.com/c/note/28)
      for community help and access documentation on the [website](https://reference.aspose.com/note/net/).
    question: Where can I find more resources and support for Aspose.Note?
  type: FAQPage
second_title: Aspose.Note .NET API
title: Создать документ в формате Rich Text с помощью Aspose.Note for .NET
url: /ru/net/loading-and-saving-operations/create-doc-with-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создание документа с форматированным текстом с помощью Aspose.Note для .NET

## Введение  

В этом руководстве вы узнаете **как создать документ с форматированным текстом** с помощью Aspose.Note для .NET и затем сохранить его как файл OneNote. Независимо от того, нужно ли вам генерировать протоколы встреч, краткие описания проектов или любой стилизованный контент программно, Aspose.Note предоставляет полный контроль над форматированием текста, стилями абзацев и структурой документа. Мы пройдём каждый шаг — от импорта пространств имён до сохранения окончательного файла *.one* — чтобы вы могли начать автоматизировать создание OneNote уже сегодня.

## Быстрые ответы  

- **Что делает Aspose.Note?** Он позволяет разработчикам .NET создавать, читать и изменять файлы OneNote без самого приложения OneNote.  
- **Сколько вариантов форматирования поддерживается?** Более 30 стилей текста, включая семейство шрифтов, размер, цвет, полужирный, курсив и подчёркивание.  
- **Можно ли программно задать стиль абзаца?** Да — используйте класс `ParagraphStyle` для определения выравнивания, отступов и интервалов.  
- **Какой формат файла получается?** Стандартный файл *.one*, который открывается в Microsoft OneNote, OneNote Online и мобильных приложениях.  
- **Нужна ли лицензия для разработки?** Бесплатная временная лицензия подходит для оценки; полная лицензия требуется для использования в продакшене.

## Что такое документ с форматированным текстом?  

**Документ с форматированным текстом** — это файл, в котором текст хранится вместе с информацией о форматировании, такой как шрифты, цвета и стили абзацев. В Aspose.Note это представлено классом `RichText`, который может быть привязан к заголовкам, структурам или любому элементу страницы.

## Почему создавать файл OneNote с форматированным текстом?  

Создание файлов OneNote с форматированным текстом позволяет получать профессионально оформленные заметки, сохраняющие стили при открытии в любом клиенте OneNote. Это идеально для автоматизированных отчётов, протоколов встреч или учебных материалов, где визуальная иерархия и акценты повышают читаемость. Возможность Aspose.Note генерировать большие многостраничные документы без загрузки всего в память делает её подходящей для корпоративных решений.

## Требования  

1. **Среда разработки** — Visual Studio 2022 или любой совместимый .NET IDE.  
2. **Aspose.Note для .NET** — скачайте с [download link](https://releases.aspose.com/note/net/).  
3. **Базовые знания C#** — вы должны быть уверены в работе с классами, объектами и встроенным кодом.

## Как импортировать необходимые пространства имён?  

Загрузите необходимые пространства имён, чтобы компилятор распознавал типы Aspose.Note. Импорт `System` и `System.Drawing` обеспечивает базовую функциональность .NET, а пространство имён Aspose.Note (автоматически подключается после добавления библиотеки) даёт доступ к классам создания документов, таким как `Document`, `Page` и `RichText`. Этот шаг гарантирует, что весь последующий код компилируется без ошибок отсутствующих ссылок.  

```csharp
using Aspose.Note;
using Aspose.Note.Rendering;
using System.Drawing;
```

Теперь у вас есть доступ к `Document`, `Page`, `Title`, `RichText` и классам стилизации.  

```csharp
using System;
using System.Drawing;
```

## Как создать объект Document?  

Создайте экземпляр класса `Document` — этот объект представляет весь файл OneNote в памяти. Класс `Document` является контейнером верхнего уровня, который хранит страницы, структуры и ресурсы, позволяя программно построить полную структуру блокнота.  

```csharp
Document oneNoteDoc = new Document();
```

```csharp
Document doc = new Document();
```

## Как инициализировать объект Page?  

Добавьте `Page` в документ; каждая страница соответствует вкладке в OneNote. Класс `Page` моделирует отдельную страницу OneNote, включая её размер, фон и иерархию содержимого, предоставляя холст для заголовков, структур и других элементов.  

```csharp
Page page = new Page(oneNoteDoc);
```

```csharp
Page page = new Page();
```

## Как создать объект Title?  

`Title` хранит заголовок страницы и отображается в верхней части вкладки OneNote. `Title` — это лёгкий контейнер для одной строки форматированного текста, который служит заголовком страницы, упрощая задачу установки чёткого, описательного названия.  

```csharp
Title pageTitle = new Title();
```

```csharp
Title title = new Title();
```

## Как задать свойства форматирования текста?  

Определите стиль `ParagraphStyle` по умолчанию, который будет применяться ко всему последующему тексту, если не переопределён. `ParagraphStyle` позволяет задать семейство шрифтов, размер, цвет, выравнивание и интервалы в одном месте, обеспечивая единообразный вид документа, при этом позволяя отдельным элементам переопределять настройки при необходимости.  

```csharp
TextStyle defaultStyle = new TextStyle
{
    FontName = "Calibri",
    FontSize = 12,
    FontColor = Color.Black
};
```

```csharp
ParagraphStyle defaultTextStyle = new ParagraphStyle
{
    FontColor = Color.Black,
    FontName = "Arial",
    FontSize = 10
};
```

## Как создать RichText с форматированием для заголовка?  

Создайте объект `RichText`, назначьте ему стиль по умолчанию, а затем примените особое форматирование для заголовка. `RichText` хранит коллекцию объектов `TextRun`, каждый из которых может иметь собственный стиль, что даёт возможность тонко управлять шрифтом, цветом и другими атрибутами внутри одного абзаца.  

```csharp
RichText titleRichText = new RichText();
titleRichText.Add(new TextRun("Quarterly Report", new TextStyle
{
    FontSize = 24,
    FontColor = Color.DarkBlue,
    Bold = true
}));
```

```csharp
RichText titleText = new RichText() { ParagraphStyle = defaultTextStyle }.Append("Title!");
```

## Как инициализировать объекты Outline и OutlineElement?  

`Outline` группирует связанное содержимое на странице, а `OutlineElement` представляет отдельный пункт‑маркер или нумерованный элемент. Эти классы позволяют построить иерархические структуры, похожие на левую навигационную панель в OneNote, предоставляя читателям чёткое, организованное представление разделов заметки.  

```csharp
Outline outline = new Outline(oneNoteDoc);
OutlineElement outlineElement = new OutlineElement();
```

```csharp
Outline outline = new Outline()
{
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
```

## Как определить дополнительные стили текста?  

Создайте отдельные экземпляры `ParagraphStyle` для заголовков, подзаголовков и обычных абзацев. Использование разных стилей позволяет **задать стиль абзаца** и **применять цвет шрифта** последовательно по всему документу, упрощая поддержание визуальной иерархии и улучшая читаемость.  

```csharp
TextStyle headingStyle = new TextStyle
{
    FontSize = 18,
    FontColor = Color.DarkGreen,
    Bold = true
};

TextStyle paragraphStyle = new TextStyle
{
    FontSize = 12,
    FontColor = Color.Black
};
```

```csharp
TextStyle textStyleForHelloWord = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

// Define more text styles as needed
```

## Как добавить отформатированный текст к объекту RichText?  

Добавьте несколько объектов `TextRun`, каждый со своим стилем, чтобы построить богато отформатированный абзац. Этот шаг демонстрирует, как **применять цвет шрифта** и **задать стиль абзаца** для разных частей одной строки, позволяя создавать смешанные стили, например, полужирные заголовки, за которыми следует цветное выделение.  

```csharp
RichText contentRichText = new RichText();
contentRichText.Add(new TextRun("Introduction: ", headingStyle));
contentRichText.Add(new TextRun("This report outlines the Q3 performance metrics.", paragraphStyle));
```

```csharp
RichText text = new RichText() { ParagraphStyle = defaultTextStyle }
    .Append("Hello", textStyleForHelloWord)
    .Append(" OneNote", textStyleForOneNoteWord)
    .Append(" text", textStyleForTextWord)
    .Append("!", TextStyle.Default);
```

## Как добавить Title и RichText в Outline?  

Присоедините заголовок и содержимое к `OutlineElement`, затем добавьте его в `Outline`. `OutlineElement` может содержать как заголовок, так и тело форматированного текста, образуя полноценный раздел заметки, который отображается как сворачиваемый элемент в навигационной панели OneNote.  

```csharp
outlineElement.Title = pageTitle;
outlineElement.RichText = contentRichText;
outline.Add(outlineElement);
```

```csharp
title.TitleText = titleText;
outlineElem.AppendChildLast(text);
```

## Как добавить Outline на страницу и страницу в документ?  

Вставьте структуру в страницу, а затем добавьте страницу в иерархию документа. Это создаёт окончательную структуру, которую OneNote отобразит как страницу с отформатированной структурой, гарантируя правильный порядок элементов при открытии файла.  

```csharp
page.Add(outline);
oneNoteDoc.Add(page);
```

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Как сохранить Document в файл OneNote?  

Укажите путь вывода и вызовите `Save`. Файл получит расширение *.one* и будет готов к открытию в OneNote. Сохранение генерирует **созданный файл OneNote**, сохраняющий всё форматирование текста и иерархию структуры, делая документ мгновенно доступным в любом клиенте OneNote.  

```csharp
oneNoteDoc.Save("QuarterlyReport.one");
```

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithFormattedRichText_out.one";
doc.Save(dataDir);
```

## Распространённые проблемы и решения  

- **Отсутствие шрифтов** — убедитесь, что указанный шрифт (например, Calibri) установлен на сервере; иначе Aspose.Note переключится на шрифт по умолчанию.  
- **Большие документы** — используйте `Document.SaveOptions` для включения потоковой записи, что предотвращает высокое потребление памяти при файлах более 200 страниц.  
- **Выравнивание абзаца не применяется** — проверьте, что вы задали `ParagraphStyle.Alignment` в `TextStyle` перед добавлением `TextRun`.

## Часто задаваемые вопросы  

**В: Можно ли применить разные стили форматирования внутри одной строки текста?**  
О: Да. Создавая несколько объектов `TextRun` с различными настройками `TextStyle`, вы можете смешивать полужирный, цветной и размерный формат в одном абзаце.  

**В: Подходит ли Aspose.Note для обработки крупномасштабных задач по обработке документов?**  
О: Абсолютно. Библиотека обрабатывает многосотстраничные файлы OneNote, используя потоковую модель, которая сохраняет низкое потребление памяти.  

**В: Можно ли интегрировать Aspose.Note с другими .NET‑библиотеками или фреймворками?**  
О: Да. Aspose.Note без проблем работает с ASP.NET Core, WPF и любой библиотекой, совместимой с .NET Standard.  

**В: Предоставляет ли Aspose.Note поддержку облачной обработки документов?**  
О: Хотя основной API работает локально, его можно разместить в Azure Functions или AWS Lambda для создания облачных сервисов.  

**В: Где можно найти дополнительные ресурсы и поддержку по Aspose.Note?**  
О: Вы можете изучить [Aspose.Note forum](https://forum.aspose.com/c/note/28) для помощи сообщества и получить доступ к документации на [website](https://reference.aspose.com/note/net/).  

**Последнее обновление:** 2026-06-20  
**Тестировано с:** Aspose.Note 24.11 для .NET  
**Автор:** Aspose  

## Связанные руководства

- [Создать документ с заголовком страницы в Aspose.Note](/note/net/loading-and-saving-operations/create-doc-with-page-title/)
- [Сохранить документ в формате OneNote в Aspose.Note](/note/net/loading-and-saving-operations/save-doc-to-onenote-format/)
- [Манипуляция текстом в OneNote с помощью Aspose.Note для .NET](/note/net/text-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}