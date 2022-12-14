# io
Библиотека ``io`` плагина почти идентична своей реализации в чистом Lua [5.1](https://www.lua.org/manual/5.1/manual.html#5.7)/[5.2](https://www.lua.org/manual/5.2/manual.html#6.8)/[5.3](https://www.lua.org/manual/5.3/manual.html#6.8)/[5.4](https://www.lua.org/manual/5.4/manual.html#6.8).

## Отключённые стандартные функции

```lua
io.input()
io.output()
io.read()
io.write()
io.stdout
io.stderr
io.stdin
```


## Новые функции

### boolean: io.ensure

```lua
io.ensure(string: folder)
```

Убеждается, что указанная папка существует.

### string: io.datafolder

```lua
io.datafolder()
```

Возвращает путь до уникальной папки для хранения скриптом каких-либо данных.

### string: io.scrname

```lua
io.scrname()
```

Возвращает название скрипта, исполнившего функцию.
