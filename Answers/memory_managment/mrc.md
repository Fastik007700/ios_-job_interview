## Как происходит `ручное управление памятью - MRC` в iOS?

[**Вернутся к списку вопросов**](https://github.com/Torlopov-Andrey/hh_interview_ios/blob/master/readme.md)

При написании программы, мы для каждого объекта выделяем память и по окончании работы очищаем.
Либо при создании отправляем команду объекту "autorelease" и он очистит память самостоятельно.

То есть, ваша работа по управлению памятью сводится к простому правилу. Если вы создается объект используя методы alloc, copy, mutableCopy, new или посылаете объекту команду retain, не забудьте отправить ему release или autorelease сообщение в конце функции. Если вы создаете объект другими способами, то не делайте ничего.