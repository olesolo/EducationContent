### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Power the portal!

## Step 1
Вам нужно вызвать молнию, стоя на **золотых пластинах**. Во-первых, вам нужно установить дождь в блоке ``||gameplay: погода||``  ``|| loops: при начале||``. Затем попробуйте использовать ``||логику: если||``, ``||blocks: проверить на||`` и ``||mobs: создать молнию||``, чтобы молния ударила в нужный момент.

### ~ tutorialHint
Отностиельные координаты золотых пластин под вами **0, -1, 0**. Помните, что вам нужно стоять на пластинах.

```ghost
player.onTravelled(WALK, function () {
    if (blocks.testForBlock(GOLD_BLOCK, pos(0, -1, 0))) {
        mobs.spawn(LIGHTNING_BOLT, pos(0, 0, 0))
    }
})
gameplay.setWeather(RAIN)
```
