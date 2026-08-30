---
title: Script
description: A script that runs in the server
---

<!--
Updated by Prouddani

August 30th, 2026
-->

## Summary

A `Script` runs in the server, and every change is replicated to every client. Moreover, it can only be placed as of now in both [Workspace](https://create.playvortex.io/reference/classes/workspace/) and [ServerScriptService](https://create.playvortex.io/reference/classes/server-script-service/), since those are the only ones that have something related to the server.

> NOTE: it is recommended to use this when dealing with server-authorative systems, to prevent exploits.
>
> e.g: shops, gamepasses, pvp, etc.

<details>
<summary><b>Inherits 2 properties from [Instance](https://create.playvortex.io/reference/classes/instance/)</b></summary>

* [Name](https://create.playvortex.io/reference/classes/instance/#name): `String`
* [Parent](https://create.playvortex.io/reference/classes/instance/#parent): `Instance`

</details>

<details>
<summary><b>Inherits 1 property from BaseScript</b></summary>

* Source: `String`

</details>

<details>
<summary><b>Inherits 3 methods from [Instance](https://create.playvortex.io/reference/classes/instance/)</b></summary>

* [Clone](https://create.playvortex.io/reference/classes/instance/#clone): `Instance`
* [Destroy](https://create.playvortex.io/reference/classes/instance/#destroy): `nil`
* [GetChildren](https://create.playvortex.io/reference/classes/instance/#getchildren): `{ Instance }`

</details>

For additional information, see [LocalScript](https://create.playvortex.io/reference/classes/localscript/).

### Examples

```luau
-- server
-- gets replicated to every client (every player will be able to see it)

local new_part = Instance.new("Part") -- or Instance.new("Part", workspace.OtherPart)
new_part.Name = "MyPart"
new_part.Parent = workspace.OtherPart -- not needed in the comment above
new_part.Position = Vector3.yAxis * 40
new_part.Anchored = false
new_part.Color = Color3.new(0, 1, 0) -- green

```