local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

local Window = OrionLib:MakeWindow({Name = "KILL21", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})

local Tab = Window:MakeTab({
	Name = "Игрок",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Игрок"
})

OrionLib:MakeNotification({
	Name = "Привет!",
	Content = "этот скрипт создан kill21",
	Image = "rbxassetid://4483345998",
	Time = 5
})

Tab:AddSlider({
	Name = "Скорость",
	Min = 0,
	Max = 500,
	Default = 16,
	Color = Color3.fromRGB(255,0,0),
	Increment = 1,
	ValueName = "скорость",
	Callback = function(Value)
		game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
	end    
})

Tab:AddSlider({
	Name = "Прыжок",
	Min = 0,
	Max = 500,
	Default = 50,
	Color = Color3.fromRGB(0,0,255),
	Increment = 1,
	ValueName = "прыжок",
	Callback = function(Value)
		game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
	end    
})

local Section = Tab:AddSection({
	Name = "функции"
})

Tab:AddButton({
	Name = "Летать!",
	Callback = function()
        loadstring("\108\111\97\100\115\116\114\105\110\103\40\103\97\109\101\58\72\116\116\112\71\101\116\40\40\39\104\116\116\112\115\58\47\47\103\105\115\116\46\103\105\116\104\117\98\117\115\101\114\99\111\110\116\101\110\116\46\99\111\109\47\109\101\111\122\111\110\101\89\84\47\98\102\48\51\55\100\102\102\57\102\48\97\55\48\48\49\55\51\48\52\100\100\100\54\55\102\100\99\100\51\55\48\47\114\97\119\47\101\49\52\101\55\52\102\52\50\53\98\48\54\48\100\102\53\50\51\51\52\51\99\102\51\48\98\55\56\55\48\55\52\101\98\51\99\53\100\50\47\97\114\99\101\117\115\37\50\53\50\48\120\37\50\53\50\48\102\108\121\37\50\53\50\48\50\37\50\53\50\48\111\98\102\108\117\99\97\116\111\114\39\41\44\116\114\117\101\41\41\40\41\10\10")()
  	end    
})

Tab:AddButton({
	Name = "тп к себе игроков,Выкидавать за карту!",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/sinret/rbxscript.com-scripts-reuploads-/main/univ6", true))()
  	end    
})

Tab:AddButton({
	Name = "Вх",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/TunaOnAir/RobloxScripts/main/ESP_v1.lua"))()
  	end    
})

Tab:AddButton({
	Name = "фри кам",
	Callback = function()
        loadstring(game:HttpGetAsync("https://raw.githubusercontent.com/richie0866/orca/master/public/snapshot.lua"))()
  	end    
})

Tab:AddButton({
	Name = "RTX",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/localyactive/projects/main/other/RTX_OBF"))()
  	end    
})

Tab:AddButton({
	Name = "Synapse X",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/AZYsGithub/Chillz-s-scripts/main/Synapse-X-Remake.lua"))()
  	end    
})

local Tab = Window:MakeTab({
	Name = "Slap Battles",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "Хит боксы",
	Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/Bilmemi/hitbox2/main/op'))()
  	end    
})

Tab:AddButton({
	Name = "ff",
	Callback = function()
        local json = game:HttpGet("https://raw.githubusercontent.com/LeoKholYt/lkhub/main/list.json")
 
function toJson(string)
    local jsonData = nil
    local s, err = pcall(function() 
        local jsonTry = game:GetService("HttpService"):JSONDecode(string)  
        jsonData = jsonTry
    end)   
    return jsonData or false
end
 
json = toJson(json)
local url = json[tostring(game.PlaceId)] or "universal.lua"
url = url.s or url
loadstring(game:HttpGet("https://lkhub.net/s/"..url))()
  	end    
})
