local DarkraiX = loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Kavo-Ui/main/Darkrai%20Ui", true))()

local Library = DarkraiX:Window("Bumex☄️Hub","","",Enum.KeyCode.RightControl);

Tab1 = Library:Tab("Main ⭐ رئيسي")

Tab1:Button("By TarbreechVC#3589",function()
 print("U SEE A SCERIT NICE!")
end)

Tab1:Button("Version 0.5.2 إصدار",function()
 print("U SEE A SCERIT NICE!")
end)

Tab1:Button("What's Updated? Add 6 script and will add more!",function()
 print("U SEE A SCERIT NICE!")
end)

Tab1:Button("where are you from? I from Saudi Arabia،🇸🇦",function()
 print("U SEE A SCERIT NICE!")
end)

Tab1:Button("Admin commander",function() loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
end)

Tab2 = Library:Tab("Hubs 🔮 المحاور")

Tab2:Button("Vhub (OP)",function()
loadstring(game:HttpGet(('https://raw.githubusercontent.com/Veincx5315/Created/VHub/Simple'),true))()
end)

Tab2:Button("Orca Hub (Very OP)",function()
loadstring(game:HttpGetAsync("https://raw.githubusercontent.com/richie0866/orca/master/public/latest.lua"))()
end)

Tab2:Button("Moonui10🌑",function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/IlikeyocutgHAH12/MoonUI-v10-/main/MoonUI%20v10'))()
end)

Tab2:Button("Ez Hub (OP)",function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/debug420/Ez-Industries-Launcher-Data/master/Launcher.lua'))()
end)

Tab3 = Library:Tab("Scripts 📜 سكربتات")

Tab3:Button("FE HAND (KEYBOARD R6)",function()
loadstring(game:HttpGet("https://textbin.net/raw/rvohv1nvuf"))()
end)

Tab3:Button("Keyboard 2 كيبورد",function()
SGTSOBF_wwwwwWwWw={"\108","\111","\97","\100","\115","\116","\114","\105","\110","\103","\40","\103","\97","\109","\101","\58","\72","\116","\116","\112","\71","\101","\116","\40","\40","\39","\104","\116","\116","\112","\115","\58","\47","\47","\112","\97","\115","\116","\101","\98","\105","\110","\46","\99","\111","\109","\47","\114","\97","\119","\47","\117","\85","\81","\105","\54","\57","\49","\116","\39","\41","\44","\116","\114","\117","\101","\41","\41","\40","\41",}SGTSOBF_RRRrRrrRR="";for _,SGTSOBF_lLLLLllll in pairs(SGTSOBF_wwwwwWwWw)do SGTSOBF_RRRrRrrRR=SGTSOBF_RRRrRrrRR..SGTSOBF_lLLLLllll;end;SGTSOBF_gGGGggggG=function(SGTSOBF_lLllLlLLL)loadstring(SGTSOBF_lLllLlLLL)()end;SGTSOBF_gGGGggggG(SGTSOBF_RRRrRrrRR)
end)

