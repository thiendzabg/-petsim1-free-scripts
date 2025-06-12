
-- 📁 LocalScript trong StarterGui > ScreenGui > PetSimUI
-- Author: ChatGPT + User
-- Dành cho bài dự án Pet Simulator 1 Roblox (trường học)

local ReplicatedStorage = game:GetService("ReplicatedStorage")
local player = game.Players.LocalPlayer

-- ⛓ RemoteEvent setup (nếu dùng executor thì phải đảm bảo server có các RemoteEvents)
local function getRemote(name)
    return ReplicatedStorage:WaitForChild(name)
end

-- 🧱 Giao diện UI cơ bản
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "PetSimUI"
screenGui.ResetOnSpawn = false
screenGui.Parent = game.CoreGui

local function createButton(text, position, callback)
    local btn = Instance.new("TextButton")
    btn.Size = UDim2.new(0, 250, 0, 50)
    btn.Position = position
    btn.Text = text
    btn.Font = Enum.Font.SourceSansBold
    btn.TextSize = 20
    btn.BackgroundColor3 = Color3.fromRGB(255, 215, 0)
    btn.BorderSizePixel = 2
    btn.Parent = screenGui
    btn.MouseButton1Click:Connect(callback)
end

-- 🐱 HUGE CAT
createButton("🎁 Nhận Huge Cat", UDim2.new(0, 30, 0, 80), function()
    getRemote("GiveHugeCat"):FireServer()
end)

-- 😈 Dominus Huge
createButton("😈 Nhận Dominus Huge", UDim2.new(0, 30, 0, 140), function()
    getRemote("GiveDominusHuge"):FireServer()
end)

-- ♾ Infinite Pets
createButton("♾ Nhận Infinite Pets", UDim2.new(0, 30, 0, 200), function()
    getRemote("GrantInfinitePets"):FireServer()
end)

-- 🎟 Nhận toàn bộ Gamepasses
createButton("🎟 Nhận ALL Gamepasses", UDim2.new(0, 30, 0, 260), function()
    getRemote("GrantAllGamepasses"):FireServer()
end)

-- 📜 Ghi chú
local label = Instance.new("TextLabel")
label.Size = UDim2.new(0, 400, 0, 30)
label.Position = UDim2.new(0, 30, 0, 20)
label.Text = "Pet Simulator 1 Project UI - ChatGPT Edition"
label.Font = Enum.Font.SourceSans
label.TextSize = 18
label.TextColor3 = Color3.new(1, 1, 1)
label.BackgroundTransparency = 1
label.Parent = screenGui
