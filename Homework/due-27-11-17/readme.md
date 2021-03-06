# Домашнее задание на 27 ноября 2017

## Сложность: Classic

В этот раз задание достаточно тривиальное.

Вам нужно научиться кидать POST-запросы. Для этого мы подготовили
вам новую версию сервера, которая умеет всё то же, что и раньше
(смотрите дз по заметкам на 6 ноября), а кроме того, выводит консоль все
POST-запросы, которые ему поступают, отвечая на них JSON-ом следующей структуры:

```javascript
{
    response: 'ok'
}
```

Сервер слушает POST-запросы на `http://localhost:8080`.

Всё просто. Кто хочет, пользуйтесь Fetch API (не забудьте почитать про Promise
перед этим), всем остальным к использованию рекомендуется XMLHttpRequest.

Перед тем, как вы начнёте делать это задание, давайте поговорим немного о JSON.

**JSON** (_JavaScript Object Notation_) &mdash; это способ сериализации объектов
JS в plain text (а напомним, что JS-объекты это пары "ключ-значение" любой глубины
вложенности, которые могут содержать любые данные), который получил широкое распространение
и стал независимым от языка и используется сейчас проактически повсеместно для передачи
структур данных и не только.

В JS есть небольшое API для работы с JSON.

### JSON.parse(*string*)

Возвращает объект, полученный после преобразования строки *string* из JSON (_парсинга_).

### JSON.stringify(*object*)

Возвращает строку, полученную в результате сериализации объекта *object* в JSON.

Поиграйтесь с POST-запросами, кидайте на сервер JSON, смотрите в консоли, как он выглядит
в формате plain text'а.

## Сложность: Software Architect

Продумайте архитектуру вашего приложения с заметками так, чтобы оно могло без особых
затруднениях синхронизировать любые изменения, вносимые пользователем, с сервером.

Продумайте, объектами какого формата вы будете обмениваться с сервером.

Реализуйте отправку POST-запросов на сервер в те моменты, когда вы считаете нужным, чтобы
прошла синхронизация.

Возможно, архитектуру вашего приложения придётся кардинально переработать вплоть до
введения некоего глобального состояния. Подумайте, какое решение подойдёт лучше именно вам.