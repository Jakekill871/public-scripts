-- default settings
_G.AutoBlock = true -- blocks most incoming hits but may also block your hits.
_G.InfEnergy = true
_G.NoCooldown = true -- works for some things like you can spam ryan's right click.

spawn(function()
a = hookfunction(wait, function(b) if b ~= 0 and tostring(getcallingscript(a)) ~= "nil" and tonumber(b) < 2.5 and _G.NoCooldown == true then return a() end return a(b) end)
end)

spawn(function()
local function CreateInstance(cls,props)
local inst = Instance.new(cls)
for i,v in pairs(props) do
	inst[i] = v
end
return inst
end
	
local ScreenGui = CreateInstance('ScreenGui',{DisplayOrder=0,Enabled=true,ResetOnSpawn=true,Name='ScreenGui', Parent=game.CoreGui})
local Frame = CreateInstance('Frame',{Style=Enum.FrameStyle.Custom,Active=true,AnchorPoint=Vector2.new(0, 0),BackgroundColor3=Color3.new(0, 0, 0),BackgroundTransparency=1,BorderColor3=Color3.new(0.105882, 0.164706, 0.207843),BorderSizePixel=1,ClipsDescendants=false,Draggable=false,Position=UDim2.new(0.717395179, 0, 0.219242901, 0),Rotation=0,Selectable=false,Size=UDim2.new(0, 531, 0, 267),SizeConstraint=Enum.SizeConstraint.RelativeXY,Visible=true,ZIndex=1,Name = 'Frame',Parent = ScreenGui})
local AutoBlock = CreateInstance('TextButton',{Font=Enum.Font.SourceSans,FontSize=Enum.FontSize.Size14,Text='Toggle Auto Block (Default)',TextColor3=Color3.new(0.792157, 0.792157, 0.792157),TextScaled=false,TextSize=14,TextStrokeColor3=Color3.new(0, 0, 0),TextStrokeTransparency=1,TextTransparency=0,TextWrapped=false,TextXAlignment=Enum.TextXAlignment.Center,TextYAlignment=Enum.TextYAlignment.Center,AutoButtonColor=true,Modal=false,Selected=false,Style=Enum.ButtonStyle.Custom,Active=true,AnchorPoint=Vector2.new(0, 0),BackgroundColor3=Color3.new(0, 0, 0),BackgroundTransparency=0,BorderColor3=Color3.new(0.105882, 0.164706, 0.207843),BorderSizePixel=1,ClipsDescendants=false,Draggable=false,Position=UDim2.new(0, 0, 0, 50),Rotation=0,Selectable=true,Size=UDim2.new(0, 170, 0, 50),SizeConstraint=Enum.SizeConstraint.RelativeXY,Visible=true,ZIndex=1,Name='Script1',Parent = Frame})
local InfEnergy = CreateInstance('TextButton',{Font=Enum.Font.SourceSans,FontSize=Enum.FontSize.Size14,Text='Toggle Infinite Energy (Default)',TextColor3=Color3.new(0.792157, 0.792157, 0.792157),TextScaled=false,TextSize=14,TextStrokeColor3=Color3.new(0, 0, 0),TextStrokeTransparency=1,TextTransparency=0,TextWrapped=false,TextXAlignment=Enum.TextXAlignment.Center,TextYAlignment=Enum.TextYAlignment.Center,AutoButtonColor=true,Modal=false,Selected=false,Style=Enum.ButtonStyle.Custom,Active=true,AnchorPoint=Vector2.new(0, 0),BackgroundColor3=Color3.new(0, 0, 0),BackgroundTransparency=0,BorderColor3=Color3.new(0.105882, 0.164706, 0.207843),BorderSizePixel=1,ClipsDescendants=false,Draggable=false,Position=UDim2.new(0, 0, 0, 105),Rotation=0,Selectable=true,Size=UDim2.new(0, 170, 0, 50),SizeConstraint=Enum.SizeConstraint.RelativeXY,Visible=true,ZIndex=1,Name='Script2',Parent = Frame})
local NoCooldown = CreateInstance('TextButton',{Font=Enum.Font.SourceSans,FontSize=Enum.FontSize.Size14,Text='Toggle No Cooldown (Default)',TextColor3=Color3.new(0.792157, 0.792157, 0.792157),TextScaled=false,TextSize=14,TextStrokeColor3=Color3.new(0, 0, 0),TextStrokeTransparency=1,TextTransparency=0,TextWrapped=false,TextXAlignment=Enum.TextXAlignment.Center,TextYAlignment=Enum.TextYAlignment.Center,AutoButtonColor=true,Modal=false,Selected=false,Style=Enum.ButtonStyle.Custom,Active=true,AnchorPoint=Vector2.new(0, 0),BackgroundColor3=Color3.new(0, 0, 0),BackgroundTransparency=0,BorderColor3=Color3.new(0.105882, 0.164706, 0.207843),BorderSizePixel=1,ClipsDescendants=false,Draggable=false,Position=UDim2.new(0, 0, 0, 160),Rotation=0,Selectable=true,Size=UDim2.new(0, 170, 0, 50),SizeConstraint=Enum.SizeConstraint.RelativeXY,Visible=true,ZIndex=1,Name='Script3',Parent = Frame})
ScreenGui.Parent = game:GetService("CoreGui")

spawn(function()
wait(0.2)
if _G.AutoBlock then AutoBlock.Text = "Toggle Auto Block (On)" else AutoBlock.Text = "Toggle Auto Block (Off)" end
if _G.InfEnergy then InfEnergy.Text = "Toggle Infinite Energy (On)" else InfEnergy.Text = "Toggle Infinite Energy (Off)" end
if _G.NoCooldown then NoCooldown.Text = "Toggle No Cooldown (On)" else NoCooldown.Text = "Toggle No Cooldown (Off)" end
end)

AutoBlock.MouseButton1Click:Connect(function()
if _G.AutoBlock == true then _G.AutoBlock = false AutoBlock.Text = "Toggle Auto Block (Off)" elseif _G.AutoBlock == false then _G.AutoBlock = true AutoBlock.Text = "Toggle Auto Block (On)" end
end)

InfEnergy.MouseButton1Click:Connect(function()
if _G.InfEnergy == true then _G.InfEnergy = false InfEnergy.Text = "Toggle Infinite Energy (Off)" elseif _G.InfEnergy == false then _G.InfEnergy = true InfEnergy.Text = "Toggle Infinite Energy (On)" end
end)

NoCooldown.MouseButton1Click:Connect(function()
if _G.NoCooldown == true then _G.NoCooldown = false NoCooldown.Text = "Toggle No Cooldown (Off)" elseif _G.NoCooldown == false then _G.NoCooldown = true NoCooldown.Text = "Toggle No Cooldown (On)" end
end)
end)

name = tostring(game.Players.LocalPlayer.Name)
game:GetService("RunService").Heartbeat:Connect(function()
spawn(function()
if _G.AutoBlock == true then
wait()
game:GetService("ReplicatedStorage").RemoteEvents.ReplicateGuardOn:FireServer()
game:GetService("Workspace")[name].Guarding.Value = false
wait()
game:GetService("ReplicatedStorage").RemoteEvents.ReplicateGuardOff:FireServer()
end
end)

spawn(function()
if _G.InfEnergy then
game:GetService("Workspace")[name].Energy.Value = 97
end
end)
end)
