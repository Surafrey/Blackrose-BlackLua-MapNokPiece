local BlackLuaGui = game:GetService("CoreGui"):FindFirstChild('BlackLua Map Nok Piece')
    if BlackLuaGui then
        BlackLuaGui:Destroy()
end

local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/GreenDeno/Venyx-UI-Library/main/source.lua"))()
local BlackLua = library.new('BlackLua Map Nok Piece')

    local AutoFarmBlackLua = BlackLua:addPage('Auto Farm' , 7040391851)
    local AutoSkill = BlackLua:addPage('Auto Skill' , 6034684949)
    local AutoStats = BlackLua:addPage('Auto Stats' , 6031225816)
    local Island = BlackLua:addPage('Island' , 6022668945)
    local Function = BlackLua:addPage('Function' , 7252023075)
    
    local SecAutoFarm = AutoFarmBlackLua:addSection('AuTo Farm : Test')
    local SecAutoFarmBoss = AutoFarmBlackLua:addSection('Auto FarmBoss LV ??? (Not Work)')
    local SecAutoSkill = AutoSkill:addSection('Auto Skill : You love me?')
    local SecAutoStats = AutoStats:addSection('Auto Stats')
    local SecIsland = Island:addSection('Where are you going?')
    local SecFunctionGui = Function:addSection("Function GuI")
    local SecFunctionPlus = Function:addSection('Function Plus')

        SecAutoFarm:addToggle('Auto GetQuest' , false , function(value)
            _G.AutoQuest = value
        end)
        
        SecAutoFarm:addToggle('Auto Farm No Quest (Not Work Lv 650 - 750 ) ' , false , function(ValueAutoFram)
            _G.AutoFarm = ValueAutoFram
        end)
        
        function EquipWeapon(ToolSe)
        if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
            local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
            wait(.4)
            game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
        end
        end  

        Weapon = {}
            for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
                if v:IsA"Tool" then
                    table.insert(Weapon,v.Name)
            end
        end
            
        local SELECTWEAPON = SecAutoFarm:addDropdown("Select Weapon",Weapon,function(t)
                _G.SelectWeapon = t
            end)    
        
        SecAutoFarm:addButton("ReSet Weapon",function()
        table.clear(Weapon)
        for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
        if v:IsA("Tool") then
        SELECTWEAPON:Add(v.Name)
                end
            end
        end)
        
        SecAutoSkill:addToggle('Auto Skill E' , false ,function(VALUEAUTOSILLE)
            _G.AUTOSKILLE = VALUEAUTOSILLE
        end)
        
        SecAutoSkill:addToggle('Auto Skill Z' , false ,function(VALUEAUTOSILLZ)
            _G.AUTOSKILLZ = VALUEAUTOSILLZ
        end)
        
        SecAutoSkill:addToggle('Auto Skill X' , false ,function(VALUEAUTOSILLX)
            _G.AUTOSKILLX = VALUEAUTOSILLX
        end)
        
        SecAutoSkill:addToggle('Auto Skill C' , false, function(VALUEAUTOSILLC)
            _G.AUTOSKILLC = VALUEAUTOSILLC
        end)
        
        SecAutoSkill:addToggle('Auto Skill V' , false, function(VALUEAUTOSILLV)
            _G.AUTOSKILLV = VALUEAUTOSILLV
        end)
        
        SecAutoStats:addToggle('Auto Stat Strength' , false , function(ValueStrength)
            _G.AutoStrength = ValueStrength
        end)
        
        SecAutoStats:addToggle('Auto Stat Sword' , false , function(ValueSword)
            _G.AutoSword = ValueSword
        end)
        
        SecAutoStats:addToggle('Auto Stat DevilFruit' , false , function(ValueDevilFruit)
            _G.AutoDevilFruit = ValueDevilFruit
        end)
        
        SecAutoStats:addToggle('Auto Stat Defense' , false , function(ValueDefense)
            _G.AutoDefense = ValueDefense
        end)
        
        SecIsland:addButton('Bandit Island' , function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(188.290451, -68.8816605, -659.209045, -0.998882055, -3.1040635e-08, -0.0472720712, -2.82679196e-08, 1, -5.9322943e-08, 0.0472720712, -5.79203387e-08, -0.998882055)
        end)
        
        SecIsland:addButton('Clown Island' , function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2510.15088, -73.5035706, 644.299988, -0.999955952, 8.37054088e-08, 0.00938345864, 8.26962818e-08, 1, -1.07931186e-07, -0.00938345864, -1.07150456e-07, -0.999955952)
        end)
        
        SecIsland:addButton('Fishman Island' , function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2810.50464, -84.2314453, -2640.46582, -0.0386906788, 0.000229172452, -0.999250948, -2.07773937e-05, 1, 0.000230148697, 0.999250948, 2.96664202e-05, -0.0386906788)
        end)
        
        SecIsland:addButton('Marine Island' , function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-44.9789314, 181.618027, 4164.61572, 0.999081671, 2.70249052e-06, -0.042846255, -2.65223616e-06, 1, 1.2297495e-06, 0.042846255, -1.1149815e-06, 0.999081671)
        end)
        
        SecIsland:addButton('Restaurant Ship Island' , function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-312.00061, -9.81440639, -5942.45996, 0.999998033, 7.19870457e-08, -0.00197183341, -7.20774693e-08, 1, -4.57869547e-08, 0.00197183341, 4.59289922e-08, 0.999998033)
        end)
        
        SecIsland:addButton('Desert Island Island' , function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5311.05566, -67.6391296, 4298.2373, -0.0483426228, -5.08638664e-07, 0.998831153, -1.28093473e-06, 1, 4.47237085e-07, -0.998831153, -1.2578173e-06, -0.0483426228)
        end)
        
        SecIsland:addButton('Sky 1' , function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(3761.66724, 1626.00281, 4837.49365, -0.211930141, -9.69561071e-08, -0.977284849, 5.20542244e-07, 1, -2.12092417e-07, 0.977284849, -5.53666723e-07, -0.211930141)
            
        end)
        
        SecIsland:addButton('Sky 2' , function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(4009.96704, 1866.22693, 2305.78491, -0.996073723, 1.0923835e-07, -0.0885274932, 1.07568454e-07, 1, 2.36337971e-08, 0.0885274932, 1.40182399e-08, -0.996073723)
        end)
        
        SecIsland:addButton('Snow Island' , function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(6157.99023, -69.0996933, 2991.52441, 0.999891162, 2.03796198e-08, -0.014754911, -1.93257712e-08, 1, 7.15661912e-08, 0.014754911, -7.12732557e-08, 0.999891162)
        end)
        
        SecFunctionGui:addKeybind("Toggle Keybind", Enum.KeyCode.RightControl, function()
            BlackLua:toggle()
            end , function()
        end)
        

        SecFunctionPlus:addButton('Copy CFrame' , function()
            setclipboard(tostring(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame))
        end)

        SecFunctionPlus:addButton('Rejoin' , function()
            game:GetService("TeleportService"):Teleport(game.PlaceId, game:GetService("Players").LocalPlayer)
        end)
        
        SecFunctionPlus:addButton('Remote' , function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/exxtremestuffs/SimpleSpySource/master/SimpleSpy.lua"))()
        end)
        
