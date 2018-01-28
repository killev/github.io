# Краткий экскурс в историю
Дело в том, что тот ООП, который мы видим сейчас - он немного отличается от того, каким он задумывался.

А задумывался ООП Аланом Кеем как парадигма разработки программного обеспечения в которой программа представлена в виде классов и экземпляров классов (объектов), которые взаимодействуют друг с другом при помощи асинхронных сообщений.

Что это значит для нас как для программистов.
* Функция не может возвращать значение.
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
