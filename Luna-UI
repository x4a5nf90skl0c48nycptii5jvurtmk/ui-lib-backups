local backFrame = Instance.new("Frame")

local UIS = game:GetService('UserInputService')
local frame = backFrame
local dragToggle = nil
local dragSpeed = 0.25
local dragStart = nil
local startPos = nil

local function updateInput(input)
	local delta = input.Position - dragStart
	local position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X,
		startPos.Y.Scale, startPos.Y.Offset + delta.Y)
	game:GetService('TweenService'):Create(frame, TweenInfo.new(dragSpeed), {Position = position}):Play()
end

frame.InputBegan:Connect(function(input)
	if (input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch) then 
		dragToggle = true
		dragStart = input.Position
		startPos = frame.Position
		input.Changed:Connect(function()
			if input.UserInputState == Enum.UserInputState.End then
				dragToggle = false
			end
		end)
	end
end)

UIS.InputChanged:Connect(function(input)
	if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
		if dragToggle then
			updateInput(input)
		end
	end
end)


local WindowTable = {}

for i,v in pairs(game.CoreGui:GetChildren()) do
	if v.Name == "uilibrary" then
		v:Destroy()
	end
end

function WindowTable:Window(options)
	local WindowTitle = options.Title or "Luna Lib"
	local gameName = options.gameName or "Untitled Game"

	local uilibrary = Instance.new("ScreenGui")

	local mainCorner = Instance.new("UICorner")
	local SideBar = Instance.new("Frame")
	local mainCorner_2 = Instance.new("UICorner")
	local Cover = Instance.new("Frame")
	local allTabs = Instance.new("Frame")
	local tabListing = Instance.new("UIListLayout")
	local Title = Instance.new("TextLabel")
	local GameName = Instance.new("TextLabel")
	local allPages = Instance.new("Frame")
	local mainCorner_3 = Instance.new("UICorner")
	local pagesFolder = Instance.new("Folder")

	--Properties:

	uilibrary.Name = "uilibrary"
	uilibrary.Parent = game.CoreGui
	uilibrary.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

	backFrame.Name = "backFrame"
	backFrame.Parent = uilibrary
	backFrame.BackgroundColor3 = Color3.fromRGB(46, 47, 62)
	backFrame.Position = UDim2.new(0.128047928, 0, 0.310115874, 0)
	backFrame.Size = UDim2.new(0, 553,0, 339)

	mainCorner.CornerRadius = UDim.new(0, 4)
	mainCorner.Name = "mainCorner"
	mainCorner.Parent = backFrame

	SideBar.Name = "SideBar"
	SideBar.Parent = backFrame
	SideBar.BackgroundColor3 = Color3.fromRGB(28, 30, 42)
	SideBar.Position = UDim2.new(-0.00154491793, 0, 0, 0)
	SideBar.Size = UDim2.new(0, 133, 0, 337)

	mainCorner_2.CornerRadius = UDim.new(0, 4)
	mainCorner_2.Name = "mainCorner"
	mainCorner_2.Parent = SideBar

	Cover.Name = "Cover"
	Cover.Parent = SideBar
	Cover.BackgroundColor3 = Color3.fromRGB(28, 30, 42)
	Cover.BorderSizePixel = 0
	Cover.Position = UDim2.new(0.514329731, 0, 0.00296731689, 0)
	Cover.Size = UDim2.new(0, 96, 0, 337)

	allTabs.Name = "allTabs"
	allTabs.Parent = SideBar
	allTabs.BackgroundColor3 = Color3.fromRGB(28, 30, 42)
	allTabs.BorderSizePixel = 0
	allTabs.Position = UDim2.new(0.0586054474, 0, 0.144090369, 0)
	allTabs.Size = UDim2.new(0, 149, 0, 284)



	tabListing.Name = "tabListing"
	tabListing.Parent = allTabs
	tabListing.SortOrder = Enum.SortOrder.LayoutOrder
	tabListing.Padding = UDim.new(0, 9)

	Title.Name = "Title"
	Title.Parent = SideBar
	Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Title.BackgroundTransparency = 1.000
	Title.Position = UDim2.new(0.0601503775, 0, 0.00295857503, 0)
	Title.Size = UDim2.new(0, 117, 0, 30)
	Title.Font = Enum.Font.GothamSemibold
	Title.Text = WindowTitle
	Title.TextColor3 = Color3.fromRGB(255, 255, 255)
	Title.TextSize = 14.000
	Title.TextXAlignment = Enum.TextXAlignment.Left

	GameName.Name = "GameName"
	GameName.Parent = SideBar
	GameName.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	GameName.BackgroundTransparency = 1.000
	GameName.Position = UDim2.new(0.172932327, 0, 0.0623057559, 0)
	GameName.Size = UDim2.new(0, 117, 0, 17)
	GameName.Font = Enum.Font.GothamSemibold
	GameName.Text = gameName
	GameName.TextColor3 = Color3.fromRGB(255, 255, 255)
	GameName.TextSize = 14.000
	GameName.TextTransparency = 0.850
	GameName.TextXAlignment = Enum.TextXAlignment.Left

	allPages.Name = "allPages"
	allPages.Parent = backFrame
	allPages.BackgroundColor3 = Color3.fromRGB(28, 30, 42)
	allPages.Position = UDim2.new(0.309485823, 0, 0.0253968369, 0)
	allPages.Size = UDim2.new(0, 375, 0, 323)

	mainCorner_3.CornerRadius = UDim.new(0, 4)
	mainCorner_3.Name = "mainCorner"
	mainCorner_3.Parent = allPages

	pagesFolder.Name = "pagesFolder"
	pagesFolder.Parent = allPages



	local TabHandler = {}

	function TabHandler:CreateTab(options)
		local TabTitle = options.tabtitle or "Tab Example"
		local newPage = Instance.new("ScrollingFrame")
		local ElementsListing = Instance.new("UIListLayout")
		local tabButton = Instance.new("TextButton")
		local buttonCorner = Instance.new("UICorner")

		newPage.Name = "newPage"
		newPage.Parent = pagesFolder
		newPage.Active = true
		newPage.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		newPage.BackgroundTransparency = 1.000
		newPage.BorderSizePixel = 0
		newPage.Position = UDim2.new(0.018666666, 0, 0.0185758509, 0)
		newPage.Size = UDim2.new(0, 362, 0, 310)
		newPage.CanvasSize = UDim2.new(0, 0, 3, 4)
		newPage.ScrollBarThickness = 5
		newPage.Visible = false

		ElementsListing.Name = "ElementsListing"
		ElementsListing.Parent = newPage
		ElementsListing.SortOrder = Enum.SortOrder.LayoutOrder
		ElementsListing.Padding = UDim.new(0, 5)

		tabButton.Name = "tabButton"
		tabButton.Parent = allTabs
		tabButton.BackgroundColor3 = Color3.fromRGB(46, 47, 62)
		tabButton.Size = UDim2.new(0, 149, 0, 32)
		tabButton.AutoButtonColor = false
		tabButton.Font = Enum.Font.Gotham
		tabButton.Text = TabTitle
		tabButton.TextColor3 = Color3.fromRGB(255, 255, 255)
		tabButton.TextSize = 15.000
		tabButton.MouseButton1Click:Connect(function()
			for i,v in next, pagesFolder:GetChildren() do
				v.Visible = false
			end
			newPage.Visible = true

			for i,v in next, allTabs:GetChildren() do
				if v:IsA("TextButton") then
					game.TweenService:Create(v, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
						BackgroundColor3 = Color3.fromRGB(46, 47, 62)
					}):Play()
				end
			end

			game.TweenService:Create(tabButton, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
				BackgroundColor3 = Color3.fromRGB(73, 75, 99)
			}):Play()
		end)

		buttonCorner.CornerRadius = UDim.new(0, 4)
		buttonCorner.Name = "buttonCorner"
		buttonCorner.Parent = tabButton

		local ElementsHandler = {}

		function ElementsHandler:Label(options)
			local LabelText = options.LabelText or "Untitled Label"

			local Label = Instance.new("TextLabel")

			--Properties:

			Label.Name = "Label"
			Label.Parent = newPage
			Label.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
			Label.BackgroundTransparency = 1.000
			Label.Position = UDim2.new(0, 0, -9.84437989e-08, 0)
			Label.Size = UDim2.new(0, 351, 0, 23)
			Label.Font = Enum.Font.SourceSansSemibold
			Label.Text = LabelText
			Label.TextColor3 = Color3.fromRGB(255, 255, 255)
			Label.TextSize = 22.000
		end

		function ElementsHandler:CreateButton(btnText, callback)

			local ButtonText = options.btnText or "Untitled Button"
			local TextButton = Instance.new("TextButton")
			local buttonCorner = Instance.new("UICorner")

			--Properties:

			TextButton.Parent = newPage
			TextButton.BackgroundColor3 = Color3.fromRGB(46, 47, 62)
			TextButton.Position = UDim2.new(0, 0, 0.0903224796, 0)
			TextButton.Size = UDim2.new(0, 352, 0, 37)
			TextButton.Font = Enum.Font.GothamSemibold
			TextButton.Text = btnText
			TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
			TextButton.TextSize = 17.000
			TextButton.MouseButton1Click:Connect(function()
				callback()
			end)
			TextButton.MouseEnter:Connect(function()
				game.TweenService:Create(TextButton, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
					BackgroundColor3 = Color3.fromRGB(73, 75, 99)
				}):Play()
			end)
			TextButton.MouseLeave:Connect(function()
				game.TweenService:Create(TextButton, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
					BackgroundColor3 = Color3.fromRGB(46, 47, 62)
				}):Play()
			end)

			buttonCorner.CornerRadius = UDim.new(0, 4)
			buttonCorner.Name = "buttonCorner"
			buttonCorner.Parent = TextButton
		end

		function ElementsHandler:Toggle(togText, callback)
			togText = togText or "toggle info"
			callback = callback or function() end

			local Toggle = Instance.new("TextButton")
			local togCorner = Instance.new("UICorner")
			local IfToggledColor = Instance.new("Frame")
			local iftogCorner = Instance.new("UICorner")
			local checktog = Instance.new("Frame")
			local iftogCorner_2 = Instance.new("UICorner")
			local TextLabel = Instance.new("TextLabel")

			--Properties:

			Toggle.Name = "Toggle"
			Toggle.Parent = newPage
			Toggle.BackgroundColor3 = Color3.fromRGB(46, 47, 62)
			Toggle.Position = UDim2.new(0, 0, 0.0903224796, 0)
			Toggle.Size = UDim2.new(0, 352, 0, 37)
			Toggle.AutoButtonColor = false
			Toggle.Font = Enum.Font.GothamSemibold
			Toggle.Text = ""
			Toggle.TextColor3 = Color3.fromRGB(255, 255, 255)
			Toggle.TextSize = 20.000


			togCorner.CornerRadius = UDim.new(0, 2)
			togCorner.Name = "togCorner"
			togCorner.Parent = Toggle

			IfToggledColor.Name = "IfToggledColor"
			IfToggledColor.Parent = Toggle
			IfToggledColor.BackgroundColor3 = Color3.fromRGB(28, 30, 42)
			IfToggledColor.Position = UDim2.new(0.803977251, 0, 0.189189196, 0)
			IfToggledColor.Size = UDim2.new(0, 62, 0, 24)

			iftogCorner.CornerRadius = UDim.new(0, 2)
			iftogCorner.Name = "iftogCorner"
			iftogCorner.Parent = IfToggledColor

			checktog.Name = "checktog"
			checktog.Parent = IfToggledColor
			checktog.BackgroundColor3 = Color3.fromRGB(255, 61, 61)
			checktog.Position = UDim2.new(0, 3, 0.0829999968, 0)
			checktog.Size = UDim2.new(0, 20, 0, 20)

			iftogCorner_2.CornerRadius = UDim.new(0, 2)
			iftogCorner_2.Name = "iftogCorner"
			iftogCorner_2.Parent = checktog

			TextLabel.Parent = Toggle
			TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
			TextLabel.BackgroundTransparency = 1.000
			TextLabel.Position = UDim2.new(0.0170454551, 0, 0, 0)
			TextLabel.Size = UDim2.new(0, 266, 0, 37)
			TextLabel.Font = Enum.Font.Gotham
			TextLabel.Text = togText
			TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
			TextLabel.TextSize = 18.000
			TextLabel.TextWrapped = true
			TextLabel.TextXAlignment = Enum.TextXAlignment.Left

			local tog = false

			Toggle.MouseButton1Click:Connect(function()
				tog = not tog

				if tog then
					checktog:TweenPosition(UDim2.new(0.6, 3,0.083, 0), "Out", "Linear", 0.15)
					game.TweenService:Create(checktog, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
						BackgroundColor3 = Color3.fromRGB(0, 255, 136)
					}):Play()
				else
					checktog:TweenPosition(UDim2.new(0, 3,0.083, 0), "Out", "Linear", 0.15)
					game.TweenService:Create(checktog, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
						BackgroundColor3 = Color3.fromRGB(255, 61, 61)
					}):Play()
				end
			end)
		end

		function ElementsHandler:Slider(Text, minvalue, maxvalue, callback)
			--Text, minvalue, maxvalue, callback
			 Text = Text or "Slider"
			 minvalue = minvalue or 0
			 maxvalue = maxvalue or 100


			callback = callback or function() end

			local mouse = game.Players.LocalPlayer:GetMouse()
			local uis = game:GetService("UserInputService")
			local Value;

			local Slider = Instance.new("Frame")
			local mainCorner = Instance.new("UICorner")
			local SliderText = Instance.new("TextLabel")
			local SliderValue = Instance.new("TextLabel")
			local SliderOuter = Instance.new("TextButton")
			local buttonCorner = Instance.new("UICorner")
			local SliderInner = Instance.new("Frame")
			local buttonCorner_2 = Instance.new("UICorner")

			--Properties:

			Slider.Name = "Slider"
			Slider.Parent = newPage
			Slider.BackgroundColor3 = Color3.fromRGB(46, 47, 62)
			Slider.Position = UDim2.new(-0.0165745858, 0, 0.35615167, 0)
			Slider.Size = UDim2.new(0, 351, 0, 52)

			mainCorner.CornerRadius = UDim.new(0, 4)
			mainCorner.Name = "mainCorner"
			mainCorner.Parent = Slider

			SliderText.Name = "SliderText"
			SliderText.Parent = Slider
			SliderText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
			SliderText.BackgroundTransparency = 1.000
			SliderText.Position = UDim2.new(0.0170940179, 0, 0, 0)
			SliderText.Size = UDim2.new(0, 176, 0, 28)
			SliderText.Font = Enum.Font.Gotham
			SliderText.Text = Text
			SliderText.TextColor3 = Color3.fromRGB(255, 255, 255)
			SliderText.TextSize = 18.000
			SliderText.TextXAlignment = Enum.TextXAlignment.Left

			SliderValue.Name = "SliderValue"
			SliderValue.Parent = Slider
			SliderValue.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
			SliderValue.BackgroundTransparency = 1.000
			SliderValue.Position = UDim2.new(0.726495743, 0, 0, 0)
			SliderValue.Size = UDim2.new(0, 90, 0, 28)
			SliderValue.Font = Enum.Font.Gotham
			SliderValue.Text = minvalue.."/"..maxvalue
			SliderValue.TextColor3 = Color3.fromRGB(255, 255, 255)
			SliderValue.TextSize = 18.000
			SliderValue.TextXAlignment = Enum.TextXAlignment.Right

			SliderOuter.Name = "SliderOuter"
			SliderOuter.Parent = Slider
			SliderOuter.BackgroundColor3 = Color3.fromRGB(26, 28, 39)
			SliderOuter.ClipsDescendants = true
			SliderOuter.Position = UDim2.new(0.0170940179, 0, 0.493307561, 0)
			SliderOuter.Size = UDim2.new(0, 339, 0, 19)
			SliderOuter.AutoButtonColor = false
			SliderOuter.Font = Enum.Font.GothamSemibold
			SliderOuter.Text = ""
			SliderOuter.TextColor3 = Color3.fromRGB(255, 255, 255)
			SliderOuter.TextSize = 20.000

			buttonCorner.CornerRadius = UDim.new(0, 4)
			buttonCorner.Name = "buttonCorner"
			buttonCorner.Parent = SliderOuter

			SliderInner.Name = "SliderInner"
			SliderInner.Parent = SliderOuter
			SliderInner.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
			SliderInner.Size = UDim2.new(0, 0, 0, 19)

			buttonCorner_2.CornerRadius = UDim.new(0, 4)
			buttonCorner_2.Name = "buttonCorner"
			buttonCorner_2.Parent = SliderInner

			SliderOuter.MouseButton1Down:Connect(function()
			
				Value = math.floor((((tonumber(maxvalue) - tonumber(minvalue)) / 339) * SliderInner.AbsoluteSize.X) + tonumber(minvalue)) or 0
				pcall(function()
					callback(Value)
				end)
				SliderInner.Size = UDim2.new(0, math.clamp(mouse.X - SliderInner.AbsolutePosition.X, 0, 339), 0, 19)
				moveconnection = mouse.Move:Connect(function()
					SliderValue.Text = Value.."/"..maxvalue
					Value = math.floor((((tonumber(maxvalue) - tonumber(minvalue)) / 339) * SliderInner.AbsoluteSize.X) + tonumber(minvalue))
					pcall(function()
						callback(Value)
					end)
					SliderInner.Size = UDim2.new(0, math.clamp(mouse.X - SliderInner.AbsolutePosition.X, 0, 339), 0, 19)
				end)
				releaseconnection = uis.InputEnded:Connect(function(Mouse)
					if Mouse.UserInputType == Enum.UserInputType.MouseButton1 then
						Value = math.floor((((tonumber(maxvalue) - tonumber(minvalue)) / 339) * SliderInner.AbsoluteSize.X) + tonumber(minvalue))
						pcall(function()
							callback(Value)
						end)
						SliderInner.Size = UDim2.new(0, math.clamp(mouse.X - SliderInner.AbsolutePosition.X, 0, 339), 0, 19)
						moveconnection:Disconnect()
						releaseconnection:Disconnect()
					end
				end)
			end)

		end

		return ElementsHandler
	end

	return TabHandler
end

--[[local win = WindowTable:Window({
	Title = "Luna Lib",
	gameName = "Untitled Game"
})

local tab = win:CreateTab({
	tabtitle = "Main"
})

tab:Slider("Slider Lmfao", 16, 100, function(args)
	game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = args
end)

tab:Label({
	LabelText = "Main"
})

tab:CreateButton("Rainbow Gun", function()
	print("Hello World!")
end)

tab:Toggle("Silent Aim", function(bool)

end)

tab:Toggle("Spread", function(bool)

end)
tab:Toggle("Fire Rate", function(bool)

end)
tab:Toggle("Recoil", function(bool)

end)
tab:Toggle("Bullets", function(bool)

end)
tab:Toggle("Bullet Speed", function(bool)

end)

local tab2 = win:CreateTab({
	tabtitle = "Others"
})]]--

return WindowTable
