--[[
 .____                  ________ ___.    _____                           __                
 |    |    __ _______   \_____  \\_ |___/ ____\_ __  ______ ____ _____ _/  |_  ___________ 
 |    |   |  |  \__  \   /   |   \| __ \   __\  |  \/  ___// ___\\__  \\   __\/  _ \_  __ \
 |    |___|  |  // __ \_/    |    \ \_\ \  | |  |  /\___ \\  \___ / __ \|  | (  <_> )  | \/
 |_______ \____/(____  /\_______  /___  /__| |____//____  >\___  >____  /__|  \____/|__|   
         \/          \/         \/    \/                \/     \/     \/                   
          \_Welcome to LuaObfuscator.com   (Alpha 0.10.9) ~  Much Love, Ferib 

]]--

local v0 = game:GetService("Players");
local v1 = game:GetService("RunService");
local v2 = v0.LocalPlayer;
local v3 = workspace.CurrentCamera;
local v4 = true;
local v5 = true;
local v6 = Color3.fromRGB(1412 - (359 + 953), 1197 - (915 + 82), 722 - 467);
local v7 = 0.35 + 0;
local v8 = Color3.fromRGB(131 - 31, 1387 - (1069 + 118), 578 - 323);
local v9 = 3 - 1;
local v10 = 0.15 + 0;
local v11 = Instance.new("ScreenGui");
v11.Name = "LocalPlayerVisuals";
v11.ResetOnSpawn = false;
v11.IgnoreGuiInset = true;
v11.Parent = v2:WaitForChild("PlayerGui");
local v16 = Instance.new("Folder");
v16.Name = "Tracers";
v16.Parent = v11;
local v19 = {};
local v20 = {};
local function v21(v27)
	if v19[v27] then
		local v62 = 0 - 0;
		while true do
			if (v62 ~= 0) then
			else
				for v91, v92 in ipairs(v19[v27]) do
					if v92 then
						v92:Destroy();
					end
				end
				v19[v27] = nil;
				break;
			end
		end
	end
end
local function v22(v28, v29)
	local v30 = 0;
	local v31;
	local v32;
	while true do
		if (v30 ~= 2) then
		else
			v32 = {"Head","UpperTorso","LowerTorso","LeftUpperArm","LeftLowerArm","LeftHand","RightUpperArm","RightLowerArm","RightHand","LeftUpperLeg","LeftLowerLeg","LeftFoot","RightUpperLeg","RightLowerLeg","RightFoot","Torso","Left Arm","Right Arm","Left Leg","Right Leg"};
			for v81, v82 in ipairs(v32) do
				local v83 = 430 - (44 + 386);
				local v84;
				while true do
					if (v83 == 0) then
						v84 = v29:FindFirstChild(v82);
						if (v84 and v84:IsA("BasePart")) then
							local v103 = 1486 - (998 + 488);
							local v104;
							while true do
								if (v103 ~= (1 + 0)) then
								else
									v104.Adornee = v84;
									v104.Size = v84.Size + Vector3.new(0.08, 0.08, 0.08 + 0);
									v103 = 774 - (201 + 571);
								end
								if (v103 ~= (1138 - (116 + 1022))) then
								else
									v104 = Instance.new("BoxHandleAdornment");
									v104.Name = "GhostBlock";
									v103 = 4 - 3;
								end
								if (v103 == 4) then
									v104.Parent = v84;
									table.insert(v31, v104);
									break;
								end
								if (v103 ~= (2 + 0)) then
								else
									v104.Color3 = v6;
									v104.Transparency = v7;
									v103 = 10 - 7;
								end
								if (v103 ~= (10 - 7)) then
								else
									v104.AlwaysOnTop = true;
									v104.ZIndex = 864 - (814 + 45);
									v103 = 9 - 5;
								end
							end
						end
						break;
					end
				end
			end
			break;
		end
		if (v30 == (1 + 0)) then
			v31 = {};
			v19[v28] = v31;
			v30 = 1 + 1;
		end
		if (v30 ~= (885 - (261 + 624))) then
		else
			if (v28 ~= v2) then
			else
				return;
			end
			v21(v28);
			v30 = 1 - 0;
		end
	end
end
local function v23(v33)
	if v20[v33] then
		v20[v33]:Destroy();
		v20[v33] = nil;
	end
end
local function v24(v34)
	local v35 = 1080 - (1020 + 60);
	local v36;
	while true do
		if (v35 == (1425 - (630 + 793))) then
			v36.BackgroundTransparency = v10;
			v36.BorderSizePixel = 0 - 0;
			v36.Size = UDim2.fromOffset(v9, 0);
			v35 = 3;
		end
		if ((14 - 11) ~= v35) then
		else
			v36.Visible = false;
			v36.Parent = v16;
			v20[v34] = v36;
			break;
		end
		if (v35 ~= (1 + 0)) then
		else
			v36.Name = v34.Name .. "_Tracer";
			v36.AnchorPoint = Vector2.new(0.5 - 0, 1747.5 - (760 + 987));
			v36.BackgroundColor3 = v8;
			v35 = 1915 - (1789 + 124);
		end
		if (v35 == (766 - (745 + 21))) then
			if (v34 ~= v2) then
			else
				return;
			end
			v23(v34);
			v36 = Instance.new("Frame");
			v35 = 1 + 0;
		end
	end
end
local function v25(v37, v38)
	local v39 = 0 - 0;
	local v40;
	local v41;
	local v42;
	local v43;
	local v44;
	local v45;
	local v46;
	local v47;
	while true do
		if (v39 == 0) then
			if not v5 then
				local v86 = 0 - 0;
				while true do
					if (v86 ~= (0 + 0)) then
					else
						v38.Visible = false;
						return;
					end
				end
			end
			v40 = v37.Character;
			if not v40 then
				local v87 = 0 + 0;
				while true do
					if (v87 ~= 0) then
					else
						v38.Visible = false;
						return;
					end
				end
			end
			v39 = 1;
		end
		if (v39 ~= (1056 - (87 + 968))) then
		else
			v41 = v40:FindFirstChild("HumanoidRootPart") or v40:FindFirstChild("Torso");
			if not v41 then
				v38.Visible = false;
				return;
			end
			v42, v43 = v3:WorldToViewportPoint(v41.Position);
			v39 = 8 - 6;
		end
		if (v39 ~= (3 + 0)) then
		else
			v46 = v45 - v44;
			v47 = v46.Magnitude;
			if (v47 > (2 - 1)) then
			else
				local v89 = 1413 - (447 + 966);
				while true do
					if (v89 ~= 0) then
					else
						v38.Visible = false;
						return;
					end
				end
			end
			v39 = 4;
		end
		if (v39 == (13 - 8)) then
			v38.Visible = true;
			break;
		end
		if (v39 ~= (1821 - (1703 + 114))) then
		else
			v38.Position = UDim2.fromOffset((v44.X + v45.X) / (703 - (376 + 325)), (v44.Y + v45.Y) / (2 - 0));
			v38.Size = UDim2.fromOffset(v9, v47);
			v38.Rotation = math.deg(math.atan2(v46.X, -v46.Y));
			v39 = 5;
		end
		if ((5 - 3) ~= v39) then
		else
			if (v42.Z > 0) then
			else
				local v90 = 0 + 0;
				while true do
					if (v90 ~= (0 - 0)) then
					else
						v38.Visible = false;
						return;
					end
				end
			end
			v44 = Vector2.new(v3.ViewportSize.X / (16 - (9 + 5)), 376 - (85 + 291));
			v45 = Vector2.new(v42.X, v42.Y);
			v39 = 1268 - (243 + 1022);
		end
	end
end
local function v26(v48)
	if (v48 ~= v2) then
	else
		return;
	end
	v24(v48);
	v48.CharacterAdded:Connect(function(v58)
		local v59 = 0 - 0;
		while true do
			if (v59 == (0 + 0)) then
				task.wait(1180.25 - (1123 + 57));
				if v4 then
					v22(v48, v58);
				end
				break;
			end
		end
	end);
	if (v48.Character and v4) then
		task.spawn(function()
			local v80 = 0 + 0;
			while true do
				if (v80 ~= 0) then
				else
					task.wait(254.25 - (163 + 91));
					if v48.Character then
						v22(v48, v48.Character);
					end
					break;
				end
			end
		end);
	end
end
for v49, v50 in ipairs(v0:GetPlayers()) do
	v26(v50);
end
v0.PlayerAdded:Connect(v26);
v0.PlayerRemoving:Connect(function(v51)
	local v52 = 1930 - (1869 + 61);
	while true do
		if (v52 ~= (0 + 0)) then
		else
			v21(v51);
			v23(v51);
			break;
		end
	end
end);
v1.RenderStepped:Connect(function()
	v3 = workspace.CurrentCamera;
	for v60, v61 in pairs(v20) do
		v25(v60, v61);
	end
end);
_G.ToggleGhosts = function(v54)
	local v55 = 0 - 0;
	while true do
		if (v55 ~= (0 - 0)) then
		else
			v4 = v54;
			if not v54 then
				for v93 in pairs(v19) do
					v21(v93);
				end
			else
				for v94, v95 in ipairs(v0:GetPlayers()) do
					if ((v95 ~= v2) and v95.Character) then
						v22(v95, v95.Character);
					end
				end
			end
			break;
		end
	end
end;
_G.ToggleTracers = function(v56)
	local v57 = 0 + 0;
	while true do
		if (v57 ~= 0) then
		else
			v5 = v56;
			if not v56 then
				for v96, v97 in pairs(v20) do
					v97.Visible = false;
				end
			end
			break;
		end
	end
end;
