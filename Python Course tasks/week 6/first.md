Напишите функцию `first`, которая будет принимать вообще все что угодно и возвращать свой первый аргумент. Если все её аргументы именованные, то пускай она возвращает тот у которого самое маленькое имя. Если ей не передано ничего, то пускай она возвращает `None`.

`first(0.0123) == 0.0123`

```python
def first(*args, **kwargs):
	if args:
		return args[0]
	elif kwargs:
		return kwargs[min(kwargs.items)[0]]
```