# 13. Example Projects

Try these mini-projects to practice your skills!

## 1. Auto Farm for Simulator Games

```lua
_G.autoFarm = true
while _G.autoFarm do
    -- Replace with your game's farming remote
    game:GetService("ReplicatedStorage").Remotes.Farm:FireServer()
    wait(1)
end
```

## 2. Simple Obby Helper (Auto-Jump)

```lua
game:GetService("UserInputService").JumpRequest:Connect(function()
    game.Players.LocalPlayer.Character.Humanoid.Jump = true
end)
```

## 3. GUI Button to Run Scripts

```lua
local ScreenGui = Instance.new("ScreenGui", game.CoreGui)
local Button = Instance.new("TextButton", ScreenGui)
Button.Size = UDim2.new(0, 200, 0, 50)
Button.Position = UDim2.new(0.5, -100, 0.5, -25)
Button.Text = "Click Me!"

Button.MouseButton1Click:Connect(function()
    print("Button clicked!")
    -- Put your script here
end)
```

## 4. Custom Chat Commands

```lua
game.Players.LocalPlayer.Chatted:Connect(function(msg)
    if msg == "!jump" then
        game.Players.LocalPlayer.Character.Humanoid.Jump = true
    end
end)
```
```

---

### 14-safety.md

```markdown
# 14. How to Stay Safe

- Never give your Roblox password to anyone.
- Don’t download executors or scripts from random links.
- Use a separate account for testing scripts.
- Don’t use scripts to harm or annoy other players.
- If something feels wrong, stop and ask for help.
- Always follow Roblox’s Terms of Service.

**Remember:** Your account is valuable. Keep it safe!
```

---

### 15-keep-learning.md

```markdown
# 15. Keep Learning

- Try making your own small game in Roblox Studio.
- Experiment with different scripts and see what happens.
- Read other people’s scripts and try to understand them.
- Watch YouTube tutorials and follow along.
- Join scripting communities and ask questions.
- Practice, practice, practice!

**The more you try, the better you’ll get. Good luck!**
```

---

**You can now copy these files into your project folder and upload them to GitHub!**  
If you want the full text for files 1–8 as well, or want a zipped folder, just ask!
