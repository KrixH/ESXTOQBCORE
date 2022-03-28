# ESXTOQBCORE
![ESXTOQBCORE](https://i.imgur.com/o6c0bUL.png) 
#
![ESXTOQBCORE](https://i.imgur.com/hjlkyIe.png)
#
![ESXTOQBCORE](https://i.imgur.com/UwJtvMZ.png)
#
![ESXTOQBCORE](https://i.imgur.com/6B7Hi5w.png)
#
![ESXTOQBCORE](https://i.imgur.com/vouVCeY.png)
#
![ESXTOQBCORE](https://i.imgur.com/bN8gVWj.png)
#
![ESXTOQBCORE](https://i.imgur.com/P0iMaN7.png)
#
![ESXTOQBCORE](https://i.imgur.com/RgE1DIE.png)
#
![ESXTOQBCORE](https://i.imgur.com/XhuiRQG.png)
#
![ESXTOQBCORE](https://i.imgur.com/VFnKylp.png)
#
![ESXTOQBCORE](https://i.imgur.com/m4D7L8A.png)
#
![ESXTOQBCORE](https://i.imgur.com/1g6Blyj.png)
#
![ESXTOQBCORE](https://i.imgur.com/G2ZInP3.png)
#
![ESXTOQBCORE](https://i.imgur.com/bzMYTa4.png)
#
![ESXTOQBCORE](https://i.imgur.com/TPdKH80.png)
#
![ESXTOQBCORE](https://i.imgur.com/mbj0AWU.png)
#
![ESXTOQBCORE](https://i.imgur.com/rmKQn69.png)
#
![ESXTOQBCORE](https://i.imgur.com/o88nRzy.png)
#
```
ESX.GetPlayerData                       = QBCore.Functions.GetPlayerData
ESX.SetPlayerData                       = QBCore:Player:SetPlayerData
ESX.TriggerServerCallback               = QBCore.Functions.TriggerCallback
ESX.Game.DeleteVehicle                  = QBCore.Functions.DeleteVehicle
ESX.Game.GetClosestPed                  = QBCore.Functions.GetClosestPed
ESX.Game.GetClosestPlayer               = QBCore.Functions.GetClosestPlayer
ESX.Game.GetClosestVehicle              = QBCore.Functions.GetClosestVehicle
ESX.Game.GetPlayers                     = QBCore.Functions.GetPlayers
ESX.Game.GetVehicles                    = QBCore.Functions.GetVehicles
ESX.Game.SetVehicleProperties           = QBCore.Functions.SetVehicleProperties
ESX.Game.SpawnVehicle                   = QBCore.Functions.SpawnVehicle
ESX.Game.Utils.DrawText3D               = QBCore.Functions.DrawText3D
ESX.GetPlayerFromId                     = QBCore.Functions.GetPlayer
ESX.GetPlayerFromIdentifier             = QBCore.Functions.GetPlayerByCitizenId
ESX.GetPlayers                          = QBCore.Functions.GetPlayers
ESX.RegisterServerCallback              = QBCore.Functions.CreateCallback
ESX.RegisterUsableItem                  = QBCore.Functions.CreateUseableItem
ESX.SavePlayer                          = QBCore.Player.Save
ESX.Trace                               = QBCore.Debug
ESX.UseItem                             = QBCore.Functions.UseItem

ESX.IsPlayerLoaded                      = None (checks if player is loaded so not relevant)
ESX.Game.DeleteObject                   = None (Can use FiveM native DeleteEntity)
ESX.Game.GetClosestObject               = None (Can use FiveM native GetClosestObjectOfType)
ESX.Game.GetObjects                     = None (uses enumeration)
ESX.Game.GetPedMugshot                  = None (Can use FiveM native RegisterPedheadshot)
ESX.Game.GetPeds                        = None (uses enumeration)
ESX.Game.GetPlayersInArea               = None (uses enumeration)
ESX.Game.GetVehicleInDirection          = None (uses ray casting)
ESX.Game.GetVehiclesInArea              = None (uses enumeration)
ESX.Game.IsSpawnPointClear              = None (uses getvehiclesinarea)
ESX.Game.SpawnLocalObject               = None (dont bother)
ESX.Game.SpawnLocalVehicle              = None (dont bother)
ESX.Game.SpawnObject                    = None (Can use FiveM Native CreateObject)
ESX.CreatePickup                        = None (irrelevant and done through qb-inventory)
ESX.GetItemLabel                        = None (Just returns item label)
ESX.SavePlayers                         = None (dont bother)
ESX.Game.Teleport                       = (Can use FiveM Native SetEntityCoords and SetEntityHeading)
  
esx:onPlayerDeath                       = hospital:server:SetDeathStatus
esx:playerLoaded                        = QBCore:Client:OnPlayerLoaded (use for setting a variable to let the script know the player is ready)
esx:showAdvancedNotification            = QBCore:Notify
esx:showHelpNotification                = QBCore:Notify
esx:showNotification                    = QBCore:Notify
esx:getSharedObject                     = QBCore:GetObject
esx:setJob                              = QBCore:Client:OnJobUpdate
esx:onPlayerSpawn                       = QBCore:Client:OnPlayerLoaded
playerSpawned                           = QBCore:Client:OnPlayerLoaded (spawnmanager compatibility)
esx:addInventoryItem                    = QBCore:Server:AddItem
esx:removeInventoryItem                 = QBCore:Server:RemoveItem
esx:useItem                             = QBCore:Server:UseItem

xPlayer.removeWeaponComponent           = xPlayer.Functions.RemoveItem (component name)
xPlayer.setAccountMoney                 = xPlayer.Functions.SetMoney (account)
xPlayer.setInventoryItem                = xPlayer.Functions.AddItem (item name)
xPlayer.setJob                          = xPlayer.Functions.SetJob
xPlayer.setMoney                        = xPlayer.Functions.SetMoney
xPlayer.showHelpNotification            = TriggerClientEvent('QBCore:Notify')
xPlayer.showNotification                = TriggerClientEvent('QBCore:Notify')
xPlayer.setCoords                       = None (used for teleporting)
xPlayer.setMaxWeight                    = None (It is set in qb-core config)
xPlayer.setName                         = None (dont bother)
xPlayer.setWeaponTint                   = None (qb-weapons does this)
xPlayer.triggerEvent                    = None (dont bother)
xPlayer.updateCoords                    = None (dont bother)
  
MySQL.Async.fetchScalar()               = exports['ghmattimysql']:scalar() or QBCore.Functions.ExecuteSql(true,
MySQL.Async.fetchAll()                  = exports['ghmattimysql']:execute() or QBCore.Functions.ExecuteSql(true,
MySQL.Async.execute()                   = exports['ghmattimysql']:execute() or QBCore.Functions.ExecuteSql(false, 
```
#
```
QBCore.Functions.GetPlayerData                    = function(cb)
QBCore.Functions.GetPlayers                       = function()
QBCore.Functions.DrawText                         = function(x, y, width, height, scale, r, g, b, a, text)
QBCore.Functions.DrawText3D                       = function(x, y, z, text)
QBCore.Functions.GetCoords                        = function(entity)
QBCore.Functions.SpawnVehicle                     = function(model, cb, coords, isnetworked)
QBCore.Functions.DeleteVehicle                    = function(vehicle)
QBCore.Functions.Notify                           = function(text, textype, length)
QBCore.Functions.TriggerCallback                  = function(name, cb, ...)
QBCore.Functions.EnumerateEntities                = function(initFunc, moveFunc, disposeFunc)
QBCore.Functions.GetVehicles                      = function()
QBCore.Functions.GetPeds                          = function(ignoreList)
QBCore.Functions.GetClosestVehicle                = function(coords)
QBCore.Functions.GetClosestPed                    = function(coords, ignoreList)
QBCore.Functions.GetClosestPlayer                 = function(coords)
QBCore.Functions.GetPlayersFromCoords             = function(coords, distance)
QBCore.Functions.HasItem                          = function(source, cb, item)
QBCore.Functions.Progressbar                      = function(name, label, duration, useWhileDead, canCancel, disableControls, animation, prop, propTwo, onFinish, onCancel)
QBCore.Functions.GetVehicleProperties             = function(vehicle)
QBCore.Functions.SetVehicleProperties             = function(vehicle, props) 
QBCore.Functions.ExecuteSql                       = function(wait, query, cb) 
QBCore.Functions.GetIdentifier                    = function(source, idtype)         
QBCore.Functions.GetSource                        = function(identifier)        
QBCore.Functions.GetPlayer                        = function(source)        
QBCore.Functions.GetPlayerByCitizenId             = function(citizenid)        
QBCore.Functions.GetPlayerByPhone                 = function(number)        
QBCore.Functions.GetPlayers                       = function()        
QBCore.Functions.CreateCallback                   = function(name, cb)        
QBCore.Functions.TriggerCallback                  = function(name, source, cb, ...)        
QBCore.Functions.CreateUseableItem                = function(item, cb)        
QBCore.Functions.CanUseItem                       = function(item)        
QBCore.Functions.UseItem                          = function(source, item)        
QBCore.Functions.AddPermission                    = function(source, permission)        
QBCore.Functions.RemovePermission                 = function(source)     
QBCore.Functions.HasPermission                    = function(source, permission)   
QBCore.Functions.GetPermission                    = function(source)      
QBCore.Functions.IsPlayerBanned                   = function (source) 
```
