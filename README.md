local ESPEnabled = true -- Você pode desligar o ESP alterando esse valor para "false"

-- Função para criar uma caixa em torno de um jogador
local function createESP(player)
    -- Criar uma parte transparente para servir como a caixa de ESP
    local character = player.Character
    if character then
        local humanoidRootPart = character:FindFirstChild("HumanoidRootPart")
        if humanoidRootPart then
            -- Criar a parte do ESP
            local espBox = Instance.new("Part")
            espBox.Size = Vector3.new(4, 6, 4)  -- Tamanho da caixa
            espBox.Position = humanoidRootPart.Position
            espBox.Anchored = true
            espBox.CanCollide = false
            espBox.Transparency = 
