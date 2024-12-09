local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "THUNDER HUB", HidePremium = false, SaveConfig = true, ConfigFolder = "THUNDER HUB SOME TOWN"})

local FarmName = nil

local Tab = Window:MakeTab({
	Name = "Tab 1",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddDropdown({
	Name = "Dropdown",
	Default = nil,
	Options = {"Wood", "ScrapIron", "Rock", "Pork", "Plant", "Giftbox", "Flower", "Corn", "Banana"},
	Callback = function(Value)
		FarmName = tostring(Value)
	end    
})

Tab:AddToggle({
	Name = "Auto Sell",
	Default = false,
	Callback = function(t)
		    if FarmName == "Wood" then
                                                            local JU = game:GetService("Workspace"):FindFirstChild("JU")
                                                            if JU then
                                                                JU:Destroy()
                                                            end
                                                        local Noclip = Instance.new("Part", workspace)
                                                            Noclip.Name = "JU"
                                                            Noclip.CanCollide = true
                                                            Noclip.Anchored = true
                                                            Noclip.Transparency = 0.5
                                                            Noclip.Size = Vector3.new(30, 1, 30)
                                                            game:GetService("Workspace"):FindFirstChild("JU").CFrame = CFrame.new(2846.16187, 3.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)

                                                    local teleport_table = {
                                                        location1 = Vector3.new(2845.45142, 14.2436848, 2079.27222, -0.388715088, 1.28141585e-06, -0.921357989, -1.4877221e-06, 1, 2.01845091e-06, 0.921357989, 2.15532691e-06, -0.388715088),
                                                        location2 = Vector3.new(1268, 14, -1705)
                                                    }

                                                    local tween_s = game:GetService('TweenService')
                                                    local tweeninfo = TweenInfo.new(0,Enum.EasingStyle.Linear)

                                                    local lp = game.Players.LocalPlayer

                                                    function bypass_teleport(v)
                                                        if lp.Character and 
                                                        lp.Character:FindFirstChild('HumanoidRootPart') then
                                                            local cf = CFrame.new(v)
                                                            local a = tween_s:Create(lp.Character.HumanoidRootPart,tweeninfo,{CFrame=cf})
                                                            a:Play()
                                                            a.Completed:Wait()
                                                            print('Teleporting Done!')
                                                        end
                                                    end

                                                    bypass_teleport(teleport_table.location2)

                                                    local Players = game:GetService("Players")

                                                    local LocalPlayer = Players.LocalPlayer

                                                    local Inventory = LocalPlayer.Inventory

                                                    _G.AutoFarm = t

                                                    while _G.AutoFarm do wait()
                                                        if Inventory:GetAttribute("Wood") >= 50 then
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 0
                                                            wait(8.5)
                                                            game:GetService("Workspace"):FindFirstChild("Character"):FindFirstChild(game.Players.LocalPlayer.Name):FindFirstChild("HumanoidRootPart").CFrame = CFrame.new(2846.16187, 5.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)
                                                            wait(2.5)
                                                            local args = {
                                                                [1] = "fire",
                                                                [3] = "Economy",
                                                                [4] = FarmName,
                                                                [5] = Inventory:GetAttribute("Wood")
                                                            }

                                                            game:GetService("ReplicatedStorage"):WaitForChild("Modules"):WaitForChild("NetworkFramework"):WaitForChild("NetworkEvent"):FireServer(unpack(args))
                                                            wait(10)
                                                            bypass_teleport(teleport_table.location2)
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 27
                                                        end
                                                    end
        elseif FarmName == "ScrapIron" then
                                                            local JU = game:GetService("Workspace"):FindFirstChild("JU")
                                                            if JU then
                                                                JU:Destroy()
                                                            end
                                                        local Noclip = Instance.new("Part", workspace)
                                                            Noclip.Name = "JU"
                                                            Noclip.CanCollide = true
                                                            Noclip.Anchored = true
                                                            Noclip.Transparency = 0.5
                                                            Noclip.Size = Vector3.new(30, 1, 30)
                                                            game:GetService("Workspace"):FindFirstChild("JU").CFrame = CFrame.new(2846.16187, 3.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)

                                                    local teleport_table = {
                                                        location1 = Vector3.new(2845.45142, 14.2436848, 2079.27222, -0.388715088, 1.28141585e-06, -0.921357989, -1.4877221e-06, 1, 2.01845091e-06, 0.921357989, 2.15532691e-06, -0.388715088),
                                                        location2 = Vector3.new(1087, 13, 3701)
                                                    }

                                                    local tween_s = game:GetService('TweenService')
                                                    local tweeninfo = TweenInfo.new(0,Enum.EasingStyle.Linear)

                                                    local lp = game.Players.LocalPlayer

                                                    function bypass_teleport(v)
                                                        if lp.Character and 
                                                        lp.Character:FindFirstChild('HumanoidRootPart') then
                                                            local cf = CFrame.new(v)
                                                            local a = tween_s:Create(lp.Character.HumanoidRootPart,tweeninfo,{CFrame=cf})
                                                            a:Play()
                                                            a.Completed:Wait()
                                                            print('Teleporting Done!')
                                                        end
                                                    end

                                                    bypass_teleport(teleport_table.location2)

                                                    local Players = game:GetService("Players")

                                                    local LocalPlayer = Players.LocalPlayer

                                                    local Inventory = LocalPlayer.Inventory

                                                    _G.AutoFarm = t

                                                    while _G.AutoFarm do wait()
                                                        if Inventory:GetAttribute("ScrapIron") >= 290 then
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 0
                                                            wait(8.5)
                                                            game:GetService("Workspace"):FindFirstChild("Character"):FindFirstChild(game.Players.LocalPlayer.Name):FindFirstChild("HumanoidRootPart").CFrame = CFrame.new(2846.16187, 5.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)
                                                            wait(2.5)
                                                            local args = {
                                                                [1] = "fire",
                                                                [3] = "Economy",
                                                                [4] = FarmName,
                                                                [5] = Inventory:GetAttribute("ScrapIron")
                                                            }

                                                            game:GetService("ReplicatedStorage"):WaitForChild("Modules"):WaitForChild("NetworkFramework"):WaitForChild("NetworkEvent"):FireServer(unpack(args))
                                                            wait(10)
                                                            bypass_teleport(teleport_table.location2)
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 27
                                                        end
                                                    end
        elseif FarmName == "Rock" then
                                                            local JU = game:GetService("Workspace"):FindFirstChild("JU")
                                                            if JU then
                                                                JU:Destroy()
                                                            end
                                                        local Noclip = Instance.new("Part", workspace)
                                                            Noclip.Name = "JU"
                                                            Noclip.CanCollide = true
                                                            Noclip.Anchored = true
                                                            Noclip.Transparency = 0.5
                                                            Noclip.Size = Vector3.new(30, 1, 30)
                                                            game:GetService("Workspace"):FindFirstChild("JU").CFrame = CFrame.new(2846.16187, 3.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)

                                                    local teleport_table = {
                                                        location1 = Vector3.new(2845.45142, 14.2436848, 2079.27222, -0.388715088, 1.28141585e-06, -0.921357989, -1.4877221e-06, 1, 2.01845091e-06, 0.921357989, 2.15532691e-06, -0.388715088),
                                                        location2 = Vector3.new(-272, -92, -2066)
                                                    }

                                                    local tween_s = game:GetService('TweenService')
                                                    local tweeninfo = TweenInfo.new(0,Enum.EasingStyle.Linear)

                                                    local lp = game.Players.LocalPlayer

                                                    function bypass_teleport(v)
                                                        if lp.Character and 
                                                        lp.Character:FindFirstChild('HumanoidRootPart') then
                                                            local cf = CFrame.new(v)
                                                            local a = tween_s:Create(lp.Character.HumanoidRootPart,tweeninfo,{CFrame=cf})
                                                            a:Play()
                                                            a.Completed:Wait()
                                                            print('Teleporting Done!')
                                                        end
                                                    end

                                                    bypass_teleport(teleport_table.location2)

                                                    local Players = game:GetService("Players")

                                                    local LocalPlayer = Players.LocalPlayer

                                                    local Inventory = LocalPlayer.Inventory

                                                    _G.AutoFarm = t

                                                    while _G.AutoFarm do wait()
                                                        if Inventory:GetAttribute("Rock") >= 90 then
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 0
                                                            wait(8.5)
                                                            game:GetService("Workspace"):FindFirstChild("Character"):FindFirstChild(game.Players.LocalPlayer.Name):FindFirstChild("HumanoidRootPart").CFrame = CFrame.new(2846.16187, 5.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)
                                                            wait(2.5)
                                                            local args = {
                                                                [1] = "fire",
                                                                [3] = "Economy",
                                                                [4] = FarmName,
                                                                [5] = Inventory:GetAttribute("Rock")
                                                            }

                                                            game:GetService("ReplicatedStorage"):WaitForChild("Modules"):WaitForChild("NetworkFramework"):WaitForChild("NetworkEvent"):FireServer(unpack(args))
                                                            wait(10)
                                                            bypass_teleport(teleport_table.location2)
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 27
                                                        end
                                                    end
        elseif FarmName == "Pork" then
                                                                        local JU = game:GetService("Workspace"):FindFirstChild("JU")
                                                            if JU then
                                                                JU:Destroy()
                                                            end
                                                        local Noclip = Instance.new("Part", workspace)
                                                            Noclip.Name = "JU"
                                                            Noclip.CanCollide = true
                                                            Noclip.Anchored = true
                                                            Noclip.Transparency = 0.5
                                                            Noclip.Size = Vector3.new(30, 1, 30)
                                                            game:GetService("Workspace"):FindFirstChild("JU").CFrame = CFrame.new(2846.16187, 3.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)

                                                    local teleport_table = {
                                                        location1 = Vector3.new(2845.45142, 14.2436848, 2079.27222, -0.388715088, 1.28141585e-06, -0.921357989, -1.4877221e-06, 1, 2.01845091e-06, 0.921357989, 2.15532691e-06, -0.388715088),
                                                        location2 = Vector3.new(-594, 14, 2344)
                                                    }

                                                    local tween_s = game:GetService('TweenService')
                                                    local tweeninfo = TweenInfo.new(0,Enum.EasingStyle.Linear)

                                                    local lp = game.Players.LocalPlayer

                                                    function bypass_teleport(v)
                                                        if lp.Character and 
                                                        lp.Character:FindFirstChild('HumanoidRootPart') then
                                                            local cf = CFrame.new(v)
                                                            local a = tween_s:Create(lp.Character.HumanoidRootPart,tweeninfo,{CFrame=cf})
                                                            a:Play()
                                                            a.Completed:Wait()
                                                            print('Teleporting Done!')
                                                        end
                                                    end

                                                    bypass_teleport(teleport_table.location2)

                                                    local Players = game:GetService("Players")

                                                    local LocalPlayer = Players.LocalPlayer

                                                    local Inventory = LocalPlayer.Inventory

                                                    _G.AutoFarm = t

                                                    while _G.AutoFarm do wait()
                                                        if Inventory:GetAttribute("Pork") >= 50 then
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 0
                                                            wait(8.5)
                                                            game:GetService("Workspace"):FindFirstChild("Character"):FindFirstChild(game.Players.LocalPlayer.Name):FindFirstChild("HumanoidRootPart").CFrame = CFrame.new(2846.16187, 5.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)
                                                            wait(2.5)
                                                            local args = {
                                                                [1] = "fire",
                                                                [3] = "Economy",
                                                                [4] = FarmName,
                                                                [5] = Inventory:GetAttribute("Pork")
                                                            }

                                                            game:GetService("ReplicatedStorage"):WaitForChild("Modules"):WaitForChild("NetworkFramework"):WaitForChild("NetworkEvent"):FireServer(unpack(args))
                                                            wait(10)
                                                            bypass_teleport(teleport_table.location2)
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 27
                                                        end
                                                    end
        elseif FarmName == "Plant" then        
                                                                                    local JU = game:GetService("Workspace"):FindFirstChild("JU")
                                                            if JU then
                                                                JU:Destroy()
                                                            end
                                                        local Noclip = Instance.new("Part", workspace)
                                                            Noclip.Name = "JU"
                                                            Noclip.CanCollide = true
                                                            Noclip.Anchored = true
                                                            Noclip.Transparency = 0.5
                                                            Noclip.Size = Vector3.new(30, 1, 30)
                                                            game:GetService("Workspace"):FindFirstChild("JU").CFrame = CFrame.new(2846.16187, 3.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)

                                                    local teleport_table = {
                                                        location1 = Vector3.new(2845.45142, 14.2436848, 2079.27222, -0.388715088, 1.28141585e-06, -0.921357989, -1.4877221e-06, 1, 2.01845091e-06, 0.921357989, 2.15532691e-06, -0.388715088),
                                                        location2 = Vector3.new(2127, 14, -3308)
                                                    }

                                                    local tween_s = game:GetService('TweenService')
                                                    local tweeninfo = TweenInfo.new(0,Enum.EasingStyle.Linear)

                                                    local lp = game.Players.LocalPlayer

                                                    function bypass_teleport(v)
                                                        if lp.Character and 
                                                        lp.Character:FindFirstChild('HumanoidRootPart') then
                                                            local cf = CFrame.new(v)
                                                            local a = tween_s:Create(lp.Character.HumanoidRootPart,tweeninfo,{CFrame=cf})
                                                            a:Play()
                                                            a.Completed:Wait()
                                                            print('Teleporting Done!')
                                                        end
                                                    end

                                                    bypass_teleport(teleport_table.location2)

                                                    local Players = game:GetService("Players")

                                                    local LocalPlayer = Players.LocalPlayer

                                                    local Inventory = LocalPlayer.Inventory

                                                    _G.AutoFarm = t

                                                    while _G.AutoFarm do wait()
                                                        if Inventory:GetAttribute("Plant") >= 50 then
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 0
                                                            wait(8.5)
                                                            game:GetService("Workspace"):FindFirstChild("Character"):FindFirstChild(game.Players.LocalPlayer.Name):FindFirstChild("HumanoidRootPart").CFrame = CFrame.new(2846.16187, 5.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)
                                                            wait(2.5)
                                                            local args = {
                                                                [1] = "fire",
                                                                [3] = "Economy",
                                                                [4] = FarmName,
                                                                [5] = Inventory:GetAttribute("Plant")
                                                            }

                                                            game:GetService("ReplicatedStorage"):WaitForChild("Modules"):WaitForChild("NetworkFramework"):WaitForChild("NetworkEvent"):FireServer(unpack(args))
                                                            wait(10)
                                                            bypass_teleport(teleport_table.location2)
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 27
                                                        end
                                                    end
        elseif FarmName == "Flower" then        
                                                                                                local JU = game:GetService("Workspace"):FindFirstChild("JU")
                                                            if JU then
                                                                JU:Destroy()
                                                            end
                                                        local Noclip = Instance.new("Part", workspace)
                                                            Noclip.Name = "JU"
                                                            Noclip.CanCollide = true
                                                            Noclip.Anchored = true
                                                            Noclip.Transparency = 0.5
                                                            Noclip.Size = Vector3.new(30, 1, 30)
                                                            game:GetService("Workspace"):FindFirstChild("JU").CFrame = CFrame.new(2846.16187, 3.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)

                                                    local teleport_table = {
                                                        location1 = Vector3.new(2845.45142, 14.2436848, 2079.27222, -0.388715088, 1.28141585e-06, -0.921357989, -1.4877221e-06, 1, 2.01845091e-06, 0.921357989, 2.15532691e-06, -0.388715088),
                                                        location2 = Vector3.new(3016, 14, -876)
                                                    }

                                                    local tween_s = game:GetService('TweenService')
                                                    local tweeninfo = TweenInfo.new(0,Enum.EasingStyle.Linear)

                                                    local lp = game.Players.LocalPlayer

                                                    function bypass_teleport(v)
                                                        if lp.Character and 
                                                        lp.Character:FindFirstChild('HumanoidRootPart') then
                                                            local cf = CFrame.new(v)
                                                            local a = tween_s:Create(lp.Character.HumanoidRootPart,tweeninfo,{CFrame=cf})
                                                            a:Play()
                                                            a.Completed:Wait()
                                                            print('Teleporting Done!')
                                                        end
                                                    end

                                                    bypass_teleport(teleport_table.location2)

                                                    local Players = game:GetService("Players")

                                                    local LocalPlayer = Players.LocalPlayer

                                                    local Inventory = LocalPlayer.Inventory

                                                    _G.AutoFarm = t

                                                    while _G.AutoFarm do wait()
                                                        if Inventory:GetAttribute("Flower") >= 290 then
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 0
                                                            wait(8.5)
                                                            game:GetService("Workspace"):FindFirstChild("Character"):FindFirstChild(game.Players.LocalPlayer.Name):FindFirstChild("HumanoidRootPart").CFrame = CFrame.new(2846.16187, 5.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)
                                                            wait(2.5)
                                                            local args = {
                                                                [1] = "fire",
                                                                [3] = "Economy",
                                                                [4] = FarmName,
                                                                [5] = Inventory:GetAttribute("Flower")
                                                            }

                                                            game:GetService("ReplicatedStorage"):WaitForChild("Modules"):WaitForChild("NetworkFramework"):WaitForChild("NetworkEvent"):FireServer(unpack(args))
                                                            wait(10)
                                                            bypass_teleport(teleport_table.location2)
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 27
                                                        end
                                                    end
        elseif FarmName == "Corn" then        
                                                                                                            local JU = game:GetService("Workspace"):FindFirstChild("JU")
                                                            if JU then
                                                                JU:Destroy()
                                                            end
                                                        local Noclip = Instance.new("Part", workspace)
                                                            Noclip.Name = "JU"
                                                            Noclip.CanCollide = true
                                                            Noclip.Anchored = true
                                                            Noclip.Transparency = 0.5
                                                            Noclip.Size = Vector3.new(30, 1, 30)
                                                            game:GetService("Workspace"):FindFirstChild("JU").CFrame = CFrame.new(2846.16187, 3.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)

                                                    local teleport_table = {
                                                        location1 = Vector3.new(2845.45142, 14.2436848, 2079.27222, -0.388715088, 1.28141585e-06, -0.921357989, -1.4877221e-06, 1, 2.01845091e-06, 0.921357989, 2.15532691e-06, -0.388715088),
                                                        location2 = Vector3.new(-205, 49, 533)
                                                    }

                                                    local tween_s = game:GetService('TweenService')
                                                    local tweeninfo = TweenInfo.new(0,Enum.EasingStyle.Linear)

                                                    local lp = game.Players.LocalPlayer

                                                    function bypass_teleport(v)
                                                        if lp.Character and 
                                                        lp.Character:FindFirstChild('HumanoidRootPart') then
                                                            local cf = CFrame.new(v)
                                                            local a = tween_s:Create(lp.Character.HumanoidRootPart,tweeninfo,{CFrame=cf})
                                                            a:Play()
                                                            a.Completed:Wait()
                                                            print('Teleporting Done!')
                                                        end
                                                    end

                                                    bypass_teleport(teleport_table.location2)

                                                    local Players = game:GetService("Players")

                                                    local LocalPlayer = Players.LocalPlayer

                                                    local Inventory = LocalPlayer.Inventory

                                                    _G.AutoFarm = t

                                                    while _G.AutoFarm do wait()
                                                        if Inventory:GetAttribute("Corn") >= 50 then
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 0
                                                            wait(8.5)
                                                            game:GetService("Workspace"):FindFirstChild("Character"):FindFirstChild(game.Players.LocalPlayer.Name):FindFirstChild("HumanoidRootPart").CFrame = CFrame.new(2846.16187, 5.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)
                                                            wait(2.5)
                                                            local args = {
                                                                [1] = "fire",
                                                                [3] = "Economy",
                                                                [4] = FarmName,
                                                                [5] = Inventory:GetAttribute("Corn")
                                                            }

                                                            game:GetService("ReplicatedStorage"):WaitForChild("Modules"):WaitForChild("NetworkFramework"):WaitForChild("NetworkEvent"):FireServer(unpack(args))
                                                            wait(10)
                                                            bypass_teleport(teleport_table.location2)
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 27
                                                        end
                                                    end
        elseif FarmName == "Banana" then        
                                                                                                            local JU = game:GetService("Workspace"):FindFirstChild("JU")
                                                            if JU then
                                                                JU:Destroy()
                                                            end
                                                        local Noclip = Instance.new("Part", workspace)
                                                            Noclip.Name = "JU"
                                                            Noclip.CanCollide = true
                                                            Noclip.Anchored = true
                                                            Noclip.Transparency = 0.5
                                                            Noclip.Size = Vector3.new(30, 1, 30)
                                                            game:GetService("Workspace"):FindFirstChild("JU").CFrame = CFrame.new(2846.16187, 3.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)

                                                    local teleport_table = {
                                                        location1 = Vector3.new(2845.45142, 14.2436848, 2079.27222, -0.388715088, 1.28141585e-06, -0.921357989, -1.4877221e-06, 1, 2.01845091e-06, 0.921357989, 2.15532691e-06, -0.388715088),
                                                        location2 = Vector3.new(72, 14, -358)
                                                    }

                                                    local tween_s = game:GetService('TweenService')
                                                    local tweeninfo = TweenInfo.new(0,Enum.EasingStyle.Linear)

                                                    local lp = game.Players.LocalPlayer

                                                    function bypass_teleport(v)
                                                        if lp.Character and 
                                                        lp.Character:FindFirstChild('HumanoidRootPart') then
                                                            local cf = CFrame.new(v)
                                                            local a = tween_s:Create(lp.Character.HumanoidRootPart,tweeninfo,{CFrame=cf})
                                                            a:Play()
                                                            a.Completed:Wait()
                                                            print('Teleporting Done!')
                                                        end
                                                    end

                                                    bypass_teleport(teleport_table.location2)

                                                    local Players = game:GetService("Players")

                                                    local LocalPlayer = Players.LocalPlayer

                                                    local Inventory = LocalPlayer.Inventory

                                                    _G.AutoFarm = t

                                                    while _G.AutoFarm do wait()
                                                        if Inventory:GetAttribute("Corn") >= 50 then
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 0
                                                            wait(8.5)
                                                            game:GetService("Workspace"):FindFirstChild("Character"):FindFirstChild(game.Players.LocalPlayer.Name):FindFirstChild("HumanoidRootPart").CFrame = CFrame.new(2846.16187, 5.34974432, 2078.43701, -0.585431039, -0.0284520276, -0.810222805, -1.68365466e-09, 0.999383986, -0.0350946672, 0.810722172, -0.0205455068, -0.585070431)
                                                            wait(2.5)
                                                            local args = {
                                                                [1] = "fire",
                                                                [3] = "Economy",
                                                                [4] = FarmName,
                                                                [5] = Inventory:GetAttribute("Banana")
                                                            }

                                                            game:GetService("ReplicatedStorage"):WaitForChild("Modules"):WaitForChild("NetworkFramework"):WaitForChild("NetworkEvent"):FireServer(unpack(args))
                                                            wait(10)
                                                            bypass_teleport(teleport_table.location2)
                                                            game.Workspace.Character[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = 27
                                                        end
                                                    end
            end
	end    
})

Tab:AddButton({
	Name = "Teleport",
	Callback = function()
      	if FarmName == "Wood" then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1268, 14, -1705)
        elseif FarmName == "ScrapIron" then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1087, 13, 3701)
        elseif FarmName == "Rock" then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-272, -92, -2066)
        elseif FarmName == "Pork" then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-594, 14, 2344)
        elseif FarmName == "Plant" then        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2127, 14, -3308)
        elseif FarmName == "Giftbox" then        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1390, 128, 1195)
        elseif FarmName == "Flower" then        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(3016, 14, -876)
        elseif FarmName == "Corn" then        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-205, 49, 533)
        elseif FarmName == "Banana" then        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(72, 14, -358)
        end
  	end    
})









