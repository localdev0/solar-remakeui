## Modified with Tween Switch
```lua
local lib = {}
local UIColor = Color3.fromRGB(83, 133, 255)

function lib:CreateWindow(title)
	
	local UI = Instance.new("ScreenGui")
	local Main = Instance.new("Frame")
	local UICorner = Instance.new("UICorner")
	local TopBar = Instance.new("Frame")
	local Icon = Instance.new("ImageLabel")
	local Title = Instance.new("TextLabel")
	local ExitButton = Instance.new("ImageButton")
	local UIAspectRatioConstraint = Instance.new("UIAspectRatioConstraint")
	local Line = Instance.new("Frame")
	local Navigation = Instance.new("ScrollingFrame")
	local UIListLayout = Instance.new("UIListLayout")
	local UIPadding = Instance.new("UIPadding")
	local Line_2 = Instance.new("Frame")
	local Content = Instance.new("Frame")
	
	UI.Name = "UI"
	UI.Parent = game:GetService("Players").LocalPlayer:WaitForChild("PlayerGui") or game:GetService("CoreGui")
	UI.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	UI.DisplayOrder = 99
	UI.ResetOnSpawn = false

	Main.Name = "Main"
	Main.Parent = UI
	Main.BackgroundColor3 = Color3.fromRGB(12, 14, 17)
	Main.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Main.BorderSizePixel = 0
	Main.Position = UDim2.new(0, 425, 0, 150)
	Main.Size = UDim2.new(0, 556, 0, 344)

	UICorner.CornerRadius = UDim.new(0, 6)
	UICorner.Parent = Main

	TopBar.Name = "TopBar"
	TopBar.Parent = Main
	TopBar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TopBar.BackgroundTransparency = 1.000
	TopBar.BorderColor3 = Color3.fromRGB(0, 0, 0)
	TopBar.BorderSizePixel = 0
	TopBar.Size = UDim2.new(0, 556, 0, 55)

	Icon.Name = "Icon"
	Icon.Parent = TopBar
	Icon.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Icon.BackgroundTransparency = 1.000
	Icon.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Icon.BorderSizePixel = 0
	Icon.Size = UDim2.new(0, 73, 0, 51)
	Icon.Image = "http://www.roblox.com/asset/?id=70944899239586"
	Icon.ImageColor3 = UIColor

	Title.Name = "Title"
	Title.Parent = TopBar
	Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Title.BackgroundTransparency = 1.000
	Title.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Title.BorderSizePixel = 0
	Title.Position = UDim2.new(0.131294966, 0, 0.0181818176, 0)
	Title.Size = UDim2.new(0, 483, 0, 54)
	Title.Font = Enum.Font.GothamBold
	Title.Text = title
	Title.TextColor3 = Color3.fromRGB(255, 255, 255)
	Title.TextSize = 30.000
	Title.TextXAlignment = Enum.TextXAlignment.Left

	ExitButton.Name = "ExitButton"
	ExitButton.Parent = TopBar
	ExitButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	ExitButton.BackgroundTransparency = 1.000
	ExitButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
	ExitButton.BorderSizePixel = 0
	ExitButton.Position = UDim2.new(0.935251772, 0, 0.25454545, 0)
	ExitButton.Size = UDim2.new(0, 28, 0, 29)
	ExitButton.AutoButtonColor = false
	ExitButton.Image = "rbxassetid://10747384394"
	ExitButton.ImageColor3 = Color3.fromRGB(45, 45, 45)
	
	ExitButton.MouseButton1Click:Connect(function()
		Main.Visible = false
	end)

	UIAspectRatioConstraint.Parent = ExitButton

	Line.Name = "Line"
	Line.Parent = Main
	Line.BackgroundColor3 = Color3.fromRGB(51, 51, 51)
	Line.BackgroundTransparency = 0.500
	Line.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Line.BorderSizePixel = 0
	Line.Position = UDim2.new(0, 0, 0.160122007, 0)
	Line.Size = UDim2.new(0, 556, 0, 1)

	Navigation.Name = "Navigation"
	Navigation.Parent = Main
	Navigation.Active = true
	Navigation.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Navigation.BackgroundTransparency = 1.000
	Navigation.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Navigation.BorderSizePixel = 0
	Navigation.Position = UDim2.new(0, 0, 0.162790701, 0)
	Navigation.Size = UDim2.new(0, 150, 0, 288)
	Navigation.ScrollBarImageColor3 = Color3.fromRGB(0, 0, 0)
	Navigation.CanvasSize = UDim2.new(0, 0, 10, 0)
	Navigation.ScrollBarThickness = 0

	UIListLayout.Parent = Navigation
	UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
	UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
	UIListLayout.Padding = UDim.new(0, 4)

	UIPadding.Parent = Navigation
	UIPadding.PaddingTop = UDim.new(0, 6)
	
	Line_2.Name = "Line"
	Line_2.Parent = Main
	Line_2.BackgroundColor3 = Color3.fromRGB(51, 51, 51)
	Line_2.BackgroundTransparency = 0.500
	Line_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Line_2.BorderSizePixel = 0
	Line_2.Position = UDim2.new(0.269784182, 0, 0.162790701, 0)
	Line_2.Size = UDim2.new(0, 1, 0, 288)

	Content.Name = "Content"
	Content.Parent = Main
	Content.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Content.BackgroundTransparency = 1.000
	Content.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Content.BorderSizePixel = 0
	Content.Position = UDim2.new(0.271582723, 0, 0.162790701, 0)
	Content.Size = UDim2.new(0, 405, 0, 288)
	
	local function UBREJ_script() -- Main.dragWindow 
		local script = Instance.new('LocalScript', Main)

		local TweenService = game:GetService("TweenService")
		local UserInputService = game:GetService("UserInputService")

		local gui = script.Parent

		local dragging
		local dragInput
		local dragStart
		local startPos

		local tweenInfo = TweenInfo.new(0.16, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)

		local function update(input)
			local delta = input.Position - dragStart
			local targetPos = UDim2.new(
				startPos.X.Scale, 
				startPos.X.Offset + delta.X, 
				startPos.Y.Scale, 
				startPos.Y.Offset + delta.Y
			)

			local tween = TweenService:Create(gui, tweenInfo, {Position = targetPos})
			tween:Play()
		end

		gui.InputBegan:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				dragging = true
				dragStart = input.Position
				startPos = gui.Position

				input.Changed:Connect(function()
					if input.UserInputState == Enum.UserInputState.End then
						dragging = false
					end
				end)
			end
		end)

		gui.InputChanged:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
				dragInput = input
			end
		end)

		UserInputService.InputChanged:Connect(function(input)
			if input == dragInput and dragging then
				update(input)
			end
		end)

		local function toggleGuiVisibility(input)
			if input.UserInputType == Enum.UserInputType.Keyboard and input.KeyCode == Enum.KeyCode.LeftControl then
				gui.Visible = not gui.Visible
			end
		end

		UserInputService.InputBegan:Connect(function(input, gameProcessed)
			if not gameProcessed then
				toggleGuiVisibility(input)
			end
		end)

	end
	coroutine.wrap(UBREJ_script)()
	
	local TweenService = game:GetService("TweenService")

function lib:CreateTab(title)
    local Tab = Instance.new("TextButton")
    local UICorner_3 = Instance.new("UICorner")
    local Items = Instance.new("ScrollingFrame")
    local UIPadding_2 = Instance.new("UIPadding")
    local UIListLayout_2 = Instance.new("UIListLayout")

    Tab.Name = "Tab"
    Tab.Parent = Navigation
    Tab.BackgroundColor3 = UIColor
    Tab.BackgroundTransparency = 1.000
    Tab.BorderColor3 = Color3.fromRGB(0, 0, 0)
    Tab.BorderSizePixel = 0
    Tab.Position = UDim2.new(0.0566666685, 0, 0, 0)
    Tab.Size = UDim2.new(0, 133, 0, 32)
    Tab.AutoButtonColor = false
    Tab.Font = Enum.Font.Gotham
    Tab.Text = title
    Tab.TextColor3 = Color3.fromRGB(255, 255, 255)
    Tab.TextSize = 14.000
    Tab.TextTransparency = 0.800

    UICorner_3.Parent = Tab

    Items.Name = title
    Items.Parent = Content
    Items.Active = true
    Items.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Items.BackgroundTransparency = 2.000
    Items.BorderColor3 = Color3.fromRGB(0, 0, 0)
    Items.BorderSizePixel = 0
    Items.Size = UDim2.new(0, 405, 0, 288)
    Items.ScrollBarImageColor3 = Color3.fromRGB(0, 0, 0)
    Items.CanvasSize = UDim2.new(0, 0, 10, 0)
    Items.ScrollBarThickness = 0
    Items.Visible = false
    Items.Position = UDim2.new(0, -350, 0, 0)

    UIPadding_2.Parent = Items
    UIPadding_2.PaddingTop = UDim.new(0, 6)

    UIListLayout_2.Parent = Items
    UIListLayout_2.HorizontalAlignment = Enum.HorizontalAlignment.Center
    UIListLayout_2.SortOrder = Enum.SortOrder.LayoutOrder
    UIListLayout_2.Padding = UDim.new(0, 8)

    local function onTabClick()
        for _, child in pairs(Navigation:GetChildren()) do
            if child:IsA("TextButton") then
                child.TextTransparency = 0.6
                child.BackgroundTransparency = 1
            end
        end

        Tab.TextTransparency = 0
        Tab.BackgroundTransparency = 0.6

        for _, item in pairs(Content:GetChildren()) do
            if item:IsA("ScrollingFrame") then
                if item.Name == title then
                    item.Visible = true
                    local tweenInfo = TweenInfo.new(0.5, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
                    local goal = {Position = UDim2.new(0, 0, 0, 0)}
                    local tween = TweenService:Create(item, tweenInfo, goal)
                    tween:Play()
                else
                    item.Visible = false
                end
            end
        end

        for _, item in pairs(Content:GetChildren()) do
            if item:IsA("ScrollingFrame") and item.Name ~= title then
                local tweenInfo = TweenInfo.new(0.5, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
                local goal = {Position = UDim2.new(0, -350, 0, 0)}
                local tween = TweenService:Create(item, tweenInfo, goal)
                tween:Play()
            end
        end
    end

    Tab.MouseButton1Click:Connect(onTabClick)
    Tab.TouchTap:Connect(onTabClick)

    return Tab, Items
end


	
	function lib:CreateSection(title, TabParent)
		local Section = Instance.new("Frame")
		
		Section.Name = title
		Section.Parent = TabParent
		Section.BackgroundColor3 = UIColor
		Section.BackgroundTransparency = 0.700
		Section.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Section.BorderSizePixel = 0
		Section.Position = UDim2.new(0.176543206, 0, 0, 0)
		Section.Size = UDim2.new(0, 297, 0, 2)
	end
	
	function lib:CreateButton(title, TabParent, callback)
		local Button = Instance.new("ImageButton")
		local UIStroke_12 = Instance.new("UIStroke")
		local UICorner_16 = Instance.new("UICorner")
		local Title_7 = Instance.new("TextLabel")
		local MouseIcon = Instance.new("ImageLabel")
		local UIAspectRatioConstraint_4 = Instance.new("UIAspectRatioConstraint")
	
		Button.Name = "Button"
		Button.Parent = TabParent
		Button.BackgroundColor3 = Color3.fromRGB(7, 9, 11)
		Button.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Button.BorderSizePixel = 0
		Button.Position = UDim2.new(0.0185185187, 0, 0, 0)
		Button.Size = UDim2.new(0, 390, 0, 36)
		Button.AutoButtonColor = false
	
		UIStroke_12.Parent = Button
		UIStroke_12.Color = UIColor
	
		UICorner_16.CornerRadius = UDim.new(0, 6)
		UICorner_16.Parent = Button
	
		Title_7.Name = "Title"
		Title_7.Parent = Button
		Title_7.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_7.BackgroundTransparency = 1
		Title_7.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_7.BorderSizePixel = 0
		Title_7.Position = UDim2.new(0.0230769236, 0, 0.138888896, 0)
		Title_7.Size = UDim2.new(0, 100, 0, 25)
		Title_7.Font = Enum.Font.Gotham
		Title_7.Text = title
		Title_7.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_7.TextSize = 17
		Title_7.TextXAlignment = Enum.TextXAlignment.Left
	
		MouseIcon.Name = "MouseIcon"
		MouseIcon.Parent = Button
		MouseIcon.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		MouseIcon.BackgroundTransparency = 1
		MouseIcon.BorderColor3 = Color3.fromRGB(0, 0, 0)
		MouseIcon.BorderSizePixel = 0
		MouseIcon.Position = UDim2.new(0.934615374, 0, 0.194444448, 0)
		MouseIcon.Size = UDim2.new(0, 21, 0, 25)
		MouseIcon.Image = "rbxassetid://12804017021"
		MouseIcon.ImageColor3 = UIColor
	
		UIAspectRatioConstraint_4.Parent = MouseIcon
	
		local function onClick()
			if callback then
				callback()
			end
		end
	
		local UserInputService = game:GetService("UserInputService")
		Button.MouseButton1Click:Connect(onClick)
		
		Button.TouchTap:Connect(onClick)
	end
	
	function lib:CreateToggle(title, TabParent, callback)
		local Toggle = Instance.new("ImageButton")
		local UIStroke_4 = Instance.new("UIStroke")
		local UICorner_7 = Instance.new("UICorner")
		local Title_3 = Instance.new("TextLabel")
		local Slide_2 = Instance.new("Frame")
		local UIStroke_5 = Instance.new("UIStroke")
		local UICorner_8 = Instance.new("UICorner")
		local Wheel_2 = Instance.new("Frame")
		local UIAspectRatioConstraint_3 = Instance.new("UIAspectRatioConstraint")
		local UIStroke_6 = Instance.new("UIStroke")
		local UICorner_9 = Instance.new("UICorner")
	
		Toggle.Name = "Toggle"
		Toggle.Parent = TabParent
		Toggle.BackgroundColor3 = Color3.fromRGB(7, 9, 11)
		Toggle.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Toggle.BorderSizePixel = 0
		Toggle.Position = UDim2.new(0.0185185187, 0, 0, 0)
		Toggle.Size = UDim2.new(0, 390, 0, 36)
		Toggle.AutoButtonColor = false
	
		UIStroke_4.Parent = Toggle
		UIStroke_4.Color = UIColor
		UIStroke_4.Transparency = 0.500
	
		UICorner_7.CornerRadius = UDim.new(0, 6)
		UICorner_7.Parent = Toggle
	
		Title_3.Name = "Title"
		Title_3.Parent = Toggle
		Title_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_3.BackgroundTransparency = 1.000
		Title_3.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_3.BorderSizePixel = 0
		Title_3.Position = UDim2.new(0.0230769236, 0, 0.138888896, 0)
		Title_3.Size = UDim2.new(0, 100, 0, 25)
		Title_3.Font = Enum.Font.Gotham
		Title_3.Text = title
		Title_3.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_3.TextSize = 17.000
		Title_3.TextTransparency = 0.600
		Title_3.TextXAlignment = Enum.TextXAlignment.Left
	
		Slide_2.Name = "Slide"
		Slide_2.Parent = Toggle
		Slide_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Slide_2.BackgroundTransparency = 1.000
		Slide_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Slide_2.BorderSizePixel = 0
		Slide_2.Position = UDim2.new(0.85128206, 0, 0.138888896, 0)
		Slide_2.Size = UDim2.new(0, 50, 0, 25)
	
		UIStroke_5.Parent = Slide_2
		UIStroke_5.Color = UIColor
		UIStroke_5.Transparency = 0.500
	
		UICorner_8.CornerRadius = UDim.new(1, 0)
		UICorner_8.Parent = Slide_2
	
		Wheel_2.Name = "Wheel"
		Wheel_2.Parent = Slide_2
		Wheel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Wheel_2.BackgroundTransparency = 1.000
		Wheel_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Wheel_2.BorderSizePixel = 0
		Wheel_2.Position = UDim2.new(0.119999997, 0, 0.200000003, 0)
		Wheel_2.Size = UDim2.new(0, 23, 0, 15)
	
		UIAspectRatioConstraint_3.Parent = Wheel_2
	
		UIStroke_6.Parent = Wheel_2
		UIStroke_6.Color = UIColor
		UIStroke_6.Transparency = 0.500
	
		UICorner_9.CornerRadius = UDim.new(1, 0)
		UICorner_9.Parent = Wheel_2
	
		local UserInputService = game:GetService("UserInputService")
		local function onClick()
			local isActive = not Toggle:GetAttribute("IsActive")
	
			Toggle:SetAttribute("IsActive", isActive)
	
			local tweenService = game:GetService("TweenService")
	
			local titleTween = tweenService:Create(Title_3, TweenInfo.new(0.2), {
				TextTransparency = isActive and 0 or 0.6
			})
	
			local strokeTween = tweenService:Create(UIStroke_4, TweenInfo.new(0.2), {
				Transparency = isActive and 0 or 0.6
			})
			
			local stroke2Tween = tweenService:Create(UIStroke_5, TweenInfo.new(0.2), {
				Transparency = isActive and 0 or 0.6
			})
			
			local stroke3Tween = tweenService:Create(UIStroke_6, TweenInfo.new(0.2), {
				Transparency = isActive and 0 or 0.6
			})
	
			local wheelTween = tweenService:Create(Wheel_2, TweenInfo.new(0.3), {
				Position = isActive and UDim2.new(0.579999983, 0, 0.200000003, 0) or UDim2.new(0.119999997, 0, 0.200000003, 0)
			})
	
			titleTween:Play()
			strokeTween:Play()
			wheelTween:Play()
			stroke2Tween:Play()
			stroke3Tween:Play()
	
			if callback then
				callback(isActive)
			end
		end
	
		if UserInputService.TouchEnabled then
			Toggle.InputBegan:Connect(function(input)
				if input.UserInputType == Enum.UserInputType.Touch then
					onClick()
				end
			end)
		else
			Toggle.MouseButton1Click:Connect(onClick)
		end
	end
	
	
	function lib:CreateSlider(title, TabParent, min, max, callback)
		local Slider = Instance.new("ImageButton")
		local UIStroke_7 = Instance.new("UIStroke")
		local UICorner_10 = Instance.new("UICorner")
		local Title_4 = Instance.new("TextLabel")
		local SliderBack = Instance.new("Frame")
		local UIStroke_8 = Instance.new("UIStroke")
		local UICorner_11 = Instance.new("UICorner")
		local Draggable = Instance.new("Frame")
		local UICorner_12 = Instance.new("UICorner")
		local Value = Instance.new("TextLabel")
	
		Slider.Name = "Slider"
		Slider.Parent = TabParent
		Slider.BackgroundColor3 = Color3.fromRGB(7, 9, 11)
		Slider.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Slider.BorderSizePixel = 0
		Slider.Position = UDim2.new(0.0185185187, 0, 0.347517729, 0)
		Slider.Size = UDim2.new(0, 390, 0, 45)
		Slider.AutoButtonColor = false
	
		UIStroke_7.Parent = Slider
		UIStroke_7.Color = UIColor
		UIStroke_7.Transparency = 0.600
	
		UICorner_10.CornerRadius = UDim.new(0, 6)
		UICorner_10.Parent = Slider
	
		Title_4.Name = "Title"
		Title_4.Parent = Slider
		Title_4.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_4.BackgroundTransparency = 1.000
		Title_4.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_4.BorderSizePixel = 0
		Title_4.Position = UDim2.new(0.0230769236, 0, 0.138888896, 0)
		Title_4.Size = UDim2.new(0, 100, 0, 18)
		Title_4.Font = Enum.Font.Gotham
		Title_4.Text = title
		Title_4.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_4.TextSize = 17.000
		Title_4.TextTransparency = 0.600
		Title_4.TextXAlignment = Enum.TextXAlignment.Left
	
		SliderBack.Name = "SliderBack"
		SliderBack.Parent = Slider
		SliderBack.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		SliderBack.BackgroundTransparency = 1.000
		SliderBack.BorderColor3 = Color3.fromRGB(0, 0, 0)
		SliderBack.BorderSizePixel = 0
		SliderBack.Position = UDim2.new(0.0230769236, 0, 0.688888907, 0)
		SliderBack.Size = UDim2.new(0, 370, 0, 6)
	
		UIStroke_8.Parent = SliderBack
		UIStroke_8.Color = Color3.fromRGB(51, 51, 51)
		UIStroke_8.Thickness = 1.500
	
		UICorner_11.Parent = SliderBack
	
		Draggable.Name = "Draggable"
		Draggable.Parent = SliderBack
		Draggable.BackgroundColor3 = UIColor
		Draggable.BackgroundTransparency = 0.600
		Draggable.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Draggable.BorderSizePixel = 0
		Draggable.Size = UDim2.new(0, 257, 0, 6)
	
		UICorner_12.Parent = Draggable
	
		Value.Name = "Value"
		Value.Parent = Slider
		Value.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Value.BackgroundTransparency = 1.000
		Value.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Value.BorderSizePixel = 0
		Value.Position = UDim2.new(0.705128193, 0, 0.138888896, 0)
		Value.Size = UDim2.new(0, 100, 0, 18)
		Value.Font = Enum.Font.Gotham
		Value.Text = "0.1"
		Value.TextColor3 = Color3.fromRGB(255, 255, 255)
		Value.TextSize = 17.000
		Value.TextTransparency = 0.600
		Value.TextXAlignment = Enum.TextXAlignment.Right
	
		local UIS = game:GetService("UserInputService")
		local TweenService = game:GetService("TweenService")
		local currentValue = min
		local isDragging = false
	
		local function UpdateTransparency(isActive)
			local targetTransparency = isActive and 0 or 0.6
	
			TweenService:Create(UIStroke_7, TweenInfo.new(0.2), {Transparency = targetTransparency}):Play()
			TweenService:Create(Title_4, TweenInfo.new(0.2), {TextTransparency = targetTransparency}):Play()
			TweenService:Create(Value, TweenInfo.new(0.2), {TextTransparency = targetTransparency}):Play()
			TweenService:Create(Draggable, TweenInfo.new(0.2), {BackgroundTransparency = targetTransparency}):Play()
		end
	
		local function UpdateSliderPosition()
			local percentage = math.clamp((currentValue - min) / (max - min), 0, 1)
			Value.Text = string.format("%.1f", currentValue)
			Draggable.Size = UDim2.new(percentage, 0, 1, 0)
			callback(currentValue)
		end
	
		local function StartDragging(input)
			isDragging = true
			UpdateTransparency(true)
		end
	
		local function UpdateDragging(input)
			if not isDragging then return end
			local sliderX = SliderBack.AbsolutePosition.X
			local sliderWidth = SliderBack.AbsoluteSize.X
			local newPercentage = math.clamp((input.Position.X - sliderX) / sliderWidth, 0, 1)
			currentValue = min + (newPercentage * (max - min))
			currentValue = math.round(currentValue * 10) / 10
			UpdateSliderPosition()
		end
	
		local function StopDragging()
			isDragging = false
			UpdateTransparency(false)
		end
	
		Slider.MouseButton1Down:Connect(StartDragging)
		UIS.InputChanged:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
				UpdateDragging(input)
			end
		end)
		UIS.InputEnded:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				StopDragging()
			end
		end)
	
		UpdateSliderPosition()
	end
	
	function lib:CreateDropdown(title, TabParent, options, callback)
		local Dropdown = Instance.new("ImageButton")
		local UIStroke_9 = Instance.new("UIStroke")
		local UICorner_13 = Instance.new("UICorner")
		local Title_5 = Instance.new("TextLabel")
		local SelectedText = Instance.new("TextLabel")
	
		Dropdown.Name = "Dropdown"
		Dropdown.Parent = TabParent
		Dropdown.BackgroundColor3 = Color3.fromRGB(7, 9, 11)
		Dropdown.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Dropdown.BorderSizePixel = 0
		Dropdown.Position = UDim2.new(0.0185185187, 0, 0, 0)
		Dropdown.Size = UDim2.new(0, 390, 0, 36)
		Dropdown.AutoButtonColor = false
	
		UIStroke_9.Parent = Dropdown
		UIStroke_9.Color = UIColor
	
		UICorner_13.CornerRadius = UDim.new(0, 6)
		UICorner_13.Parent = Dropdown
	
		Title_5.Name = "Title"
		Title_5.Parent = Dropdown
		Title_5.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_5.BackgroundTransparency = 1.000
		Title_5.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_5.BorderSizePixel = 0
		Title_5.Position = UDim2.new(0.0230769236, 0, 0.138888896, 0)
		Title_5.Size = UDim2.new(0, 100, 0, 25)
		Title_5.Font = Enum.Font.Gotham
		Title_5.Text = title
		Title_5.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_5.TextSize = 17.000
		Title_5.TextXAlignment = Enum.TextXAlignment.Left
	
		SelectedText.Name = "SelectedText"
		SelectedText.Parent = Dropdown
		SelectedText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		SelectedText.BackgroundTransparency = 1.000
		SelectedText.BorderColor3 = Color3.fromRGB(0, 0, 0)
		SelectedText.BorderSizePixel = 0
		SelectedText.Position = UDim2.new(0.725641012, 0, 0.138888896, 0)
		SelectedText.Size = UDim2.new(0, 100, 0, 25)
		SelectedText.Font = Enum.Font.Gotham
		SelectedText.Text = options[1]
		SelectedText.TextColor3 = Color3.fromRGB(255, 255, 255)
		SelectedText.TextSize = 17.000
		SelectedText.TextXAlignment = Enum.TextXAlignment.Right
	
		local function onClick()
			local currentIndex = table.find(options, SelectedText.Text) or 0
			local nextIndex = (currentIndex % #options) + 1
			SelectedText.Text = options[nextIndex]
	
			if callback then
				callback(SelectedText.Text)
			end
		end
	
		Dropdown.MouseButton1Click:Connect(onClick)
		
		Dropdown.TouchTap:Connect(onClick)
	end
	
	
	function lib:CreateInput(title, TabParent, TextHolder, callback)
		local Input = Instance.new("ImageButton")
		local UIStroke_10 = Instance.new("UIStroke")
		local UICorner_14 = Instance.new("UICorner")
		local Title_6 = Instance.new("TextLabel")
		local Box = Instance.new("Frame")
		local UIStroke_11 = Instance.new("UIStroke")
		local UICorner_15 = Instance.new("UICorner")
		local TextBox = Instance.new("TextBox")
	
		Input.Name = "Input"
		Input.Parent = TabParent
		Input.BackgroundColor3 = Color3.fromRGB(7, 9, 11)
		Input.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Input.BorderSizePixel = 0
		Input.Position = UDim2.new(0.359259248, 0, 0.769503534, 0)
		Input.Size = UDim2.new(0, 390, 0, 36)
		Input.AutoButtonColor = false
	
		UIStroke_10.Parent = Input
		UIStroke_10.Color = UIColor
	
		UICorner_14.CornerRadius = UDim.new(0, 6)
		UICorner_14.Parent = Input
	
		Title_6.Name = "Title"
		Title_6.Parent = Input
		Title_6.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_6.BackgroundTransparency = 1.000
		Title_6.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_6.BorderSizePixel = 0
		Title_6.Position = UDim2.new(0.0230769236, 0, 0.138888896, 0)
		Title_6.Size = UDim2.new(0, 100, 0, 25)
		Title_6.Font = Enum.Font.Gotham
		Title_6.Text = title
		Title_6.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_6.TextSize = 17.000
		Title_6.TextXAlignment = Enum.TextXAlignment.Left
	
		Box.Name = "Box"
		Box.Parent = Input
		Box.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Box.BackgroundTransparency = 1.000
		Box.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Box.BorderSizePixel = 0
		Box.Position = UDim2.new(0.77692306, 0, 0.138888896, 0)
		Box.Size = UDim2.new(0, 80, 0, 25)
	
		UIStroke_11.Parent = Box
		UIStroke_11.Color = UIColor
	
		UICorner_15.CornerRadius = UDim.new(0, 4)
		UICorner_15.Parent = Box
	
		TextBox.Parent = Box
		TextBox.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		TextBox.BackgroundTransparency = 1.000
		TextBox.BorderColor3 = Color3.fromRGB(0, 0, 0)
		TextBox.BorderSizePixel = 0
		TextBox.Size = UDim2.new(0, 80, 0, 25)
		TextBox.Font = Enum.Font.Gotham
		TextBox.PlaceholderText = TextHolder
		TextBox.Text = ""
		TextBox.TextColor3 = Color3.fromRGB(255, 255, 255)
		TextBox.TextSize = 16.000
	
		local function onSubmit()
			local userInput = TextBox.Text
			callback(userInput)
		end
	
		local function onButtonClick()
			onSubmit()
		end
	
		Input.InputBegan:Connect(function(input, gameProcessed)
			if not gameProcessed then
				if input.UserInputType == Enum.UserInputType.Touch then
					onButtonClick()
				end
			end
		end)
	
		TextBox.FocusLost:Connect(function(enterPressed)
			if enterPressed then
				onSubmit()
			end
		end)
	
		Input.MouseButton1Click:Connect(function()
			onButtonClick()
		end)
	end

	return lib
end
```
## Create Window
```lua
lib:CreateWindow("test")
```
## Create Tab
```lua
local tab1, tab1 = lib:CreateTab("Ca")
local tab2, tab2 = lib:CreateTab("Ing")
```
## Create Section
```lua
lib:CreateSection("test", tab1)
```
## Create Button
```lua
lib:CreateButton("Click Me", tab1, function()
	print("Button clicked!")
end)
```
## Create Toggle
```lua
lib:CreateToggle("Test Toggle", tab1, function(state)
	print(state)
end)
```
## Create Slider
```lua
lib:CreateSlider("Volume", tab1, 0, 100, function(value)
	print("Current Value: " .. value)
end)
```
## Create Dropdown
```lua
local options = {"Option 1", "Option 2", "Option 3", "Option 4"}
lib:CreateDropdown("Magnet Mode", tab1, options, function(selectedOption)
	print("You selected: " .. selectedOption)
end)
```
## Create Input
```lua
lib:CreateInput("Set Jersey Name", tab1, "Name...", function(input)
	print("User input:", input)
end)
```
