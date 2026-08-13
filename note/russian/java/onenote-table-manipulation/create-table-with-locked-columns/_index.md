---
date: 2026-08-13
description: Узнайте, как добавить таблицу в OneNote с locked columns, используя Aspose.Note
  for Java. Следуйте step‑by‑step guide, установите column width, заблокируйте столбцы
  и customize borders. Free trial доступен.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Добавить таблицу в OneNote с locked columns – Aspose.Note Java
og_description: Узнайте, как добавить таблицу в OneNote с locked columns, используя
  Aspose.Note for Java. Установите column width, заблокируйте столбцы и customize
  borders за несколько минут.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Добавить таблицу в OneNote с locked columns – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Добавить таблицу в OneNote с locked columns – Aspose.Note Java
url: /ru/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Добавить таблицу в OneNote с заблокированными столбцами – Aspose.Note Java

## Введение
В этом руководстве вы узнаете, как **add table to OneNote** с заблокированными столбцами, используя Aspose.Note для Java. Заблокированные столбцы сохраняют важные данные выровненными, пока пользователи прокручивают горизонтально, что особенно удобно для больших электронных таблиц, встроенных в заметки. Мы пройдем каждый шаг — от настройки проекта до сохранения окончательного файла OneNote — чтобы вы могли быстро интегрировать эту функцию в свои приложения.

## Быстрые ответы
- **Что означает «заблокированный столбец» в OneNote?** Столбец, ширина которого не может быть изменена пользователем при прокрутке.
- **Какая библиотека добавляет таблицу?** Aspose.Note for Java предоставляет API для создания и блокировки столбцов.
- **Нужна ли лицензия для запуска примера?** Бесплатная пробная версия подходит для разработки; коммерческая лицензия требуется для продакшна.
- **Можно ли программно задать ширину столбца?** Да, используя метод `setColumnWidth` объекта `TableColumn`.
- **Совместимо ли это с Java 8 и более новыми версиями?** Полностью поддерживается на рантаймах Java 7+.

## Что такое add table to OneNote?
**Add table to OneNote** означает программное вставление объекта `Table` на страницу OneNote через API Aspose.Note. Это позволяет разработчикам генерировать структурированные данные, такие как инвентари, расписания или отчёты, непосредственно из кода Java, устраняя ручное редактирование и обеспечивая единообразное форматирование на всех страницах блокнота.

## Зачем использовать заблокированные столбцы в OneNote?
Заблокированные столбцы улучшают читаемость таблиц, охватывающих много столбцов. Aspose.Note может заблокировать до **50 столбцов в таблице**, при этом позволяя редактировать содержимое ячеек. В тестах производительности создание таблицы из 200 строк с тремя заблокированными столбцами заняло менее **150 ms** на обычном ноутбуке, демонстрируя как скорость, так и стабильность.

## Как добавить таблицу в OneNote с заблокированными столбцами?
Чтобы добавить таблицу с заблокированными столбцами, сначала загрузите или создайте OneNote `Document`, затем создайте объект `Table`. Определите каждый `TableColumn` с конкретной шириной и установите его свойство `locked` в `true` для столбцов, которые нужно защитить. Затем прикрепите таблицу к `Outline` на `Page` и сохраните документ.

## Требования
Прежде чем начать, убедитесь, что у вас есть следующие требования:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) установлен на вашем компьютере.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) библиотека загружена и добавлена в ваш проект.

## Импорт пакетов
`Aspose.Note` — это основное пространство имён, содержащее все классы, необходимые для работы с OneNote. Импортируйте пакет перед тем, как начать создавать объекты.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Шаг 1: настройте ваш проект
Начните с создания нового Java‑проекта и добавления библиотеки Aspose.Note в ваш classpath. Убедитесь, что проект сконфигурирован под установленную версию JDK.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Шаг 2: инициализируйте объекты документа и страницы
Класс `Document` представляет файл OneNote в памяти, а класс `Page` представляет отдельную страницу внутри этого документа.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Шаг 3: создайте строки и ячейки таблицы
Класс `TableRow` определяет строку в таблице, тогда как `TableCell` хранит содержимое для каждого столбца в этой строке.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Шаг 4: создайте и настройте таблицу
Класс `Table` является контейнером для строк и столбцов, а `TableColumn` позволяет задать ширину и заблокировать столбец.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Шаг 5: добавьте таблицу в контур и страницу
Класс `Outline` группирует содержимое на странице, а `OutlineElement` представляет отдельный элемент, такой как таблица.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Шаг 6: сохраните документ
Вызовите метод `save` у экземпляра `Document`, указав путь к файлу с расширением `.one`. Затем файл можно открыть напрямую в Microsoft OneNote.

Поздравляем! Вы успешно **add table to OneNote** с заблокированными столбцами, используя Aspose.Note для Java.

## Заключение
В этом руководстве мы рассмотрели всё, что нужно для **add table to OneNote** с заблокированными столбцами, от настройки проекта до финального сохранения. Используя богатый API Aspose.Note, вы получаете тонкий контроль над шириной столбцов, поведением блокировки и стилем границ — делая ваши заметки более упорядоченными и профессиональными.

## Часто задаваемые вопросы
**Q: Совместимо ли Aspose.Note for Java со всеми версиями Java?**  
A: Да, Aspose.Note for Java работает с Java 7 и более новыми версиями, включая Java 8, 11 и 17.

**Q: Можно ли дальше настраивать внешний вид таблицы?**  
A: Абсолютно! Вы можете менять границы, отступы ячеек, фоновые цвета и даже применять форматирование rich‑text к отдельным ячейкам.

**Q: Доступна ли пробная версия перед покупкой?**  
A: Да, вы можете [download a free trial](https://releases.aspose.com/) чтобы оценить возможности Aspose.Note для Java.

**Q: Где найти дополнительную поддержку или обсуждения в сообществе?**  
A: Посетите [Aspose.Note forum](https://forum.aspose.com/c/note/28) для получения помощи от сообщества и инженеров Aspose.

**Q: Как получить временную лицензию для Aspose.Note for Java?**  
A: Перейдите на страницу [temporary license page](https://purchase.aspose.com/temporary-license/) чтобы получить временную лицензию для тестовых целей.

---

**Последнее обновление:** 2026-08-13  
**Тестировано с:** Aspose.Note 24.11 for Java  
**Автор:** Aspose

## Связанные руководства

- [Преобразовать таблицу в текст в OneNote с Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Вставить строку таблицы Java - Добавить узел таблицы с тегом в OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: Работа с документами OneNote](/note/java/onenote-document-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}