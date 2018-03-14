# ObjectMgr

#### The object manager keep a track of all the objects close to you in the world.

#### Consider taking at look at the [Objects](Objects.md) documentation



## Properties

------

| Name                  | Type                              | Description                                                  |
| --------------------- | :-------------------------------- | ------------------------------------------------------------ |
| self.ActivePlayer     | [CGLocalPlayer](CGLocalPlayer.md) | Return the active player object, or nil if not ingame        |
| self.ActivePlayerGuid | [SmartGuid](SmartGuid.md)         | Return the active player guid                                |
| self.GameObjects      | table                             | Return a table with all the [CGGameObject](CGGameObject.md) in the object manager |
| self.Players      | table                             | Return a table with all the [CGPlayer](CGPlayer.md) in the object manager |
| self.Units      | table                             | Return a table with all the [CGUnit](CGUnit.md) in the object manager |



## Methods

------

| Name                                       | Description                                                  |
| ------------------------------------------ | :----------------------------------------------------------- |
| self:GetActivePlayer()                     | Return the [active player object](CGLocalPlayer.md) or nil if not ingame |
| self:GetActivePlayerGuid()                 | Return the active player [guid](SmartGuid.md)                |
| self:GetDistanceTo([position](Vector3.md)) | Return the distance between this object and the position     |

