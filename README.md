-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local Textlabel = Instance.new("TextLabel")
local INFMoney = Instance.new("TextButton")
local FOV200 = Instance.new("TextButton")
local AimbotESP = Instance.new("TextButton")
local DestroyGUI = Instance.new("TextButton")

--Properties:

ScreenGui.Parent = game.Core.Gui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(52, 52, 52)
Frame.Position = UDim2.new(0.614879668, 0, 0.55214721, 0)
Frame.Size = UDim2.new(0, 459, 0, 250)
ScreenGui.Active = true
ScreenGui.Draggable = true

Textlabel.Name = "Textlabel"
Textlabel.Parent = Frame
Textlabel.BackgroundColor3 = Color3.fromRGB(52, 52, 52)
Textlabel.Size = UDim2.new(0, 459, 0, 36)
Textlabel.Font = Enum.Font.SourceSans
Textlabel.Text = "Game is Street ShootOut"
Textlabel.TextColor3 = Color3.fromRGB(0, 0, 0)
Textlabel.TextSize = 14.000

INFMoney.Name = "INF Money"
INFMoney.Parent = Frame
INFMoney.BackgroundColor3 = Color3.fromRGB(255, 128, 106)
INFMoney.BorderColor3 = Color3.fromRGB(255, 172, 151)
INFMoney.Position = UDim2.new(0.015250545, 0, 0.727999985, 0)
INFMoney.Size = UDim2.new(0, 200, 0, 50)
INFMoney.Font = Enum.Font.SourceSans
INFMoney.Text = "INF Money"
INFMoney.TextColor3 = Color3.fromRGB(0, 0, 0)
INFMoney.TextSize = 14.000
INFMoney.MouseButton1Down:connect(function()
	local ohString1 = "GLOCK27"
	local ohString2 = "ExtendedClip"
	local ohNumber3 = -6000000000000

	workspace.GunStore.BuyAndInteract:FireServer(ohString1, ohString2, ohNumber3)
end)


FOV200.Name = "FOV 200"
FOV200.Parent = Frame
FOV200.BackgroundColor3 = Color3.fromRGB(255, 128, 106)
FOV200.BorderColor3 = Color3.fromRGB(255, 172, 151)
FOV200.Position = UDim2.new(0.015250545, 0, 0.472000003, 0)
FOV200.Size = UDim2.new(0, 200, 0, 50)
FOV200.Font = Enum.Font.SourceSans
FOV200.Text = "FOV 200"
FOV200.TextColor3 = Color3.fromRGB(0, 0, 0)
FOV200.TextSize = 14.000
FOV200.MouseButton1Down:connect(function()
	workspace.CurrentCamera.FieldOfView = 200
end)

AimbotESP.Name = "Aimbot ESP"
AimbotESP.Parent = Frame
AimbotESP.BackgroundColor3 = Color3.fromRGB(255, 128, 106)
AimbotESP.BorderColor3 = Color3.fromRGB(255, 172, 151)
AimbotESP.Position = UDim2.new(0.015250545, 0, 0.228, 0)
AimbotESP.Size = UDim2.new(0, 200, 0, 50)
AimbotESP.Font = Enum.Font.SourceSans
AimbotESP.Text = "Aimbot ESP"
AimbotESP.TextColor3 = Color3.fromRGB(0, 0, 0)
AimbotESP.TextSize = 14.000
AimbotESP.MouseButton1Down:connect(function()
	loadstring(game:HttpGet('https://raw.githubusercontent.com/fatesc/fates-esp/main/main.lua'))()
end)

DestroyGUI.Name = "Destroy GUI"
DestroyGUI.Parent = Frame
DestroyGUI.BackgroundColor3 = Color3.fromRGB(132, 70, 51)
DestroyGUI.Position = UDim2.new(0, 358, 0, 0)
DestroyGUI.Size = UDim2.new(0, 101, 0, 30)
DestroyGUI.Font = Enum.Font.SourceSans
DestroyGUI.Text = "Destroy GUI"
DestroyGUI.TextColor3 = Color3.fromRGB(0, 0, 0)
DestroyGUI.TextSize = 14.000
DestroyGUI.MouseButton1Down:connect(function()
	local myPart = script.Parent

	myPart:Destroy()
end)
