--[=[
 d888b  db    db d888888b      .d888b.      db      db    db  .d8b.  
88' Y8b 88    88   `88'        VP  `8D      88      88    88 d8' `8b 
88      88    88    88            odD'      88      88    88 88ooo88 
88  ooo 88    88    88          .88'        88      88    88 88~~~88 
88. ~8~ 88b  d88   .88.        j88.         88booo. 88b  d88 88   88 
 Y888P  ~Y8888P' Y888888P      888888D      Y88888P ~Y8888P' YP   YP  CONVERTER
]=]

-- Instances: 9 | Scripts: 1 | Modules: 0
local G2L = {};

-- StarterGui.Gui
G2L["1"] = Instance.new("ScreenGui", game:GetService("Players").LocalPlayer:WaitForChild("PlayerGui"));
G2L["1"]["Name"] = [[Gui]];
G2L["1"]["ZIndexBehavior"] = Enum.ZIndexBehavior.Sibling;

-- StarterGui.Gui.Main
G2L["2"] = Instance.new("Frame", G2L["1"]);
G2L["2"]["BorderSizePixel"] = 0;
G2L["2"]["BackgroundColor3"] = Color3.fromRGB(0, 0, 0);
G2L["2"]["BackgroundTransparency"] = 0.5;
G2L["2"]["Size"] = UDim2.new(0, 531, 0, 340);
G2L["2"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["2"]["Position"] = UDim2.new(0.174161896109581, 0, 0.11086956411600113, 0);
G2L["2"]["Name"] = [[Main]];

-- StarterGui.Gui.Main.Title
G2L["3"] = Instance.new("TextLabel", G2L["2"]);
G2L["3"]["TextWrapped"] = true;
G2L["3"]["BorderSizePixel"] = 0;
G2L["3"]["TextScaled"] = true;
G2L["3"]["BackgroundColor3"] = Color3.fromRGB(0, 0, 0);
G2L["3"]["FontFace"] = Font.new([[rbxasset://fonts/families/IndieFlower.json]], Enum.FontWeight.Regular, Enum.FontStyle.Normal);
G2L["3"]["TextSize"] = 14;
G2L["3"]["TextColor3"] = Color3.fromRGB(149, 0, 0);
G2L["3"]["Size"] = UDim2.new(0, 531, 0, 44);
G2L["3"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["3"]["Text"] = [[Welcome.]];
G2L["3"]["Name"] = [[Title]];
G2L["3"]["BackgroundTransparency"] = 0.5;

-- StarterGui.Gui.Main.LocalScript
G2L["4"] = Instance.new("LocalScript", G2L["2"]);


-- StarterGui.Gui.Main.Rejoin
G2L["5"] = Instance.new("TextButton", G2L["2"]);
G2L["5"]["TextWrapped"] = true;
G2L["5"]["BorderSizePixel"] = 0;
G2L["5"]["TextScaled"] = true;
G2L["5"]["BackgroundColor3"] = Color3.fromRGB(0, 0, 0);
G2L["5"]["TextSize"] = 14;
G2L["5"]["FontFace"] = Font.new([[rbxasset://fonts/families/IndieFlower.json]], Enum.FontWeight.Regular, Enum.FontStyle.Normal);
G2L["5"]["TextColor3"] = Color3.fromRGB(181, 0, 0);
G2L["5"]["Size"] = UDim2.new(0, 113, 0, 50);
G2L["5"]["Name"] = [[Rejoin]];
G2L["5"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["5"]["Text"] = [[Rejoin]];
G2L["5"]["Position"] = UDim2.new(0.39283397793769836, 0, 0.820332407951355, 0);
G2L["5"]["BackgroundTransparency"] = 0.4000000059604645;

-- Create Execute Button
local executeButton = Instance.new("TextButton")
Font.new([[rbxasset://fonts/families/IndieFlower.json]], Enum.FontWeight.Regular, Enum.FontStyle.Normal);
executeButton.Name = "ExecuteButton"
executeButton.Size = UDim2.new(0, 113, 0, 50)
executeButton.Position = UDim2.new(0.03051372803747654, 0, 0.820332407951355, 0)
executeButton.BackgroundColor3 = Color3.new(0, 0, 0)
executeButton.TextColor3 = Color3.new(181, 0, 0)
executeButton.Text = "Execute"
executeButton.Parent = G2L["2"]



-- StarterGui.Gui.Main.TextBox
G2L["7"] = Instance.new("TextBox", G2L["2"]);
G2L["7"]["BorderSizePixel"] = 0;
G2L["7"]["TextSize"] = 14;
G2L["7"]["BackgroundColor3"] = Color3.fromRGB(255, 0, 0);
G2L["7"]["TextColor3"] = Color3.fromRGB(0, 0, 0);
G2L["7"]["FontFace"] = Font.new([[rbxasset://fonts/families/IndieFlower.json]], Enum.FontWeight.Regular, Enum.FontStyle.Normal);
G2L["7"]["BackgroundTransparency"] = 0.5;
G2L["7"]["Size"] = UDim2.new(0, 496, 0, 194);
G2L["7"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["7"]["Text"] = [[]];
G2L["7"]["Position"] = UDim2.new(0.033053699880838394, 0, 0.2136828750371933, 0);

-- StarterGui.Gui.Main.Coming Soon
G2L["8"] = Instance.new("TextButton", G2L["2"]);
G2L["8"]["TextWrapped"] = true;
G2L["8"]["BorderSizePixel"] = 0;
G2L["8"]["TextScaled"] = true;
G2L["8"]["BackgroundColor3"] = Color3.fromRGB(0, 0, 0);
G2L["8"]["TextSize"] = 14;
G2L["8"]["FontFace"] = Font.new([[rbxasset://fonts/families/IndieFlower.json]], Enum.FontWeight.Regular, Enum.FontStyle.Normal);
G2L["8"]["TextColor3"] = Color3.fromRGB(181, 0, 0);
G2L["8"]["Size"] = UDim2.new(0, 113, 0, 50);
G2L["8"]["Name"] = [[Coming Soon]];
G2L["8"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["8"]["Text"] = [[Coming Soon]];
G2L["8"]["Position"] = UDim2.new(0.7525326609611511, 0, 0.820332407951355, 0);
G2L["8"]["BackgroundTransparency"] = 0.4000000059604645;

-- StarterGui.Gui.Main.ImageLabel
G2L["9"] = Instance.new("ImageLabel", G2L["2"]);
G2L["9"]["BorderSizePixel"] = 0;
G2L["9"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["9"]["Image"] = [[http://www.roblox.com/asset/?id=15442297688]];
G2L["9"]["Size"] = UDim2.new(0, 46, 0, 44);
G2L["9"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["9"]["Position"] = UDim2.new(0.9133710265159607, 0, 0, 0);

-- StarterGui.Gui.Main.LocalScript
local function C_4()
local script = G2L["4"];
	script.Parent.Draggable = true
	script.Parent.Active = true
end;
task.spawn(C_4);

-- Function to execute the scripts
local function executeScripts()
    local textBox = G2L["7"] -- Assuming textBox is the TextBox instance in your structure
    local scripts = textBox.Text:split("\n")
    
    for _, script in ipairs(scripts) do
        -- Execute the script with bypassed filtering enabled
        local success, error = pcall(function()
            loadstring(script)()
        end)
        
        if not success then
            warn("Error executing script:", error)
        end
    end
end

-- Bind the executeScripts function to the executeButton's MouseButton1Click event
executeButton.MouseButton1Click:Connect(executeScripts)


-- Function to handle rejoining
local function rejoinPlayer()
    game:GetService("TeleportService"):Teleport(game.PlaceId, game:GetService("Players").LocalPlayer)
end

-- Bind the rejoinPlayer function to the Rejoin button's MouseButton1Click event
G2L["5"].MouseButton1Click:Connect(rejoinPlayer)

return G2L["1"], require;
