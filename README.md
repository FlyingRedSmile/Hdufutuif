-- RedX Executor with Custom Title and Image
local gui = Instance.new("ScreenGui")
gui.Name = "RedX"
gui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Name = "MainFrame"
frame.Size = UDim2.new(0, 300, 0, 200)
frame.Position = UDim2.new(0.5, -150, 0.5, -100)
frame.BackgroundColor3 = Color3.new(1, 0, 0)
frame.Parent = gui

-- Add a title that says "RedX :)"
local title = Instance.new("TextLabel")
title.Name = "TitleLabel"
title.Size = UDim2.new(1, 0, 0.1, 0)
title.Position = UDim2.new(0, 0, 0, 0)
title.BackgroundColor3 = Color3.new(0, 0, 0)
title.TextColor3 = Color3.new(1, 1, 1)
title.TextSize = 18
title.Font = Enum.Font.SourceSansBold
title.Text = "RedX :)"
title.Parent = frame

local textBox = Instance.new("TextBox")
textBox.Name = "ScriptTextBox"
textBox.Size = UDim2.new(0.9, 0, 0.6, 0)
textBox.Position = UDim2.new(0.05, 0, 0.2, 0)
textBox.BackgroundColor3 = Color3.new(0, 0, 0)
textBox.TextColor3 = Color3.new(1, 1, 1)
textBox.TextWrapped = true
textBox.Text = "-- Insert your script here"
textBox.Parent = frame


-- RedX Executor
-- This script creates a Roblox executor with a customizable UI that can execute scripts with bypassed filtering enabled.

-- Create a new ScreenGui to hold the UI elements
local gui = Instance.new("ScreenGui")
gui.Name = "RedX"
gui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Create a Frame to hold the UI elements
local frame = Instance.new("Frame")
frame.Name = "MainFrame"
frame.Size = UDim2.new(0, 300, 0, 200)
frame.Position = UDim2.new(0.5, -150, 0.5, -100)
frame.BackgroundColor3 = Color3.new(1, 0, 0)
frame.Parent = gui

-- Create a TextBox for the scripts
local textBox = Instance.new("TextBox")
textBox.Name = "ScriptTextBox"
textBox.Size = UDim2.new(0.9, 0, 0.8, 0)
textBox.Position = UDim2.new(0.05, 0, 0.05, 0)
textBox.BackgroundColor3 = Color3.new(0, 0, 0)
textBox.TextColor3 = Color3.new(1, 1, 1)
textBox.TextWrapped = true
textBox.Text = "-- Insert your script here"
textBox.Parent = frame

-- Create a Button to execute the scripts
local executeButton = Instance.new("TextButton")
executeButton.Name = "ExecuteButton"
executeButton.Size = UDim2.new(0.2, 0, 0.1, 0)
executeButton.Position = UDim2.new(0.4, 0, 0.9, 0)
executeButton.BackgroundColor3 = Color3.new(0, 0, 0)
executeButton.TextColor3 = Color3.new(1, 1, 1)
executeButton.Text = "Execute"
executeButton.Parent = frame

-- Create a Button to close the UI
local closeButton = Instance.new("TextButton")
closeButton.Name = "CloseButton"
closeButton.Size = UDim2.new(0.1, 0, 0.1, 0)
closeButton.Position = UDim2.new(0.9, 0, 0, 0)
closeButton.BackgroundColor3 = Color3.new(0, 0, 0)
closeButton.TextColor3 = Color3.new(1, 1, 1)
closeButton.Text = "X"
closeButton.Parent = frame

-- Function to execute the scripts
local function executeScripts()
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

-- Function to close the UI
local function closeUI()
    gui:Destroy()
end

-- Bind the executeScripts function to the executeButton's MouseButton1Click event
executeButton.MouseButton1Click:Connect(executeScripts)

-- Bind the closeUI function to the closeButton's MouseButton1Click event
closeButton.MouseButton1Click:Connect(closeUI)

-- Example usage of the RedX executor

-- Usage Example: Execute a script
textBox.Text = "print('Hello, RedX!')"
executeScripts()

-- Add more UI elements or features to the RedX Executor

-- Create a Slider for customization
local slider = Instance.new("TextLabel")
slider.Name = "CustomSlider"
slider.Size = UDim2.new(0.6, 0, 0.1, 0)
slider.Position = UDim2.new(0.2, 0, 0.7, 0)
slider.BackgroundColor3 = Color3.new(0, 0, 0)
slider.TextColor3 = Color3.new(1, 1, 1)
slider.Text = "Custom Slider"
slider.Parent = frame

-- Create a Checkbox for options
local checkbox = Instance.new("TextLabel")
checkbox.Name = "CustomCheckbox"
checkbox.Size = UDim2.new(0.6, 0, 0.1, 0)
checkbox.Position = UDim2.new(0.2, 0, 0.8, 0)
checkbox.BackgroundColor3 = Color3.new(0, 0, 0)
checkbox.TextColor3 = Color3.new(1, 1, 1)
checkbox.Text = "Custom Checkbox"
checkbox.Parent = frame

-- Function to handle additional features
local function additionalFeatures()
    -- Add your custom functionality here
    print("Executing additional features!")
end

-- Bind the additionalFeatures function to a new button
local customButton = Instance.new("TextButton")
customButton.Name = "CustomButton"
customButton.Size = UDim2.new(0.2, 0, 0.1, 0)
customButton.Position = UDim2.new(0.7, 0, 0.9, 0)
customButton.BackgroundColor3 = Color3.new(0, 0, 0)
customButton.TextColor3 = Color3.new(1, 1, 1)
customButton.Text = "Custom Feature"
customButton.Parent = frame
customButton.MouseButton1Click:Connect(additionalFeatures)

-- Add color-changing feature to the RedX Executor UI

-- Function to change frame color randomly
local function changeColor()
    frame.BackgroundColor3 = Color3.new(math.random(), math.random(), math.random())
end

-- Create a Button for color change
local colorButton = Instance.new("TextButton")
colorButton.Name = "ColorButton"
colorButton.Size = UDim2.new(0.2, 0, 0.1, 0)
colorButton.Position = UDim2.new(0.4, 0, 0.8, 0)
colorButton.BackgroundColor3 = Color3.new(0, 0, 0)
colorButton.TextColor3 = Color3.new(1, 1, 1)
colorButton.Text = "Change Color"
colorButton.Parent = frame
colorButton.MouseButton1Click:Connect(changeColor)


-- Create a custom image
local customImage = Instance.new("ImageLabel")
customImage.Name = "CustomImage"
customImage.Size = UDim2.new(0.2, 0, 0.2, 0)
customImage.Position = UDim2.new(0.75, 0, 0, 0)
customImage.BackgroundColor3 = Color3.new(0, 0, 0)
customImage.Image = "rbxassetid://15415668627"
customImage.Parent = frame
