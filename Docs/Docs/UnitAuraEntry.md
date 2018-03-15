# UnitAuraEntry
Represent an unit aura (buff/debuff)


## Properties
| Name | Type | Description                                                  |
| ------ | :----------------------------------------------------------- | ------ |
| self.Id | number |Return the aura/spell id that can be looked up on wowhead|
| self.CasterGuid | [SmartGuid](SmartGuid.md) |Return the caster guid|
| self.Duration | number |Return the aura duration|
| self.Stack | number |Return the aura stack count|
| self.TimeLeft | number |Return the aura time left (in seconds)|