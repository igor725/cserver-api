# Config

## Functions

### config:get

```lua
config:get(string: configKey)
```

Returns the value of the given configKey.

### config:set

```lua
config:set(string: configKey, value: configValue)
```

Sets the given config key to the given value.

### boolean: config:load

```lua
config:load()
```

Returns whether or not the config loaded successfully.

### boolean: config:save

```lua
config:save(boolean: force)
```

Returns whether or not the config saved successfully. If ``force`` is true, it forces the save, even if its the same as the default config.

If it returns false, ``config:poperror()`` will tell you what went wrong.

### ECError, ECExtra: config:poperror

```lua
config.error(configObj:poperror())
```

``config:poperror()`` will return information about what went wrong with the last config operation.

``config.error()`` will return string representation of these codes.


## Examples

```lua
function onStart()
	mycfg = config.new {
		name = 'mycfg.cfg',
		items = {
			{
				name = 'my-key-int',
				type = CONFIG_TYPE_INT,
				comment = 'Signed int key',
				default = -1
			},
			{
				name = 'my-key-str',
				type = CONFIG_TYPE_STR,
				default = 'Wtf is that string?'
			},
			{
				name = 'my-key-bool',
				type = CONFIG_TYPE_BOOL,
				comment = 'No way it\'s a boolean!',
				default = true
			}
		}
	}

	mycfg:save(not mycfg:load())
	print('Config string:', mycfg:get('my-key-str'))
	print('Config boolean:', mycfg:get('my-key-bool'))
	print('Config short:', mycfg:get('my-key-i16'))
end
```

![Screenshot](/resources/mycfg.png)
