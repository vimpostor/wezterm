# `wezterm.color.get_default_colors()`

*Since: nightly builds only*

Returns the set of colors that would be used by default.

This is useful if you want to reference those colors in a color scheme
definition.

This contrived example sets up two color schemes and overrides their background
colors to red.  One of the schemes is the default set of colors, while the
other is one of the many built-in schemes:

```lua
local wezterm = require 'wezterm'

local gruvbox = wezterm.color.get_builtin_schemes()["Gruvbox Light"]
gruvbox.background = "red"

local my_default = wezterm.color.get_default_colors()
my_default.background = "red"

return {
  color_schemes = {
    ["My Gruvbox"] = my_gruvbox,
    ["My Default"] = my_default,
  },
  color_scheme = "My Gruvbox",
}
```
