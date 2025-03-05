---
title: Сохранение с использованием указанных шрифтов в Aspose.Note
linktitle: Сохранение с использованием указанных шрифтов в Aspose.Note
second_title: Aspose.Note .NET API
description: Узнайте, как сохранять документы с указанными шрифтами в Aspose.Note для .NET. Легко настраивайте параметры шрифта для единообразного форматирования документа.
type: docs
weight: 28
url: /ru/net/loading-and-saving-operations/save-using-specified-fonts/
---
## Введение

В этом уроке мы научимся сохранять документы, используя указанные шрифты в Aspose.Note для .NET. Мы рассмотрим различные методы достижения этой цели, шаг за шагом.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас есть следующее:

1.  Aspose.Note для .NET: убедитесь, что вы установили Aspose.Note для .NET. Вы можете скачать его с[здесь](https://releases.aspose.com/note/net/).

2. Среда разработки: вам нужна среда разработки, настроенная для разработки .NET.

## Импортировать пространства имен

Сначала давайте импортируем необходимые пространства имен:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Шаг 1. Сохранение с именем шрифта по умолчанию.

На этом этапе мы сохраним документ, используя указанное имя шрифта по умолчанию.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // Путь к каталогу документов.
    string dataDir = "Your Document Directory";

    // Загрузите документ в Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Сохраните документ в формате PDF с указанным шрифтом по умолчанию.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Шаг 2. Сохранение шрифта по умолчанию из файла

Далее давайте сохраним документ, используя шрифт по умолчанию, загруженный из файла.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // Путь к каталогу документов.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Загрузите документ в Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Сохраните документ в формате PDF со шрифтом по умолчанию, загруженным из файла.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Шаг 3. Сохранение со шрифтом по умолчанию из потока

Наконец, давайте сохраним документ, используя шрифт по умолчанию, загруженный из потока.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // Путь к каталогу документов.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Загрузите документ в Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Сохраните документ в формате PDF со шрифтом по умолчанию, загруженным из потока.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Заключение

В этом уроке мы рассмотрели, как сохранять документы с использованием указанных шрифтов в Aspose.Note для .NET. Выполнив эти шаги, вы сможете настроить параметры шрифта в соответствии со своими требованиями, гарантируя, что ваши документы будут отформатированы по желанию.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать любой шрифт для сохранения документов в Aspose.Note?

О1: Да, вы можете указать любой шрифт для сохранения документов. Просто убедитесь, что файл шрифта доступен и загружен правильно.

### Вопрос 2: Совместим ли Aspose.Note с различными форматами документов?

A2: Aspose.Note в основном работает с документами OneNote, но предоставляет возможность сохранения в различных форматах, включая PDF.

### Вопрос 3. Как устранить отсутствие шрифтов при сохранении документов?

A3: Aspose.Note предлагает возможность использовать шрифты по умолчанию в случае отсутствия указанного шрифта, обеспечивая единообразное форматирование документа.

### Вопрос 4: Поддерживает ли Aspose.Note встраивание шрифтов в выходные документы?

О4: Да, Aspose.Note позволяет встраивать шрифты для обеспечения переносимости документов и единообразного отображения на разных платформах.

### Вопрос 5: Где я могу получить дополнительную помощь по Aspose.Note?

 A5: Для получения дополнительной помощи или технической поддержки вы можете посетить[Форум Aspose.Note](https://forum.aspose.com/c/note/28).