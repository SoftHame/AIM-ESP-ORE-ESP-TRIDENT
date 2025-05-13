local ScreenGui = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local MainImageLabel = Instance.new("ImageLabel")
local UICorner = Instance.new("UICorner")
local OreEspButton = Instance.new("TextButton")
local UICorner_2 = Instance.new("UICorner")
local ESPButton = Instance.new("TextButton")
local UICorner_3 = Instance.new("UICorner")
local AimButton = Instance.new("TextButton")
local UICorner_4 = Instance.new("UICorner")
local UICorner_5 = Instance.new("UICorner")
local MainButton = Instance.new("TextButton")
local ImageLabel = Instance.new("ImageLabel")
local UICorner_6 = Instance.new("UICorner")
local TextLabel = Instance.new("TextLabel")
local UICorner_7 = Instance.new("UICorner")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

MainFrame.Name = "MainFrame"
MainFrame.Parent = ScreenGui
MainFrame.BackgroundColor3 = Color3.fromRGB(93, 92, 92)
MainFrame.BorderColor3 = Color3.fromRGB(0, 0, 0)
MainFrame.BorderSizePixel = 0
MainFrame.Position = UDim2.new(0.380230874, 0, 0.329297811, 0)
MainFrame.Size = UDim2.new(0, 282, 0, 214)
MainFrame.Visible = false

MainImageLabel.Name = "MainImageLabel"
MainImageLabel.Parent = MainFrame
MainImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
MainImageLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
MainImageLabel.BorderSizePixel = 0
MainImageLabel.Size = UDim2.new(0, 282, 0, 214)
MainImageLabel.Image = "http://www.roblox.com/asset/?id=13639732367"

UICorner.CornerRadius = UDim.new(0, 7)
UICorner.Parent = MainImageLabel

OreEspButton.Name = "OreEspButton"
OreEspButton.Parent = MainFrame
OreEspButton.BackgroundColor3 = Color3.fromRGB(84, 84, 84)
OreEspButton.BackgroundTransparency = 0.500
OreEspButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
OreEspButton.BorderSizePixel = 0
OreEspButton.Position = UDim2.new(0.0283687934, 0, 0.0607476644, 0)
OreEspButton.Size = UDim2.new(0, 266, 0, 50)
OreEspButton.Font = Enum.Font.FredokaOne
OreEspButton.Text = "OreESP"
OreEspButton.TextColor3 = Color3.fromRGB(0, 0, 0)
OreEspButton.TextSize = 24.000

UICorner_2.Parent = OreEspButton

ESPButton.Name = "ESPButton"
ESPButton.Parent = MainFrame
ESPButton.BackgroundColor3 = Color3.fromRGB(84, 84, 84)
ESPButton.BackgroundTransparency = 0.500
ESPButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
ESPButton.BorderSizePixel = 0
ESPButton.Position = UDim2.new(0.0283687934, 0, 0.383177578, 0)
ESPButton.Size = UDim2.new(0, 266, 0, 50)
ESPButton.Font = Enum.Font.FredokaOne
ESPButton.Text = "ESP"
ESPButton.TextColor3 = Color3.fromRGB(0, 0, 0)
ESPButton.TextSize = 24.000

UICorner_3.Parent = ESPButton

AimButton.Name = "AimButton"
AimButton.Parent = MainFrame
AimButton.BackgroundColor3 = Color3.fromRGB(84, 84, 84)
AimButton.BackgroundTransparency = 0.500
AimButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
AimButton.BorderSizePixel = 0
AimButton.Position = UDim2.new(0.0283687934, 0, 0.696261704, 0)
AimButton.Size = UDim2.new(0, 266, 0, 50)
AimButton.Font = Enum.Font.FredokaOne
AimButton.Text = "AIMBOT"
AimButton.TextColor3 = Color3.fromRGB(0, 0, 0)
AimButton.TextSize = 24.000

UICorner_4.Parent = AimButton

UICorner_5.CornerRadius = UDim.new(0, 7)
UICorner_5.Parent = MainFrame

MainButton.Name = "MainButton"
MainButton.Parent = ScreenGui
MainButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
MainButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
MainButton.BorderSizePixel = 0
MainButton.Position = UDim2.new(0.728715718, 0, 0.176755443, 0)
MainButton.Size = UDim2.new(0, 54, 0, 50)
MainButton.Font = Enum.Font.SourceSans
MainButton.TextColor3 = Color3.fromRGB(0, 0, 0)
MainButton.TextSize = 14.000

ImageLabel.Parent = MainButton
ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
ImageLabel.BorderSizePixel = 0
ImageLabel.Size = UDim2.new(0, 54, 0, 50)
ImageLabel.Image = "http://www.roblox.com/asset/?id=13639732367"

UICorner_6.Parent = ImageLabel

TextLabel.Parent = ImageLabel
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.BorderSizePixel = 0
TextLabel.Position = UDim2.new(0.129629627, 0, 0.0799999982, 0)
TextLabel.Size = UDim2.new(0, 39, 0, 42)
TextLabel.Font = Enum.Font.FredokaOne
TextLabel.Text = "Y"
TextLabel.TextColor3 = Color3.fromRGB(255, 0, 0)
TextLabel.TextSize = 36.000

UICorner_7.Parent = MainButton

-- Scripts:

local function HSSMQ_fake_script() -- ESPButton.LocalScript 
	local script = Instance.new('LocalScript', ESPButton)

	script.Parent.MouseButton1Click:Connect(function()
		while wait(0.5) do
			for i, childrik in ipairs(workspace:GetDescendants()) do
				if childrik:FindFirstChild("HumanoidRootPart") then
					if not childrik:FindFirstChild("EspBox") then
						if childrik ~= game.Players.LocalPlayer.Character then
							local esp = Instance.new("BoxHandleAdornment",childrik)
							esp.Adornee = childrik
							esp.ZIndex = 0
							esp.Size = Vector3.new(4, 3, 1)
							esp.Transparency = 0.50
							esp.Color3 = Color3.fromRGB(70, 3, 99)
							esp.AlwaysOnTop = true
							esp.Name = "EspBox"
						end
					end
				end
			end
		end
	end)
end
coroutine.wrap(HSSMQ_fake_script)()
local function BDPW_fake_script() -- AimButton.LocalScript 
	local script = Instance.new('LocalScript', AimButton)

	script.Parent.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet("https://pastebin.com/raw/ygp8Enye"))()
	end)
end
coroutine.wrap(BDPW_fake_script)()
local function INQXLD_fake_script() -- MainButton.LocalScript 
	local script = Instance.new('LocalScript', MainButton)

	script.Parent.MouseButton1Click:Connect(function()
		if script.Parent.Parent.MainFrame.Visible == false then
			script.Parent.Parent.MainFrame.Visible = true
		else
			script.Parent.Parent.MainFrame.Visible = false
		end
	end)
end
coroutine.wrap(INQXLD_fake_script)()
