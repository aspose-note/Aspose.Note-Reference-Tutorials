---
title: Получить список маркеров или номеров в тексте Aspose.Note
linktitle: Получить список маркеров или номеров в тексте Aspose.Note
second_title: Aspose.Note .NET API
description: Раскройте потенциал Aspose.Note для .NET с помощью нашего пошагового руководства по получению списков маркеров или номеров. Совершенствуйте свои навыки работы с документами OneNote!
weight: 23
url: /ru/net/text-manipulation/retrieve-bullet-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Получить список маркеров или номеров в тексте Aspose.Note

## Введение
Добро пожаловать в мир Aspose.Note для .NET, надежной и универсальной библиотеки, которая позволяет разработчикам легко манипулировать документами OneNote. В этом уроке мы углубимся в процесс получения списков маркеров или номеров с помощью Aspose.Note для .NET. Независимо от того, являетесь ли вы опытным разработчиком или энтузиастом кодирования, это руководство предоставит вам знания, необходимые для понимания тонкостей работы со списками в Aspose.Note.
## Предварительные условия
Прежде чем мы приступим к этому путешествию по кодированию, убедитесь, что у вас есть следующие предварительные условия:
-  Aspose.Note для .NET: убедитесь, что у вас установлена библиотека Aspose.Note. Если нет, вы можете скачать его с сайта[Документация Aspose.Note для .NET](https://reference.aspose.com/note/net/).
- Среда разработки: на вашем компьютере должна быть установлена работающая среда разработки, предпочтительно Microsoft Visual Studio.
- Базовые знания C#: ознакомьтесь с C#, поскольку это руководство написано на этом языке.
## Импортировать пространства имен
Чтобы взаимодействовать с Aspose.Note for .NET, вам необходимо импортировать необходимые пространства имен в ваш проект. Включите следующие пространства имен в начало вашего кода:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
Теперь давайте шаг за шагом разберем процесс получения списков маркеров или номеров:
## Шаг 1. Установите каталог документов
```csharp
// Путь к каталогу документов.
string dataDir = "Your Document Directory";
```
 Заменять`"Your Document Directory"` с фактическим путем, по которому находится ваш документ Aspose.Note.
## Шаг 2. Загрузите документ
```csharp
// Загрузите документ в Aspose.Note.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 Убедитесь, что вы заменили`"ApplyNumberingOnText.one"` с именем вашего конкретного документа OneNote.
## Шаг 3: Получение коллекции узлов
```csharp
// Получите коллекцию узлов элемента контура.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
На этом шаге извлекается коллекция узлов структуры из загруженного документа.
## Шаг 4. Перебор каждого узла
```csharp
// Перебрать каждый узел.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Перейдите к следующим шагам...
    }
}
```
Этот цикл гарантирует, что мы имеем дело только с узлами, содержащими список номеров.
## Шаг 5. Получите информацию о шрифте
```csharp
// Получить имя шрифта
Console.WriteLine("Font Name: " + list.Font);
// Получить длину шрифта
Console.WriteLine("Font Length: " + list.Font.Length);
// Получить размер шрифта
Console.WriteLine("Font Size: " + list.FontSize);
// Получить цвет шрифта
Console.WriteLine("Font Color: " + list.FontColor);
// Получить формат
Console.WriteLine("Font format: " + list.Format);
// Отметьте жирным шрифтом
Console.WriteLine("Is bold: " + list.IsBold);
// Проверьте курсив
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
Эти строки кода извлекают из списка номеров различную информацию, связанную со шрифтами.
## Заключение
 Поздравляем! Вы успешно научились получать списки маркеров или номеров с помощью Aspose.Note для .NET. Продолжая исследование, обратитесь к[документация](https://reference.aspose.com/note/net/) для более глубокого понимания и функциональности.
## Часто задаваемые вопросы
### Могу ли я использовать Aspose.Note для .NET с другими языками программирования?
Aspose.Note в первую очередь поддерживает .NET, но существуют и другие версии библиотеки, адаптированные для разных платформ и языков.
### Совместим ли Aspose.Note с новейшими форматами OneNote?
Да, Aspose.Note поддерживает широкий спектр форматов OneNote, обеспечивая совместимость с последними версиями.
### Как я могу получить временную лицензию для Aspose.Note?
 Посещать[эта ссылка](https://purchase.aspose.com/temporary-license/) получить временную лицензию для ознакомительных целей.
### Какие варианты поддержки доступны для пользователей Aspose.Note?
Вы можете изучить и обратиться за помощью в[Форум Aspose.Note](https://forum.aspose.com/c/note/28) по любым вопросам или проблемам, с которыми вы можете столкнуться.
### Существует ли бесплатная пробная версия Aspose.Note для .NET?
 Да, вы можете получить доступ к бесплатной пробной версии Aspose.Note для .NET.[здесь](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