-- function TP

function TP(ValueTP) 
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = ValueTP
end

-- function YourLv
function GetQuest()
    fireclickdetector(game:GetService("Workspace").Quest[NameQuest].ClickDetector)
    wait(0.1)
    game:GetService("Players").LocalPlayer.PlayerGui.QuestDisplay.Enabled = true
end

function YourLv()
    local Lv = game:GetService("Players").LocalPlayer.Data.Level.Value
        if Lv == 1 or Lv <= 14 then
            Mon = 'Bandit LV. 1'
            NameMon = 'Bandit'
            NameQuest = 'Bandit Quest'
            CFrameQuest = CFrame.new(309.610626, -77.0029068, -649.314758, 0.00500066346, 1.969244e-13, -0.999987483, -1.60908087e-08, 1, -8.02687986e-11, 0.999987483, 1.60910076e-08, 0.00500066346)
        elseif Lv == 15 or Lv <= 24 then
            Mon = 'Blue Hair Pirate LV. 15'
            NameMon = 'Blue'
            NameQuest = 'Blue Hair Quest'
            CFrameQuest = CFrame.new(186.661911, -77.4029083, -802.818604, 0.996393383, -4.63621994e-08, 0.0848543048, 4.63774548e-08, 1, 1.79142123e-09, -0.0848543048, 2.15036655e-09, 0.996393383)
        elseif Lv == 25 or Lv <= 49 then
            Mon = 'Clown Pirate LV. 25'
            NameMon = 'ClownP'
            NameQuest = 'Clown Pirate'
            CFrameQuest = CFrame.new(-2612.05054, -74.1158829, 691.766663, -0.0111457044, -3.83060197e-08, 0.999937892, -1.22707169e-08, 1, 3.81716241e-08, -0.999937892, -1.18445049e-08, -0.0111457044)
        elseif Lv == 50 or Lv <= 74 then
            Mon = 'Clown Captain LV. 50'
            NameMon = 'ClownC'
            NameQuest = 'Clown Captain'
            CFrameQuest = CFrame.new(-2532.91016, -73.9904633, 682.70282, -0.00964645948, -7.43733269e-11, -0.999953449, -4.10701195e-10, 1, -7.04147851e-11, 0.999953449, 4.10002837e-10, -0.00964645948)
        elseif Lv == 75 or Lv <= 99 then
            Mon = 'Fishman Pirate LV. 75'
            NameMon = 'FishmanP'
            NameQuest ='Fishman Pirate'
            CFrameQuest = CFrame.new(-2633.15308, -83.1915054, -2685.92773, -0.705699623, 7.51078488e-08, 0.708511174, 7.17821935e-09, 1, -9.88582656e-08, -0.708511174, -6.46783889e-08, -0.705699623)
        elseif Lv == 100 or Lv <= 149 then
            Mon = 'Fishman Captain LV. 100'  and 'Fishman Pirate LV. 75'
            NameMon = 'FishmanC' and 'FishmanP'
            NameQuest = 'Fishman Captain'
            CFrameQuest = CFrame.new(-2664.14233, -83.6780624, -2652.92212, 0.999900639, -2.29401671e-08, -0.0140978163, 2.4746555e-08, 1, 1.27957946e-07, 0.0140978163, -1.2829409e-07, 0.999900639)
        elseif Lv == 150 or Lv <= 199 then
            Mon = 'Marine LV. 150'
            NameMon = 'Marine'
            NameQuest = 'MarineQUest'
            CFrameQuest = CFrame.new(-260.934357, -72.5353394, 3519.44922, -0.00487919711, 4.45836346e-09, 0.999988079, -2.36216907e-10, 1, -4.45956916e-09, -0.999988079, -2.57973226e-10, -0.00487919711)
        elseif Lv == 200 or Lv <= 249 then
            Mon = 'Smokeman LV. 200' and 'Marine LV. 150'
            NameMon = 'Smoke' and 'Marine'
            NameQuest = 'Smokeman'
            CFrameQuest = CFrame.new(-57.0223656, 53.5396385, 3965.71631, 0.999848187, -1.02759621e-07, 0.0174254719, 1.02772404e-07, 1, 1.61774497e-10, -0.0174254719, 1.62910763e-09, 0.999848187)
        elseif Lv == 250 or Lv <= 299 then
            Mon = 'Chef Pirate LV. 250'
            NameMon = 'Chef'
            NameQuest = 'ChefPirateQuest'
            CFrameQuest = CFrame.new(-435.233826, -75.7741013, -5833.38379, 0.581290483, -3.75609055e-09, -0.813696146, 4.37560477e-09, 1, -1.49022861e-09, 0.813696146, -2.69415712e-09, 0.581290483)
        elseif Lv == 300 or Lv <= 349 then
            Mon = 'Golden Armour Pirate LV. 300'
            NameMon = 'Golden'
            NameQuest = 'Golden Armour Quest'
            CFrameQuest = CFrame.new(-267.582397, -71.7318649, -5997.85938, -0.888764143, 4.25987494e-08, 0.458364874, 2.16206324e-08, 1, -5.10141795e-08, -0.458364874, -3.54294336e-08, -0.888764143)
        elseif Lv == 350 or Lv <= 399 then
            Mon = 'Blackleg Chef LV. 350'
            NameMon = 'Blackleg'
            NameQuest = 'Blackleg Man'
            CFrameQuest = CFrame.new(-349.85025, -9.37687492, -5873.43018, 0.999720275, 1.45395767e-08, 0.0236490201, -1.47710306e-08, 1, 9.61233404e-09, -0.0236490201, -9.95896698e-09, 0.999720275)
        elseif Lv == 400 or Lv <= 499 then
            Mon = 'Desert Pirate LV. 400'
            NameMon = 'Desert'
            NameQuest = 'Mr Bomb'
            CFrameQuest = CFrame.new(-5334.41602, -67.4241867, 4224.21729, -0.999511123, -1.41052841e-08, -0.0312653892, -1.8337353e-08, 1, 1.35072796e-07, 0.0312653892, 1.35580095e-07, -0.999511123)
        elseif Lv == 500 or Lv <= 574 then
            Mon = 'Sky Bandit LV. 500'
            NameMon = 'SkyB'
            NameQuest = 'Sky Bandit'
            CFrameQuest = CFrame.new(3643.9248, 1689.63416, 4768.27148, -0.767415285, 3.32930412e-08, -0.641150355, 3.70508104e-08, 1, 7.57963381e-09, 0.641150355, -1.79384116e-08, -0.767415285)
        elseif Lv == 575 or Lv <= 649 then
            Mon = 'Sky Pirate LV. 575'
            NameMon = 'SkyP'
            NameQuest = 'SkyPirateQuest'
            CFrameQuest = CFram.new(4003.75024, 1866.94812, 2304.46387, -0.992277861, -1.25066331e-08, -0.1240348, -1.44993484e-09, 1, -8.92321737e-08, 0.1240348, -8.83632651e-08, -0.992277861)
