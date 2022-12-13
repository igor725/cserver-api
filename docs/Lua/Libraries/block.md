# block
Creation and interaction with custom blocks.

## Functions

### Block: block.define

```lua
block.define(table: blockDefinition)
```

Returns a new block with the defined parameters.

### boolean: block.isvalid

```lua
block.isvalid(int: blockId)
```

Returns whether or not the block is valid.

### int: block.fallbackfor

```lua
block.fallbackfor(int: blockId)
```

Returns the fallback id for the block.

### BulkBlockUpdate: block.bulk

```lua
block.bulk()
```

```lua
block.bulk([World: worldObj, boolean: autoSend])
```

Creates a new BulkBlockUpdate object. If given, will automatically set the world and/or autoSend.

## blockDefinition table structure

| Parameter     | Description                                                   |
|---------------|---------------------------------------------------------------|
| name          | string: The name of your block.                               |
| fallback      | int: ID of the fallback block (for vanilla clients).          |
| extended      | boolean: Whether or not the block is extended.                |
| param         | table: List of block parameters.                              |

## General parameters for non-extended and extended blocks

| Parameter     | Description                                                             |
| solidity      | EBlockSolidity: Collision mode for this block.                          |
| movespeed     | int: Speed modifier of the block. Look at DefineBlock [movespeed](https://wiki.vg/Classic_Protocol_Extension#DefineBlock_Packet) for more info |
| toptex        | int: Texture ID for the top of the block.                               |
| bottomtex     | int: Texture ID for the bottom of the block.                            |
| transmitsLight| boolean: Whether or not this block allows sunlight to go through.       |
| walksound     | EBlockSounds: Sound the block makes when walked on.                     |
| fullbright    | boolean: Whether or not this block affected by shadows.                 |
| drawType      | EBlockDrawTypes: The way the block is drawn client-side.                |
| fogdensity    | int: Density of fog while the client's camera is inside the block.      |
| fogR          | int: R Color of the fog while the client's camera is inside the block.  |
| fogG          | int: G Color of the fog while the client's camera is inside the block.  |
| fogB          | int: B Color of the fog while the client's camera is inside the block.  |

## For non-extended blocks, the follow params is used

| Parameter     | Description                                                             |
|---------------|-------------------------------------------------------------------------|
| sidetex       | int: Texture ID for the side of the block.                              |
| shape         | int: 0 - Sprite; 1 -> 16 Height of the block.                           |

## For extended blocks, the following params is used

| Parameter     |      Description                                                       |
|---------------|------------------------------------------------------------------------|
| lefttex       | int: Texture ID for the left side of the block.                        |
| righttex      | int: Texture ID for the right side of the block.                       |
| fronttex      | int: Texture ID for the front of the block.                            |
| backtex       | int: Texture ID for the back of the block.                             |
| minx          | int: Minimum X coordinate in pixels. Values between 0 and 15 allowed.  |
| miny          | int: Minimum Y coordinate in pixels. Values between 0 and 15 allowed.  |
| minz          | int: Minimum Z coordinate in pixels. Values between 0 and 15 allowed.  |
| maxx          | int: Maximum X coordinate in pixels. Values between 0 and 15 allowed.  |
| maxy          | int: Maximum Y coordinate in pixels. Values between 0 and 15 allowed.  |
| maxz          | int: Maximum Z coordinate in pixels. Values between 0 and 15 allowed.  |

## EBlockSolidity

| Name          | Description                                                       |
|---------------|-------------------------------------------------------------------|
| BDSOL_WALK    | No collision(can walk through the block).                         |
| BDSOL_SWIM    | Liquid collision(can swim through the block: water, lava etc.)    |
| BDSOL_SOLID   | Block collision(can walk on the block).                           |

## EBlockSounds

| Name          |
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

| Name               | Description                                         |
|--------------------|-----------------------------------------------------|
| BDDRW_OPAQUE       | Opaque block.                                       |
| BDDRW_TRANSPARENT  | Transparent with face culling of same neighbour.    |
| BDDRW_TRANSPARENT2 | Transparent with no face culling of same neighbour. |
| BDDRW_TRANSLUCENT  | Transparent and shaded by texture (water, ice etc.) |
| BDDRW_GAS          | Fully transparent(air).                             |
