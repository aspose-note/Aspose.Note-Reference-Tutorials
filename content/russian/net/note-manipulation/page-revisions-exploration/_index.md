---
title: Изучите версии страниц в документах Aspose.Note
linktitle: Изучите версии страниц в документах Aspose.Note
second_title: Aspose.Note .NET API
description: Узнайте, как исследовать версии страниц в документах Aspose.Note с помощью .NET Framework, с пошаговыми инструкциями.
type: docs
weight: 14
url: /ru/net/note-manipulation/page-revisions-exploration/
---
## Введение

В этом руководстве мы углубимся в изучение редакций страниц в документах Aspose.Note с использованием платформы .NET. Aspose.Note — это мощная библиотека, которая позволяет разработчикам программно работать с файлами Microsoft OneNote, предлагая различные функции для управления и извлечения данных из этих файлов.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас настроены следующие предварительные условия:

### 1. Загрузите и установите Aspose.Note для .NET.

 Посетить[страница загрузки](https://releases.aspose.com/note/net/) и загрузите библиотеку Aspose.Note для .NET. Следуйте инструкциям по установке, чтобы настроить библиотеку в вашей среде разработки.

### 2. Загрузите необходимые пространства имен

Обязательно импортируйте необходимые пространства имен в свой проект .NET, чтобы обеспечить беспрепятственный доступ к функциям Aspose.Note.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

Теперь давайте разобьем процесс изучения изменений страницы на пошаговые инструкции:

## Шаг 1. Загрузите документ

Во-первых, нам нужно загрузить документ Aspose.Note, убедившись, что загрузка истории документа включена.

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## Шаг 2. Получите версии страницы.

После загрузки документа мы можем получить версии для конкретной страницы. В этом примере мы получим изменения для первой страницы.

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## Шаг 3. Перебор изменений

В цикле выполните итерацию по каждой ревизии страницы и получите доступ к ее свойствам, таким как время последнего изменения, время создания, заголовок, уровень и автор.

## Заключение

Изучение редакций страниц в документах Aspose.Note с использованием .NET — простой процесс. Выполнив действия, описанные в этом руководстве, вы сможете эффективно получать и анализировать историю изменений файлов OneNote программными средствами.

## Часто задаваемые вопросы

### Вопрос 1. Могу ли я использовать Aspose.Note для .NET для создания новых документов OneNote?

О1: Да, Aspose.Note для .NET позволяет вам программно создавать, редактировать и манипулировать документами OneNote.

### Вопрос 2. Поддерживает ли Aspose.Note историю загрузки для всех типов файлов OneNote?

A2: Aspose.Note поддерживает историю загрузки для файлов форматов .one и .onepkg.

### Вопрос 3. Существует ли бесплатная пробная версия Aspose.Note для .NET?

 О3: Да, вы можете загрузить бесплатную пробную версию Aspose.Note для .NET с сайта[здесь](https://releases.aspose.com/).

### Вопрос 4: Как получить временную лицензию на Aspose.Note для .NET?

 A4: Вы можете запросить временную лицензию у[эта ссылка](https://purchase.aspose.com/temporary-license/).

### Вопрос 5: Где я могу найти поддержку Aspose.Note для .NET?

 О5: Вы можете найти поддержку и ресурсы на[Форум Aspose.Note](https://forum.aspose.com/c/note/28).