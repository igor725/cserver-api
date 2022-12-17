# World

## Available functions

### World_HasError

```c++
cs_bool World_HasError(World *world);
```

### World_PopError

```c++
EWorldError World_PopError(World *world, EWorldExtra *extra);
```

### World_Create

```c++
World *World_Create(cs_str name);
```

### World_AllocBlockArray

```c++
void World_AllocBlockArray(World *world);
```

### World_CleanBlockArray

```c++
cs_bool World_CleanBlockArray(World *world);
```

### World_FreeBlockArray

```c++
void World_FreeBlockArray(World *world);
```

### World_Free

```c++
void World_Free(World *world);
```

### World_Add

```c++
void World_Add(World *world);
```

### World_Remove

```c++
cs_bool World_Remove(World *world);
```

### World_IsReadyToPlay

```c++
cs_bool World_IsReadyToPlay(World *world);
```

### World_IsInMemory

```c++
cs_bool World_IsInMemory(World *world);
```

### World_IsModified

```c++
cs_bool World_IsModified(World *world);
```

### World_FinishEnvUpdate

```c++
cs_bool World_FinishEnvUpdate(World *world);
```

### World_CountPlayers

```c++
cs_byte World_CountPlayers(World *world);
```

### World_Load

```c++
cs_bool World_Load(World *world);
```

### World_Unload

```c++
void World_Unload(World *world);
```

### World_Save

```c++
cs_bool World_Save(World *world);
```

### World_Lock

```c++
cs_bool World_Lock(World *world, cs_ulong timeout);
```

### World_Unlock

```c++
void World_Unlock(World *world);
```

### World_StartTask

```c++
void World_StartTask(World *world);
```

### World_EndTask

```c++
void World_EndTask(World *world);
```

### World_WaitAllTasks

```c++
void World_WaitAllTasks(World *world);
```

### World_SetInMemory

```c++
void World_SetInMemory(World *world, cs_bool state);
```

### World_SetIgnoreModifications

```c++
void World_SetIgnoreModifications(World *world, cs_bool state);
```

### World_SetSpawn

```c++
void World_SetSpawn(World *world, Vec *svec, Ang *sang);
```

### World_SetDimensions

```c++
cs_bool World_SetDimensions(World *world, const SVec *dims);
```

### World_SetBlock

```c++
cs_bool World_SetBlock(World *world, SVec *pos, BlockID id);
```

### World_SetBlockO

```c++
cs_bool World_SetBlockO(World *world, cs_uint32 offset, BlockID id);
```

### World_SetEnvColor

```c++
cs_bool World_SetEnvColor(World *world, EColor type, Color3* color);
```

### World_SetEnvProp

```c++
cs_bool World_SetEnvProp(World *world, EProp prop, cs_int32 value);
```

### World_SetTexturePack

```c++
cs_bool World_SetTexturePack(World *world, cs_str url);
```

### World_SetWeather

```c++
cs_bool World_SetWeather(World *world, EWeather type);
```

### World_SetSeed

```c++
void World_SetSeed(World *world, cs_uint32 seed);
```

### World_GetName

```c++
cs_str World_GetName(World *world);
```

### World_GetSpawn

```c++
void World_GetSpawn(World *world, Vec *svec, Ang *sang);
```

### World_GetData

```c++
void *World_GetData(World *world, cs_uint32 *size);
```

### World_GetBlockArray

```c++
BlockID *World_GetBlockArray(World *world, cs_uint32 *size);
```

### World_GetBlockArraySize

```c++
cs_uint32 World_GetBlockArraySize(World *world);
```

### World_GetOffset

```c++
cs_uint32 World_GetOffset(World *world, SVec *pos);
```

### World_GetDimensions

```c++
void World_GetDimensions(World *world, SVec *dims);
```

### World_GetBlock

```c++
BlockID World_GetBlock(World *world, SVec *pos);
```

### World_GetBlockO

```c++
BlockID World_GetBlockO(World *world, cs_uint32 offset);
```

### World_GetEnvProp

```c++
cs_int32 World_GetEnvProp(World *world, EProp prop);
```

### World_GetEnvColor

```c++
cs_bool World_GetEnvColor(World *world, EColor type, Color3 *dst);
```

### World_GetWeather

```c++
EWeather World_GetWeather(World *world);
```

### World_GetTexturePack

```c++
cs_str World_GetTexturePack(World *world);
```

### World_GetSeed

```c++
cs_uint32 World_GetSeed(World *world);
```

### World_GetByName

```c++
World *World_GetByName(cs_str name);
```
