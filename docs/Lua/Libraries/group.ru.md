# group
Библиотека для взаимодействия с ситемой групп.

## Функции 

### int: group.add

```lua
local groupId = group.add(string: name, int: rank)
```

Создаёт новую группу и возвращает её id. Игроки с низжшими рангами расположены ниже игроков с высшими.

### boolean: group.remove

```lua
group.remove(int: groupId)
```

Удаляет группу с указанным id.

### string, int: group.getinfo

```lua
local groupName, groupRank = group.getinfo(int: groupId)
```

Возвращает информацию о группе - её название и ранг.
