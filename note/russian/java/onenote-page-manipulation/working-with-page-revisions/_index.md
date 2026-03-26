---
date: 2026-01-15
description: Узнайте, как отслеживать изменения в OneNote и управлять версиями страниц
  в документах OneNote с помощью Aspose.Note для Java. Включает пример сводки ревизий
  и информацию о том, как изменить дату ревизии.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Отслеживание изменений в OneNote – Управление версиями страниц с помощью Aspose.Note
url: /ru/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Работа с ревизиями страниц в OneNote - Aspose.Note

## Введение

OneNote — мощный инструмент для организации заметок, и когда вам нужно **track changes onenote**, управление ревизиями страниц становится необходимым для эффективного сотрудничества. С помощью Aspose.Note for Java вы можете программно обрабатывать ревизии, просматривать, кто отредактировал страницу, и даже корректировать метки времени. Этот учебник проведёт вас через каждый шаг, от загрузки документа до обновления сводки ревизий.

## Быстрые ответы
- **What does “track changes onenote” mean?** Это относится к мониторингу того, кто редактировал страницу OneNote и когда.
- **Which library is required?** Aspose.Note for Java.
- **Can I change the author or date of a revision?** Да, используя RevisionSummary API (`modify revision date`).
- **Do I need a OneNote file beforehand?** Да, требуется пример файла `.one`.
- **Is a license needed for production?** Да, для коммерческого использования требуется действующая лицензия Aspose.Note.

## Что такое пример сводки ревизий?

*revision summary* предоставляет метаданные о последних изменениях на странице — имя автора, время последнего изменения и другие детали. В этом руководстве мы получим и отобразим эту информацию, а затем покажем, как **modify revision date**.

## Почему стоит использовать track changes onenote с Aspose.Note?

- **Collaboration:** Быстро увидеть, кто внес последние правки.
- **Auditing:** Сохранять надёжную историю изменений для соответствия требованиям.
- **Automation:** Интегрировать обработку ревизий в back‑end сервисы или инструменты миграции.

## Требования

### Java Development Environment
Убедитесь, что на вашей системе установлен Java Development Kit (JDK).

### Aspose.Note for Java Library
Скачайте и установите библиотеку Aspose.Note for Java по ссылке [here](https://releases.aspose.com/note/java/).

### OneNote Document
Подготовьте пример документа OneNote для тестирования.

## Импорт пакетов

В вашем Java‑проекте импортируйте необходимые пакеты для работы с Aspose.Note for Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Давайте разберём предоставленный пример на несколько шагов для лучшего понимания.

## Шаг 1: Загрузка документа OneNote

Сначала загрузите документ OneNote и получите первую дочернюю страницу.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Шаг 2: Чтение сводки ревизий страницы

Прочитайте сводку ревизий содержимого страницы. Это **revision summary example**, показывающая, кто отредактировал страницу последним.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Шаг 3: Обновление сводки ревизий страницы

Обновите сводку ревизий страницы, указав нового автора и новую дату изменения. Это демонстрирует, как программно **modify revision date**.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Заключение

Программное управление ревизиями страниц в документах OneNote можно упростить с помощью Aspose.Note for Java. Следуя шагам, описанным в этом учебнике, вы сможете эффективно **track changes onenote**, просматривать детали ревизий и даже **modify revision date**, чтобы соответствовать вашему рабочему процессу.

## Часто задаваемые вопросы

### Q1: Можно ли использовать Aspose.Note for Java с другими Java‑библиотеками?
A: Да, Aspose.Note for Java можно интегрировать с другими Java‑библиотеками для расширения функциональности.

### Q2: Поддерживает ли Aspose.Note for Java все версии документов OneNote?
A: Aspose.Note for Java поддерживает различные версии документов OneNote, включая более старые версии.

### Q3: Подходит ли Aspose.Note for Java для корпоративных приложений?
A: Абсолютно, Aspose.Note for Java разработан для удовлетворения потребностей корпоративных приложений с надёжными функциями и масштабируемостью.

### Q4: Могу ли я настраивать ревизии страниц с помощью Aspose.Note for Java?
A: Да, вы можете настраивать ревизии страниц в соответствии с вашими требованиями, используя Aspose.Note for Java.

### Q5: Где я могу получить поддержку для Aspose.Note for Java?
A: Вы можете получить поддержку для Aspose.Note for Java на форуме [Aspose.Note forum](https://forum.aspose.com/c/note/28).

---

**Последнее обновление:** 2026-01-15  
**Тестировано с:** Aspose.Note for Java 24.12  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}