--[[
        elseif Lv == 650 or Lv <= 750 then
            Mon = 'Snow Pirate LV. 650'
            NameMon = 'Snow'
            NameQuest = 'SkyPirateQuest'
            CFrameQuest = CFrame.new(6264.55225, -23.1725445, 2850.19531, 0.313084066, -3.76711498e-08, 0.949725449, 9.12607874e-08, 1, 9.58050883e-09, -0.949725449, 8.36731857e-08, 0.313084066)
]]
        
end
end
-- spawn function

spawn(function()
        game:GetService("RunService").Heartbeat:Connect(function()
        if _G.AutoFarm then
        if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Humanoid") then
            setfflag("HumanoidParallelRemoveNoPhysics", "False")
            setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
            game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
            end
        end
    end)
end)

spawn(function()
    while wait() do
        if _G.AutoFarm then
        pcall(function()
        YourLv()
        EquipWeapon(_G.SelectWeapon)
        Click()
        for i, v in pairs(game:GetService("Workspace").Lives:GetDescendants()) do
        if v.Name == Mon and v:FindFirstChild('HumanoidRootPart') and v:FindFirstChild('Humanoid') then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.Angles(math.rad(90),0,0) * CFrame.new(0,0,0)
                    end
                end
            end)
        end
    end
end)

