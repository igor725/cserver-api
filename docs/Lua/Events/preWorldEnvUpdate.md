# preWorldEnvUpdate

Fires before updating the world environment.

!!! note
	Returning ``false`` will cancel the environment update.

## Usage

```lua
function preWorldEnvUpdate(World: wlrd, int: updvals, int: updprops, int: updcolors)
	print(string.format("Environment in %s updated (%d, %d, %d)", wrld, updvals, updprops, updcolors))
end
```

### Flags of updated values
| Flag                | Description                                       |
|---------------------|---------------------------------------------------|
| CPE_WMODVAL_COLORS  | The environment colors have been changed.         |
| CPE_WMODVAL_PROPS   | The environment parameters have been changed.     |
| CPE_WMODVAL_TEXPACK | The texture pack of the world have been changed.  |
| CPE_WMODVAL_WEATHER | The weather in the world have been changed.       |

### Flags of changed properties
| Flag                        | Description                            |
|-----------------------------|----------------------------------------|
| CPE_WMODPROP_SIDESID        | World sides block have been changed.   |
| CPE_WMODPROP_EDGEID         | World horizon block have been changed. |
| CPE_WMODPROP_EDGEHEIGHT     | World edge height have been changed.   |
| CPE_WMODPROP_CLOUDSHEIGHT   | Clouds height have been changed.       |
| CPE_WMODPROP_FOGDISTANCE    | Fog distance have been changed.        |
| CPE_WMODPROP_CLOUDSSPEED    | Clouds speed have been changed.        |
| CPE_WMODPROP_WEATHERSPEED   | Weather speed have been changed.       |
| CPE_WMODPROP_WEATHERFADE    | Weather fade have been changed.        |
| CPE_WMODPROP_EXPONENTIALFOG | Exponential fog have been changed.     |
| CPE_WMODPROP_MAPEDGEHEIGHT  | Map edge height have been changed.     |

### Flags of changed colors
| Flag                | Description                            |
|---------------------|----------------------------------------|
| CPE_WMODCOL_SKY     | Sky color have been changed.           |
| CPE_WMODCOL_CLOUD   | Cloud color have been changed.         |
| CPE_WMODCOL_FOG     | Fog color have been changed.           |
| CPE_WMODCOL_AMBIENT | Ambient light color have been changed. |
| CPE_WMODCOL_DIFFUSE | Diffuse light color have been changed. |
| CPE_WMODCOL_SKYBOX  | Skybox color have been changed.        |
