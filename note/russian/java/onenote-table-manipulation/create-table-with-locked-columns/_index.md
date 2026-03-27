---
date: 2026-01-23
description: Узнайте, как зафиксировать ширину столбцов при добавлении таблицы в OneNote
  с помощью Aspose.Note для Java. Пошаговое руководство с кодом, советами и часто
  задаваемыми вопросами.
linktitle: How to Lock Column in OneNote Table – Aspose.Note
second_title: Aspose.Note Java API
title: Как заблокировать столбец в таблице OneNote – Aspose.Note
url: /ru/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как заблокировать столбец в таблице OneNote – Aspose.Note

## Введение
OneNote — универсальная платформа для заметок, а Aspose.Note for Java упрощает **блокировку ширины столбца** при добавлении таблицы в OneNote. В этом руководстве вы увидите полный практический пример, показывающий, как задать ширину столбца таблицы, заблокировать её и настроить границы таблицы OneNote — всё это с помощью нескольких строк кода на Java.

## Быстрые ответы
- **Что означает «заблокировать столбец»?** Это фиксирует ширину столбца, чтобы пользователь не мог изменить её в OneNote.  
- **Какая библиотека предоставляет эту возможность?** Aspose.Note for Java.  
- **Нужна ли лицензия для запуска примера?** Бесплатная пробная версия подходит для оценки; для продакшна требуется коммерческая лицензия.  
- **Можно ли добавить новые строки после блокировки столбца?** Да, строки можно продолжать добавлять; заблокированная ширина сохраняется.  
- **Какая версия Java поддерживается?** Java 6 и новее.

## Что такое «заблокировать столбец» в таблице OneNote?
Блокировка столбца означает назначение фиксированной ширины объекту `TableColumn` и установку его свойства `LockedWidth` в `true`. Это предотвращает случайное изменение размеров пользователями и сохраняет согласованность макета.

## Почему стоит блокировать ширину столбца в OneNote?
- **Последовательный макет** — ваши заметки выглядят одинаково на всех устройствах.  
- **Повышенная читаемость** — длинный текст переносится внутри предсказуемого размера столбца.  
- **Профессиональный вид** — заблокированные столбцы придают отчетному оформлению законченный вид.

## Предварительные требования
Прежде чем начать, убедитесь, что подготовлено следующее:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) установлен на вашем компьютере.  
- Библиотека [Aspose.Note for Java](https://downloads.aspose.com/note/java) загружена и добавлена в classpath вашего проекта.

## Импорт пакетов
В вашем Java‑проекте импортируйте необходимые пакеты для работы с Aspose.Note:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Шаг 1: Настройка проекта
Создайте новый Java‑проект (или используйте существующий) и добавьте JAR‑файлы Aspose.Note в путь сборки. Убедитесь, что проект компилируется с установленным JDK.

## Шаг 2: Инициализация объектов Document и Page
Начинаем с создания нового `Document` и `Page`, где будет размещена таблица.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Шаг 3: Создание строк и ячеек таблицы
Здесь мы формируем две строки, каждая с одной ячейкой, содержащей примерный текст. Это демонстрирует, как работает заблокированный столбец при коротком и длинном содержимом.

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

## Шаг 4: Создание и настройка таблицы
Теперь создаём таблицу, **задаём ширину столбца**, **блокируем столбец** и **настраиваем границы таблицы OneNote**.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);               // customize onenote table borders
TableColumn col = new TableColumn();
col.setWidth(200);                           // set table column width
col.setLockedWidth(true);                    // onenote table locked width
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Шаг 5: Добавление таблицы в Outline и страницу
Присоединяем таблицу к `OutlineElement` и, наконец, добавляем её на страницу — это шаг **add outline element java**.

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

## Шаг 6: Сохранение документа
Сохраните файл OneNote (`.one`) в каталог, указанный ранее.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

Поздравляем! Вы успешно **add table to OneNote** с заблокированным столбцом, фиксированной шириной и настроенными границами, используя Aspose.Note for Java.

## Распространённые проблемы и решения
| Проблема | Решение |
|----------|---------|
| Таблица отображается без границ | Убедитесь, что вызвано `table.setBordersVisible(true);`. |
| Ширина столбца меняется после добавления строк | Проверьте, что `col.setLockedWidth(true);` установлен **до** добавления строк. |
| Файл не сохраняется | Проверьте, что `dataDir` указывает на папку с правом записи и заканчивается корректным именем файла. |

## Часто задаваемые вопросы

**В: Совместима ли Aspose.Note for Java со всеми версиями Java?**  
О: Да, работает с Java 6 и новее, включая Java 11 и Java 17.

**В: Можно ли дальше настраивать внешний вид таблицы?**  
О: Конечно! Вы можете менять стили границ, отступы ячеек, фон и многое другое через свойства `Table` и `TableCell`.

**В: Есть ли пробная версия перед покупкой?**  
О: Да, вы можете [скачать бесплатную пробную версию](https://releases.aspose.com/) и оценить возможности Aspose.Note for Java.

**В: Где найти дополнительную поддержку или обсуждения сообщества?**  
О: Посетите [форум Aspose.Note](https://forum.aspose.com/c/note/28) для получения поддержки и общения с сообществом.

**В: Как получить временную лицензию для Aspose.Note for Java?**  
О: Перейдите по [этой ссылке](https://purchase.aspose.com/temporary-license/) для получения временной лицензии в тестовых целях.

---

**Последнее обновление:** 2026-01-23  
**Тестировано с:** Aspose.Note for Java 24.11  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}