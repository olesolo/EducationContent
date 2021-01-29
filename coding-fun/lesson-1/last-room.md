### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# Program the Agent to move up to the gold plate!

## Step 1
Запрограммируйте агента, чтобы он добрался до золотой пластины. Вам нужно оставаться на своей золотой пластине, в то время как агент должен оставаться на другой. Когда закончите, нажмите кнопку **Start**, чтобы скомпилировать код. Зайдите в Minecraft, чтобы запустить свой код.


```ghost
player.onChat("last", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```  