February 2018 UPDATE
-------------------------------------
*ANS_ToggleWeaponAttachment-Player was changed to AN_ToggleHandItems
*CollisionHandlerComponent is no longer limited to skeletal meshes, static mesh can be used now as well  
*New function in MontagesManagerComponent, 'GetRandomMontageIndex'
*New function in BPL_CombatSystemFunctionLibrary 'GetStatisticComponent' which allows to get StatisticComponent by it's type (Health/Stamina)
*AI Strafing behavior works now on curved locations
*All used input keys are now stored in ConfigFile (Edit->ProjectSettings->Input)
*RotateTowardsTarget logic was moved entirely from BP_BaseAI to Anim notify (ANS_RotateTowardsTarget)
*Equipment Component Added (Allows player to equipp weapons/armor parts)
*Inventory Component Added (Allows player to store, use and drop items)
*Behavior Component Added (for now it only allows to specify enemies of AI, will be extended in next updates)
*New event dispatcher OnTargetChanged added to DynamicTargetingComponent
*New event dispatcher OnValueChanged added to StatisticComponent

Changes are described more precisely in attached pdf file
-------------------------------------

March 2018 UPDATE
-------------------------------------
*Support 4.19
*Changed hardcoded Jump/Roll Inputs to ActionEvents in 'BP_CombatCharacter'
*Added functions 'FindById' & 'EquipItems' & 'AddStartItems' to 'InventoryComponent'
*Added Array 'EquippedItems' to 'InventoryComponent'
*Added new struct F_StartingItem (ItemId, Count)
*Replaced 'StartingItems' variable(Map<Name,Int>) in 'InventoryComponent' to array of F_StartingItem
*Added function 'GetWeaponType to 'EquipmentComponent'
*Added Delay(0) node before getting 'EquipmentComponent' in 'ABP_CombatCharacter'
*Variable 'WeaponType' from 'ABP_CombatCharacter' is updated on 'BlueprintInitializeAnimation' in case weapon was equipped on game start
*Replaced Input Helpers below inventory to Widget showing item stats & description
*Modified function UpdateFocusedWidget in WB_InGame
*Modified function UpdateItemDescription in WB_Inventory
*Modified function 'AddItem' in 'InventoryComponent', it returns index of added item
-------------------------------------

