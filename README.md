local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
    Name = "[🏝️ Summer UPD + Event] Anime Fighters Simulator",
    LoadingTitle = "[🏝️ Summer UPD + Event] Anime Fighters Simulator",
    LoadingSubtitle = "by Arik",
    ConfigurationSaving = {
       Enabled = true,
       FolderName = nil, -- Create a custom folder for your hub/game
       FileName = "Big Hub"
    },
    Discord = {
       Enabled = true,
       Invite = "https://discord.gg/K7AY6egK", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
       RememberJoins = true -- Set this to false to make them join the discord every time they load it up
    },
    KeySystem = true, -- Set this to true to use our key system
    KeySettings = {
       Title = "Silver Hub",
       Subtitle = "Key System",
       Note = "Get Key On Sever Silver Hub  Discord : VJKVXsNZ",
       FileName = "Key", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
       SaveKey = false, -- The user's key will be saved, but if you change the key, they will be unable to use your script
       GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
       Key = {"Silver"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
    }
 })


 --Tab
 local MainTab = Window:CreateTab("Main", 4483362458) -- Title, Image

 local FramTab = Window:CreateTab("Fram", 4483362458) -- Title, Image

 local EggTab = Window:CreateTab("Start", 4483362458) -- Title, Image

 local TrialTab = Window:CreateTab("Trial", 4483362458) -- Title, Image

 local RaidTab = Window:CreateTab("Raid", 4483362458) -- Title, Image

 local Defendab = Window:CreateTab("Defense Tower", 4483362458) -- Title, Image

 local PassiveTab = Window:CreateTab("Reroll Passive", 4483362458) -- Title, Image

 local PlayerTab = Window:CreateTab("Local Player", 4483362458) -- Title, Image
 local Section = PlayerTab:CreateSection("Movement")
 local Slider = PlayerTab:CreateSlider({
   Name = "WalkSpeed",
   Range = {16, 500},
   Increment = 10,
   Suffix = "WS",
   CurrentValue = 10,
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
      game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
   -- The function that takes place when the slider changes
   -- The variable (Value) is a number which correlates to the value the slider is currently at
   end,
})
local Slider = PlayerTab:CreateSlider({
   Name = "JumpPower",
   Range = {16, 500},
   Increment = 10,
   Suffix = "JP",
   CurrentValue = 10,
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
      game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
   -- The function that takes place when the slider changes
   -- The variable (Value) is a number which correlates to the value the slider is currently at
   end,
})

 local OtherTab = Window:CreateTab("Others", 4483362458) -- Title, Image

 local Discord = Window:CreateTab("Discord", 4483362458) -- Title, Image
