# CPE

## Доступные функции

### CPE_IsModelDefined

```c++
cs_bool CPE_IsModelDefined(cs_byte id);
```

### CPE_IsModelDefinedPtr

```c++
cs_bool CPE_IsModelDefinedPtr(CPEModel *model);
```

### CPE_GetDefaultModelName

```c++
cs_str CPE_GetDefaultModelName(void);
```

### CPE_DefineModel

```c++
cs_bool CPE_DefineModel(cs_byte id, CPEModel *model);
```

### CPE_UndefineModel

```c++
cs_bool CPE_UndefineModel(cs_byte id);
```

### CPE_UndefineModelPtr

```c++
cs_bool CPE_UndefineModelPtr(CPEModel *mdl);
```

### CPE_CheckModel

```c++
cs_bool CPE_CheckModel(Client *client, cs_int16 model);
```

### CPE_GetModelNum

```c++
cs_int16 CPE_GetModelNum(cs_str model);
```

### CPE_GetModelStr

```c++
cs_uint32 CPE_GetModelStr(cs_int16 num, cs_char *buffer, cs_uint32 buflen);
```


### CPE_IsParticleDefined

```c++
cs_bool CPE_IsParticleDefined(cs_byte id);
```

### CPE_IsParticleDefinedPtr

```c++
cs_bool CPE_IsParticleDefinedPtr(CPEParticle *part);
```

### CPE_DefineParticle

```c++
cs_bool CPE_DefineParticle(cs_byte id, CPEParticle *part);
```

### CPE_UndefineParticle

```c++
cs_bool CPE_UndefineParticle(cs_byte id);
```

### CPE_UndefineParticlePtr

```c++
cs_bool CPE_UndefineParticlePtr(CPEParticle *ptr);
```


### Cuboid_SetPositions

```c++
void Cuboid_SetPositions(CPECuboid *cub, SVec start, SVec end);
```

### Cuboid_SetColor

```c++
void Cuboid_SetColor(CPECuboid *cub, Color4 color);
```

### Cuboid_GetID

```c++
cs_byte Cuboid_GetID(CPECuboid *cub);
```

### Cuboid_GetSize

```c++
cs_uint32 Cuboid_GetSize(CPECuboid *cub);
```

### Cuboid_GetPositions

```c++
void Cuboid_GetPositions(CPECuboid *cub, SVec *start, SVec *end);
```

