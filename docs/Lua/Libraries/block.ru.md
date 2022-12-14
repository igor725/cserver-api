# block
Эта библиотека предназначена для различных манипуляций над блоками.

## Функции

### Block: block.define

```lua
block.define(table: blockDefinition)
```

Возвращает новый объект Block с переданными параметрами.

### boolean: block.isvalid

```lua
block.isvalid(int: blockId)
```

Возвращаемое значение указывает на то, существует ли блок с данным id.

### int: block.fallbackfor

```lua
block.fallbackfor(int: blockId)
```

Возвращает ванильный блок сопоставимый с кастомным. Фоллбек-блоки используются для отправки клиентам без CPE, т.е. ванильному Classic клиенту.

### BulkBlockUpdate: block.bulk

```lua
block.bulk()
```

```lua
block.bulk([World: wrld, boolean: autoSend])
```

Создаёт новый объект BulkBlockUpdate. Если указать первым параметром объект мира и/или вторым boolean автоотправки, то создастся настроенный объект.

## Структура таблицы blockDefinition

| Параметр      | Описание                                                      |
|---------------|---------------------------------------------------------------|
| name          | string: Имя создаваемого блока.                               |
| fallback      | int: ID сопоставимого блока (для ванильных клиентов).         |
| extended      | boolean: Использует ли блок расширенный набор параметров.     |
| param         | table: Параметры создаваемого блока.                          |

## Общие параметры для расширенных и нерасширенных блоков
| Параметр      | Описание                                                          |
| solidity      | EBlockSolidity: Режим коллизии для блока.                         |
| movespeed     | int: Модификатор скорости для блока. Подробное описание [здесь](https://wiki.vg/Classic_Protocol_Extension#DefineBlock_Packet) |
| toptex        | int: ID текстуры на вершине блока.                                |
| bottomtex     | int: ID текстуры нижней границы блока.                            |
| transmitsLight| boolean: Пропускает ли блок солнечный свет.                            |
| walksound     | EBlockSounds: Звук, издаваемый блоком, когда игрок на него наступает.  |
| fullbright    | boolean: Затеняется ли блок.                                           |
| drawType      | EBlockDrawTypes: Тип отрисовки блока клиентом.                         |
| fogdensity    | int: Густота тумана, когда игрок находится внутри блока.               |
| fogR          | int: Красный компонент цвета тумана.                                   |
| fogG          | int: Зелёный компонент цвета тумана.                                   |
| fogB          | int: Синий компонент цвета тумана.                                     |

## Для нерасширенных блоков необходимы следующие параметры

| Параметр      | Описание                                                          |
|---------------|-------------------------------------------------------------------|
| sidetex       | int: ID боковой текстуры блока.                                   |

| shape         | int: 0 - Спрайт; 1 -> 16 Высота блока.                            |


## Для расширенных блоков необходимы следующие параметры

| Параметр      | Описание                                                          |
|---------------|-------------------------------------------------------------------|
| lefttex       | int: ID текстуры левой грани блока.                        |
| righttex      | int: ID текстуры правой грани блока.                       |
| fronttex      | int: ID текстуры передней грани блока.                            |
| backtex       | int: ID текстуры задней грани блока.                             |
| minx          | int: Minimum X coordinate in pixels. Values between 0 and 15 allowed.  |
| miny          | int: Minimum Y coordinate in pixels. Values between 0 and 15 allowed.  |
| minz          | int: Minimum Z coordinate in pixels. Values between 0 and 15 allowed.  |
| maxx          | int: Maximum X coordinate in pixels. Values between 0 and 15 allowed.  |
| maxy          | int: Maximum Y coordinate in pixels. Values between 0 and 15 allowed.  |
| maxz          | int: Maximum Z coordinate in pixels. Values between 0 and 15 allowed.  |

## EBlockSolidity

| Имя           | Описание                                            |
|---------------|-----------------------------------------------------|
| BDSOL_WALK    | Коллизии нет (игрок может пройти сквозь блок).      |
| BDSOL_SWIM    | Физика жидкости (игрок может плавать внутри блока). |
| BDSOL_SOLID   | Твёрдый блок (игрок может ходить по блоку).         |

## EBlockSounds

| Имя           |
|---------------|
| BDSND_NONE    |
| BDSND_WOOD    |
| BDSND_GRAVEL  |
| BDSND_GRASS   |
| BDSND_STONE   |
| BDSND_METAL   |
| BDSND_GLASS   |
| BDSND_WOOL    |
| BDSND_SAND    |
| BDSND_SNOW    |

## EBlockDrawTypes

| Имя                | Описание                                                  |
|--------------------|-----------------------------------------------------------|
| BDDRW_OPAQUE       | Непрозрачный блок.                                        |
| BDDRW_TRANSPARENT  | Прозрачный со скрытием общих граней.                      |
| BDDRW_TRANSPARENT2 | Прозрачный без скрытия общих граней.                      |
| BDDRW_TRANSLUCENT  | Полупрозрачный с наложенной текстурой (вода, лёд и т.д.)  |
| BDDRW_GAS          | Полностью прозрачный (воздух).                            |
