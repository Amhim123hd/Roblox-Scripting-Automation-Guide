# 🎉 16. Fun Stuff: Advanced & Creative Roblox Scripting 🎮

Welcome to the **fun and creative side** of Roblox scripting!  
This guide will show you how to make your own auto farms, custom GUIs, cool player powers, and more.  
Each section is easy to follow and builds on what you’ve learned so far.

---

## 📖 Table of Contents
1. [Auto Farm: Collect and Sell Automatically](#1-auto-farm-collect-and-sell-automatically)
2. [Make a Simple GUI Button](#2-make-a-simple-gui-button)
3. [Using a GUI Library (OrionLib Example)](#3-using-a-gui-library-orionlib-example)
4. [Player Powers: Teleport, Speed, and Jump](#4-player-powers-teleport-speed-and-jump)
5. [No-Clip: Walk Through Walls](#5-no-clip-walk-through-walls)
6. [ESP: See Players or Items Through Walls](#6-esp-see-players-or-items-through-walls)
7. [Custom Chat Commands](#7-custom-chat-commands)
8. [Auto Buy, Auto Quest, and More](#8-auto-buy-auto-quest-and-more)
9. [How to Find Remotes (SimpleSpy)](#9-how-to-find-remotes-simplespy)
10. [Roblox Terms of Service & Getting Banned](#10-roblox-terms-of-service--getting-banned)
11. [Keep Exploring!](#11-keep-exploring)

---

## 1. 🚜 Auto Farm: Collect and Sell Automatically

Auto farms help you collect coins, items, or points without doing anything!

```lua
_G.autoFarm = true

while _G.autoFarm do
    -- Collect all coins
    for _, coin in ipairs(workspace:GetDescendants()) do
        if coin:IsA("BasePart") and coin.Name == "Coin" then
            game:GetService("ReplicatedStorage").Remotes.Pickups.CollectPickup:FireServer(coin:GetAttribute("ID"))
        end
    end
    wait(1)
end
```

> 💡 **Tip:** Replace the sell remote with the one from your game if you want to auto-sell!

---

## 2. 🖱️ Make a Simple GUI Button

Add buttons to your screen that run scripts when clicked.

```lua
local ScreenGui = Instance.new("ScreenGui", game.CoreGui)
local Button = Instance.new("TextButton", ScreenGui)
Button.Size = UDim2.new(0, 200, 0, 50)
Button.Position = UDim2.new(0.5, -100, 0.5, -25)
Button.Text = "Start Auto Farm"

Button.MouseButton1Click:Connect(function()
    print("Auto Farm Started!")
    -- Put your auto farm code here
end)
```

---

## 3. 🎨 Using a GUI Library (OrionLib Example)

Libraries like OrionLib make it easy to create beautiful UIs.

```lua
local OrionLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/shlexware/Orion/main/source"))()
local Window = OrionLib:MakeWindow({Name = "Fun Stuff", HidePremium = false, SaveConfig = true, ConfigFolder = "FunStuff"})

local Tab = Window:MakeTab({Name = "Main", Icon = "rbxassetid://4483345998", PremiumOnly = false})

Tab:AddButton({
    Name = "Say Hello",
    Callback = function()
        print("Hello from OrionLib!")
    end
})

OrionLib:Init()
```

---

## 4. 🦸 Player Powers: Teleport, Speed, and Jump

Change how your character moves!

```lua
-- Teleport
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0, 100, 0)

-- Speed and Jump
local h = game.Players.LocalPlayer.Character.Humanoid
h.WalkSpeed = 100
h.JumpPower = 200
```

---

## 5. 🚶 No-Clip: Walk Through Walls

Walk through anything (for fun and learning)!

```lua
_G.noclip = true
game:GetService('RunService').Stepped:Connect(function()
    if _G.noclip then
        game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
    end
end)
```

---

## 6. 👀 ESP: See Players or Items Through Walls

Draw boxes around things you want to see!

```lua
for _, player in ipairs(game.Players:GetPlayers()) do
    if player ~= game.Players.LocalPlayer then
        local box = Instance.new("BoxHandleAdornment")
        box.Adornee = player.Character and player.Character:FindFirstChild("HumanoidRootPart")
        box.Size = Vector3.new(4, 6, 2)
        box.Color3 = Color3.new(1, 0, 0)
        box.AlwaysOnTop = true
        box.Parent = game.CoreGui
    end
end
```

---

## 7. 💬 Custom Chat Commands

Make your own chat commands!

```lua
game.Players.LocalPlayer.Chatted:Connect(function(msg)
    if msg == "!jump" then
        game.Players.LocalPlayer.Character.Humanoid.Jump = true
    end
end)
```

---

## 8. 🔄 Auto Buy, Auto Quest, and More

Automate anything you can find a remote for!

```lua
-- Auto Buy Example
_G.autoBuy = true
while _G.autoBuy do
    -- Replace with your game's buy remote
    wait(1)
end
```

---

## 9. 🔍 How to Find Remotes (SimpleSpy)

1. Get [SimpleSpy](https://github.com/exxtremestuffs/SimpleSpySource).
2. Paste the script into your executor and run it.
3. Do something in the game (like collect a coin).
4. SimpleSpy will show you the remote event and code to use!

---

## 10. ⚠️ Roblox Terms of Service & Getting Banned

**Important!**  
Roblox has rules. Here’s what can get you banned:
- Using scripts to harm, annoy, or scam other players.
- Using scripts to steal accounts or items.
- Sharing or selling malicious scripts.
- Exploiting in games where it’s not allowed.

**What’s usually safe?**
- Scripting in Roblox Studio for your own games.
- Learning and experimenting in private servers or with friends (with permission).
- Using scripts that don’t harm others or break the game for everyone.

> ❗ **Always use scripts responsibly and for learning or fun with friends!**

---

## 11. 🌟 Keep Exploring!

- Try making your own mini-games in Roblox Studio.
- Experiment with new scripts and see what you can automate.
- Join scripting communities and share your creations.
- Watch YouTube tutorials for more ideas.

---

**Have fun, be creative, and always play fair!**
