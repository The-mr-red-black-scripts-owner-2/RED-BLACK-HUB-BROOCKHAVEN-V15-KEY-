--== CONFIG ==--
local CorrectKey = "RBH-FreeKey-broockhaven-9F7A2C6D-3E8B-41C2-A7F9-XX4G_2025-V1.0[✓]"
local KeyLink = "https://discord.gg/ffuFGauPdS"

local TikTokLink = "https://www.tiktok.com/@the_mr_red_black_owner?_r=1&_t=ZM-925YlY0ADmq"
local YoutubeLink = "https://m.youtube.com/@THE_MR_RED_BLACK_SCRIPTS_OWNER"

--== GUI ==--
local gui = Instance.new("ScreenGui", game.CoreGui)
gui.Name = "RBH_KEY_GUI"

local frame = Instance.new("Frame", gui)
frame.Size = UDim2.new(0, 380, 0, 330)
frame.Position = UDim2.new(0.5, -190, 0.5, -165)
frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
frame.BorderSizePixel = 0
Instance.new("UICorner", frame).CornerRadius = UDim.new(0,18)

-- TextBox para a Key
local box = Instance.new("TextBox", frame)
box.Size = UDim2.new(1, -30, 0, 40)
box.Position = UDim2.new(0, 15, 0, 20)
box.PlaceholderText = "ENTER KEY"
box.TextColor3 = Color3.fromRGB(255,255,255)
box.BackgroundColor3 = Color3.fromRGB(20,20,20)
box.BorderSizePixel = 0
Instance.new("UICorner", box).CornerRadius = UDim.new(0,10)

-- Botão CHECK KEY
local check = Instance.new("TextButton", frame)
check.Size = UDim2.new(1, -30, 0, 40)
check.Position = UDim2.new(0, 15, 0, 75)
check.Text = "CHECK KEY"
check.TextColor3 = Color3.fromRGB(255,255,255)
check.BackgroundColor3 = Color3.fromRGB(255,0,255)
check.BorderSizePixel = 0
Instance.new("UICorner", check).CornerRadius = UDim.new(0,10)

-- Botão GET KEY
local getkey = Instance.new("TextButton", frame)
getkey.Size = UDim2.new(1, -30, 0, 40)
getkey.Position = UDim2.new(0, 15, 0, 130)
getkey.Text = "GET KEY"
getkey.TextColor3 = Color3.fromRGB(255,255,255)
getkey.BackgroundColor3 = Color3.fromRGB(255,0,255)
getkey.BorderSizePixel = 0
Instance.new("UICorner", getkey).CornerRadius = UDim.new(0,10)

-- Status
local status = Instance.new("TextLabel", frame)
status.Size = UDim2.new(1, -30, 0, 30)
status.Position = UDim2.new(0, 15, 0, 180)
status.BackgroundTransparency = 1
status.TextColor3 = Color3.fromRGB(255,255,255)
status.Text = ""

-- Botão TIKTOK
local tiktok = Instance.new("TextButton", frame)
tiktok.Size = UDim2.new(1, -30, 0, 40)
tiktok.Position = UDim2.new(0, 15, 0, 225)
tiktok.Text = "TIK TOK"
tiktok.TextColor3 = Color3.fromRGB(255,255,255)
tiktok.BackgroundColor3 = Color3.fromRGB(255,0,255)
tiktok.BorderSizePixel = 0
Instance.new("UICorner", tiktok).CornerRadius = UDim.new(0,10)

-- Botão YOUTUBE
local youtube = Instance.new("TextButton", frame)
youtube.Size = UDim2.new(1, -30, 0, 40)
youtube.Position = UDim2.new(0, 15, 0, 280)
youtube.Text = "YOUTUBE"
youtube.TextColor3 = Color3.fromRGB(255,255,255)
youtube.BackgroundColor3 = Color3.fromRGB(255,0,255)
youtube.BorderSizePixel = 0
Instance.new("UICorner", youtube).CornerRadius = UDim.new(0,10)

--== FUNÇÕES ==--

check.MouseButton1Click:Connect(function()
    if box.Text == CorrectKey then
        status.Text = "KEY CORRETA"
        frame:Destroy()
        -- coloque aqui o loadstring do hub
    else
        status.Text = "KEY ERRADA"
    end
end)

getkey.MouseButton1Click:Connect(function()
    setclipboard(KeyLink)
    if syn and syn.request then
        syn.request({Url = KeyLink, Method = "GET"})
    elseif request then
        request({Url = KeyLink, Method = "GET"})
    end
end)

tiktok.MouseButton1Click:Connect(function()
    setclipboard(TikTokLink)
end)

youtube.MouseButton1Click:Connect(function()
    setclipboard(YoutubeLink)
end)
