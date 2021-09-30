### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# The Climb

## Step 1
Ваша задача подняться в недоступную область. Для этого используйте блок ``||мобы:применить усиление прыжка||`` чтобы подпрыгнуть выше. 


```ghost
loops.forever(function () {
    mobs.applyEffect(JUMP_BOOST, mobs.target(NEAREST_PLAYER), 10, 1)
    mobs.clearEffect(mobs.target(NEAREST_PLAYER))
})
```
