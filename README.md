# Lithium
Lithium Commands: A Server-Sided ROBLOX Command Handler meant for Game Developers!
#### Warning: Lithium is currently in BETA, this means this won't be the final version.

## What is Lithium?
Lithium is basically just a very lightweight, simplistic Adminstration Utility for ROBLOX game developers, it's super easy to use and probably one of the best Admin Tools out.
It also has a awesome advantage and it's mostly Server Sided, it's highly secure and makes it great for ROBLOX game developers who doesn't want ROBLOX Exploiters "exploiting" their Functions and Commands!


## How to use Lithium
These are .rbxm files, these are "model files" for ROBLOX and they can be imported by using the "Insert from File" feature in ROBLOX,
Files like these will need to be imported by hand.

To import these 2 files ("Server Script Service.rbxm" & "Replicated Storage.rbxm") go download these 2 files, then right click on `ServerScriptService` on ROBLOX studio to Import one of the .RBXM files, the file that you'd be importing in `ServerScriptService` is "Server Script Service.rbxm"


The other file called "Replicated Storage.rbxm" will be imported into `ReplicatedStorage`


## How to add commands?
1. To add a Command go to ServerScriptService > Lithium Server Script > LithiumData > Commands
2. You will need to make a new table sort of like this:
```lua
return {
    Example1 = {
        ["Title"] = "",
	["Description"] = "",
	["Usage"] = "",
	["CommandInvoked"] = (function(...)
            -- Command Inputted Here
	end)
    }
}
```

> Title: Is the title of your Command.
> Description: Is the description of your Command.
> Usage: Shows the usage of the Command, (Note: you can keep this empty)
> CommandInvoked: This is what will be invoked when your command is called by the Interface.

#### WARNING: With `CommandInvoked`, be aware that all arguments are passed as strings, this may soon change though as there is possible methods via Functions that exist.


## Example Commands (Default Example)
```lua
-- Commands Module @ Lithium Commands - (C) 2023

return {
	Example1 = {
		["Title"] = "Example1",
		["Description"] = "Id sit quas et ut sunt sapiente nobis. Sint aut quibusdam sed quisquam excepturi et. Autem modi quisquam fugiat.",
		["Usage"] = "<username> <bool> <int>",
		
		["CommandInvoked"] = (function(username, bool, int)
			print(tostring(username), tostring(bool), tostring(int))
		end)
	},
	Example2 = {
		["Title"] = "Example2",
		["Description"] = "Id sit quas et ut sunt sapiente nobis. Sint aut quibusdam sed quisquam excepturi et. Autem modi quisquam fugiat.",
		["Usage"] = "None",

		["CommandInvoked"] = (function()
			print("Called Example 2 via Client to Server")
		end)
	},
	Example3 = {
		["Title"] = "Example3",
		["Description"] = "Id sit quas et ut sunt sapiente nobis. Sint aut quibusdam sed quisquam excepturi et. Autem modi quisquam fugiat.",
		["Usage"] = "<bool>",

		["CommandInvoked"] = (function(bool)
			if (bool == "true") then
				print("Called Example 3 via Client to Server but it's a Bool = true")
			else
				print("Called Example 3 via Client to Server but it's a Bool = false")
			end
		end)
	}
}
```


## Discord/Guilded Webhook Support!
### WARNING: This is a beta feature, we are looking to prevent spamming! If you know how to do this please make a Pull Request, we're trying to make a better method to this!

## FAQ
<h3>Question: <span>How to use a Command?</span></h3>
<h3>Answer: <span>Please refer to the above text :)</span></h3>


<h3>Question: <span>How to use a Discord/Guilded Webhook for ROBLOX?</span></h3>
<h3>Answer: <span>Please refer to the above text (x2)</span></h3>


<h3>Question: <span>Do you have a Discord Server?</span></h3>
<h3>Answer: <span>Not yet, in the future there soon will be one for Lithium and it's other Projects</span></h3>
