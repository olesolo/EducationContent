### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Sandcastle!

## Step 1
Используйте свои навыки программирования, чтобы преодолеть возникшие проблемы. Помните, что есть много способов их решить.

```ghost
blocks.onBlockBroken(GRASS, function () {
	
})
blocks.onBlockPlaced(GRASS, function () {
	
})
player.onTravelled(SNEAK, function () {
    mobs.applyEffect(INVISIBILITY, mobs.target(NEAREST_PLAYER), 3, 1)
    mobs.spawn(CHICKEN, pos(0, 0, 0))
    mobs.give(
    mobs.target(NEAREST_PLAYER),
    GRASS,
    1
    )
})
player.onChat("jump", function () {
	
})

```