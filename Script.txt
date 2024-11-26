local Players = game:GetService("Players")
local player = Players.LocalPlayer

local gui = Instance.new("ScreenGui", player.PlayerGui)
gui.Name = "WelcomeGui"

local frame = Instance.new("Frame", gui)
frame.Size = UDim2.new(0.5, 0, 0.5, 0)
frame.Position = UDim2.new(0.25, 0, 0.25, 0)
frame.BackgroundColor3 = Color3.new(0.2, 0.2, 0.2)

local textLabel = Instance.new("TextLabel", frame)
textLabel.Size = UDim2.new(1, 0, 0.6, 0)
textLabel.Text = "¡Bienvenido a Blox Fruits, " .. player.Name .. "!"
textLabel.BackgroundTransparency = 1
textLabel.TextColor3 = Color3.new(1, 1, 1)
textLabel.TextScaled = true

local button = Instance.new("TextButton", frame)
button.Size = UDim2.new(0.6, 0, 0.3, 0)
button.Position = UDim2.new(0.2, 0, 0.65, 0)
button.Text = "Cerrar"
button.BackgroundColor3 = Color3.new(0.4, 0.4, 0.4)
button.TextColor3 = Color3.new(1, 1, 1)
button.TextScaled = true

button.MouseButton1Click:Connect(function()
    gui:Destroy()
end)
