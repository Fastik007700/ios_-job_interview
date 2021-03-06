## Использование instancetype.

[**Вернутся к списку вопросов**](https://github.com/Torlopov-Andrey/hh_interview_ios/blob/master/readme.md)

В `ObjC` имеется замечательный тип `id`, который по сути является `NSObject *`, то есть, самым базовым типом для объектов, к которому можно привести любой другой объект. Удобно, но в некоторых случаях могут возникнуть проблемы. К примеру:

```Objective-C
[[MyClass sharedInstance] count];
```

Если sharedInstance возвращает id, то код соберётся без предупреждений даже если в `MyClass` нет метода `count`. Если же sharedInstance будет возвращать `instancetype`, то ворнинг всё же появится, ведь компилятор явно понимает, что возвращается объект того класса, у которого вызван `sharedInstance`.

Рекомендации по использованию: уместно в методах типа `init/new/copy` и т.п.

**Дополнительно**
* [Источник + доп материал.](https://habrahabr.ru/company/mailru/blog/210672/)
