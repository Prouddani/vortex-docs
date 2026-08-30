---
title: BindableEvent
description: Communication between one side only (server or client)
---

## Summary

`BindableEvents` are used for communication from a [Script](https://create.playvortex.io/reference/classes/script/) or a [LocalScript](https://create.playvortex.io/reference/classes/localscript/) to another one of the side.

### Example

```luau
-- server (the same would work with a local script)

local ReplicatedStorage = game:GetService("ReplicatedStorage")
local MyBindableEvn = ReplicatedStorage:WaitForChild("MyBindable")

MyBindableEvn:Fire(67) -- we send 67 to another script
```

```luau
-- server 2

local ReplicatedStorage = game:GetService("ReplicatedStorage")
local MyBindableEvn = ReplicatedStorage:WaitForChild("MyBindable")

local function received_bindable(number)
    print("The number ".. number.. " was received!")
end

MyBindableEvn.Event:Connect(received_bindable)
```