spawn(function()
    while wait() do
        pcall(function()
        if _G.AutoQuest then
            YourLv()
                repeat wait()
                    if game:GetService("Players").LocalPlayer.PlayerGui.QuestDisplay.Dialogue.Visible == false then
                    TP(CFrameQuest)
                    wait(.1)
                    GetQuest()
                      wait(0.1)
                      game:GetService("Players").LocalPlayer.PlayerGui.QuestDisplay.Enabled = true
                      end
                until not _G.AutoQuest
            end
        end)
    end
end)

-- Click 

function Click()
   game:GetService'VirtualUser':CaptureController()
   game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
end


-- Spawn Stats
spawn(function()
    while wait() do
        if _G.AUTOSKILLX then
            game:GetService("VirtualInputManager"):SendKeyEvent(true,101,false,game.Players.LocalPlayer.Character.HumanoidRootPart)
            game:GetService("VirtualInputManager"):SendKeyEvent(false,101,false,game.Players.LocalPlayer.Character.HumanoidRootPart)
        end
    end
end)

spawn(function()
    while wait() do
        if _G.AUTOSKILLZ then
            game:GetService("VirtualInputManager"):SendKeyEvent(true,122,false,game.Players.LocalPlayer.Character.HumanoidRootPart)
            game:GetService("VirtualInputManager"):SendKeyEvent(false,122,false,game.Players.LocalPlayer.Character.HumanoidRootPart)
        end
    end
end)

