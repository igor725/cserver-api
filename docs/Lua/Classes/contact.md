# Contact

### any: contact:pop

```lua
contact:pop()
```

Returns the last value from the contact's local queue.

### contact:push

```lua
contact:push(any: value)
```

Pushes new value to the contact's global queue.

### contact:bind

```lua
contact:bind(function: func)
```

Binds a callback function to the contact object. The callback function will be called when the local queue is updated (received a new value).

### int: contact:avail

```lua
contact:avail()
```

Returns number of available values in the contact's local queue.

### contact:clear

```lua
contact:clear()
```

Clears the contact's local queue.

### contact:close

```lua
contact:close()
```

Closes connection to the contact.
