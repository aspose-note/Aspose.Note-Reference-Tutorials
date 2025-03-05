---
title: Сохранение в двоичном изображении с использованием фиксированного порога в OneNote
linktitle: Сохранение в двоичном изображении с использованием фиксированного порога в OneNote
second_title: Aspose.Note Java API
description: С легкостью сохраняйте документы Microsoft OneNote в виде двоичных изображений, используя фиксированный порог с помощью Aspose.Note Java. Расширьте возможности манипулирования файлами OneNote.
type: docs
weight: 14
url: /ru/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
---
## Введение

Aspose.Note для Java — это мощный API, который позволяет разработчикам программно работать с файлами Microsoft OneNote. В этом уроке мы рассмотрим, как сохранить документ в виде двоичного изображения, используя фиксированный порог. Чтобы добиться этого, выполните следующие действия.

## Предварительные условия

Прежде чем начать, убедитесь, что у вас есть следующее:

1. В вашей системе установлен Java Development Kit (JDK).
2.  Скачана библиотека Aspose.Note для Java. Вы можете скачать его с[здесь](https://releases.aspose.com/note/java/).
3. Базовые знания Java-программирования.

## Импортировать пакеты

Сначала импортируйте необходимые пакеты в ваш Java-файл.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Шаг 1. Загрузите документ

Загрузите документ OneNote с помощью API Aspose.Note.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Шаг 2. Установите параметры бинаризации

Определите параметры бинаризации для сохранения документа в виде двоичного изображения.

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

## Шаг 3. Установите параметры сохранения изображения

Установите параметры сохранения изображения, включая цветовой режим и параметры бинаризации.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## Шаг 4. Сохраните документ

Сохраните документ как двоичное изображение с указанными параметрами.

```java
oneFile.save(dataDir, options);
```

## Заключение

В этом уроке мы узнали, как сохранить документ в виде двоичного изображения, используя фиксированный порог в Aspose.Note для Java. Выполнив эти шаги, вы сможете легко манипулировать файлами OneNote программным способом.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я настроить пороговое значение для бинаризации?

 A1: Да, вы можете настроить пороговое значение в соответствии с вашими требованиями, изменив`setBinarizationThreshold()` параметр метода.

### Вопрос 2. Совместим ли Aspose.Note для Java со всеми версиями Microsoft OneNote?

A2: Aspose.Note для Java поддерживает различные версии Microsoft OneNote, включая 2010, 2013 и 2016.

### Вопрос 3. Существуют ли какие-либо ограничения на размер обрабатываемых документов?

О3: Aspose.Note for Java не имеет ограничений на размер обрабатываемых документов, что позволяет эффективно обрабатывать большие файлы.

### Вопрос 4. Могу ли я конвертировать несколько документов OneNote одновременно?

A4: Да, вы можете обрабатывать несколько документов OneNote в пакетном режиме, перебирая каждый файл и применяя необходимые операции.

### Вопрос 5: Доступна ли техническая поддержка для Aspose.Note для Java?

 A5: Да, техническая поддержка доступна через[Форум Aspose.Note](https://forum.aspose.com/c/note/28), где можно задать вопросы и обратиться за помощью к экспертам.