spawn(function()
    while wait() do
        if _G.AUTOSKILLX then
            game:GetService("VirtualInputManager"):SendKeyEvent(true,120,false,game.Players.LocalPlayer.Character.HumanoidRootPart)
            game:GetService("VirtualInputManager"):SendKeyEvent(false,120,false,game.Players.LocalPlayer.Character.HumanoidRootPart)
        end
    end
end)

spawn(function()
    while wait() do
        if _G.AUTOSKILLC then
            game:GetService("VirtualInputManager"):SendKeyEvent(true,99,false,game.Players.LocalPlayer.Character.HumanoidRootPart)
            game:GetService("VirtualInputManager"):SendKeyEvent(false,99,false,game.Players.LocalPlayer.Character.HumanoidRootPart)
        end
    end
end)

spawn(function()
    while wait() do
        if _G.AUTOSKILLV then
            game:GetService("VirtualInputManager"):SendKeyEvent(true,118,false,game.Players.LocalPlayer.Character.HumanoidRootPart)
            game:GetService("VirtualInputManager"):SendKeyEvent(false,118,false,game.Players.LocalPlayer.Character.HumanoidRootPart)
        end
    end
end)

spawn(function()
    while wait() do 
        if _G.AutoStrength then
        repeat 
            wait()
                game:GetService("ReplicatedStorage").UpdateStats:FireServer('StrengthText' , 1)
            until 
                _G.AutoStrength == false
        end
    end
end)

spawn(function()
    while wait() do 
        if _G.AutoSword then
        repeat 
            wait()
                game:GetService("ReplicatedStorage").UpdateStats:FireServer('SwordText' , 1 )
            until 
                _G.AutoStrength == false
        end
    end
end)

spawn(function()
    while wait() do 
        if _G.AutoDevilFruit then
        repeat 
            wait()
                game:GetService("ReplicatedStorage").UpdateStats:FireServer('DevilFruitText' , 1)
            until 
                _G.AutoStrength == false
        end
    end
end)

spawn(function()
    while wait() do 
        if _G.AutoDefense then
        repeat 
            wait()
                game:GetService("ReplicatedStorage").UpdateStats:FireServer('DefenseText' , 1)
            until 
                _G.AutoStrength == false
        end
    end
end)
