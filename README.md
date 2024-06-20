# Bysuskhmer UI Library 

Introducing the Bysuskhmer UI Library, a Roblox Exploit UI Library created just for fun! Feel free to modify it as you wish, and using our library has already helped us a lot! You can check out an example code [here](./Example.lua).

## Getting Started

To begin, you need to declare a variable to access the library.

```lua
local redzlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/REDzHUB/RedzLibV5/main/Source.Lua"))()
```

To load the UI, simply call the function:

```lua
local Window = redzlib:MakeWindow({
  Title = "Bysuskhmer 10.0",
  SubTitle = "by Bysuskhmer",
  SaveFolder = "Bysuskhmer Folder"
})
```

Section Tab UI

```lua
local Section = Tab1:AddSection({"Tab1"})
```
You can create multiple tabs to organize your features.

```lua
local Tab1 = Window:MakeTab({"Local Player", "rbxassetid://17760813932"})
```

**Argument 1: Name of your tab (type: `string`)**

**Argument 2: The Image ID (type: `string`)**

### Button

Create functional buttons with ease!

```lua
local Button = Tab1:AddButton({"Button", function()
  
end})
```

**Argument 1: Name of the Button (type: `string`)**

**Argument 2: Function to execute when the button is clicked (type: `function`)**

### Toggle

Use toggles that can be turned on or off.

```lua
local Toggle1 = Tab1:AddToggle({
  Name = "Toggle",
  Default = false
})

Toggle1:Callback(function(Value)
  
end)
```

**Argument 1: Name (type: `string`)**

**Argument 2: Default toggle state (type: `boolean`)**

**Argument 3: Function to execute (return: `bool`) (type: `function`)**

### Slider

Add sliders, which work well for mobile users too!

```lua
Tab1:AddSlider({
  Name = "Slider",
  Min = 0,
  Max = 700,
  Increase = 1,
  Default = 16,
  Callback = function(value)
    game:GetService("Players").LocalPlayer.Character.Humanoid.WalkSpeed = value
  end
})
```

**Argument 1: Name/Title (type: `string`)**

**Argument 2: Maximum value for the slider (type: `int`)**

**Argument 3: Function to execute (return: int) (type: `function`)**

## Built-in UI Features

We also provide features to toggle the UI, change the theme, and more.

### Dropdown

```lua
local Dropdown = Tab1:AddDropdown({
  Name = "",
  Description = "Select the <font color='rgb(88, 101, 242)'>teleport to</font>",
  Options = {"VIP", "Mega Vip", "User VIP"},
  Default = "VIP",
  Flag = "dropdown teste",
  Callback = function(Value)
    
})
```
