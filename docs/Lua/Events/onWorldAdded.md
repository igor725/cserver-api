# onWorldAdded

Fired when a world gets added to the world list.

## Usage

```lua
function onWorldAdded(World: wrld)
    print(string.format("A new world has been added: %s", wrld:getname()))
end
```
