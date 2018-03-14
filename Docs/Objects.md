# CGObject
#### Represent an object manager entity, all entity inherit from this object.


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
##### Represent an object manager unit, it inherit from [CGObject](#CGObject)
##### Example : Any NPC, monster, etc.. in the game world


## Properties
| Name | Type | Description                                                  |
| ------ | :----------------------------------------------------------- | ------ |
| self.DisplayId | number |Get or set the unit display id|
| self.HasTarget | boolean |Return true if that unit has a target, false otherwise|
| self.Health | number |Return the unit health|
| self.HealthMax | number |Return the unit max health|
| self.HealthPercent | number |Return the unit health in percent|
| self.IsAlive | boolean |Return if the unit is alive|
| self.IsAttackable | boolean |Return if the unit is attackable|
| self.IsDead | boolean |Return if the unit is dead|
| self.IsFriendly | boolean |Return if the unit is friendly|
| self.IsHostile | boolean |Return if the unit is hostile|
| self.Reaction | number |Return unit reaction|
| self.TargetGuid | [SmartGuid](SmartGuid.md) |Return unit's target guid|
| self.IsLocked | boolean |Return if the object is in locked state (that happen when fishing bobber is active)|
| self.IsLineOfSight | boolean |Return if the object is in line of sight|
| self.Name | string |Return the object name|
| self.Position | [Vector3](Vector3.md) |Return the object position|
| self.Type | number |Return the object type (player, unit, gameobject, etc..)|


## Methods
| Name | Description |
| ------- | :----------------------------------------------------------- |
| self:GetTarget() |Return the unit's target (return type depend of the target type)|
| self:UpdateDisplayInfo() |Update the unit display (call it after replacing self.DisplayId)|



# CGPlayer
#### Represent an object manager player, it inherit from [CGUnit](#CGUnit)
#### Example : Any players in the game world


## Properties
| Name | Type | Description                                                  |
| ------ | :----------------------------------------------------------- | ------ |
| self.Specialization | number |Return the active talent / spec id|




# CGGameObject
#### Represent an object manager game object, it inherit from [CGObject](#CGObject)
#### Example : Mining node, fishing bobber, boat, campfire...


## Properties
| Name | Type | Description                                                  |
| ------ | :----------------------------------------------------------- | ------ |
| self.CreatedByGuid | [SmartGuid](SmartGuid.md) |Return the creator guid of that object|
| self.DisplayId | number |Return the object display id|
| self.Flags | number |Return the object flags|





