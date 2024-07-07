local player = game.Players.LocalPlayer
while true do
    if player.Character then
        if player.Character:FindFirstChild("HumanoidRootPart") then
            local pos = player.Character.HumanoidRootPart.CFrame
            wait(0)
            if not player.Character or not player.Character:FindFirstChild("HumanoidRootPart") or player.Character.HumanoidRootPart.CFrame ~= pos then
                wait(0)
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId)
            end
        end
    end
    wait(0)
end
