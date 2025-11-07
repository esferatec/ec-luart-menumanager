# ec-luart-menumanager

The project is a menu management module written in Lua. It defines a MenuManager object that contains methods for managing menus in LuaRT desktop applications.

[![LuaRT 2.1.0](https://badgen.net/badge/LuaRT/2.1.0/blue)](https://github.com/samyeyo/LuaRT)

## Features

The project provides a modular and flexible way to manage menus in desktop applications. It allows you to add, uncheck, disable and enable child menus. Several menu managers can be used in one application.

## Installation

1. Create a folder called "ecluart" in your application.
2. Copy the "mm.lua" file into this folder.

```text
[application]
|
|----ecluart
|   |
|   |----mm.lua
|   |----...
|
|----app.wlua
```

## Usage

The menu manager (mm) can be loaded using the function *require()*:

```lua
local mm = require("ecluart.mm") 
```

## Constructor

```Lua
MenuManager() -> object
```

Initializes a new menu manager instance.

## Method - add

```Lua
MenuManager:add(menu: object, name: string) -> none
```

Adds a menu object and name.

## Method - uncheck

```Lua
MenuManager:uncheck() -> none
```

 Unchecks all child menus.

## Method - disable

```Lua
MenuManager:disable() -> none
```

Disables all child menus.

## Method - enable

```Lua
MenuManager:enable() -> none
```

Enables all child menus.

## License

Copyright (c) 2023 by esferatec.
It is open source, released under the MIT License.
See full copyright notice in the LICENSE.md file.
