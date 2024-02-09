---
title: Вставить список китайских номеров в текст Aspose.Note
linktitle: Вставить список китайских номеров в текст Aspose.Note
second_title: Aspose.Note .NET API
description: Узнайте, как легко вставлять списки номеров на китайском языке в документы Aspose.Note для .NET. Совершенствуйте свои навыки форматирования документов с помощью этого пошагового руководства.
type: docs
weight: 20
url: /ru/net/text-manipulation/insert-chinese-number-list/
---
## Введение
Вы хотите улучшить свои навыки работы с Aspose.Note для .NET, включив в свои документы списки номеров на китайском языке? Если да, то вы находитесь в правильном месте! В этом уроке мы покажем вам процесс вставки списков номеров на китайском языке с помощью Aspose.Note для .NET. Эта мощная библиотека позволяет вам легко манипулировать документами OneNote.
## Предварительные условия
Прежде чем мы углубимся в руководство, убедитесь, что у вас есть следующие предварительные условия:
- Базовые знания программирования на C#.
-  Aspose.Note для .NET установлен. Вы можете скачать его[здесь](https://releases.aspose.com/note/net/).
## Импортировать пространства имен
Для начала импортируйте необходимые пространства имен в свой проект:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Шаг 1. Инициализируйте документ OneNote
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Шаг 2. Инициализация страницы OneNote
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## Шаг 3. Примените настройки стиля текста
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Шаг 4. Создайте элементы контура
Теперь давайте создадим три элемента структуры со списками китайских номеров:
### Шаг 4.1: Первый элемент
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Шаг 4.2: Второй элемент
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Шаг 4.3: Третий элемент
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Шаг 5. Добавьте элементы в структуру
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Шаг 6. Добавьте схему на страницу
```csharp
page.AppendChildLast(outline);
```
## Шаг 7. Добавьте страницу в документ
```csharp
doc.AppendChildLast(page);
```
## Шаг 8. Сохраните документ OneNote
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Поздравляем! Вы успешно вставили списки номеров на китайском языке в документ Aspose.Note с помощью библиотеки .NET.
## Заключение
В этом уроке мы рассмотрели пошаговый процесс включения списков номеров на китайском языке в ваши документы Aspose.Note для .NET. Совершенствуйте свои навыки форматирования документов и делайте свой контент более привлекательным с помощью этих методов.
## Часто задаваемые вопросы
### Вопрос: Могу ли я настроить форматирование списков номеров на китайском языке?
 О: Да, вы можете настроить форматирование, настроив параметры в`NumberList` конструктор.
### Вопрос: Совместим ли Aspose.Note с последней версией .NET?
О: Да, Aspose.Note регулярно обновляется для поддержки последних версий .NET.
### Вопрос: Где я могу найти дополнительные примеры и документацию?
 A: Изучите всестороннее[Документация Aspose.Note](https://reference.aspose.com/note/net/).
### Вопрос: Как я могу получить временную лицензию на Aspose.Note?
 О: Получите временную лицензию[здесь](https://purchase.aspose.com/temporary-license/).
### Вопрос: Где я могу обратиться за помощью или обсудить вопросы, связанные с Aspose.Note?
 А: Посетите[Форум поддержки Aspose.Note](https://forum.aspose.com/c/note/28) для поддержки сообщества.