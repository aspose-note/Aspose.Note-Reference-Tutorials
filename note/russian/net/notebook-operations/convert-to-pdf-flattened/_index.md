---
title: Преобразование блокнотов в PDF (сведенный) в Aspose Note .NET
linktitle: Преобразование блокнотов в PDF (сведенный) в Aspose Note .NET
second_title: Aspose.Note .NET API
description: Узнайте, как легко конвертировать записные книжки OneNote в плоские PDF-файлы с помощью Aspose.Note для .NET. Сохраняйте свой контент без проблем.
weight: 15
url: /ru/net/notebook-operations/convert-to-pdf-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Преобразование блокнотов в PDF (сведенный) в Aspose Note .NET

## Введение

Вы хотите преобразовать свои записные книжки OneNote в плоские PDF-файлы с помощью Aspose Note .NET? Вы находитесь в правильном месте! В этом уроке мы шаг за шагом рассмотрим этот процесс.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас есть следующее:

1.  Aspose.Note для .NET: убедитесь, что вы загрузили и установили Aspose.Note для .NET. Если нет, вы можете получить его от[здесь](https://releases.aspose.com/note/net/).
2. Visual Studio: вам понадобится установленная в вашей системе Visual Studio для кодирования и компиляции.
3. Записная книжка OneNote. Подготовьте записную книжку OneNote, которую вы хотите преобразовать в PDF-файл.

## Импортировать пространства имен

Начнем с импорта необходимых пространств имен в ваш код C#:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## Шаг 1. Загрузите записную книжку OneNote

```csharp
// Путь к каталогу документов.
string dataDir = "Your Document Directory";

// Загрузите записную книжку OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

 На этом этапе мы загружаем записную книжку OneNote, используя`Notebook` класс, предоставленный Aspose.Note.

## Шаг 2. Преобразование в PDF с помощью выравнивания

```csharp
// Сохраните блокнот в формате PDF с выравниванием.
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

 Здесь мы сохраняем загруженный блокнот в формате PDF с`Flatten` свойство установлено в`true`. Это свойство объединяет все содержимое, включая аннотации и изображения, в PDF-файл.

## Шаг 3. Распечатайте сообщение об успехе

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

Наконец, мы печатаем сообщение об успехе вместе с путем сохранения PDF-файла.

## Заключение

Поздравляем! Вы успешно преобразовали свой блокнот OneNote в плоский PDF-файл с помощью Aspose.Note для .NET. Этот процесс гарантирует, что весь ваш контент будет точно сохранен в формате PDF, что упрощает обмен и распространение.

## Часто задаваемые вопросы

### Вопрос 1. Могу ли я сохранить интерактивные элементы в PDF-файле?

A1: Aspose.Note выравнивает содержимое, включая интерактивные элементы, такие как флажки или поля формы, в PDF-файл, делая их статичными.

### Вопрос 2: Поддерживает ли Aspose.Note преобразование блокнотов в другие форматы?

О2: Да, Aspose.Note поддерживает преобразование блокнотов в различные форматы, такие как PDF, HTML, изображения и другие.

### В3: Могу ли я настроить параметры преобразования?

А3: Абсолютно! Aspose.Note предоставляет широкие возможности настройки в процессе преобразования, позволяя адаптировать вывод в соответствии с вашими требованиями.

### В4: Доступна ли пробная версия?

 О4: Да, вы можете получить бесплатную пробную версию Aspose. Примечание от[здесь](https://releases.aspose.com/).

### В5: Где я могу получить поддержку, если у меня возникнут какие-либо проблемы?

 О5: Вы можете обратиться за поддержкой к сообществу Aspose по адресу[Форумы Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
