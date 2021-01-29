### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# Program the Agent to move up to the gold plate!

## Step 1
Используйте команды ``||player: on chat||`` и ``||agent: agent move||``, чтобы запрограммировать агента двигаться к золотой пластине. Вы можете запрограммировать агента на движение **вверх**. Когда закончите, нажмите кнопку **Start**, чтобы скомпилировать код. Зайдите в Minecraft, чтобы запустить свой код в игре.



```ghost
player.onChat("up", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})

```  
