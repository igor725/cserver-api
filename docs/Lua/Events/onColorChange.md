# onColorChange

Fired when an EnvColor in a world changes.

## Usage

```lua
function onColorChange(World: wrld)
    print(string.format("An EnvColor has changed in world %s", wrld:getname()))
end
```
