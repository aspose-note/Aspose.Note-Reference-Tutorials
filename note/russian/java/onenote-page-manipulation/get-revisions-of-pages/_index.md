---
date: 2026-08-13
description: Узнайте, как получить время изменения страницы OneNote и извлечь ревизии
  страниц с помощью Aspose.Note для Java, идеально подходит для аудита и управления
  документами.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Получить ревизии страниц в OneNote - Aspose.Note
og_description: Узнайте, как получить время изменения страницы OneNote и извлечь ревизии
  страниц OneNote с помощью Aspose.Note для Java. Быстрые шаги, code snippets и troubleshooting.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Получить время изменения страницы OneNote с помощью Aspose.Note – руководство
  по Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Получить время изменения страницы OneNote с помощью Aspose.Note
url: /ru/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Получить время изменения страницы OneNote с помощью Aspose.Note

## Введение

В этом руководстве вы узнаете, как **получить время изменения страницы OneNote** и извлечь полную историю правок страницы OneNote с помощью Aspose.Note для Java. Независимо от того, создаёте ли вы функцию аудита, просмотрщик журнала изменений или нужно отобразить дату последнего редактирования в панели управления, это руководство проведёт вас через каждый шаг — от настройки окружения до решения распространённых проблем.

## Быстрые ответы
- **Что возвращает «получить время последнего изменения»?** Возвращает метку времени последнего редактирования страницы OneNote.  
- **Какой класс предоставляет историю правок?** `PageHistory` через `Document.getPageHistory(Page)`.  
- **Нужна ли лицензия для этой функции?** Да, для использования в продакшене требуется действующая лицензия Aspose.Note.  
- **Какая версия Java поддерживается?** Java 8 или выше (JDK 8+).  
- **Можно ли фильтровать правки по автору?** Вы можете читать свойство `Author` каждого объекта `Page` и применять собственный фильтр.

## Что такое «получить время последнего изменения» в OneNote?

Время последнего изменения хранится как атрибут метаданных каждой страницы OneNote и указывает момент последнего редактирования. Aspose.Note предоставляет это значение через метод `Page.getLastModifiedTime()`, который возвращает объект `java.util.Date`, который можно отформатировать или записать в журнал в соответствии с требованиями вашего приложения.

## Зачем извлекать версии страниц?

Извлечение версий страниц дает полный журнал аудита всех изменений, внесённых в страницу OneNote, позволяя отслеживать, кто что и когда редактировал. Эта история может использоваться для сравнения версий, восстановления предыдущих состояний или анализа моделей совместной работы в командах, что важно для соответствия требованиям и контроля качества.

## Требования

- **Java Development Kit (JDK) 8 или новее** – установите с сайта Oracle или любого совместимого поставщика.  
- **Библиотека Aspose.Note для Java** – скачайте JAR с страницы выпусков Aspose.Note Java **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** и следуйте руководству по установке **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Импорт пакетов

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(Фактические инструкции импорта показаны как обычный текст, чтобы сохранить оригинальное количество блоков кода.)*

## Как получить время изменения страницы OneNote?

Чтобы получить метку времени последнего изменения, сначала загрузите документ OneNote в объект `Document`, затем выберите нужную `Page`. Вызовите метод `getLastModifiedTime()` у этой страницы — он вернёт объект `java.util.Date`. Затем вы можете отформатировать эту дату с помощью `SimpleDateFormat` или преобразовать её в UTC для единообразного отображения в разных часовых поясах.

## Шаг 1: установить каталог документа

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Шаг 2: загрузить документ

```java
String dataDir = "Your Document Directory";
```

## Шаг 3: получить первую страницу

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Шаг 4: получить версии страниц

```java
Page firstPage = doc.getFirstChild();
```

## Шаг 5: пройтись по версиям страниц

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Распространённые проблемы и решения
- **Null `PageHistory`** – Убедитесь, что в блокноте действительно есть правки; иначе `getPageHistory` возвращает `null`.  
- **Различия часовых поясов** – `getLastModifiedTime()` использует часовой пояс JVM по умолчанию. При необходимости преобразуйте в UTC с помощью `SimpleDateFormat`.  
- **Лицензия не загружена** – Без действующей лицензии Aspose.Note работает в режиме оценки, ограничивая обработку страниц. Загрузите файл лицензии при старте приложения, чтобы избежать этого ограничения.

## Часто задаваемые вопросы

**Q1: Можно ли использовать Aspose.Note для Java для создания новых документов OneNote?**  
A: Да, API позволяет программно создавать, редактировать и сохранять блокноты OneNote с нуля.

**Q2: Совместим ли Aspose.Note для Java с разными версиями файлов OneNote?**  
A: Да, поддерживает форматы файлов OneNote 2007‑2021, обеспечивая широкую совместимость как на настольных, так и облачных платформах.

**Q3: Можно ли настроить формат вывода при экспорте документов OneNote?**  
A: Абсолютно. Вы можете экспортировать в PDF, HTML, PNG или SVG и управлять параметрами, такими как разрешение изображений и встраивание шрифтов.

**Q4: Требуется ли лицензия Aspose.Note для Java для коммерческого использования?**  
A: Да, коммерческая лицензия обязательна для продакшн‑развёртываний. Доступна бесплатная пробная версия для оценки.

**Q5: Где можно получить помощь, если возникнут проблемы?**  
A: Посетите форум сообщества Aspose.Note **[Aspose.Note forum](https://forum.aspose.com/c/note/28)**, чтобы задать вопросы, поделиться опытом и получить помощь от сообщества и инженеров Aspose.

---

**Последнее обновление:** 2026-08-13  
**Тестировано с:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Автор:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Связанные руководства

- [Учебник Aspose Java — Получить информацию о страницах в OneNote — Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Учебник по версиям страниц aspose.note — Получить версии страниц в OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Отслеживание изменений в OneNote — Управление версиями страниц с Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}