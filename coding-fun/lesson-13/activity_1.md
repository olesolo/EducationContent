### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Lava swim

## Step 1
Ваша задача использовать стартовый блок условие ``||игрок:при условии что игрок - плыть в лаве||``. И внутрь добавить ``||мобы: применить огнестойкость||`` к **ближайшему игроку**. Теперь вы сможете безопасно пересечь лаву.



```ghost
player.onTravelled(SWIM_LAVA, function () {
    mobs.applyEffect(FIRE_RESISTANCE, mobs.target(NEAREST_PLAYER), 10, 1)
    mobs.clearEffect(mobs.target(NEAREST_PLAYER))
})
```
