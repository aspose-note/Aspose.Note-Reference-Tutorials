---
title: Составляйте таблицы с помощью Aspose.Note
linktitle: Составляйте таблицы с помощью Aspose.Note
second_title: Aspose.Note .NET API
description: Узнайте, как составлять структурированные таблицы с форматированным текстовым содержимым с помощью Aspose.Note для .NET. Улучшите организацию документов и удобочитаемость без особых усилий.
weight: 11
url: /ru/net/table-manipulation/compose-tables/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Составляйте таблицы с помощью Aspose.Note

## Введение

Таблицы являются основными компонентами документов, обеспечивающими структурированное представление информации. Aspose.Note для .NET предоставляет надежные инструменты для легкого составления таблиц. В этом уроке мы покажем вам процесс создания таблиц с форматированным текстовым содержимым с помощью Aspose.Note.

## Предварительные условия

Прежде чем углубляться в составление таблиц с помощью Aspose.Note для .NET, убедитесь, что у вас есть следующие предварительные условия:

1. Настройка среды. Убедитесь, что у вас настроена подходящая среда разработки с использованием .NET Framework или .NET Core.
2.  Установка: Загрузите и установите Aspose.Note для .NET с сайта[Веб-сайт](https://releases.aspose.com/note/net/).
3. Базовые знания: ознакомьтесь с основными понятиями программирования на C# и манипулирования документами.

## Импортировать пространства имен

Прежде чем приступить к составлению таблиц, убедитесь, что вы импортировали необходимые пространства имен:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Давайте разобьем приведенный пример на выполнимые шаги:

## Шаг 1. Настройте каталог документов

Прежде чем составлять таблицу, определите каталог, в котором будет сохранен документ.

```csharp
string dataDir = "Your Document Directory";
```

## Шаг 2. Создайте текст заголовка

Определите текст заголовка с помощью определенных стилей, таких как размер и жирность шрифта.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## Шаг 3. Создайте страницу и структуру

Инициализируйте страницу и структуру, чтобы структурировать контент.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## Шаг 4. Добавьте текст сводки

Перед таблицей добавьте краткий текст.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## Шаг 5: Создайте таблицу

Инициализируйте таблицу, чтобы организовать данные в строках и столбцах.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## Шаг 6. Добавьте строку заголовка

Заполните таблицу строкой заголовка, содержащей заголовки столбцов.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## Шаг 7. Добавьте пустые строки

Вставьте пустые строки, чтобы подготовиться к вставке данных.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## Шаг 8: Добавьте контактную информацию

Заполните столбец «Контакты» содержимым шаблона.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## Шаг 9: Сохраните документ

Сохраните составленный табличный документ.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## Шаг 10: Подтверждение

Подтвердите успешное составление документа.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## Заключение

В этом уроке мы рассмотрели, как составлять таблицы с форматированным текстовым содержимым с помощью Aspose.Note для .NET. Следуя этим пошаговым инструкциям, вы сможете эффективно создавать структурированные таблицы в своих документах, улучшая их читаемость и организацию.

## Часто задаваемые вопросы

### Вопрос 1. Могу ли я настроить стиль элементов таблицы?
   
О1: Да, вы можете настроить различные аспекты, такие как размер, цвет и выравнивание шрифта, в соответствии с вашими требованиями.

### Вопрос 2. Совместим ли Aspose.Note с другими библиотеками .NET?
   
О2: Aspose.Note легко интегрируется с другими библиотеками .NET, обеспечивая большую гибкость в манипулировании документами.

### Вопрос 3: Поддерживает ли Aspose.Note экспорт таблиц в разные форматы?
   
О3: Конечно, Aspose.Note позволяет экспортировать таблицы в различные форматы, включая PDF, DOCX и HTML.

### Вопрос 4. Могу ли я динамически заполнять таблицы данными из внешних источников?
   
О4: Да, вы можете динамически заполнять таблицы, получая данные из баз данных, API или пользовательских данных.

### В5: Доступна ли техническая поддержка для пользователей Aspose.Note?
   
О5: Да, Aspose предоставляет комплексную техническую поддержку через свои форумы и специальные каналы поддержки.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
