# CGObject
Represent an object manager entity, all entity inherit from this object.


## Properties
| Name | Type | Description                                                  |
| ------ | :----------------------------------------------------------- | ------ |
| self.DistanceToActivePlayer | number |Return the distance between this object and the active player|
| self.EntryId | number |Return the entry id of this object (same as wowhead)|
| self.Guid | [SmartGuid](SmartGuid.md) |Return the guid of the object|
| self.IsLocked | boolean |Return if the object is in locked state (that happen when fishing bobber is active)|
| self.IsLineOfSight | boolean |Return if the object is in line of sight|
| self.Name | string |Return the object name|
| self.Position | [Vector3](Vector3.md) |Return the object position|
| self.Type | number |Return the object type (player, unit, gameobject, etc..)|


## Methods
| Name | Description |
| ------- | :----------------------------------------------------------- |
| self:Interact() |Interact with the object (similar to right clicking it)|
| self:GetDistanceTo([otherObject](#CGObject)) |Return the distance between this object and the other object|
| self:GetDistanceTo([position](Vector3.md)) |Return the distance between this object and the position|



# CGUnit
Represent an object manager unit, it inherit from [CGObject](#CGObject)
Example : Any NPC, monster, etc.. in the game world


## Properties
| Name | Type | Description                                                  |
| ------ | :----------------------------------------------------------- | ------ |
| self.Auras | table |Return a table of [UnitAuraEntry](UnitAuraEntry.md) for each player buff/debuff|
| self.BoundingRadius | number |Return the bounding radius of the unit|
| self.CastingSpellId | number |Return unit's casting/channeling spell id|
| self.CastingTimeLeft | number |Return unit's casting/channeling time left in seconds|
| self.CombatReach | number |Return the combat reach range of the unit|
| self.CharmedByGuid | [SmartGuid](SmartGuid.md) |Return the guid of the unit that charmed this unit|
| self.CreatedByGuid | [SmartGuid](SmartGuid.md) |Return the guid of the unit that created this unit|
| self.EffectiveLevel | number |Return the scaled level of the unit|
| self.HasTarget | boolean |Return true if that unit has a target, false otherwise|
| self.Health | number |Return the unit health|
| self.HealthMax | number |Return the unit max health|
| self.HealthPercent | number |Return the unit health in percent|
| self.IsAlive | boolean |Return if the unit is alive|
| self.IsAttackable | boolean |Return if the unit is attackable|
| self.IsCasting | boolean |Return if the unit is casting/channeling|
| self.IsConfused | boolean |Return if the unit is confused|
| self.IsDisarmed | boolean |Return if the unit is disarmed|
| self.IsFeigningDeath | boolean |Return if the unit is using feign death|
| self.IsFleeing | boolean |Return if the unit is fleeing|
| self.IsLootable | boolean |Return if the unit is lootable|
| self.IsLooting | boolean |Return if the unit is looting a corpse|
| self.IsDead | boolean |Return if the unit is dead|
| self.IsFriendly | boolean |Return if the unit is friendly|
| self.IsHostile | boolean |Return if the unit is hostile|
| self.IsInParty | boolean |Return if the unit is in our party|
| self.IsInRaid | boolean |Return if the unit is in our raid|
| self.IsMounted | boolean |Return if the unit is using a mount|
| self.IsPacified | boolean |Return if the unit is pacified|
| self.IsSilenced | boolean |Return if the unit is silenced|
| self.IsSkinnable | boolean |Return if the unit is skinnable|
| self.IsStunned | boolean |Return if the unit is stunned|
| self.Level | number |Return the level of the unit|
| self.MountDisplayId | number |Return the display id of the unit's mount|
| self.NativeDisplayId | number |Return the original display id of the unit|
| self.Reaction | number |Return unit reaction|
| self.SummonedByGuid | [SmartGuid](SmartGuid.md) |Return the guid of the unit that summoned this unit|
| self.TargetGuid | [SmartGuid](SmartGuid.md) |Return unit's target guid|


## Methods
| Name | Description |
| ------- | :----------------------------------------------------------- |
| self:GetTarget() |Return the unit's target (return type depend of the target type)|
| self:HasAuraById(id) |Return true if the unit has the aura with the specified id|
| self:UpdateDisplayInfo() |Update the unit display (call it after replacing self.DisplayId)|



# CGPlayer
Represent an object manager player, it inherit from [CGUnit](#CGUnit)
Example : Any players in the game world


## Properties
| Name | Type | Description                                                  |
| ------ | :----------------------------------------------------------- | ------ |
| self.Specialization | number |Return the active talent / spec id|



# CGLocalPlayer
Represent your local player object, it inherit from [CGPlayer](#CGPlayer)
This is only valid for your own player.


## Methods
| Name | Description |
| ------- | :----------------------------------------------------------- |
| self:ClickToMove(position) |Move the player using Click to Move to the selected destination (no path finding)|



# CGGameObject
Represent an object manager game object, it inherit from [CGObject](#CGObject)
Example : Mining node, fishing bobber, boat, campfire...


## Properties
| Name | Type | Description                                                  |
| ------ | :----------------------------------------------------------- | ------ |
| self.CreatedByGuid | [SmartGuid](SmartGuid.md) |Return the creator guid of that object|
| self.DisplayId | number |Return the object display id|
| self.Flags | number |Return the object flags|