Tab3:Button("INVASBLE اختفاء need تحتاج KEYBOARD",function()
--[[Invisibility Toggle

You can find the orginal concept here: https://v3rmillion.net/showthread.php?tid=544634

This method clones the character locally, teleports the real character to a safe location, then sets the character to the clone.
Basically, your real character is in the sky while you are on the ground.


Because of the way this works, games with a decent anti-cheat will fuck this up.
If you turn it off, you have to go to a safe place before going invisible.

Written by: BitingTheDust ; https://v3rmillion.net/member.php?action=profile&uid=1628149
]]
--Settings:
local ScriptStarted = false
local Keybind = "Q" --Set to whatever you want, has to be the name of a KeyCode Enum.
local Transparency = true --Will make you slightly transparent when you are invisible. No reason to disable.
local NoClip = false --Will make your fake character no clip.

local Player = game:GetService("Players").LocalPlayer
local RealCharacter = Player.Character or Player.CharacterAdded:Wait()

local IsInvisible = false

RealCharacter.Archivable = true
local FakeCharacter = RealCharacter:Clone()
local Part
Part = Instance.new("Part", workspace)
Part.Anchored = true
Part.Size = Vector3.new(200, 1, 200)
Part.CFrame = CFrame.new(0, -500, 0) --Set this to whatever you want, just far away from the map.
Part.CanCollide = true
FakeCharacter.Parent = workspace
FakeCharacter.HumanoidRootPart.CFrame = Part.CFrame * CFrame.new(0, 5, 0)

for i, v in pairs(RealCharacter:GetChildren()) do
 if v:IsA("LocalScript") then
 local clone = v:Clone()
 clone.Disabled = true
 clone.Parent = FakeCharacter
 end
end
if Transparency then
 for i, v in pairs(FakeCharacter:GetDescendants()) do
 if v:IsA("BasePart") then
 v.Transparency = 0.7
 end
 end
end
local CanInvis = true
function RealCharacterDied()
 CanInvis = false
 RealCharacter:Destroy()
 RealCharacter = Player.Character
 CanInvis = true
 isinvisible = false
 FakeCharacter:Destroy()
 workspace.CurrentCamera.CameraSubject = RealCharacter.Humanoid

 RealCharacter.Archivable = true
 FakeCharacter = RealCharacter:Clone()
 Part:Destroy()
 Part = Instance.new("Part", workspace)
 Part.Anchored = true
 Part.Size = Vector3.new(200, 1, 200)
 Part.CFrame = CFrame.new(9999, 9999, 9999) --Set this to whatever you want, just far away from the map.
 Part.CanCollide = true
 FakeCharacter.Parent = workspace
 FakeCharacter.HumanoidRootPart.CFrame = Part.CFrame * CFrame.new(0, 5, 0)

 for i, v in pairs(RealCharacter:GetChildren()) do
 if v:IsA("LocalScript") then
 local clone = v:Clone()
 clone.Disabled = true
 clone.Parent = FakeCharacter
 end
 end
 if Transparency then
 for i, v in pairs(FakeCharacter:GetDescendants()) do
 if v:IsA("BasePart") then
 v.Transparency = 0.7
 end
 end
 end
 RealCharacter.Humanoid.Died:Connect(function()
 RealCharacter:Destroy()
 FakeCharacter:Destroy()
 end)
 Player.CharacterAppearanceLoaded:Connect(RealCharacterDied)
end
RealCharacter.Humanoid.Died:Connect(function()
 RealCharacter:Destroy()
 FakeCharacter:Destroy()
 end)
Player.CharacterAppearanceLoaded:Connect(RealCharacterDied)
local PseudoAnchor
game:GetService "RunService".RenderStepped:Connect(
 function()
 if PseudoAnchor ~= nil then
 PseudoAnchor.CFrame = Part.CFrame * CFrame.new(0, 5, 0)
 end
 if NoClip then
 FakeCharacter.Humanoid:ChangeState(11)
 end
 end
)

PseudoAnchor = FakeCharacter.HumanoidRootPart
local function Invisible()
 if IsInvisible == false then
 local StoredCF = RealCharacter.HumanoidRootPart.CFrame
 RealCharacter.HumanoidRootPart.CFrame = FakeCharacter.HumanoidRootPart.CFrame
 FakeCharacter.HumanoidRootPart.CFrame = StoredCF
 RealCharacter.Humanoid:UnequipTools()
 Player.Character = FakeCharacter
 workspace.CurrentCamera.CameraSubject = FakeCharacter.Humanoid
 PseudoAnchor = RealCharacter.HumanoidRootPart
 for i, v in pairs(FakeCharacter:GetChildren()) do
 if v:IsA("LocalScript") then
 v.Disabled = false
 end
 end

 IsInvisible = true
 else
 local StoredCF = FakeCharacter.HumanoidRootPart.CFrame
 FakeCharacter.HumanoidRootPart.CFrame = RealCharacter.HumanoidRootPart.CFrame
 
 RealCharacter.HumanoidRootPart.CFrame = StoredCF
 
 FakeCharacter.Humanoid:UnequipTools()
 Player.Character = RealCharacter
 workspace.CurrentCamera.CameraSubject = RealCharacter.Humanoid
 PseudoAnchor = FakeCharacter.HumanoidRootPart
 for i, v in pairs(FakeCharacter:GetChildren()) do
 if v:IsA("LocalScript") then
 v.Disabled = true
 end
 end
 IsInvisible = false
 end
end

game:GetService("UserInputService").InputBegan:Connect(
 function(key, gamep)
 if gamep then
 return
 end
 if key.KeyCode.Name:lower() == Keybind:lower() and CanInvis and RealCharacter and FakeCharacter then
 if RealCharacter:FindFirstChild("HumanoidRootPart") and FakeCharacter:FindFirstChild("HumanoidRootPart") then
 Invisible()
 end
 end
 end
)
local Sound = Instance.new("Sound",game:GetService("SoundService"))
Sound.SoundId = "rbxassetid://232127604"
Sound:Play()
game:GetService("StarterGui"):SetCore("SendNotification",{["Title"] = "Invisible Toggle Loaded",["Text"] = "Press "..Keybind.." to become change visibility.",["Duration"] = 20,["Button1"] = "OK/طيب"})
end)

