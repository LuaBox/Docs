# CGObject

### Represent an object manager entity, all entity inherit from this object.



## Properties

------

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
------

| Name | Description |
| ------- | :----------------------------------------------------------- |
| self:Interact() |Interact with the object (similar to right clicking it)|
| self:GetDistanceTo([otherObject](CGObject.md)) |Return the distance between this object and the other object|
| self:GetDistanceTo([position](Vector3.md)) |Return the distance between this object and the position|


