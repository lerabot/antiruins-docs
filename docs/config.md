## CONFIGURE

```lua
-- config.lua holds some configuration for the engine
-- the most important is which game to load by default.

local config = {
    games = {
        {dir="game_example", name="Example"},
        {dir="game_tower",   name="Tower"},
    },
    -- Default game to load
    defaultGame = "Example",

		-- console output - disable this is you get slowdowns using BBA or Serial.
		contole = true,

    -- Path for lackages, libraries. The require function.
    -- Don't forget to add a semicolom at the end. ' ; '
    reqPath = "lua/?.lua;" .. "lua/lib/?.lua;",
}
return config