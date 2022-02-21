
## Documentation RageUI

Exemple de fxmanifest.lua

```lua
fx_version 'adamant'
game 'gta5'

author 'RageUI Exemple'

client_scripts {
 "RageUI/RMenu.lua",
 "RageUI/menu/RageUI.lua",
 "RageUI/menu/Menu.lua",
 "RageUI/menu/MenuController.lua",
 "RageUI/components/*.lua",
 "RageUI/menu/elements/*.lua",
 "RageUI/menu/items/*.lua",
 "RageUI/menu/panels/*.lua",
 "RageUI/menu/windows/*.lua",
}
```

Menu

```lua
local Menu = RageUI.CreateMenu('Titre', 'Sous Titre')
```

SubMenu

```lua
local SubMenu = RageUI.CreateSubMenu(Menu, 'Titre', 'Sous Titre')
```

Bouton

```lua
RageUI.Button("Text", 'Description', {},true, {
    onSelected = function()
      print('Bouton')
    end
})
```

CheckBox

```lua
local checkbox = false

RageUI.Checkbox("Checkbox", nil, checkbox, {}, {
    onChecked = function()
        checkbox = true
    end,
    onUnChecked = function()
        checkbox = false
    end,
    onSelected = function(index)
        checkbox = index
    end
})
```

List

```lua
local list = 1

RageUI.List("List",{"1","2"},list,nil,{},true,{
    onListChange = function(Index)
        list = Index
    end,
    onSelected = function(index)
        print(index)
    end
})
```

Separator

```lua
RageUI.Separator('Text')
```

Keys Register

```lua
Keys.Register("E", "E", "Exemple", function()
  -- function / Trigger
end)
```
