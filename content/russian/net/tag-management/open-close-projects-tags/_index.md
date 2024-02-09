---
title: Открытие и закрытие проектов с помощью тегов в Aspose.Note
linktitle: Открытие и закрытие проектов с помощью тегов в Aspose.Note
second_title: Aspose.Note .NET API
description: Узнайте, как программно манипулировать файлами Microsoft OneNote с помощью Aspose.Note для .NET. Эффективно открывайте и закрывайте проекты с помощью тегов.
type: docs
weight: 15
url: /ru/net/tag-management/open-close-projects-tags/
---
## Введение

В этом уроке мы научимся использовать Aspose.Note для .NET для открытия и закрытия проектов с помощью тегов. Aspose.Note — это мощный API, который позволяет разработчикам программно работать с файлами Microsoft OneNote, выполняя такие задачи, как манипулирование текстом, изображениями и тегами в документах.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас настроены следующие предварительные условия:

## Импортировать пространства имен

```csharp
using System.IO;
using System.Linq;
```

Теперь давайте разобьем каждый пример на несколько шагов:

## Шаг 1. Загрузите документ

Сначала нам нужно загрузить документ в Aspose.Note.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Шаг 2. Закрытие элементов проекта C

Теперь давайте закроем все флажки, относящиеся к «Проекту C».

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Шаг 3. Сохраните заметки C закрытого проекта

Сохраните измененный документ с закрытыми элементами «Проект C».

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Шаг 4. Откройте элементы проекта C.

Далее давайте откроем все элементы флажков, относящиеся к «Проекту C».

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Шаг 5. Сохраните примечания C к открытому проекту.

Сохраните измененный документ с открытыми элементами «Проект C».

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Теперь вы узнали, как открывать и закрывать проекты с тегами в Aspose.Note с помощью .NET.

## Заключение

Aspose.Note для .NET предоставляет удобный способ программного управления документами OneNote. Следуя этому руководству, вы сможете эффективно управлять своими проектами, открывая и закрывая элементы с помощью тегов.

## Часто задаваемые вопросы

### Вопрос 1. Совместим ли Aspose.Note со всеми версиями OneNote?

A1: Aspose.Note поддерживает Microsoft OneNote 2010 и более поздние версии.

### Вопрос 2: Могу ли я использовать Aspose.Note для коммерческих проектов?

 О2: Да, вы можете использовать Aspose.Note как для личных, так и для коммерческих проектов. Посещать[здесь](https://purchase.aspose.com/buy) приобрести лицензию.

### Вопрос 3: Предлагает ли Aspose.Note бесплатную пробную версию?

A3: Да, вы можете получить бесплатную пробную версию.[здесь](https://releases.aspose.com/).

### Вопрос 4: Где я могу найти документацию для Aspose.Note?

 A4: Вы можете найти документацию[здесь](https://reference.aspose.com/note/net/).

### В5: Где я могу получить поддержку для Aspose.Note?

A5: Для получения поддержки вы можете посетить Aspose.Note.[Форум](https://forum.aspose.com/c/note/28).