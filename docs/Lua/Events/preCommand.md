# preCommand

Fires before executing server's command created by this script.

!!! note
	Returning ``false`` will cancel the command execution and send a "Access denied" message.

## Usage

```lua
function preCommand(string: cmd, Client: caller, string: args, boolean: allowed)
	print(string.format("%s executed by %s with args %q", cmd, caller and caller:getname() or "console", args))
	return true
end
```
