local QBCore = exports['qb-core']:GetCoreObject()

# Client Side

esx:onPlayerDeath -> hospital:server:SetDeathStatus

esx:playerLoaded -> QBCore:Client:OnPlayerLoaded

esx:showAdvancedNotification -> QBCore:Notify

esx:showHelpNotification -> QBCore:Notify

esx:showNotification -> QBCore:Notify

ESX.GetPlayerData -> QBCore.Functions.GetPlayerData

ESX.IsPlayerLoaded -> None

ESX.SetPlayerData -> QBCore:Player:SetPlayerData

ESX.TriggerServerCallback -> QBCore.Functions.TriggerCallback

ESX.Game.DeleteObject -> None (Can use FiveM native DeleteEntity)

ESX.Game.DeleteVehicle -> QBCore.Functions.DeleteVehicle

ESX.Game.GetClosestObject -> None (Can use FiveM native GetClosestObjectOfType)

ESX.Game.GetClosestPed -> QBCore.Functions.GetClosestPed

ESX.Game.GetClosestPlayer -> QBCore.Functions.GetClosestPlayer

ESX.Game.GetClosestVehicle -> QBCore.Functions.GetClosestVehicle

ESX.Game.GetObjects -> None (uses enumeration)

ESX.Game.GetPedMugshot -> None (Can use FiveM native RegisterPedheadshot)

ESX.Game.GetPeds -> None (uses enumeration)

ESX.Game.GetPlayers -> QBCore.Functions.GetPlayers

ESX.Game.GetPlayersInArea -> None (uses enumeration)

ESX.Game.GetVehicleInDirection -> None (uses ray casting)

ESX.Game.GetVehicles -> QBCore.Functions.GetVehicles

ESX.Game.GetVehiclesInArea -> None (uses enumeration)

ESX.Game.IsSpawnPointClear -> None (uses getvehiclesinarea)

ESX.Game.SetVehicleProperties -> QBCore.Functions.SetVehicleProperties

ESX.Game.SpawnLocalObject -> None (dont bother)

ESX.Game.SpawnLocalVehicle -> None (dont bother)

ESX.Game.SpawnObject -> None (Can use FiveM Native CreateObject)

ESX.Game.SpawnVehicle -> QBCore.Functions.SpawnVehicle

ESX.Game.Teleport -> (Can use FiveM Native SetEntityCoords and SetEntityHeading)

ESX.Game.Utils.DrawText3D -> None (use local function)

# Server Side

ESX.CreatePickup -> None (irrelevant and done through qb-inventory)

ESX.GetItemLabel -> None (Just returns item label)

ESX.GetPlayerFromId -> QBCore.Functions.GetPlayer

ESX.GetPlayerFromIdentifier -> QBCore.Functions.GetPlayerByCitizenId

ESX.GetPlayers -> QBCore.Functions.GetPlayers

ESX.RegisterServerCallback -> QBCore.Functions.CreateCallback

ESX.RegisterUsableItem -> QBCore.Functions.CreateUseableItem

ESX.SavePlayer -> QBCore.Player.Save

ESX.SavePlayers -> None (dont bother)

ESX.Trace -> Use QBCore.Debug but dont bother converting this

ESX.UseItem -> QBCore.Functions.UseItem

# xPlayer

xPlayer.addAccountMoney -> xPlayer.Functions.AddMoney (account)

xPlayer.addInventoryItem -> xPlayer.Functions.AddItem (item name)

xPlayer.addMoney -> xPlayer.Functions.AddMoney (cash)

xPlayer.addWeapon -> xPlayer.Functions.AddItem (weapon name)

xPlayer.addWeaponAmmo -> xPlayer.Functions.AddItem (ammo name)

xPlayer.addWeaponComponent -> xPlayer.Functions.AddItem (component name)

xPlayer.canCarryItem -> None (xPlayer.Functions.AddItem already checks this)

xPlayer.canSwapItem -> None (xPlayer.Functions.AddItem already checks this)

xPlayer.getAccount -> None (use player data)

xPlayer.getAccounts -> None (use player data)

xPlayer.getCoords -> None (Can use FiveM Native GetEntityCoords)

