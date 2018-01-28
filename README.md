# Краткий экскурс в историю
Дело в том, что тот ООП, который мы видим сейчас - он немного отличается от того, каким он задумывался.

А задумывался ООП Аланом Кеем как парадигма разработки программного обеспечения в которой программа представлена в виде классов и экземпляров классов (объектов), которые взаимодействуют друг с другом при помощи асинхронных сообщений.

Что это значит для нас как для программистов.
* Перовое: функция не может возвращать значение.
  Мы больше не можем написать: 

```swift
class TextFile
{
...
func numberOfLines()->Int
...
```
вместо этого предлагались разные варианты. Самым удобным (с точки зрения синтаксиса, а не внутренне реализации) оказалась передача callback:
```swift
class TextFile
{
...
void numberOfLines(callback: (Int)->Void)
...
```
* И второе (непосредственно сдледует из первого). У класса не может быть свойств. Если рассматривать свойство класса *getter* и *setter*, то *getter* не возможен т.к. мы не можем возвращать значение.

