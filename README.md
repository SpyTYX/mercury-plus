[![discord server](https://cdn.discordapp.com/attachments/1063180819952324719/1069684390172577843/image.png)](https://discord.gg/jaunk8nhN5)


# Mercury+
This project is just [Mercury UI](https://github.com/deeeity/mercury-lib) but better with more themes, more settings and more customization.

I have not created this UI, or developed it. All UI credits goes to [Mercury UI](https://github.com/deeeity/mercury-lib)'s Developers.
***Release 1.0.5**



## Features
- Customizable Themes
- Browser-like Navigation
- Buttons
- Sliders
- TextBoxes
- Dropdowns
- Toggles
- Inputs
- Keybinds
- Color Picker
- Notifications
- Prompts
- **And more.**

## Credits

***MercuryUI Credits***
  - Deity (Deeeity)
  - Abstract

***MercuryPlus Credits***
  - Mnxtri (aka Moons)
  
## Documentation

### **Get MercuryPlus Library**
```lua
local MercuryPlus = loadstring(game:HttpGet("https://raw.githubusercontent.com/SpyTYX/mercury-plus/main/mercury-plus.lua"))()
```

### **Create a Window**
```lua
local Window = MercuryPlus:Create{
  Theme = MercuryPlus.Themes.Dark,
}
```

### **Create Tabs**
```lua
local Tab = Window:Tab{
	Name = 'New Tab',
	Icon = 'rbxassetid://8569322835'
}
```

### **Buttons**
```lua
Tab:Button{
	Name = 'Button',
	Description = 'Description',
	Callback = function() 
    print('Pressed')
  end
}
```

### **Toggles**
```lua
Tab:Toggle{
  Name = 'Toggle',
  Description = 'Description',
  Callback = function(state)
    print(state)
  end
}
```

### **Textboxes**
```lua
Tab:TextBox{
  Name = 'TextBox',
  Callback = function(state)
    print(state)
  end
}
```

### **Dropdowns**
```lua
local Dropdown = Tab:Dropdown{
	Name = 'Dropdown',
	StartingText = 'Select Item',
	Description = 'Description',
	Items = {
		{"Item 1", 1}, -- Display Name of Item, Value
		12,	-- Only value which is automatically taken by name
		{"Test", "bump the thread pls"} -- Display Name of Item and String Value
	},
	Callback = function(Items) 
    print(Items)
  end
}

Dropdown:AddItems({
  {"New Item", 69},
  420
})

Dropdown:RemoveItems({
	"NewItem", "Hello" --Names to get Removed (Uppercase/Lowercase ignored)
})

Dropdown:Clear()
```

### **Sliders**
```lua
Tab:Slider{
  Name = 'Slider',
  Default = 50,
  Min = 0,
  Max = 100,
  Callback = function(state)
    print(state)
  end
}
```

### **Keybinds**
```lua
Tab:Keybind{
  Name = 'Keybind',
  Description = 'Description',
  Keybind = nil,
}
```

### **Prompts**
```lua
Window:Prompt{
	Followup = false,
	Title = 'Mercury+',
	Text = "mercury but better",
	Buttons = {
		ok = function()
			print('yey')
		end,
		no = function()
			print('GRRR')
		end
	}
}
```

### **Notifications**
```lua
Window:Notification{
	Title = 'Notification',
	Text = "MercuryPlus pog",
	Duration = 3,
	Callback = function() 
    -- yes
  end
}
```

### **Color Picker**
```lua
Tab:ColorPicker{
	Style = MercuryPlus.ColorPickerStyles.Legacy, -- Modes: Legacy, Modern
	Callback = function(color) 
    print(color)
  end
}
```
### **Credits**
```lua
Window:Credit{
	Name = 'Credit',
	Description = 'Description',
	V3rm = 'link/name',
	Discord = 'test#0000'
}
```

**WHILE CALLING LIBRARY FUNCTIONS UPPERCASE/LOWERCASE CHARACTERS DOES NOT MATTER**
