# Домашнее задание к занятию «2.6. База данных и хранение данных»

**Правила выполнения домашней работы:** 
* выполняйте домашнее задание в отдельной ветке проекта на GitHub,
* в поле для сдачи работы прикрепите ссылку на ваш проект в Git,
* присылать на проверку можно каждую задачу по отдельности или все задачи вместе, 
* во время проверки по частям ваша домашняя работа будет обозначаться статусом «На доработке»,
* любые вопросы по решению задач задавайте в канале вашей группы.


#### Задание 1
Чтобы в будущем вам было легче работать с **MongoDB**, изучите раздел 
документации об использовании [**CRUD Operations**](https://docs.mongodb.com/manual/crud/).

#### Задание 2
В файле **README.md** написать следующие запросы для **MongoDB**:
 - запрос(ы) для *вставки* данных минимум о двух книгах в коллекцию **books**,
 - запрос для *поиска* полей документов коллекции **books** по полю *title*,
 - запрос для *редактирования* полей: *description* и *authors* коллекции **books** по *_id* записи.
 
*Каждый документ коллекции **books** должен содержать следующую структуру данных: 
```javascript
{
  title: "string",
  description: "string",
  authors: "string"
}
``` 
#### Выполнение заданий.

- запрос(ы) для *вставки* данных минимум о двух книгах в коллекцию **books**,
- 
```javascript  
db.books.insertMany([
  {
    title: 'string',
    authors: 'string',
    description: 'string',
  },
  {
    title: 'string',
    authors: 'string',
    description: 'string', 
  },
]);
``` 
 - запрос для *поиска* полей документов коллекции **books** по полю *title*,
 - 
```javascript  
db.books.find({ title: 'string' });
``` 
 - запрос для *редактирования* полей: *description* и *authors* коллекции **books** по *_id* записи.
 - 
```javascript  
db.books.updateOne(
  { _id: 'id' },
  { $set: { description: 'new string', authors: 'new string' } }
);
``` 