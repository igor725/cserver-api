# world
Allows you to interact with the worlds.

## Functions

### World: world.create

```lua 
world.create(string: worldName, Short Vector: worldDimensions)
```

Creates a new world.

### World: world.getbyname

```lua 
world.getbyname(string: worldName)
```

Returns a World object by its name.

### world.iterall

```lua
World.iterall(func: ITERATE_FUNCTION(World: worldObj))
```

Iterates through all worlds, passing them to ``ITERATE_FUNCTION()``.

### World: world.getmain

```lua
world.getmain()
```

Returns the current world that set as main.

### world.setmain

```lua
world.setmain(World: world)
```

Sets the specified world as main.
