---
ns: ENTITY
---
## SET_ENTITY_ANIM_SPEED

```c
// 0x28D1A16553C51776 0x3990C90A
void SET_ENTITY_ANIM_SPEED(Entity entity, char* animDictionary, char* animName, float speedMultiplier);
```

```
speedMultplier is by default 1.0. This native allow you to change the spend of an animation.
speeeMultiplier = 0.5 will slow the animation (Networked)
speedMultiplier = 0.0 will pause the animation (Networked)
speedMultipler = -1.0 will reverse the animation (not sync with other player)

To reverse an animation sync with players, set speedMultiplier to 0.0 then use SET_ENTITY_ANIM_CURRENT_TIME manually instead.

Exemple :

SetEntityAnimSpeed(PlayerPedId(), animDict, animName, 0.0)
SetEntityAnimCurrentTime(PlayerPedId(), animDict, animName, 1.0)
local t = 0.99
while GetEntityAnimCurrentTime(PlayerPedId(), animDict, animName) > 0.0 do
  Wait(100)
  SetEntityAnimCurrentTime(PlayerPedId(), animDict, animName, t)
  t = t - 0.1
end

Evy.

```

[Animations list](https://alexguirre.github.io/animations-list/)

## Parameters
* **entity**: 
* **animDictionary**: 
* **animName**: 
* **speedMultiplier**: 


