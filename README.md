-- RedX Executor with Inject Button
local gui = Instance.new("ScreenGui")
gui.Name = "RedX"
gui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Name = "MainFrame"
frame.Size = UDim2.new(0, 300, 0, 200)
frame.Position = UDim2.new(0.5, -150, 0.5, -100)
frame.BackgroundColor3 = Color3.new(1, 0, 0)
frame.Parent = gui

local textBox = Instance.new("TextBox")
textBox.Name = "ScriptTextBox"
textBox.Size = UDim2.new(0.9, 0, 0.8, 0)
textBox.Position = UDim2.new(0.05, 0, 0.05, 0)
textBox.BackgroundColor3 = Color3.new(0, 0, 0)
textBox.TextColor3 = Color3.new(1, 1, 1)
textBox.TextWrapped = true
textBox.Text = "-- Insert your script here"
textBox.Parent = frame

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
