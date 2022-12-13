# io
The plugin's ``io`` library almost identical to pure Lua [5.1](https://www.lua.org/manual/5.1/manual.html#5.7)/[5.2](https://www.lua.org/manual/5.2/manual.html#6.8)/[5.3](https://www.lua.org/manual/5.3/manual.html#6.8)/[5.4](https://www.lua.org/manual/5.4/manual.html#6.8) implementation.

## Blocked standard implementations

```lua
io.input()
io.output()
io.read()
io.write()
io.stdout
io.stderr
io.stdin
```


## New functions

### boolean: io.ensure

```lua
io.ensure(string: folder)
```

Ensures that the specified folder exists.

### string: io.datafolder()

```lua
io.datafolder()
```

Returns the path to unique data folder for the current script.

### string: io.scrname()

```lua
io.scrname()
```

Returns the current script name.
