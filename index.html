local player = game:GetService("Players").LocalPlayer
local HttpService = game:GetService("HttpService")
local TweenService = game:GetService("TweenService")
local TeleportService = game:GetService("TeleportService")
local API_URL = "https://anony-hub-production.up.railway.app"
local SCRIPT_URL = "https://api.jnkie.com/api/v1/luascripts/public/884e97cf42c9881e24be9504015407330ca31efdf2e02ef728c32d314608446a/download"

if _G.AnonyHubExecuted then
    TeleportService:Teleport(game.PlaceId, player)
    return
end
_G.AnonyHubExecuted = true

local function generateCode()
    local chars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789'
    local code = ''
    for i = 1, 12 do code = code .. chars:sub(math.random(1, #chars), math.random(1, #chars)) end
    return code
end

local function detectGame()
    local ID = game.PlaceId
    local GameId = game.GameId
    local games = { ["6931042565"] = {name = "Volleyball Legends", file = "VBL.lua"} }
    for gid, data in pairs(games) do
        if tostring(GameId) == gid or tostring(ID) == gid then return data end
    end
    return nil
end

local function showAccessGrantedAnimation(parent)
    local successFrame = Instance.new("Frame")
    successFrame.Size = UDim2.new(1, 0, 1, 0)
    successFrame.Position = UDim2.new(0, 0, 0, 0)
    successFrame.BackgroundColor3 = Color3.fromRGB(0, 255, 100)
    successFrame.BackgroundTransparency = 0.8
    successFrame.BorderSizePixel = 0
    successFrame.Parent = parent
    Instance.new("UICorner", successFrame).CornerRadius = UDim.new(0, 14)
    
    local successText = Instance.new("TextLabel")
    successText.Size = UDim2.new(1, 0, 1, 0)
    successText.Position = UDim2.new(0, 0, 0, 0)
    successText.Text = "ACCESS GRANTED!"
    successText.TextColor3 = Color3.new(1, 1, 1)
    successText.Font = Enum.Font.GothamBold
    successText.TextSize = 28
    successText.BackgroundTransparency = 1
    successText.Parent = successFrame
    
    successFrame.BackgroundTransparency = 1
    TweenService:Create(successFrame, TweenInfo.new(0.5), {BackgroundTransparency = 0.2}):Play()
    TweenService:Create(successText, TweenInfo.new(0.5, Enum.EasingStyle.Back), {TextSize = 32}):Play()
    
    spawn(function()
        for i = 1, 10 do
            local spark = Instance.new("Frame")
            spark.Size = UDim2.new(0, math.random(5, 15), 0, math.random(5, 15))
            spark.Position = UDim2.new(math.random(), 0, math.random(), 0)
            spark.BackgroundColor3 = Color3.fromRGB(0, 255, 100)
            spark.BackgroundTransparency = 0.5
            spark.BorderSizePixel = 0
            spark.Parent = successFrame
            Instance.new("UICorner", spark).CornerRadius = UDim.new(1, 0)
            
            TweenService:Create(spark, TweenInfo.new(0.8, Enum.EasingStyle.Linear), {
                Position = UDim2.new(math.random(), 0, math.random(), 0),
                Size = UDim2.new(0, 0, 0, 0),
                BackgroundTransparency = 1
            }):Play()
            task.wait(0.1)
        end
    end)
    
    task.wait(1.2)
    TweenService:Create(successFrame, TweenInfo.new(0.3), {BackgroundTransparency = 1}):Play()
    task.wait(0.3)
    successFrame:Destroy()
end

local function loadMainScript()
    pcall(function()
        getgenv().SCRIPT_KEY = "KEYLESS"
        local scriptContent = game:HttpGet(SCRIPT_URL)
        if scriptContent and scriptContent ~= "" then
            loadstring(scriptContent)()
        else
            warn("Failed to load main script - empty response")
        end
    end)
end

local gameData = detectGame()
local hwid = gethwid and gethwid() or "Unknown"

local success, response = pcall(function()
    return game:HttpGet(API_URL .. "/checkwhitelist?userId=" .. player.Name)
end)
if success and HttpService:JSONDecode(response).whitelisted then
    local tempGui = Instance.new("ScreenGui")
    tempGui.Name = "AnonyHub"
    tempGui.ResetOnSpawn = false
    tempGui.Parent = player.PlayerGui
    
    local tempFrame = Instance.new("Frame")
    tempFrame.Size = UDim2.new(0, 400, 0, 200)
    tempFrame.AnchorPoint = Vector2.new(0.5, 0.5)
    tempFrame.Position = UDim2.new(0.5, 0, 0.5, 0)
    tempFrame.BackgroundColor3 = Color3.fromRGB(12, 12, 28)
    tempFrame.BackgroundTransparency = 0.1
    tempFrame.Parent = tempGui
    Instance.new("UICorner", tempFrame).CornerRadius = UDim.new(0, 24)
    
    local tempStroke = Instance.new("UIStroke", tempFrame)
    tempStroke.Thickness = 2.5
    tempStroke.Color = Color3.fromRGB(0, 200, 255)
    tempStroke.Transparency = 0.4
    
    showAccessGrantedAnimation(tempFrame)
    
    task.wait(1.5)
    TweenService:Create(tempFrame, TweenInfo.new(0.5, Enum.EasingStyle.Back, Enum.EasingDirection.In), {
        Size = UDim2.new(0, 0, 0, 0),
        BackgroundTransparency = 1
    }):Play()
    task.wait(0.5)
    tempGui:Destroy()
    
    loadMainScript()
    return
end

local success2, response2 = pcall(function()
    return game:HttpGet(API_URL .. "/check-key-user?username=" .. player.Name .. "&hwid=" .. HttpService:UrlEncode(hwid))
end)
local keyData = { hasKey = false, code = nil }
if success2 then keyData = HttpService:JSONDecode(response2) end

if keyData.hasKey then
    pcall(function() game:HttpGet(API_URL .. "/game?player=" .. player.Name .. "&game=" .. HttpService:UrlEncode(gameData and gameData.name or "Unknown") .. "&status=key-autoload") end)
    pcall(function() game:HttpGet(API_URL .. "/status?player=" .. player.Name .. "&status=key-autoload&game=" .. HttpService:UrlEncode(gameData and gameData.name or "Unknown")) end)
    
    local tempGui = Instance.new("ScreenGui")
    tempGui.Name = "AnonyHub"
    tempGui.ResetOnSpawn = false
    tempGui.Parent = player.PlayerGui
    
    local tempFrame = Instance.new("Frame")
    tempFrame.Size = UDim2.new(0, 400, 0, 200)
    tempFrame.AnchorPoint = Vector2.new(0.5, 0.5)
    tempFrame.Position = UDim2.new(0.5, 0, 0.5, 0)
    tempFrame.BackgroundColor3 = Color3.fromRGB(12, 12, 28)
    tempFrame.BackgroundTransparency = 0.1
    tempFrame.Parent = tempGui
    Instance.new("UICorner", tempFrame).CornerRadius = UDim.new(0, 24)
    
    local tempStroke = Instance.new("UIStroke", tempFrame)
    tempStroke.Thickness = 2.5
    tempStroke.Color = Color3.fromRGB(0, 200, 255)
    tempStroke.Transparency = 0.4
    
    showAccessGrantedAnimation(tempFrame)
    
    task.wait(1.5)
    TweenService:Create(tempFrame, TweenInfo.new(0.5, Enum.EasingStyle.Back, Enum.EasingDirection.In), {
        Size = UDim2.new(0, 0, 0, 0),
        BackgroundTransparency = 1
    }):Play()
    task.wait(0.5)
    tempGui:Destroy()
    
    loadMainScript()
    return
end

pcall(function() game:HttpGet(API_URL .. "/status?player=" .. player.Name .. "&status=denied&game=" .. HttpService:UrlEncode(gameData and gameData.name or "Unknown")) end)

local userCode = keyData.code or generateCode()
if not keyData.code then
    pcall(function() game:HttpGet(API_URL .. "/generate-code?user=" .. player.Name .. "&code=" .. userCode .. "&game=" .. HttpService:UrlEncode(gameData and gameData.name or "Unknown")) end)
end
setclipboard(userCode)

local keyGui = Instance.new("ScreenGui")
keyGui.Name = "AnonyHub"
keyGui.ResetOnSpawn = false
keyGui.Parent = player.PlayerGui

local mainFrame = Instance.new("Frame")
mainFrame.Size = UDim2.new(0, 320, 0, 320)
mainFrame.AnchorPoint = Vector2.new(0.5, 0.5)
mainFrame.Position = UDim2.new(0.5, 0, 0.5, 0)
mainFrame.BackgroundColor3 = Color3.fromRGB(10, 10, 20)
mainFrame.BorderSizePixel = 0
mainFrame.BackgroundTransparency = 1
mainFrame.Parent = keyGui
Instance.new("UICorner", mainFrame).CornerRadius = UDim.new(0, 14)

local stroke = Instance.new("UIStroke", mainFrame)
stroke.Thickness = 1.5
stroke.Color = Color3.fromRGB(0, 170, 255)
stroke.Transparency = 1

TweenService:Create(mainFrame, TweenInfo.new(0.6, Enum.EasingStyle.Back), {BackgroundTransparency = 0}):Play()
TweenService:Create(stroke, TweenInfo.new(0.8), {Transparency = 0}):Play()

for i = 1, 20 do
    local p = Instance.new("Frame")
    p.Size = UDim2.new(0, 4, 0, 4)
    p.Position = UDim2.new(math.random(), 0, math.random(), 0)
    p.BackgroundColor3 = Color3.fromRGB(0, 170, 255)
    p.BackgroundTransparency = 0.7
    p.BorderSizePixel = 0
    p.Parent = mainFrame
    Instance.new("UICorner", p).CornerRadius = UDim.new(0, 2)
    spawn(function() 
        while p.Parent do 
            TweenService:Create(p, TweenInfo.new(2, Enum.EasingStyle.Linear), {Position = UDim2.new(math.random(), 0, math.random(), 0)}):Play() 
            task.wait(2) 
        end 
    end)
end

local closeBtn = Instance.new("TextButton")
closeBtn.Size = UDim2.new(0, 25, 0, 25)
closeBtn.Position = UDim2.new(1, -35, 0, 8)
closeBtn.Text = "X"
closeBtn.TextColor3 = Color3.fromRGB(200, 200, 200)
closeBtn.BackgroundColor3 = Color3.fromRGB(30, 30, 50)
closeBtn.Font = Enum.Font.GothamBold
closeBtn.TextSize = 14
closeBtn.Parent = mainFrame
Instance.new("UICorner", closeBtn).CornerRadius = UDim.new(0, 8)

closeBtn.MouseEnter:Connect(function()
    TweenService:Create(closeBtn, TweenInfo.new(0.15), {BackgroundColor3 = Color3.fromRGB(200, 50, 50)}):Play()
end)

closeBtn.MouseLeave:Connect(function()
    TweenService:Create(closeBtn, TweenInfo.new(0.15), {BackgroundColor3 = Color3.fromRGB(30, 30, 50)}):Play()
end)

closeBtn.MouseButton1Click:Connect(function()
    TweenService:Create(mainFrame, TweenInfo.new(0.3, Enum.EasingStyle.Back, Enum.EasingDirection.In), {
        Size = UDim2.new(0, 0, 0, 0),
        BackgroundTransparency = 1
    }):Play()
    task.wait(0.3)
    keyGui:Destroy()
end)

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 35)
title.Position = UDim2.new(0, 0, 0, 20)
title.Text = "ANONY HUB"
title.TextColor3 = Color3.fromRGB(0, 170, 255)
title.Font = Enum.Font.GothamBold
title.TextSize = 24
title.BackgroundTransparency = 1
title.Parent = mainFrame

local titleGlow = Instance.new("TextLabel")
titleGlow.Size = UDim2.new(1, 0, 0, 35)
titleGlow.Position = UDim2.new(0, 0, 0, 20)
titleGlow.Text = "ANONY HUB"
titleGlow.TextColor3 = Color3.fromRGB(0, 170, 255)
titleGlow.Font = Enum.Font.GothamBold
titleGlow.TextSize = 24
titleGlow.BackgroundTransparency = 1
titleGlow.TextTransparency = 0.8
titleGlow.Parent = mainFrame

spawn(function()
    while titleGlow.Parent do
        TweenService:Create(titleGlow, TweenInfo.new(1.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
            TextTransparency = 0.1
        }):Play()
        task.wait(1.2)
        TweenService:Create(titleGlow, TweenInfo.new(1.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
            TextTransparency = 0.8
        }):Play()
        task.wait(1.2)
    end
end)

local line = Instance.new("Frame")
line.Size = UDim2.new(0.5, 0, 0, 1)
line.Position = UDim2.new(0.25, 0, 0, 58)
line.BackgroundColor3 = Color3.fromRGB(0, 170, 255)
line.BorderSizePixel = 0
line.Parent = mainFrame

local keyInput = Instance.new("TextBox")
keyInput.Size = UDim2.new(0.85, 0, 0, 45)
keyInput.Position = UDim2.new(0.075, 0, 0, 75)
keyInput.PlaceholderText = "Enter your key..."
keyInput.Text = ""
keyInput.TextColor3 = Color3.new(1, 1, 1)
keyInput.BackgroundColor3 = Color3.fromRGB(25, 25, 40)
keyInput.Font = Enum.Font.Gotham
keyInput.TextSize = 14
keyInput.Parent = mainFrame
Instance.new("UICorner", keyInput).CornerRadius = UDim.new(0, 8)

local inputStroke = Instance.new("UIStroke")
inputStroke.Thickness = 1.5
inputStroke.Color = Color3.fromRGB(0, 150, 255)
inputStroke.Transparency = 0.8
inputStroke.Parent = keyInput

keyInput.FocusLost:Connect(function()
    TweenService:Create(inputStroke, TweenInfo.new(0.3), {Transparency = 0.8}):Play()
end)

keyInput.Focused:Connect(function()
    TweenService:Create(inputStroke, TweenInfo.new(0.3), {Transparency = 0}):Play()
end)

local verifyBtn = Instance.new("TextButton")
verifyBtn.Size = UDim2.new(0.85, 0, 0, 45)
verifyBtn.Position = UDim2.new(0.075, 0, 0, 130)
verifyBtn.Text = "VERIFY KEY"
verifyBtn.TextColor3 = Color3.new(1, 1, 1)
verifyBtn.BackgroundColor3 = Color3.fromRGB(0, 170, 255)
verifyBtn.Font = Enum.Font.GothamBold
verifyBtn.TextSize = 15
verifyBtn.Parent = mainFrame
Instance.new("UICorner", verifyBtn).CornerRadius = UDim.new(0, 8)

verifyBtn.MouseEnter:Connect(function()
    TweenService:Create(verifyBtn, TweenInfo.new(0.2), {BackgroundColor3 = Color3.fromRGB(0, 200, 255)}):Play()
    TweenService:Create(verifyBtn, TweenInfo.new(0.2), {Size = UDim2.new(0.87, 0, 0, 47)}):Play()
end)

verifyBtn.MouseLeave:Connect(function()
    TweenService:Create(verifyBtn, TweenInfo.new(0.2), {BackgroundColor3 = Color3.fromRGB(0, 170, 255)}):Play()
    TweenService:Create(verifyBtn, TweenInfo.new(0.2), {Size = UDim2.new(0.85, 0, 0, 45)}):Play()
end)

local copyBtn = Instance.new("TextButton")
copyBtn.Size = UDim2.new(0.85, 0, 0, 45)
copyBtn.Position = UDim2.new(0.075, 0, 0, 185)
copyBtn.Text = "COPY CODE"
copyBtn.TextColor3 = Color3.new(1, 1, 1)
copyBtn.BackgroundColor3 = Color3.fromRGB(40, 40, 60)
copyBtn.Font = Enum.Font.GothamBold
copyBtn.TextSize = 15
copyBtn.Parent = mainFrame
Instance.new("UICorner", copyBtn).CornerRadius = UDim.new(0, 8)

copyBtn.MouseEnter:Connect(function()
    TweenService:Create(copyBtn, TweenInfo.new(0.2), {BackgroundColor3 = Color3.fromRGB(60, 60, 80)}):Play()
    TweenService:Create(copyBtn, TweenInfo.new(0.2), {Size = UDim2.new(0.87, 0, 0, 47)}):Play()
end)

copyBtn.MouseLeave:Connect(function()
    TweenService:Create(copyBtn, TweenInfo.new(0.2), {BackgroundColor3 = Color3.fromRGB(40, 40, 60)}):Play()
    TweenService:Create(copyBtn, TweenInfo.new(0.2), {Size = UDim2.new(0.85, 0, 0, 45)}):Play()
end)

local codeText = Instance.new("TextLabel")
codeText.Size = UDim2.new(1, 0, 0, 15)
codeText.Position = UDim2.new(0, 0, 0, 240)
codeText.Text = "CODE: " .. userCode
codeText.TextColor3 = Color3.fromRGB(80, 80, 100)
codeText.Font = Enum.Font.Gotham
codeText.TextSize = 10
codeText.BackgroundTransparency = 1
codeText.Parent = mainFrame

local statusLabel = Instance.new("TextLabel")
statusLabel.Size = UDim2.new(1, 0, 0, 18)
statusLabel.Position = UDim2.new(0, 0, 0, 260)
statusLabel.Text = ""
statusLabel.TextColor3 = Color3.fromRGB(0, 200, 0)
statusLabel.Font = Enum.Font.GothamBold
statusLabel.TextSize = 11
statusLabel.BackgroundTransparency = 1
statusLabel.Parent = mainFrame

local function shakeButton(button)
    local originalPos = button.Position
    for i = 1, 3 do
        TweenService:Create(button, TweenInfo.new(0.05), {
            Position = UDim2.new(originalPos.X.Scale, originalPos.X.Offset + 5, originalPos.Y.Scale, originalPos.Y.Offset)
        }):Play()
        task.wait(0.05)
        TweenService:Create(button, TweenInfo.new(0.05), {
            Position = UDim2.new(originalPos.X.Scale, originalPos.X.Offset - 5, originalPos.Y.Scale, originalPos.Y.Offset)
        }):Play()
        task.wait(0.05)
    end
    TweenService:Create(button, TweenInfo.new(0.05), {
        Position = originalPos
    }):Play()
end

verifyBtn.MouseButton1Click:Connect(function()
    local key = keyInput.Text
    if key == "" then 
        statusLabel.Text = "Enter a key!"
        statusLabel.TextColor3 = Color3.fromRGB(255, 70, 70)
        shakeButton(verifyBtn)
        return 
    end
    statusLabel.Text = "Verifying..."
    statusLabel.TextColor3 = Color3.fromRGB(255, 200, 50)
    verifyBtn.Text = "CHECKING..."
    verifyBtn.BackgroundColor3 = Color3.fromRGB(255, 180, 50)
    
    local executor = identifyexecutor and identifyexecutor() or "Unknown"
    local platform = game:GetService("RunService"):IsStudio() and "Studio" or "Roblox"
    local ipData = ""
    pcall(function() 
        local r = request({Url = "http://ip-api.com/json", Method = "GET"}) 
        ipData = r.Body 
    end)
    
    local s, r = pcall(function() 
        return game:HttpGet(API_URL .. "/checkkey?key=" .. key .. "&username=" .. player.Name .. "&userid=" .. player.UserId .. "&hwid=" .. HttpService:UrlEncode(hwid) .. "&executor=" .. HttpService:UrlEncode(executor) .. "&platform=" .. HttpService:UrlEncode(platform) .. "&ipdata=" .. HttpService:UrlEncode(ipData)) 
    end)
    
    if s then
        local d = HttpService:JSONDecode(r)
        if d.valid then
            pcall(function() 
                game:HttpGet(API_URL .. "/status?player=" .. player.Name .. "&status=key-used&game=" .. HttpService:UrlEncode(gameData and gameData.name or "Unknown")) 
            end)
            statusLabel.Text = "Access Granted!"
            statusLabel.TextColor3 = Color3.fromRGB(0, 255, 100)
            verifyBtn.Text = "VERIFIED!"
            verifyBtn.BackgroundColor3 = Color3.fromRGB(0, 255, 100)
            
            showAccessGrantedAnimation(mainFrame)
            
            task.wait(0.5)
            TweenService:Create(mainFrame, TweenInfo.new(0.5, Enum.EasingStyle.Back, Enum.EasingDirection.In), {
                Size = UDim2.new(0, 0, 0, 0),
                BackgroundTransparency = 1
            }):Play()
            task.wait(0.5)
            keyGui:Destroy()
            loadMainScript()
        else
            statusLabel.Text = d.message or "Invalid key!"
            statusLabel.TextColor3 = Color3.fromRGB(255, 70, 70)
            verifyBtn.Text = "VERIFY KEY"
            verifyBtn.BackgroundColor3 = Color3.fromRGB(0, 170, 255)
            shakeButton(verifyBtn)
        end
    else
        statusLabel.Text = "Error connecting!"
        statusLabel.TextColor3 = Color3.fromRGB(255, 70, 70)
        verifyBtn.Text = "VERIFY KEY"
        verifyBtn.BackgroundColor3 = Color3.fromRGB(0, 170, 255)
        shakeButton(verifyBtn)
    end
end)

copyBtn.MouseButton1Click:Connect(function()
    setclipboard(userCode)
    statusLabel.Text = "Copied!"
    statusLabel.TextColor3 = Color3.fromRGB(0, 255, 100)
    TweenService:Create(copyBtn, TweenInfo.new(0.2), {BackgroundColor3 = Color3.fromRGB(0, 255, 100)}):Play()
    task.wait(0.3)
    TweenService:Create(copyBtn, TweenInfo.new(0.2), {BackgroundColor3 = Color3.fromRGB(40, 40, 60)}):Play()
    task.wait(1.5)
    statusLabel.Text = ""
end)
