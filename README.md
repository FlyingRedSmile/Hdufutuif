-- RedX Executor with Inject Button
local gui = Instance.new("ScreenGui")
gui.Name = "RedX"
gui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

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

local executeButton = Instance.new("TextButton")
executeButton.Name = "ExecuteButton"
executeButton.Size = UDim2.new(0.2, 0, 0.1, 0)
executeButton.Position = UDim2.new(0.2, 0, 0.9, 0)
executeButton.BackgroundColor3 = Color3.new(0, 0, 0)
executeButton.TextColor3 = Color3.new(1, 1, 1)
executeButton.Text = "Execute"
executeButton.Parent = frame

local injectButton = Instance.new("TextButton")
injectButton.Name = "InjectButton"
injectButton.Size = UDim2.new(0.2, 0, 0.1, 0)
injectButton.Position = UDim2.new(0.6, 0, 0.9, 0)
injectButton.BackgroundColor3 = Color3.new(0, 0, 0)
injectButton.TextColor3 = Color3.new(1, 1, 1)
injectButton.Text = "Inject"
injectButton.Parent = frame

local closeButton = Instance.new("TextButton")
closeButton.Name = "CloseButton"
closeButton.Size = UDim2.new(0.1, 0, 0.1, 0)
closeButton.Position = UDim2.new(0.9, 0, 0, 0)
closeButton.BackgroundColor3 = Color3.new(0, 0, 0)
closeButton.TextColor3 = Color3.new(1, 1, 1)
closeButton.Text = "X"
closeButton.Parent = frame

local function executeScripts()
    local scripts = textBox.Text:split("\n")
    for _, script in ipairs(scripts) do
        local success, error = pcall(function()
            loadstring(script)()
        end)
        if not success then
            warn("Error executing script:", error)
        end
    end
end

local function injectScripts()
    local scripts = textBox.Text:split("\n")
    for _, script in ipairs(scripts) do
        loadstring(script)()
    end
end

local function closeUI()
    gui:Destroy()
end

executeButton.MouseButton1Click:Connect(executeScripts)
injectButton.MouseButton1Click:Connect(injectScripts)
closeButton.MouseButton1Click:Connect(closeUI)
