-- Criação do Frame
local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local ButtonInfAllPatchet = Instance.new("TextButton")
local ButtonInfAllBeta = Instance.new("TextButton")
local ButtonKillAllPatchet = Instance.new("TextButton")

-- Configurações gerais do ScreenGui e Frame
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
Frame.Parent = ScreenGui
Frame.Size = UDim2.new(0, 300, 0, 200)
Frame.Position = UDim2.new(0.5, -150, 0.5, -100)
Frame.BackgroundColor3 = Color3.new(0.3, 0.3, 0.3)
Frame.Active = true
Frame.Draggable = true -- Permite mover o frame

-- Configurações do botão Inf All (Patchet)
ButtonInfAllPatchet.Parent = Frame
ButtonInfAllPatchet.Size = UDim2.new(0, 260, 0, 30)
ButtonInfAllPatchet.Position = UDim2.new(0, 20, 0, 20)
ButtonInfAllPatchet.Text = "Inf all (patchet)"
ButtonInfAllPatchet.BackgroundColor3 = Color3.new(0.2, 0.6, 0.8)

-- Configurações do botão Inf All (Beta)
ButtonInfAllBeta.Parent = Frame
ButtonInfAllBeta.Size = UDim2.new(0, 260, 0, 30)
ButtonInfAllBeta.Position = UDim2.new(0, 20, 0, 70)
ButtonInfAllBeta.Text = "Inf all (beta)"
ButtonInfAllBeta.BackgroundColor3 = Color3.new(0.2, 0.6, 0.8)

-- Função para adicionar recursos no botão Inf All (Beta)
ButtonInfAllBeta.MouseButton1Click:Connect(function()
    game:GetService("ReplicatedStorage").RemoteEvents.AddFans:FireServer(9e999999)
    game:GetService("ReplicatedStorage").RemoteEvents.WinsGiver:FireServer(9e99999)
    game:GetService("ReplicatedStorage").RemoteEvents.GemsGiver:FireServer(9e99999)
end)

-- Configurações do botão Kill All (Patchet)
ButtonKillAllPatchet.Parent = Frame
ButtonKillAllPatchet.Size = UDim2.new(0, 260, 0, 30)
ButtonKillAllPatchet.Position = UDim2.new(0, 20, 0, 120)
ButtonKillAllPatchet.Text = "Kill all (patchet)"
ButtonKillAllPatchet.BackgroundColor3 = Color3.new(0.2, 0.6, 0.8)