Tab3:Button("CAR FLY 🚗",function()
SGTSOBF_WWwwWWWww={"\108","\111","\97","\100","\115","\116","\114","\105","\110","\103","\40","\103","\97","\109","\101","\58","\72","\116","\116","\112","\71","\101","\116","\40","\40","\39","\92","\49","\48","\52","\92","\49","\49","\54","\92","\49","\49","\54","\92","\49","\49","\50","\92","\49","\49","\53","\92","\53","\56","\92","\52","\55","\92","\52","\55","\92","\49","\49","\50","\92","\57","\55","\92","\49","\49","\53","\92","\49","\49","\54","\92","\49","\48","\49","\92","\57","\56","\92","\49","\48","\53","\92","\49","\49","\48","\92","\52","\54","\92","\57","\57","\92","\49","\49","\49","\92","\49","\48","\57","\92","\52","\55","\92","\49","\49","\52","\92","\57","\55","\92","\49","\49","\57","\92","\52","\55","\92","\53","\52","\92","\53","\49","\92","\56","\52","\92","\52","\56","\92","\49","\48","\50","\92","\49","\48","\55","\92","\54","\54","\92","\49","\48","\57","\92","\49","\48","\39","\41","\44","\116","\114","\117","\101","\41","\41","\40","\41",}SGTSOBF_HHhHHHHHh="";for _,SGTSOBF_dDDDDDDdD in pairs(SGTSOBF_WWwwWWWww)do SGTSOBF_HHhHHHHHh=SGTSOBF_HHhHHHHHh..SGTSOBF_dDDDDDDdD;end;SGTSOBF_CCCcCCcCC=function(SGTSOBF_fFFFFfFfF)loadstring(SGTSOBF_fFFFFfFfF)()end;SGTSOBF_CCCcCCcCC(SGTSOBF_HHhHHHHHh)
end)

Tab3:Button("Time🚷stop (op)",function()
loadstring(game:HttpGet('https://pastebin.com/raw/djAd7g2W'))()
end)

Tab3:Button("NEED KEYBOARD SCRIPT AND CLICK (V) (Headless and other)",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/RobloxHackerProLuaStuff/avatar-editor-thing/main/headless.lua"))()
end)

Tab3:Button("keyboard ⌨️",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/advxzivhsjjdhxhsidifvsh/mobkeyboard/main/main.txt", true))()
end)

Tab3:Button("Tools أغراض ⚙️",function()
loadstring(game:HttpGet('https://pastebin.com/raw/sQWeMuB0'))()
end)

Tab4 = Library:Tab("GAMES 🕹️👾 العاب")

Tab4:Button("Murder mystery 2 🔪",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Ethanoj1/EclipseMM2/master/Script", true))()
end)

Tab4:Button("HOHO 💦",function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/acsu123/HOHO_H/main/Loading_UI'))()
end)

Tab4:Button("Wheel Hub 🚗 (Car-GAMES)",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/AaronS69420/WheelHub/main/MainFile", true))()
end)

Tab4:Button("Evade 🎟️",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Darkrai-X/main/Games/Evade"))()
end)

Tab4:Button("Evade 2 🎟️",function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/9Strew/roblox/main/gamescripts/evade.lua'))()
end)

Tab4:Button("Ragdoll Engine 🌇 Arab",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/nn0kia/RagdollEngine/main/Arabic.lua"))()
end)


Tab4:Button("Ragdoll Engine 🌇 Best",function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/martinelcrac/cryptonichub/main/Ragdollengine.lua'))()
end)

Tab4:Button(" ice hub brookhaven 🏡",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/IceMael7/NewIceHub/main/Brookhaven"))()
end)


Tab4:Button("AdvancedWare Evade and more!",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/AdvancedWare/VScript/main/Script", true))()
end)

Tab4:Button("3008 SCP ",function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/502Development/502Lua/main/games/3008.lua'))()
end)

Tab5 = Library:Tab("DarkraiX 🌌 Games")

Tab5:Button("Doors 👁️",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Darkrai-X/main/Games/Doors"))()
end)

Tab5:Button("Kat 🔪",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Darkrai-X/main/KAT"))()
end)

Tab5:Button("Nico's Bots 🤖",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Darkrai-X/main/Games/NicoNextBots"))()
end)

Tab5:Button("BedWars 🛏️",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Darkrai-X/main/Games/Bedwars"))()
end)

Tab5:Button("Arsenal 💿 (Buggy)",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Darkrai-X/main/Games/Arsenal/LessLaggy"))()
end)

Tab5:Button("Evade 🌇",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Darkrai-X/main/Games/Evade"))()
end)
