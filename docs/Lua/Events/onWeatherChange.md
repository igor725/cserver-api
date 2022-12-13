# onWeatherChange

Fired when the weather in a world changes.

## Usage

```lua
function onWeatherChange(World: wrld)
    local weather_types = {
        [0] = "Sun",
        [1] = "Rain",
        [2] = "Snow"
    }
    print(string.format("Weather has changed in world %s to %s", wrld:getname(), weather_types[wrld:getweather()]))
end
```
