# world
Библиотека, которая позволяет взаимодействовать с мирами.

## Функции

### World: world.create

```lua
world.create(string: worldName, Short Vector: worldDimensions)
```

Создаёт новый мир и возвращает представляющий его объект.

### World: world.getbyname

```lua
world.getbyname(string: worldName)
```

Возвращает объект, представляющий мир с указанным именем.

### world.iterall

```lua
World.iterall(func: ITERATE_FUNCTION(World: worldObj))
```

Запускает итерацию по всем мирам, передавая каждый в ``ITERATE_FUNCTION()``.

### World: world.getmain

```lua
world.getmain()
```

Возвращает текущий мир, который установлен как основной.

### world.setmain

```lua
world.setmain(World: world)
```

Устанавливает указанный мир основным.
