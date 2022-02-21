
## Documentation RageUI

La documentation n'est pas terminée elle sera souvent à jour hésiter pas à Star le repo pour être au courant des mises à jour

# Exemple de fxmanifest.lua

```lua
fx_version 'adamant'
game 'gta5'

author 'Shazuub'

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

# Menu

```lua
local Menu = RageUI.CreateMenu('Titre', 'Sous Titre')
```

# SubMenu

```lua
local SubMenu = RageUI.CreateSubMenu(Menu, 'Titre', 'Sous Titre')
```

# Bouton

```lua
RageUI.Button("Text", 'Description', {},true, {
    onSelected = function()
    -- function / Trigger
    end
})
```

# CheckBox

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

# List

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

# Separator

```lua
RageUI.Separator('Text')
```

# Slider

```lua
local progressmin = 0
local progressmax = 100

RageUI.Slider('Slider', progressmin, progressmax, nil, 50, {}, true, {})
```

# UISliderHeritage

```lua
local sliderheritage = 1

RageUI.UISliderHeritage('SliderHeritage', sliderheritage, nil, {}, 1)
```

# BoutonPanel

```lua
RageUI.BoutonPanel('Gauche', 'Droite', 1)
```

# StatisticPanel

```lua
RageUI.StatisticPanel(0.5, 'StatisticPanel', 1)
```

# StatisticPanelAdvanced

```lua
RageUI.StatisticPanelAdvanced('StatisticPanelAdvanced', 0.5, nil, 0.5, nil, nil, 1)
```

# Keys Register

```lua
Keys.Register("E", "E", "Exemple", function()
  -- function / Trigger
end)
```
