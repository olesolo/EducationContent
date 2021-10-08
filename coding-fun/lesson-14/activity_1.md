### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Pass the dinosaur!

## Step 1
Вам нужно ``||player: при условии крадется||`` динозавра, сделав себя ``||mobs: невидимым||``. Сможете ли вы сделать это?


### ~ tutorialHint
Попробуйте нажать Shift и W, чтобы прокрасться в Minecraft.


```ghost
player.onTravelled(SNEAK, function () {
    mobs.applyEffect(INVISIBILITY, mobs.target(NEAREST_PLAYER), 3, 1)
})
```
