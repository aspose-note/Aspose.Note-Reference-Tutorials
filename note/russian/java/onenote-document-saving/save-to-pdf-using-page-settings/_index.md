---
title: Сохранение в PDF с использованием настроек страницы в OneNote — Aspose.Note
linktitle: Сохранение в PDF с использованием настроек страницы в OneNote — Aspose.Note
second_title: Aspose.Note Java API
description: Узнайте, как сохранить документы OneNote в PDF на Java с помощью библиотеки Aspose.Note. Пошаговое руководство с примерами кода для различных настроек страницы.
weight: 19
url: /ru/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Сохранение в PDF с использованием настроек страницы в OneNote — Aspose.Note

## Введение

В этом уроке мы узнаем, как сохранять документы OneNote в формате PDF, используя различные настройки страницы с помощью Aspose.Note для Java. Мы рассмотрим два метода: сохранение с настройками страницы Letter и сохранение с настройками страницы A4 без ограничения высоты.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас есть следующие предварительные условия:

1. В вашей системе установлен Java Development Kit (JDK).
2. Библиотека Aspose.Note для Java загружена и включена в ваш Java-проект.
3. Базовое понимание языка программирования Java.

## Импортировать пакеты

Убедитесь, что вы импортировали необходимые пакеты для использования Aspose.Note for Java в вашем проекте. Вот оператор импорта:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Сохранить в PDF с использованием настроек страницы Letter

### Шаг 1. Загрузите документ

Сначала загрузите документ OneNote в Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Шаг 2. Определите путь назначения

Укажите путь назначения для PDF-файла:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Шаг 3. Сохраните документ

Сохраните документ с настройками страницы Letter:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Сохранение в PDF с использованием настроек страницы A4 без ограничения высоты

### Шаг 1. Загрузите документ

Аналогично загрузите документ OneNote в Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Шаг 2. Определите путь назначения

Укажите путь назначения для PDF-файла:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Шаг 3. Сохраните документ

Сохраните документ с настройками страницы А4 без ограничения высоты:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Выполнив эти действия, вы успешно сохраните документ OneNote в формате PDF, используя различные настройки страницы.

## Заключение

В этом уроке мы рассмотрели, как сохранить документы OneNote в формате PDF с помощью библиотеки Aspose.Note для Java. Следуя пошаговому руководству, вы сможете легко интегрировать эту функцию в свои приложения Java.

## Часто задаваемые вопросы

### В1: Могу ли я дополнительно настроить параметры страницы?

О1: Да, вы можете настроить параметры страницы в соответствии с вашими требованиями, используя Aspose.Note для Java.

### Вопрос 2. Поддерживает ли Aspose.Note другие форматы вывода, кроме PDF?

О2: Да, Aspose.Note поддерживает различные форматы вывода, включая изображения и HTML.

### Вопрос 3. Совместим ли Aspose.Note с различными версиями файлов OneNote?

О3: Да, Aspose.Note поддерживает файлы OneNote разных версий, включая .one и .onetoc2.

### Вопрос 4. Могу ли я преобразовать несколько файлов OneNote в PDF за один проход?

A4: Да, вы можете обрабатывать несколько файлов OneNote в пакетном режиме с помощью Aspose.Note для Java.

### В5: Есть ли пробная версия для тестирования?

О5: Да, вы можете получить бесплатную пробную версию Aspose.Note для Java на веб-сайте.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
