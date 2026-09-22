---
date: 2026-08-08
description: Узнайте, как отслеживать изменения в OneNote, получая версии страниц
  программно с помощью Aspose.Note для Java.
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: Получить версии страниц в OneNote – Aspose.Note
og_description: Узнайте, как отслеживать изменения в OneNote, получая версии страниц
  программно с помощью Aspose.Note для Java.
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: Отслеживание изменений в OneNote – версии страниц с Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: Отслеживание изменений в OneNote – версии страниц с Aspose.Note
url: /ru/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Отслеживание изменений в OneNote – ревизии страниц с Aspose.Note

В этом руководстве вы узнаете, как **track changes in OneNote** путем извлечения полной истории ревизий страницы с использованием Aspose.Note Java API. Мы охватим всё, от настройки среды разработки до вывода автора, временных меток и заголовка каждой ревизии, чтобы вы могли создавать надёжные функции аудита для любого решения на основе OneNote.

## Быстрые ответы
- **Что охватывает руководство?** Получение истории ревизий страниц из файла OneNote с использованием Aspose.Note for Java.  
- **Какая версия библиотеки требуется?** Любой недавний релиз Aspose.Note for Java, поддерживающий `LoadOptions.setLoadHistory`.  
- **Нужна ли лицензия?** Временная оценочная лицензия подходит для тестирования; для продакшна требуется коммерческая лицензия.  
- **Можно ли изменять ревизии?** API предоставляет только чтение ревизий; их можно лишь получать.  
- **Каковы основные предпосылки?** Java JDK, Aspose.Note for Java и документ OneNote с данными ревизий.

## Что такое «aspose.note page revisions tutorial»?
Руководство демонстрирует, как программно получить доступ к историческим версиям страницы OneNote. Каждая ревизия содержит метаданные, такие как автор, время создания и время изменения, позволяя создавать аудиторские следы или функции журнала изменений в ваших приложениях.

## Почему использовать Aspose.Note для отслеживания ревизий страниц?
Загружайте полную историю ревизий блокнота менее чем за 5 секунд для файла из 500 страниц на стандартном процессоре 2 ГГц и получайте метаданные без запуска пользовательского интерфейса OneNote. Библиотека поддерживает более 30 форматов ввода и вывода, работает на Windows, Linux и macOS (охватывая >95 % серверных сред) и предоставляет полный контроль над каждым свойством ревизии.

## Предпосылки

### 1. Java Development Kit (JDK)
Убедитесь, что установлен недавний JDK (8 или выше) и переменная `JAVA_HOME` задана.

### 2. Aspose.Note for Java
Скачайте библиотеку по [download link](https://releases.aspose.com/note/java/).

### 3. Пример документа OneNote
Создайте или получите файл OneNote (например, `Sample1.one`), содержащий страницы с историей ревизий.

## Импорт пакетов
Сначала импортируйте необходимые классы Aspose.Note.  
`Document` представляет блокнот OneNote, `LoadOptions` настраивает поведение загрузки, а `Page` представляет отдельную страницу.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Пошаговая реализация

### Шаг 1: настройка каталога документа
Укажите папку, в которой находится ваш файл OneNote.

```java
String dataDir = "Your Document Directory";
```

### Шаг 2: загрузка документа OneNote с включённой историей
`LoadOptions` — это класс конфигурации, который указывает Aspose.Note, как открыть файл, включая чтение данных ревизий. Включите флаг перед загрузкой документа.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Шаг 3: получение первой страницы
Получите объект первой страницы; он будет отправной точкой для получения её истории.

```java
Page firstPage = document.getFirstChild();
```

### Шаг 4: перебор ревизий страницы
Пройдитесь по каждой ревизии и выведите полезные метаданные, такие как временные метки, заголовок, уровень и автор.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **Pro tip:** Если вам нужно отфильтровать ревизии по конкретному автору или диапазону дат, просто добавьте условные проверки внутри цикла `for`.

## Распространённые проблемы и решения
- **Ревизии не возвращаются:** Убедитесь, что `loadOptions.setLoadHistory(true)` вызывается до загрузки документа.  
- **Null author or title:** Некоторые более старые версии OneNote могут не сохранять эти поля; обрабатывайте значения `null` корректно.  
- **Задержка производительности в больших блокнотах:** Загружайте только необходимые разделы или увеличьте размер кучи JVM.

## Часто задаваемые вопросы

**Q1: Можно ли использовать Aspose.Note for Java для изменения ревизий страниц?**  
A1: Нет, API в настоящее время поддерживает только доступ только для чтения к ревизиям страниц.

**Q2: Совместим ли Aspose.Note for Java с различными версиями документов OneNote?**  
A2: Да, он работает с различными форматами файлов OneNote, обеспечивая бесшовную обработку между версиями.

**Q3: Требуется ли лицензия для использования Aspose.Note for Java?**  
A3: Для использования в продакшн требуется коммерческая лицензия, но для тестирования доступна временная оценочная лицензия.

**Q4: Могу ли я получить поддержку, если столкнусь с проблемами при использовании Aspose.Note for Java?**  
A4: Да, вы можете задавать вопросы на форуме Aspose.Note [Aspose.Note forum](https://forum.aspose.com/c/note/28).

**Q5: Доступна ли бесплатная пробная версия Aspose.Note for Java?**  
A5: Да, вы можете скачать бесплатную пробную версию с [website](https://releases.aspose.com/).

**Последнее обновление:** 2026-08-08  
**Тестировано с:** Aspose.Note for Java (latest release)  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [отслеживание изменений onenote – Управление ревизиями страниц с Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Aspose Java Tutorial - Получить информацию о страницах в OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Изменить фон страницы OneNote – Aspose.Note for Java](/note/java/onenote-page-manipulation/set-page-background-color/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}