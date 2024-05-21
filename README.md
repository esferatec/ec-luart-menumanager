# ec-luart-MenuManager

The project is a menu management module written in Lua. It defines a MenuManager object that contains methods for managing menus in LuaRT desktop applications.

[![LuaRT 1.8.0](https://badgen.net/badge/LuaRT/1.8.0/blue)](https://github.com/samyeyo/LuaRT)

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

The code above initializes a new instance of the menu manager object. It returns the newly created object.

## Method - add

```Lua
MenuManager:add(menu: object, name: string) -> none
```

This function adds a menu to the MenuManager object. It takes an object menu and a string name as parameters. It first checks if the menu is a valid child menu using the isValidChild function. If it is not a valid child menu or the name is not a string, the function returns early. Otherwise, it adds the menu to the children table using the name as the key.

## Method - uncheck

```Lua
MenuManager:uncheck() -> none
```

The method iterates through child menus and unchecks them if they were previously checked. The function structure includes a loop to iterate over each child menu and a conditional check to determine if the menu is checked.

## Method - disable

```Lua
MenuManager:disable() -> none
```

This method is responsible for disabling all child menus. It achieves this by iterating over each child menu and setting its enabled property to false.

## Method - enable

```Lua
MenuManager:enable() -> none
```

This method, on the other hand, enables all child menus. It follows a similar approach as the disable method, but instead sets the enabled property to true.

## License

Copyright (c) 2023 by esferatec.
It is open source, released under the MIT License.
See full copyright notice in the LICENSE.md file.
