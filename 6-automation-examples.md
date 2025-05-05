# 6. Automation Examples

## Auto Collect Coins

```lua
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local CollectPickup = ReplicatedStorage.Remotes.Pickups.CollectPickup

for _, coin in ipairs(workspace:GetDescendants()) do
    if coin:IsA("BasePart") and (coin.Name == "Coin" or string.match(coin.Name, "Meshes/bgscoin%d+")) then
        CollectPickup:FireServer(coin:GetAttribute("ID"))
    end
end

workspace.DescendantAdded:Connect(function(obj)
    if obj:IsA("BasePart") and (obj.Name == "Coin" or string.match(obj.Name, "Meshes/bgscoin%d+")) then
        CollectPickup:FireServer(obj:GetAttribute("ID"))
    end
end)
```

## Make Your Hitbox Bigger

```lua
local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local root = character:FindFirstChild("HumanoidRootPart")
if root then
    root.Size = Vector3.new(10, 10, 10)
    root.Transparency = 1
end
```

## Auto Clicker

```lua
_G.autoClick = true
while _G.autoClick do
    -- Replace with your game's click remote
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.ClickService.Click:FireServer(1)
    wait(0.1)
end
```

Next: [7-safety-tips.md](7-safety-tips.md)
