## window:tabs_with_info()

*Since: nightly builds only*

Returns an array table holding an extended info entry for each of the tabs
contained within this window.

Each element is a lua table with the following fields:

* `index` - the 0-based tab index
* `is_active` - a boolean indicating whether this is the active tab within the window
* `tab` - the [MuxTab](../MuxTab.md) object

