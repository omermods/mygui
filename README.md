local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- İlk konuma ışınlama
character:WaitForChild("HumanoidRootPart").CFrame = CFrame.new(322.8979187011719, 3.6317925453186035, 239.74664306640625)

-- GUI oluşturma
local ScreenGui = Instance.new("ScreenGui")
local Label = Instance.new("TextLabel")

ScreenGui.Parent = player:WaitForChild("PlayerGui")

Label.Parent = ScreenGui
Label.Size = UDim2.new(0, 300, 0, 50)
Label.Position = UDim2.new(0.5, -150, 0.1, 0)
Label.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
Label.TextColor3 = Color3.fromRGB(255, 255, 0)
Label.Font = Enum.Font.SourceSansBold
Label.TextSize = 24
Label.Text = "OMER MODS ÇÖL FARMS"

-- Loadstring çalıştırma
loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Auto-Kill-All-Npc-6259"))()

wait(2) -- İşlemleri sırayla yapmak için biraz bekletme

-- Son konuma ışınlama
character:WaitForChild("HumanoidRootPart").CFrame = CFrame.new(333.553772, 3.63179207, 238.236481, 0.943683147, -3.38946933e-08, -0.330850571, 8.06098566e-09, 1, -7.94548285e-08, 0.330850571, 7.23132061e-08, 0.943683147)

wait(1) -- Tıklama işlemi öncesi bekleme

-- Otomatik tıklama işlemi
local UIS = game:GetService("UserInputService")
UIS.InputBegan:Fire(Enum.UserInputType.MouseButton1)
