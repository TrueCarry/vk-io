# Attachment

```js
import { Attachment } from 'vk-io';
```

Наследуется потомками

## Constructor
Инициализация новой инстанции

```js
new Attachment(type, ownerId, id, accessKey);
```

Пример использования

```js
new Attachment('photo', 1, 456264771);
```

| Параметр  | Тип    | Описание                     |
|-----------|--------|------------------------------|
| type      | string | Тип прикрепления             |
| ownerId   | number | Идентификатор владелеца      |
| id        | number | Идентификатор прикрепления   |
| accessKey | string | Ключ доступа (необязательно) |

## fromString (static)
Парсирит прикрепление из строки в объект

```js
Attachment.fromString(attachment); // => Attachment
```

| Параметр   | Тип    | Описание     |
|------------|--------|--------------|
| attachment | string | Прикрепление |

Пример использования

```js
Attachment.fromString('photo1_456264771'); // => Attachment
```

## isFilled
Заполнен ли объект прикрепления, используется в классах наследниках

```js
attachment.isFilled; // => boolean
```

## type
Возвращает тип прикрепления

```js
attachment.type; // => string
```

## ownerId
Возвращает идентификатор владельца

```js
attachment.ownerId; // => number
```

## id
Возвращает идентификатор прикрепления

```js
attachment.id; // => number
```

## accessKey
Возвращает ключ доступа

```js
attachment.accessKey; // => ?string
```

## equals

Проверяет эквивалентность прикрепления

```js
attachment.equals(attachment); // => boolean
```

| Параметр   | Тип        | Описание     |
|------------|------------|--------------|
| attachment | Attachment | Прикрепление |

## equalString

Проверяет эквивалентность прикрепления строки с объектом

```js
attachment.equalString(attachment); // => boolean
```

| Параметр   | Тип    | Описание     |
|------------|--------|--------------|
| attachment | string | Прикрепление |

## toString
Возвращает строковое представление прикрепления

```js
String(attachment);

// OR

attachment.toString();
```

Пример использования

```js
const attachment = new Attachment('photo', 1, 456264771);

console.log(String(attachment)); // => photo1_456264771
```