xPlayer.getGroup -> xPlayer.Functions.GetPermission

xPlayer.getIdentifier -> xPlayer.Functions.GetIdentifier

xPlayer.getInventory -> QBCore.Player.LoadInventory

xPlayer.getInventoryItem -> xPlayer.Functions.GetItemByName

xPlayer.getJob -> None (use player data)

xPlayer.getLoadout -> None (fuck loadouts)

xPlayer.getMoney -> None (use player data)

xPlayer.getName -> None (use player data)

xPlayer.getWeapon -> xPlayer.Functions.GetItemByName (weapon name)

xPlayer.getWeight -> xPlayer.Player.GetTotalWeight

xPlayer.hasWeapon -> xPlayer.Functions.GetItemByName (weapon name)

xPlayer.hasWeaponComponent -> xPlayer.Functions.GetItemByName (component name)

xPlayer.kick -> xPlayer.Functions.Kick

xPlayer.removeAccountMoney -> xPlayer.Functions.RemoveMoney (account)

xPlayer.removeInventoryItem -> xPlayer.Functions.RemoveItem (item name)

xPlayer.removeMoney -> xPlayer.Functions.RemoveMoney (cash)

xPlayer.removeWeapon -> xPlayer.Functions.RemoveItem (weapon name)

xPlayer.removeWeaponAmmo -> xPlayer.Functions.RemoveItem (ammo name)

xPlayer.removeWeaponComponent -> xPlayer.Functions.RemoveItem (component name)

xPlayer.setAccountMoney -> xPlayer.Functions.SetMoney (account)

xPlayer.setCoords -> None (used for teleporting)

xPlayer.setInventoryItem -> xPlayer.Functions.AddItem (item name)

xPlayer.setJob -> xPlayer.Functions.SetJob

xPlayer.setMaxWeight -> None (It is set in qb-core config) 

xPlayer.setMoney -> xPlayer.Functions.SetMoney

xPlayer.setName -> None (dont bother)

xPlayer.setWeaponTint -> None (qb-weapons does this)

xPlayer.showHelpNotification -> TriggerClientEvent('QBCore:Notify')

xPlayer.showNotification -> TriggerClientEvent('QBCore:Notify')

xPlayer.triggerEvent -> None (dont bother)

xPlayer.updateCoords -> None (dont bother)

# Events

esx:setJob -> QBCore:Client:OnJobUpdate

esx:onPlayerSpawn -> QBCore:Client:OnPlayerLoaded

playerSpawned -> QBCore:Client:OnPlayerLoaded (spawnmanager compatibility)

esx:addInventoryItem -> QBCore:Server:AddItem

esx:removeInventoryItem -> QBCore:Server:RemoveItem

esx:useItem -> QBCore:Server:UseItem

# ghmatti to oxmysql

ghmattimysql:execute('UPDATE... -> oxmysql:execute('UPDATE...

ghmattimysql:execute('DELETE... -> oxmysql:execute('DELETE...

ghmattimysql:execute('SELECT... -> oxmysql:fetch('SELECT...

ghmattimysql:execute('INSERT... -> oxmysql:insert('INSERT...

['ghmattimysql']:execute('UPDATE... -> .oxmysql:execute('UPDATE...

['ghmattimysql']:execute('DELETE... -> .oxmysql:execute('DELETE...

['ghmattimysql']:execute('SELECT... -> .oxmysql:fetch('SELECT...

['ghmattimysql']:execute('INSERT... -> .oxmysql:insert('INSERT...

# SQL Export

exports.ghmattimysql.execute -> exports.oxmysql:execute

exports.ghmattimysql.executeSync -> exports.oxmysql:executeSync

exports.ghmattimysql.scalar -> exports.oxmysql:scalar

exports.ghmattimysql.scalarSync -> exports.oxmysql:scalarSync

MySQL.Async.execute -> exports.oxmysql:execute

MySQL.Async.fetchAll -> exports.oxmysql:execute

MySQL.Sync.fetchAll -> exports.oxmysql:executeSync

MySQL.Async.fetchScalar -> exports.oxmysql:scalar

MySQL.Async.insert -> exports.oxmysql:insert
