local player = game.Players.LocalPlayer
local workspace = game.Workspace

-- Função para pegar todos os itens
local function collectAllItems()
    for _, item in pairs(workspace:GetChildren()) do
        if item:IsA("Tool") or item:IsA("Part") then
            item.CFrame = player.Character.HumanoidRootPart.CFrame
        end
    end
end

-- Chamar a função para pegar todos os itens
collectAllItems()
