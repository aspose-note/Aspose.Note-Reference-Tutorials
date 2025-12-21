---
date: 2025-12-21
description: Узнайте, как получить размеры изображения в Java с помощью Aspose.Note.
  Извлеките ширину, высоту, имя файла и многое другое из файлов OneNote всего за несколько
  шагов.
linktitle: Get Image Dimensions Java from OneNote
second_title: Aspose.Note Java API
title: Получить размеры изображения Java из OneNote
url: /ru/java/onenote-hyperlinks-images/get-image-info/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Получить размеры изображений Java из OneNote

## Введение

Если вам нужно **получить размеры изображений Java** из блокнотов OneNote, вы попали по адресу. Во многих сценариях автоматизации — генерация отчетов, миграция контента или аналитика — вам понадобится знать ширину, высоту, оригинальный размер и имя файла каждой картинки без ручного открытия блокнота. Этот учебник покажет, как программно извлечь эту информацию с помощью Aspose.Note for Java.

## Быстрые ответы
- **Что делает код?** Извлекает каждое изображение из файла OneNote и выводит его размеры, оригинальный размер, имя файла и дату изменения.  
- **Какая библиотека требуется?** Aspose.Note for Java.  
- **Нужна ли лицензия?** Временная лицензия подходит для тестирования; полная лицензия требуется для продакшна.  
- **Сколько строк кода?** Около 30 строк, разбитых на понятные, переиспользуемые шаги.  
- **Типичное время выполнения?** Миллисекунды для стандартного блокнота с несколькими десятками изображений.

## Предварительные требования

Прежде чем приступить к реализации, убедитесь, что у вас есть следующие условия:

### 1. Java Development Kit (JDK)

Убедитесь, что Java Development Kit (JDK) установлен на вашей системе. Вы можете скачать и установить последнюю версию JDK с [сайта Oracle](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Библиотека Aspose.Note for Java

Скачайте и подключите библиотеку Aspose.Note for Java в ваш проект. Вы можете получить библиотеку со [страницы загрузки](https://releases.aspose.com/note/java/).

### 3. Документ OneNote

Подготовьте пример документа OneNote, содержащего изображения. Этот документ будет использоваться для программного извлечения информации об изображениях.

## Импорт пакетов

Для начала импортируйте необходимые пакеты из Aspose.Note for Java:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

Разберём приведённый выше код пошагово:

## Как получить размеры изображений Java из OneNote

### Шаг 1: Установить каталог документа

```java
String dataDir = "Your Document Directory";
```

Замените `"Your Document Directory"` на путь к вашему документу OneNote.

### Шаг 2: Загрузить документ

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Загрузите документ OneNote с помощью библиотеки Aspose.Note for Java. Убедитесь, что указали правильный путь к документу.

### Шаг 3: Получить все изображения

```java
List<Image> list = doc.getChildNodes(Image.class);
```

Получите все изображения из загруженного документа OneNote.

### Шаг 4: Вывести общее количество изображений

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

Выведите общее количество изображений, найденных в документе.

### Шаг 5: Перебрать и вывести информацию об изображениях

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

Пройдите по списку изображений и выведите детали, такие как ширина, высота, оригинальные размеры, имя файла и время последнего изменения для каждого изображения.

## Зачем извлекать изображения из OneNote с помощью Java?

- **Автоматизация:** Исключить ручную проверку блокнотов.  
- **Аналитика данных:** Передавать метаданные изображений в конвейеры отчетности.  
- **Миграция:** Сохранить атрибуты изображений при переносе контента на другие платформы.  
- **Производительность:** Получать только необходимые метаданные, избегая тяжёлого парсинга файлов.

## Распространённые ошибки и советы

- **Неправильный путь:** Проверьте, что `dataDir` заканчивается правильным разделителем файлов (`/` или `\`).  
- **Проблемы с лицензией:** Без действующей лицензии Aspose.Note может выдавать предупреждения об оценочной версии.  
- **Большие блокноты:** Для блокнотов с тысячами изображений рассмотрите обработку пакетами, чтобы снизить потребление памяти.

## Часто задаваемые вопросы

### Q1: Может ли Aspose.Note for Java работать с другими форматами документов, помимо OneNote?

A1: Да, Aspose.Note for Java поддерживает различные форматы документов, включая OneNote, PDF и Microsoft Word.

### Q2: Подходит ли Aspose.Note for Java для личного и коммерческого использования?

A2: Да, вы можете использовать Aspose.Note for Java как в личных, так и в коммерческих проектах.

### Q3: Предоставляет ли Aspose.Note for Java техническую поддержку?

A3: Да, техническая поддержка доступна через форумы Aspose по адресу [здесь](https://forum.aspose.com/c/note/28).

### Q4: Можно ли попробовать Aspose.Note for Java перед покупкой?

A4: Да, вы можете ознакомиться с бесплатной пробной версией Aspose.Note for Java на странице [Aspose.Note for Java](https://releases.aspose.com/note/java/).

### Q5: Как получить временную лицензию для Aspose.Note for Java?

A5: Вы можете получить временную лицензию по ссылке [Temporary license/](https://purchase.aspose.com/temporary-license/).

## Заключение

Следуя шагам, описанным в этом учебнике, вы сможете эффективно **получить размеры изображений Java** из документов OneNote с помощью Aspose.Note for Java. Интеграция этой функции в ваши приложения позволит автоматизировать задачи, связанные с обработкой документов, повышая эффективность и продуктивность.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Последнее обновление:** 2025-12-21  
**Тестировано с:** Aspose.Note for Java 23.12  
**Автор:** Aspose  

---