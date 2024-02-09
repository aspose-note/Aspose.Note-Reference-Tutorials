---
title: Применение маркеров к тексту в Aspose.Note
linktitle: Применение маркеров к тексту в Aspose.Note
second_title: Aspose.Note .NET API
description: Узнайте, как применять маркеры к тексту в Aspose.Note для .NET, чтобы улучшить ваши документы OneNote. Следуйте этому пошаговому руководству для эффективного форматирования.
type: docs
weight: 10
url: /ru/net/text-manipulation/apply-bullets-on-text/
---
## Введение
Добро пожаловать в это пошаговое руководство по нанесению маркеров на текст с помощью Aspose.Note для .NET. Aspose.Note — это мощная библиотека, которая позволяет разработчикам беспрепятственно работать с файлами Microsoft OneNote в своих .NET-приложениях. В этом уроке мы покажем вам процесс применения маркеров к тексту, улучшая визуальную привлекательность ваших документов OneNote.
## Предварительные условия
Прежде чем мы углубимся в руководство, убедитесь, что у вас есть следующие предварительные условия:
- Базовые знания программирования на C# и .NET.
-  Установлена библиотека Aspose.Note для .NET. Вы можете скачать его[здесь](https://releases.aspose.com/note/net/).
## Импортировать пространства имен
Обязательно включите в свой код C# необходимые пространства имен:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Шаг 1. Настройте свой документ
```csharp
// Путь к каталогу документов.
string dataDir = "Your Document Directory";
// Создайте объект класса Document
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Шаг 2. Инициализируйте страницу и структуру
```csharp
// Инициализировать объект класса страницы
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Инициализировать объект класса Outline
Outline outline = new Outline(doc);
```
## Шаг 3. Установите стиль текста по умолчанию
```csharp
// Инициализируйте объект класса TextStyle и установите свойства форматирования.
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Шаг 4. Создайте элементы контура с помощью маркеров
```csharp
// Инициализируйте объекты класса OutlineElement и примените маркеры.
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Повторите эти действия для других элементов контура.
```
## Шаг 5. Добавьте элементы структуры в структуру
```csharp
// Добавьте элементы контура
outline.AppendChildLast(outlineElem1);
// Повторите эти действия для других элементов контура.
```
## Шаг 6. Добавьте схему на страницу
```csharp
// Добавить узел структуры
page.AppendChildLast(outline);
```
## Шаг 7. Добавьте страницу в документ
```csharp
// Добавить узел страницы
doc.AppendChildLast(page);
```
## Шаг 8. Сохраните документ OneNote.
```csharp
// Сохранить документ OneNote
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## Заключение
Поздравляем! Вы успешно научились применять маркеры к тексту с помощью Aspose.Note для .NET. Эта функция может значительно улучшить форматирование ваших документов OneNote, сделав их более привлекательными.
## Часто задаваемые вопросы
### Могу ли я применить разные стили маркеров к каждому элементу списка?
 Да, вы можете настроить стили маркеров, изменив`NumberList` свойства для каждого`OutlineElement`.
### Совместим ли Aspose.Note с последней версией Microsoft OneNote?
Aspose.Note поддерживает различные версии Microsoft OneNote, обеспечивая совместимость как со старыми, так и с новыми версиями.
### Могу ли я использовать Aspose.Note в коммерческих целях?
 Да, вы можете использовать Aspose.Note для .NET в коммерческих проектах. Чтобы получить лицензию, посетите[здесь](https://purchase.aspose.com/buy).
### Доступна ли пробная версия Aspose.Note для .NET?
 Да, вы можете скачать бесплатную пробную версию[здесь](https://releases.aspose.com/).
### Где я могу найти дополнительную поддержку и ресурсы?
 Вы можете посетить форум сообщества Aspose.Note.[здесь](https://forum.aspose.com/c/note/28) за поддержку и обсуждения.