# Bysuskhmer UI Library 

Introducing the Bysuskhmer UI Library, a Roblox Exploit UI Library created just for fun! Feel free to modify it as you wish, and using our library has already helped us a lot! You can check out an example code [here](./Example.lua).

## Getting Started

To begin, you need to declare a variable to access the library.

```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Vcsk/UI-Library/main/Source/MyUILib(Unamed).lua"))();
```

To load the UI, simply call the function:

```lua
local Window = Library:Create("Titler")
```
You can create multiple tabs to organize your features.

```lua
local HTab = Window:Tab("Tab","rbxassetid://10888331510")
```

**Argument 1: Name of your tab (type: `string`)**

**Argument 2: The Image ID (type: `string`)**

### Button

Create functional buttons with ease!

```lua
Tab:Button("Button!", function()
    
end)
```

**Argument 1: Name of the Button (type: `string`)**

**Argument 3: Function to execute when the button is clicked (type: `function`)**

### Toggle

Use toggles that can be turned on or off.

```lua
Tab:Toggle("Toggle", function(state)
    
end)
```

**Argument 1: Name (type: `string`)**

**Argument 3: Default toggle state (type: `boolean`)**

**Argument 4: Function to execute (return: `bool`) (type: `function`)**

### Input Text

Get input text from the user.

```lua
Tab:TextBox("TextBox", function(value)
    
end)

```

**Argument 1: Name/Title (type: `string`)**

**Argument 3: Function to execute (type: `function`)**

### Keybind

Get user input when the keybind button is clicked.

```lua
Tab:Keybind("Keybind", Enum.KeyCode.F, function()

end)
```

**Argument 1: Name/Title (type: `string`)**

**Argument 3: Function to execute (return: input) (type: `function`)**

### Slider

Add sliders, which work well for mobile users too!

```lua
Tab:Slider("Slider", 0,120, function(v)
     
end)
```

**Argument 1: Name/Title (type: `string`)**

**Argument 3: Maximum value for the slider (type: `int`)**

**Argument 5: Function to execute (return: int) (type: `function`)**

## Built-in UI Features

We also provide features to toggle the UI, change the theme, and more.

### Toggle UI

To toggle the UI, use the following:

```lua
local ToggleGui = Instance.new("ScreenGui")
local Toggle = Instance.new("TextButton")

ToggleGui.Name = "ToggleGui_HE"
ToggleGui.Parent = game.CoreGui

Toggle.Name = "Toggle"
Toggle.Parent = ToggleGui
Toggle.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
Toggle.BackgroundTransparency = 0.660
Toggle.Position = UDim2.new(0, 0, 0.454706937, 0)
Toggle.Size = UDim2.new(0.0650164187, 0, 0.0888099447, 0)
Toggle.Font = Enum.Font.SourceSans
Toggle.Text = "Toggle"
Toggle.TextScaled = true
Toggle.TextColor3 = Color3.fromRGB(40, 40, 40)
Toggle.TextSize = 24.000
Toggle.TextXAlignment = Enum.TextXAlignment.Left
Toggle.Active = true
Toggle.Draggable = true
Toggle.MouseButton1Click:connect(function()
    Library:ToggleUI()
end)
```
