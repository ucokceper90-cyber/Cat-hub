local Players = game:GetService("Players")
local StarterGui = game:GetService("StarterGui")
local LocalPlayer = Players.LocalPlayer

-- Target player (ganti manual atau bisa dibuat auto)
local target = Players:GetPlayers()[2] -- contoh ambil player lain

local function reportPlayer(reasonText, descriptionText)
	if target then
		StarterGui:SetCore("ReportAbuse", {
			UserId = target.UserId,
			Reason = reasonText,
			Description = descriptionText
		})
	end
end

-- GUI sederhana
local ScreenGui = Instance.new("ScreenGui", game.CoreGui)

local function createButton(text, posY, reason, desc)
	local btn = Instance.new("TextButton")
	btn.Parent = ScreenGui
	btn.Size = UDim2.new(0,200,0,40)
	btn.Position = UDim2.new(0,20,0,posY)
	btn.Text = text
	btn.BackgroundColor3 = Color3.fromRGB(30,30,30)
	btn.TextColor3 = Color3.new(1,1,1)

	btn.MouseButton1Click:Connect(function()
		reportPlayer(reason, desc)
	end)
end

createButton("Report Avatar 18+", 100, "Inappropriate Avatar", "Avatar mengandung unsur 18+")
createButton("Report Avatar Sus", 150, "Inappropriate Avatar", "Avatar mencurigakan")
createButton("Report Toxic Chat", 200, "Swearing", "Toxic chat / kata kasar")
