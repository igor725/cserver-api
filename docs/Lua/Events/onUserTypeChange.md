# onUserTypeChange

Fired when a user's type changes.

!!! note
    Used when a player gets opped or deopped.

## Usage

```lua
function onUserTypeChange(Client: cl)
    cl:chat(string.format("Your user type has changed OP: %s", cl:isop()))
end
```
